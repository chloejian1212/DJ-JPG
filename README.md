# DJ JPG

**Music discovery that begins with a photograph.**

[Original team repository ↗](https://github.com/nithyaindla/DJ-JPG) · [中文介绍](README.zh-CN.md) · [Design case study](docs/CASE_STUDY.md)

<img src="assets/visuals/project-illustration.png" alt="DJ JPG project illustration: a cat wearing headphones with a palette and magnifying glass" width="640">

DJ JPG is a collaborative web application that uses a photo as the starting point for a Spotify playlist. The experience connects image upload, AI interpretation of the scene, and music discovery, with a chance to review the result before adding it to Spotify.

I contributed **interface design, Figma prototyping, and visual design**. This repository includes the original team application together with my design case study and supporting materials. It is a fork of [nithyaindla/DJ-JPG](https://github.com/nithyaindla/DJ-JPG), preserving the team's original commit history.

| Project | Details |
| --- | --- |
| Portfolio author | Chloe Jian |
| My role | Interface design, Figma prototyping, visual design |
| Team | Emma Coye, Nithya Sunkara Indlamuri, Luna Jiang, Chloe Jian |
| Period | 2025 |
| Product | Photo-to-playlist web application |
| Tools | Figma; team implementation in Next.js, React, TypeScript, OpenAI API, and Spotify API |
| Status | Team implementation available; the historical hosted demo is currently unavailable |

## The idea

Choosing music often begins with a search term or an existing playlist. DJ JPG explores another starting point: a moment someone has already photographed. A sunset, a quiet room, or a night out can become a prompt for discovering music with a similar atmosphere.

The project asks: **How can an image help someone choose a soundtrack without requiring them to describe the feeling first?**

## The experience

1. **Connect Spotify and choose a photo.** The upload screen supports drag-and-drop or file selection.
2. **Review the image interpretation.** The interface presents the photo alongside a mood profile and musical descriptors.
3. **Explore a playlist.** Review tracks, refresh the suggestions, or switch between Mainstream, Mixed, and Indie & Emerging.
4. **Add it to Spotify.** Save the selected result and continue listening in Spotify.

The team source contains these interface states and API routes. The current review did not execute a complete authenticated image-to-playlist session. The [demo notes](docs/DEMO.md) explain what can be viewed now.

## My design contribution

My work covered interface design, interactive prototyping in Figma, and visual design. The design connects a playful visual identity with a guided sequence from photo selection to playlist review. The supplied materials use warm yellow, cream, muted green, and purple accents, with a headphone-wearing cat character.

The [design notes](docs/DESIGN.md) connect these visible choices to the experience. The [case study](docs/CASE_STUDY.md) explains the product problem, user journey, team implementation, and reflection. Development is credited to the team; this case study does not attribute the backend or all product decisions to me.

## Explore the project

| Document | Contents |
| --- | --- |
| [Case study](docs/CASE_STUDY.md) | Context, my role, experience, outcomes, and reflection |
| [Design notes](docs/DESIGN.md) | Interface structure, visual language, and interaction states |
| [User flow](docs/USER_FLOW.md) | Photo-to-playlist journey and recovery states |
| [Technical overview](docs/TECHNICAL_OVERVIEW.md) | How the team source connects the interface and services |
| [Demo and assets](docs/DEMO.md) | Available materials and the historical demo's status |
| [Portfolio copy](docs/PORTFOLIO_COPY.md) | English and Chinese text for a project card and detail page |
| [Sources](docs/SOURCES.md) | Evidence used and the limits of the case study |
| [Credits](CREDITS.md) | Team attribution and artwork notes |
| [Local setup](docs/LOCAL_SETUP.md) | Start the included application and configure your own service credentials |
| [Upstream source](UPSTREAM.md) | Original repository, copied version, and changes in this fork |

## Outcome

The team produced a web application implementation spanning photo upload, scene interpretation, playlist review, popularity filtering, and Spotify playlist creation. My contribution focused on how that experience is presented and explored through interface design, a Figma prototype, and visual design.

This is a design and implementation case study. It does not claim measured improvements in music matching, user satisfaction, artist exposure, or time saved. Future directions in the presentation include video input, mobile access, and additional music services.

## Using this repository

Open the Markdown documents directly; no installation is needed to read the case study. The application code is included in `pages/`, `components/`, `lib/`, `public/`, and `styles/` at this repository's root. Follow the [local setup guide](docs/LOCAL_SETUP.md) to work on the application; run it from the root rather than the nested `djjpg/` starter folder.

The original team source remains attributed to its authors. This fork adds portfolio documentation, presentation artwork, setup notes, and a blank environment template. It does not include working service credentials or create a new hosted demo. The [original README](docs/UPSTREAM_README.md) is retained for reference.

The visual assets were extracted from the supplied project presentation and retain their original proportions. They are presentation artwork, not screenshots of the current live service.

Image processing in the implementation includes browser session storage and transmission to external services; see the [technical notes](docs/TECHNICAL_OVERVIEW.md#image-handling) for details. AI mood labels are interpretations of an image, not validated measurements of someone's emotions.
