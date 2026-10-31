# Sources and evidence

## Supplied project materials

The case study uses materials supplied by the portfolio author. Original working documents and private Drive links are not redistributed in this package.

| Material | What it supports |
| --- | --- |
| `Project Proposal 11/9/2025` | Initial concept, audience framing, alternative technical directions, and planned features |
| `Project Document` | Final team summary, collaborators, technology choices, incremental development, and integration challenges |
| `DJ JPG.pptx` | Project identity, role slide, visual materials, historical demo URL, and future directions |
| `DJ JPG - Music from Photos` | Earlier presentation wording; includes placeholder course/team/demo fields, so it is not used to establish final attribution or a working demo |
| Chloe Jian's clarification | Interface design, Figma prototyping, and visual design contribution |

## Implementation evidence

Repository: [nithyaindla/DJ-JPG](https://github.com/nithyaindla/DJ-JPG).

Inspected commit: [`0a1bdba336368022e33aee4ee0f5a77d3151db08`](https://github.com/nithyaindla/DJ-JPG/tree/0a1bdba336368022e33aee4ee0f5a77d3151db08).

Relevant files:

- [Landing page](https://github.com/nithyaindla/DJ-JPG/blob/0a1bdba336368022e33aee4ee0f5a77d3151db08/pages/index.tsx)
- [Photo upload](https://github.com/nithyaindla/DJ-JPG/blob/0a1bdba336368022e33aee4ee0f5a77d3151db08/pages/upload.tsx)
- [Analysis interface](https://github.com/nithyaindla/DJ-JPG/blob/0a1bdba336368022e33aee4ee0f5a77d3151db08/pages/analyze.tsx)
- [Playlist interface](https://github.com/nithyaindla/DJ-JPG/blob/0a1bdba336368022e33aee4ee0f5a77d3151db08/pages/playlist.tsx)
- [Image-analysis route](https://github.com/nithyaindla/DJ-JPG/blob/0a1bdba336368022e33aee4ee0f5a77d3151db08/pages/api/analyze.ts)
- [Track retrieval and filtering](https://github.com/nithyaindla/DJ-JPG/blob/0a1bdba336368022e33aee4ee0f5a77d3151db08/pages/api/playlist-preview.ts)
- [Playlist creation and cover upload](https://github.com/nithyaindla/DJ-JPG/blob/0a1bdba336368022e33aee4ee0f5a77d3151db08/pages/api/playlist.ts)

## How conflicting material is handled

Later project reporting and source are used for implementation details. Alternate names, browser-extension concepts, Azure/Hugging Face options, and planned features in the proposal are not automatically described as delivered.

The source already contains playlist saving and popularity filters. Video input, additional music services, and a mobile app remain presentation directions. The source also stores images in browser session storage and can transmit them to OpenAI and Spotify, so absolute no-storage/no-sharing language is not repeated as a factual guarantee.

## Limits

The historical hosted demo was directly checked and returned `DEPLOYMENT_NOT_FOUND`. A full authenticated Spotify session was not executed. Source inspection does not establish API compatibility, recommendation quality, production security, data retention, or accessibility conformance.

No supplied study dataset supports quantitative usability or business outcomes. Unreferenced market-size claims, creator time percentages, and API-cost estimates from presentation slides are omitted. No original Figma file or prototype link was available to inspect. The artwork is credited as supplied presentation material, not as independently verified original illustration authorship.
