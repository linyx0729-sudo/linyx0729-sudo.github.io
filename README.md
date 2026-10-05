# Yuxuan Lin Academic Homepage

This repository powers a lightweight academic homepage for GitHub Pages.

The page presents a research profile, publications, education, selected honors,
and contact information. It uses Times New Roman throughout, a white background,
and a restrained single-page layout inspired by academic CVs.

## Structure

- `index.html` contains the homepage sections and academic content.
- `styles.css` contains the responsive layout and visual system.
- `.nojekyll` tells GitHub Pages to publish the static files directly.

## Local preview

No build step or JavaScript dependencies are required. From this directory, run:

```sh
python -m http.server 8000 --bind 127.0.0.1
```

Open `http://127.0.0.1:8000`. GitHub Pages publishes the repository root on `main`.

## Content maintenance

- Contact addresses appear at the top, in the order Hohai, Melbourne, personal.
- Add new publications at the beginning of `.publication-list`; the
  bibliography numbering updates automatically. Keep author order, italicized
  venues, and acceptance notices consistent with the existing entries.
- The layout adapts to small screens and includes a print stylesheet.
- Times New Roman is used when installed, with Times and the browser's serif font
  as fallbacks. No fonts or other assets are loaded from external services.
