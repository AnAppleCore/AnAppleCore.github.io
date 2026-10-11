# Hongwei Yan — academic website

Personal website at [anapplecore.github.io](https://anapplecore.github.io), built with Jekyll and compatible with GitHub Pages.

## Updating content

- `_pages/about.md`: short biography, two research directions, and selected publications.
- `_data/research.yml`: contact links, portrait, CV download paths, and all paper metadata. The homepage selects entries with `selected: true`; the publications page displays the complete list.
- `_pages/publications.md`: publication groups and a short ongoing-work entry with related patent information.
- `_pages/cv.md`: education, research experience, honors, and service. Full paper descriptions live on the publications page.
- `files/Hongwei_Yan_CV_en.pdf` and `files/Hongwei_Yan_CV_zh.pdf`: the downloadable English and Chinese CVs, exported from the separate LaTeX repository.

Keep author order, equal-contribution marks and publication status consistent with the final paper. Use `status: published` only for accepted/published work; use `status: preprint` for manuscripts under review. Code links are optional. Add an `image` path and a descriptive `image_alt` only when the corresponding original paper figure is available in `images/publications/`; thumbnails preserve the figure's aspect ratio. A paper's `id` should stay stable because it is also used for page anchors.

The four pre-existing `/publication/...` URLs remain available through `_publications/` and `_layouts/research-paper.html`. Their visible content is drawn from the same data file as the publication list.

## Layout

`_layouts/research.html` and `assets/css/research.css` define the shared white-and-blue layout. It uses system fonts, semantic HTML, visible keyboard focus, responsive mobile layouts, and no external scripts or font services. `_includes/research-paper.html` is the shared publication component.

Upstream template posts, talks, teaching pages, portfolios and example PDFs remain in the repository but are excluded from the generated site in `_config.yml`. Local design comparisons and temporary build files belong in the ignored `tmp/` folder.

## Local preview

With Ruby and Bundler installed:

```sh
bundle install
bundle exec jekyll serve --config _config.yml,_config.dev.yml
```

Open `http://localhost:4000`. For a production build, run `bundle exec jekyll build`.

Before publishing, check the homepage, publications and CV pages at desktop and narrow mobile widths, both PDF links, and the four legacy publication links. The site contains no deployment automation beyond the repository's existing GitHub Pages setup.

## Attribution

The repository originated from [Academic Pages](https://academicpages.github.io/) and the [Minimal Mistakes](https://mmistakes.github.io/minimal-mistakes/) theme. Original upstream files and the MIT license are retained; the current primary pages use the self-contained research layout described above.
