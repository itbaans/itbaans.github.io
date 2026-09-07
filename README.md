# itbaans.github.io

Personal site. A timeline of the projects that led me into research, plus a
research statement and a gallery of digital paintings.

Everything is one static page with no build step, so it can be opened by
double-clicking `index.html` or served as-is by GitHub Pages.

## Layout

```
index.html                  the whole site: home, five chapters, statement, gallery
cv.tex                      LaTeX source for my CV (compile with pdflatex, twice)
assets/
  img/profile.jpg
  scrabble/gameplay.gif     a full game against the Scrabble engine, sped up
  sketch-rnn/               reconstruction clip, loss curves, per-epoch samples
  mtl/                      figures from the MICCAI 2026 workshop paper
  mediaeval/                figures from the MediaEval 2025 Medico submission
  paintings/                web-sized copies of the gallery images
writeups/
  vlm-interp/index.html     the full write-up for the interpretability experiment
```

The page is self-contained apart from `assets/`: the chapter diagrams are
inline SVG, and the logit-lens widget in chapter 5 carries its own data.

## The projects

The code for each project lives in its own repository:

- [scrabble_with_ai](https://github.com/itbaans/scrabble_with_ai)
- [sketch-rnn-pytorch](https://github.com/itbaans/sketch-rnn-pytorch)
- [vlm-interp-perception](https://github.com/itbaans/vlm-interp-perception)

Their working copies are ignored here (see `.gitignore`); only the figures the
site displays are committed, under `assets/`.

## Editing

Chapters are entries in the `CHAPTERS` array near the bottom of `index.html`,
each with a `label`, `title` and an `html` template literal. The home page,
research statement and gallery are plain markup above that array.
