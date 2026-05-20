# Table site — proposed image selections

> Reviewed 18 of 65 candidate JPGs across both Drive folders. Pairings below match images to specific content slots from `content-outline.md`. Each row gives the file, where it lands, and a one-line rationale. Once Geoff confirms (or swaps), the chosen files get renamed and moved into `assets/images/`; everything else stays in `incoming/` (gitignored).
>
> **Sources:**
> - November 2025 folder: DSC01076–DSC01122 (28 files) — current "Table" era, sticky-notes plentiful, organizers visible.
> - June 2025 folder: DSC08322–DSC08434 (32 files) — pre-rebrand "Startup Lean Coffee" era, useful for historical/origin slots.

---

## HOME PAGE

| Slot | File | Rationale |
|---|---|---|
| **Hero (full-width)** | `DSC01100.JPG` | Wide shot looking down the table. ~8 diverse attendees, post-its on the table, projector screen in background. Reads as "real room, real people" immediately. Strong horizontal composition with the table receding in perspective — perfect for a hero band with a text overlay on the left or center. |
| **Real rooms.** | `DSC01093.JPG` | Three organizers standing at the front of the room, audience visible in foreground, NYC skyline through the window. Establishes "in person, around a real table" with a sense of place. |
| **Real questions.** | `DSC01102.JPG` | Five attendees lined up at a long table; foreground attendee speaking with a pen in hand, others listening. Post-its and coffee cups everywhere. Captures "every attendee proposes the topics" energy. |
| **Real talk.** | `DSC01117.JPG` | Two attendees in intimate conversation. Sticky notes cover the table foreground in a riot of color. No organizers in frame — pure peer-to-peer moment. Best "real talk" image in the library. |

### Members band — 6 thumbnails

The "Who's at Table — 1,300+" section uses a small grid of attendee photos. Picking 6 with visual variety (different angles, group sizes, lighting) so the grid feels like a collage of moments, not a stock-portrait lineup.

| Slot | File | Rationale |
|---|---|---|
| Members 1 | `DSC01118.JPG` | 4 attendees side-by-side listening; post-its on table. |
| Members 2 | `DSC01110.JPG` | Karina + 3 attendees in conversation; candid attentive faces. |
| Members 3 | `DSC08398.JPG` | 4 attendees listening; mixed expressions, daylight. |
| Members 4 | `DSC08393.JPG` | 4 attendees with NYC view; warm smile in center. |
| Members 5 | `DSC08377.JPG` | Woman gesturing mid-sentence to attentive listener. |
| Members 6 | `DSC01088.JPG` | 2 foreground attendees + 2 standing in back; layered depth. |

### Aha moments section (optional banner)

| Slot | File | Rationale |
|---|---|---|
| Section header | `DSC08339.JPG` *(optional)* | Overhead shot of saturated post-its on wood with a Sharpie and a reaching hand. Pure brand-cue image. The aha-moments section is otherwise CSS-rendered post-its (no photo required), but this image could anchor the section header if we want a real-photo moment to set up the synthetic post-its below. Or hold for a future use. |

---

## ABOUT PAGE

| Slot | File | Rationale |
|---|---|---|
| **Three-organizer photo** | `DSC01076.JPG` | Geoff, Karina, Benjamin posed together. Same photo (or near-identical) used in the prior Squarespace site. Rotation note: file has portrait EXIF — needs `image-orientation: from-image` in CSS or a re-saved landscape crop. |
| **Origin 4a — 2018 start** | `DSC08322.JPG` | Wide-angle establishing shot with "Startup Lean Coffee README" visible on the screen. Historical authenticity for the 2018-era paragraph. |
| **Origin 4b — raw conversations** | `DSC08363.JPG` | Three attendees listening intently; intimate framing; post-its and name cards on the table. Visual analog for "genuine, raw conversations about the things that actually keep them up at night." |
| **Origin 4c — outcomes/relationships** | `DSC08410.JPG` | Speaker mid-thought with Lean Coffee instructions visible on slides behind. Pairs with the paragraph about diverse topics (fundraising, hiring, AI, etc.) — shows the format that produced those conversations. |
| **Origin 4d — 2025 co-organizers join** | `DSC01084.JPG` | Karina and Benjamin standing in casual conversation. Quiet, behind-the-scenes feel that matches the paragraph naming them as co-organizers. |
| **Origin 4e — Table today** | `DSC01122.JPG` | Group around the table with thumbs-up, candid energy, post-its everywhere. Celebratory closer for "There's always a seat for you at Table." |

---

## SPONSORS PAGE

No images proposed for v1 — the page is mostly typographic (hero + 3 short blocks + 3 sponsor logo cards + contact). Adding photography here would compete with the logos and dilute focus. If we want one atmospheric shot for the hero band, easiest pull would be `DSC01100.JPG` (same as home hero) reused at smaller scale, or none at all.

---

## File rename plan

When approved, the chosen 16 files (12 + 4 from June, + the optional banner) move into `assets/images/` with descriptive names:

```
DSC01100.JPG → hero-table-wide.jpg
DSC01093.JPG → real-rooms-organizers-audience.jpg
DSC01102.JPG → real-questions-attendee-speaking.jpg
DSC01117.JPG → real-talk-pair-conversation.jpg
DSC01118.JPG → members-01-row-listening.jpg
DSC01110.JPG → members-02-karina-attendees.jpg
DSC08398.JPG → members-03-row-daylight.jpg
DSC08393.JPG → members-04-nyc-window.jpg
DSC08377.JPG → members-05-conversation.jpg
DSC01088.JPG → members-06-layered.jpg
DSC08339.JPG → aha-moments-postits-overhead.jpg   (optional)
DSC01076.JPG → organizers-three.jpg
DSC08322.JPG → origin-2018-lean-coffee.jpg
DSC08363.JPG → origin-raw-conversations.jpg
DSC08410.JPG → origin-format-speaker.jpg
DSC01084.JPG → origin-coorganizers-2025.jpg
DSC01122.JPG → origin-today-group.jpg
```

`incoming/` stays gitignored; we don't ship the unused 49.

---

## Open questions for Geoff

1. **Hero choice** — `DSC01100` is the strongest wide shot I saw. If you'd prefer the higher-energy thumbs-up `DSC01122` instead, easy swap (move 1122 → hero, find a different origin-today closer).
2. **Sponsors hero photo** — none vs. reusing `DSC01100` smaller. Recommendation: none. Confirm.
3. **Aha moments banner image** — yes or no on using `DSC08339` (overhead post-its) as a real-photo header above the CSS post-it collage. Either works.
4. **More candidates to view?** — I sampled ~28% of the library. If you have specific shots in mind that I haven't proposed, point me at the file numbers and I'll pull them.
