# Elementor homepage conversion

Files:
- `homepage-elementor.json`
- `homepage-elementor-html-fallback.json`
- `homepage-custom-css.css`
- `assets/home-hero-reference.jpg`

Use:
1. Set the page as your WordPress front page if you want the CSS rules scoped to `body.home` to apply exactly as written.
2. Open the page in Elementor and set `Page Layout` to `Elementor Canvas`.
3. Import `homepage-elementor.json` as a template/page structure.
4. Add the CSS from `homepage-custom-css.css` in `Appearance -> Customize -> Additional CSS`.
5. Replace the hero image with `assets/home-hero-reference.jpg` after uploading it to Media Library.

Fallback for free Elementor:
1. If the class-based import still renders incorrectly, import `homepage-elementor-html-fallback.json` instead.
2. That fallback uses HTML widgets for each section and embeds the critical CSS directly, so it is much less dependent on theme wrappers and container-class behavior.
3. The tradeoff is that each section is edited inside an HTML widget instead of fully granular Elementor text/image controls.

Notes:
- This is a first-pass homepage builder version, not a finished theme.
- It is meant to be edited visually in Elementor.
- I have not import-tested it inside a live WordPress + Elementor install from this workspace.
- If this is not your actual front page yet, replace `body.home` in the CSS with the page-specific class from your browser source, such as `body.page-id-123`.
