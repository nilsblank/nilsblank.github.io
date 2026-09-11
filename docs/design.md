# Website design

## Structure

A lightly bordered profile, a short factual bio, and four publications. Education and internships are included in the bio; the SPARC award is attached to its paper. There is no research-directions grid, separate experience/recognition section, slogan, section numbering, or oversized featured entry.

The page is 800px wide at most. Navigation contains About, Publications, and Scholar. The profile combines a 128px circular portrait with the name, role, and text links. The bio spans the reading column below. Publication rows use 220px figures, serif titles, and compact sans-serif authors and metadata. On mobile the portrait shrinks to 80px and publication figures sit above their text. The footer is one line with an email link.

## References

[Satvik Sharma](https://satvik1701.github.io/) uses Source Serif 4 for prose and titles and Inter for metadata. That font pairing is retained. [Ria Doshi](https://riadoshi.github.io/#home) informs the compact profile, simple navigation, and restrained hierarchy. Both reference repositories use plain HTML and CSS.

## Palette

[KIT’s color guide](https://kit-cd.km.kit.edu/english/341.php) specifies purple as RGB 163/16/124 (`#A3107C`). The current personal-site accent moves further toward a cool slate violet, `#545D85`, reducing the red/pink component at the user’s request. It is an individual palette rather than an implementation of KIT’s official corporate design.

| Token | Value |
| --- | --- |
| Background | `#FCFCFD` |
| Surface | `#FFFFFF` |
| Text | `#30323A` |
| Muted text | `#626571` |
| Accent | `#545D85` |
| Accent hover | `#3A4266` |
| Accent subtle | `#F0F2F7` |
| Selected publication background | `#E8ECF5` |
| Award text / background | `#79531C` / `#FFF1D4` |
| Border | `#DFE2E9` |

Slate violet appears in links, the role subtitle, selection/focus states, and the favicon. Selected publication entries use a light tint and an explicit Selected label. The full Best Paper Award text, including its workshop and year, shares a gold badge. Resource links use dark, bold, underlined text. These are controlled by the `is-selected` class. The social preview uses the existing portrait.

## Implementation

Plain `index.html` and `stylesheet.css`, local WOFF2 fonts, and pre-optimized responsive WebP figures. No dependencies, generator, build step, or browser JavaScript. The CSS defines shared color, typography, spacing, and width tokens. Fonts use swap rendering and primary font preloads.

Content remains visible without JavaScript. The page includes a skip link, keyboard focus styles, image alternatives and explicit dimensions, 44px navigation and touch-device resource targets, reduced-motion support, and print styles. Original figures remain linked for closer inspection. Browser visual and Lighthouse checks remain unverified in this session.
