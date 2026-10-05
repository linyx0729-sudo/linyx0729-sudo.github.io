# Yuxuan Lin Academic Homepage

This repository powers a lightweight academic homepage for GitHub Pages.

The page presents a research profile, publications, conferences, education, selected honors,
and contact information. It uses Times New Roman throughout, a white background,
and a restrained single-page layout inspired by academic CVs.

## Structure

- `index.html` contains the homepage sections and academic content.
- `styles.css` contains the responsive layout and visual system.
- `assets/conferences/` contains the supplied conference photographs, grouped by year and event.
- `.nojekyll` tells GitHub Pages to publish the static files directly.

## Local preview

No build step or JavaScript dependencies are required. From this directory, run:

```sh
python -m http.server 8000 --bind 127.0.0.1
```

Open `http://127.0.0.1:8000`. GitHub Pages publishes the repository root on `main`.

## Content maintenance

- Contact addresses appear at the top, in the order Hohai, Melbourne, personal.
- Conference entries use native HTML `details` elements. The most recent event is
  open initially; opening another closes the previous one in supported browsers.
  Each album scrolls horizontally, supports keyboard focus and touch scrolling,
  and links to the full photograph. Images are loaded lazily and retain the
  supplied originals; no image content has been altered.
- To add a conference, duplicate a `.conference` entry, update dates, location,
  description, image dimensions and alternative text, and add its photographs
  to `assets/conferences/`. Keep the entries in reverse chronological order.
- Leadership and teaching entries are retained in `index.html` but temporarily
  hidden. To restore them, remove `hidden` from both the `#leadership` section
  and its navigation link. The shared `[hidden]` rule also applies when printing.
- Add new publications at the beginning of `.publication-list`; the
  bibliography numbering updates automatically. Keep author order, italicized
  venues, and acceptance notices consistent with the existing entries.
- The layout adapts to small screens and includes a print stylesheet.
- When changing the stylesheet, update its version query in `index.html` so
  returning visitors load the matching styles instead of a cached older copy.
- Times New Roman is used when installed, with Times and the browser's serif font
  as fallbacks. No fonts or other assets are loaded from external services.
