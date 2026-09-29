# The Daily Brief — Design Direction

## Direction shortlist

### 1. Editorial Signal
A confident, newspaper-inspired interface with crisp typography, warm paper tones, and a signature red alert bar. Probability: 0.06

### 2. Coastal Current
A bright, airy publication with ocean blues, sand neutrals, and fluid card layouts inspired by East Africa's coast. Probability: 0.03

### 3. Midnight Desk
A high-contrast newsroom interface with ink navy, signal orange, and compact information density for fast scanning. Probability: 0.08

## Chosen direction: Editorial Signal

**Design movement:** Contemporary editorial minimalism with a digital newspaper rhythm.

**Core principles:** News-first hierarchy, fast scanning, calm confidence, clear provenance, and generous breathing room around dense information.

**Color philosophy:** Warm ivory canvas (#f6f3ed) and deep ink (#14202b) establish trust; signal red (#d94b3d) marks breaking news and calls to action; muted blue (#55758b) supports secondary information; pale sand (#e8e0d3) creates quiet card surfaces.

**Layout paradigm:** A narrow utility strip and masthead lead into a horizontal section nav, then a two-column editorial grid: dominant lead story, supporting top stories, and a lower-density feed with a complementary most-read rail.

**Signature elements:** A red breaking-news ticker, oversized serif headlines, small uppercase section labels, thumbnail-first story rows, and a compact circular arrow mark used in the logo.

**Interaction philosophy:** Everything should feel one tap away. Search expands from the header, category chips filter the feed, story cards have obvious hover/focus states, and dark mode flips the palette without changing hierarchy.

**Animation:** Restrained 160–220ms transitions for hover, filter, search reveal, and theme change; no looping motion that competes with headlines.

**Typography system:** Fraunces for display headlines and wordmark; DM Sans for navigation, metadata, body copy, and controls. Use fluid clamp-based sizing for the masthead and hero headline.

**Brand essence:** Trusted, Kenyan-rooted, globally aware, quick without being frantic.

**Brand voice:** Direct, informed, human, and lightly conversational. Prefer “Here’s what matters” over breathless clickbait.

**Wordmark/logo:** “The Daily Brief” paired with a compact circular arrow/briefing mark suggesting a news cycle and forward motion. The symbol should remain legible at favicon scale.

**Signature brand color:** Signal red (#d94b3d).

## Planned visual assets

- `assets/hero-nairobi.webp`: A pinned local copy of the custom editorial hero image for the lead story, composed as a cinematic dawn view over Nairobi with warm light, subtle urban texture, and enough negative space for a headline overlay. Keeping it in the repository prevents a session-scoped image URL from disappearing.
- `assets/logo.svg` and `assets/logo.png`: A flat, minimal circular-arrow briefing mark in signal red and deep ink for the header and favicon.
