# Technical overview

[Original team repository](https://github.com/nithyaindla/DJ-JPG) · [Source scope](SOURCES.md)

This summarizes the team implementation inspected at commit `0a1bdba336368022e33aee4ee0f5a77d3151db08`. It is a source review, not a claim that the hosted application or every external API currently works.

## Structure

The functional flow is implemented in the root project's `pages/` directory using Next.js and React with TypeScript. The repository also contains a nested `djjpg/` starter application; its presence should not be confused with the root implementation documented here.

| Layer | Relevant files | Responsibility |
| --- | --- | --- |
| Introduction and input | `pages/index.tsx`, `pages/upload.tsx` | Product explanation, login link, image validation and compression |
| Interpretation | `pages/analyze.tsx`, `pages/api/analyze.ts` | Send the photo for analysis and display structured results |
| Playlist preview | `pages/playlist.tsx`, `pages/api/playlist-preview.ts` | Retrieve tracks, refresh results, apply popularity controls |
| Playlist creation | `pages/api/playlist.ts` | Create the Spotify playlist, add tracks, attempt a photo cover upload |
| Spotify session | `pages/api/auth/`, `lib/spotify.ts` | Authentication routes and token-aware API client |

The inspected dependency manifest lists Next.js 16.0.1, React 19.2.0, Tailwind CSS, Radix/shadcn-style components, Lucide icons, Sonner notifications, and `spotify-web-api-node`. These describe the source snapshot, not a recommendation to use particular versions today.

## Image-to-music interpretation

The analysis route sends image content to OpenAI's Chat Completions API using the `gpt-4o` model identifier. Its prompt requests a scene description, colors, lighting, mood labels, mood scores, musical keywords, genres, energy, tempo, a playlist theme, and artist suggestions.

This is model interpretation plus application logic. The materials do not establish a separately trained, proprietary recommendation model. If the model output cannot be parsed, the route includes a generic fallback response; a polished result is therefore not by itself proof that detailed analysis succeeded.

## Music retrieval and controls

The preview route attempts Spotify recommendations using artist or genre seeds and musical targets. It also searches for tracks and has fallback retrieval paths. Returned tracks are filtered into Mainstream, Mixed, or Indie & Emerging views using Spotify popularity values.

The latter label is part of the product UI. Popularity is a discovery proxy, not verification of an artist's label affiliation, independence, or career stage. Recommendation endpoints, catalog data, permissions, and preview availability were not exercised in this review.

The playlist screen submits the reviewed track URIs to the creation route. That route includes a Spotify playlist creation request, track insertion, and an optional cover-image upload. It requests `public: false`; this documentation does not turn that flag into a promise of complete confidentiality.

## Image handling

The proposal's statement that images are never saved or shared is broader than the implementation supports:

- The browser compresses the selected photo and stores it as `uploadedImage` in `sessionStorage` to carry it across screens. The analysis result is also stored for the next screen.
- The photo is sent through the application server to OpenAI for analysis.
- On playlist creation, the source can also send the photo to Spotify as the playlist cover.

No separate application photo database is evident in the reviewed routes. That does not establish the retention behavior of hosting, logs, browsers, or external providers. The portfolio therefore avoids an absolute “no storage or sharing” claim.

## Availability

The presentation's old Vercel address returns `DEPLOYMENT_NOT_FOUND`. End-to-end runtime behavior, real Spotify consent, playlist creation, image-cover upload, and AI response quality remain unverified in this review. Original credentials are deliberately excluded. This fork includes the application source and a blank environment template, but is not a configured application deployment. See [local setup](LOCAL_SETUP.md) to configure an independent copy.
