# Nils Blank · Academic website

A personal academic website built with **plain HTML and CSS**, hosted on GitHub Pages. No framework, package manager, build step, or JavaScript is required.

## Preview

Open `index.html` directly in your browser, or serve the folder locally:

```sh
python3 -m http.server 8000
```

Then visit http://localhost:8000. Changes take effect after refreshing the page.

## Edit the site

- **Content:** `index.html`. Comments mark the profile and individual publications.
- **Design:** `stylesheet.css`. The `:root` tokens control the colors, type scale, spacing, and page width.
- **Portrait and original figures:** `images/`.
- **Responsive WebP images:** `images/optimized/`.
- **Self-hosted fonts:** `fonts/`, with the SIL Open Font Licenses in `fonts/licenses/`.
- **Social preview:** the portrait in `images/Nils.jpg`, referenced in the metadata of both HTML pages.
- **404 page:** `404.html`.

The design uses Source Serif 4 and Inter, an almost-white background, charcoal text, and a cool slate violet (`#545D85`). The page contains a bordered profile, short bio, and publications. See `docs/design.md` for the reference analysis and visual decisions.

## Add a publication

Copy a complete `<article class="publication">` block in `index.html`, then edit:

1. Its unique `id`, `aria-labelledby`, and corresponding heading `id`.
2. Title, author list, venue/year, and one-sentence description. Wrap your name in `<strong>`.
3. Figure source, dimensions, alt text, and optional responsive `srcset`.
4. Actual Project, Paper, and Code links. Omit unavailable resources.

All papers use the same compact layout. Keep them in the desired order directly in the HTML. Your name is emphasized in each author list, and awards appear beside the relevant publication.

To highlight a paper, add `is-selected` to its article class and include `<span class="selection-label">Selected</span>` in its publication metadata. Remove both to return to the ordinary style. This changes the background without enlarging the entry.

A new paper can use a single reasonably sized image with `src`, `width`, `height`, `alt`, and `loading="lazy"`; a `srcset` is optional. Existing figures have 360, 600, 900, and 1200px WebP variants. The figure link opens the original diagram so readers can inspect its labels.

Optional citations use native HTML:

```html
<details class="citation">
  <summary>BibTeX</summary>
  <pre><code>Paste the exact citation here.</code></pre>
</details>
```

This direct HTML workflow intentionally favors minimal tooling over automatic content validation or generation.

## Portrait, CV, and service

To omit the portrait, remove `<figure class="portrait">`. The layout adapts without changing CSS.

Add a CV link only after supplying your own PDF. `data/CV_Moritz_Reuss.pdf` belongs to someone else and is not linked. Awards are listed with the corresponding paper. Education and internship information is included in the bio.

Publication metadata, affiliation, advisor, experience, and award information were carried over from the previous homepage. No new dates or service roles were invented.

## GitHub Pages

The root `index.html` is the website. GitHub Pages can serve it directly from the repository branch and `/ (root)` folder. `.nojekyll` tells GitHub Pages to serve the static files as-is. No custom Actions workflow or deployment service is needed.

The canonical address is `https://nilsblank.github.io`. If it changes, update the metadata in `index.html` and `404.html`, plus `robots.txt` and `sitemap.xml`.

The original `index.bk.html` and original image/data files are preserved.

## Accessibility and verification

The site includes semantic landmarks, a skip link, visible keyboard focus, descriptive image alternatives, explicit image dimensions, 44px navigation targets and 44px resource targets on touch devices, reduced-motion support, print styling, and responsive layouts. There is no content hidden behind JavaScript.

Local checks cover internal links, anchors, image/font paths, metadata, duplicate IDs, and text contrast. Browser visual testing and Lighthouse have not been performed because no browser was connected in the implementation session.
