# Design notes

[Overview](../README.md) · [Case study](CASE_STUDY.md) · [User flow](USER_FLOW.md)

Chloe Jian's confirmed contribution is interface design, Figma prototyping, and visual design. The descriptions below use the supplied project presentation and the team's implementation. Where a rationale is an interpretation of the visible design, it is described as such rather than attributed to an undocumented design workshop.

## Interface hierarchy

| Stage | Information to make clear | Visible design or implementation |
| --- | --- | --- |
| Introduction | What the product does and what to do first | Product name, short promise, mascot, three-step sequence, Spotify login |
| Upload | What input is expected | Image drop zone and file-selection action |
| Analysis | How the photo is being interpreted | Original image, visual descriptors, mood profile, music direction |
| Playlist | What the result contains and how to explore it | Track list, image context, popularity toggles, refresh action |
| Save | Whether an account action has succeeded | Add to Spotify, creating state, success feedback, Spotify link |

The review-before-save sequence gives the user a decision point between an AI suggestion and an action in their Spotify account. This is visible in the source; its usability benefit remains to be evaluated.

## Color and visual identity

These are observed implementation colors, not a newly invented brand specification.

| Color | Observed use |
| --- | --- |
| `#FFD740` → `#FFE8A0` | Landing-page yellow gradient |
| `#F5F1E8` | Cream content surfaces |
| `#8B9A6B` | Muted green step markers |
| `#504E76` | Purple primary controls and selected popularity options |
| `#1DB954` | Spotify save action |

The supplied illustration uses warm orange, green headphones, and dark outlines. Its friendly character is consistent with a product intended for casual music discovery. Figma files were not available for inspection, so this document does not claim an independently verified component library, typography specification, or formal token system.

## Figma prototype

Figma prototyping is a confirmed part of Chloe's work. The supplied folder contains proposals, a project report, and presentations, but no accessible Figma project or prototype URL. This package therefore describes that contribution without inventing a clickable prototype link.

When the original prototype is available, useful evidence would include the introduction, upload, analysis, playlist review, and save-feedback screens. The current project artwork should retain its label as presentation material until original interface captures are supplied.

## Interaction states

The implementation includes states beyond the primary path:

- Dragging a file into the upload area, file validation, compression, and upload errors.
- Analysis loading, missing input, and failed service responses.
- Playlist loading, empty or failed results, refresh, and popularity selection.
- Missing Spotify authorization and a route back to login.
- Playlist creation in progress, success feedback, and an external Spotify destination.

These are code-supported states. Their presence does not establish that every state has been tested on a live deployment or that the complete interface meets an accessibility standard.

## Design questions for a next iteration

| Question | Proposed check |
| --- | --- |
| Do people understand what a mood score represents? | Ask users to explain the analysis in their own words; label scores as descriptive model output. |
| Can they find the next action during loading or failure? | Walk through analysis errors, missing sessions, and an empty playlist. |
| Does “Indie & Emerging” communicate the actual filter? | Compare the label with its popularity-based behavior; do not equate popularity with artist independence. |
| Is the save action distinct from previewing? | Ask users to identify when Spotify is changed and how success is confirmed. |
| Is image handling understandable? | Explain browser storage, external analysis, and possible playlist-cover use before those actions. |

These questions are a proposed evaluation plan. No results are claimed.
