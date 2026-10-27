![Descrizione della prima foto](mytau.png)
![Descrizione della seconda foto](mytau2.png)
# mystyletau — Custom Tau glyphs for topology

# mystyletau

**Authors:** Antonello Meccariello & Francesco Meccariello  
**Version:** 2.1 (2026-10-27)  
**License:** LPPL 1.3c

## Description
The `mystyletau` package provides two unique graphical variants of the Tau symbol: `\vtau` and `\atau`. 

## Technical Workflow
The custom symbols were first designed in **Inkscape** and saved as `.svg` files (now saved in the `src` directory). 
These vectors were then imported into the **IcoMoon App** (https://icomoon.io/app) to be converted into high-quality font glyphs and exported as the final `mytautwo.ttf` file.

**Major updates in v2.1:** 
- **Universal Engine Support:** Now fully compatible with **pdfLaTeX**, in addition to **LuaLaTeX** and **XeLaTeX**.
- Dynamic color changes (compatible with `xcolor`).
- Perfect scaling across all math sizes (subscripts, superscripts).
- Full `\ensuremath` support for both text and math mode.
- Custom kerning for mathematical subscripts (e.g., specific spacing for `\vtau_X`).

## Requirements
- **Engines:** pdfLaTeX, LuaLaTeX, or XeLaTeX.
- **Packages:** `fontspec` (for Lua/XeLaTeX) or standard font encoding packages (for pdfLaTeX), plus `amsmath`.

## Files Included
- `mystyletau.sty`: The LaTeX package file.
- `mytautwo.ttf`: The TrueType font file containing the glyphs.
- `mystyletau.pdf`: Package documentation.
- `mystyletau.tex`: Documentation source.
- `src/`: Directory containing the original SVG source files for the glyphs.

## Installation 1: If you have a modern LaTeX distribution
It is sufficient to use `\usepackage{mystyletau}` in your preamble.

## Installation 2 - Manual Installation (macOS)
If your distribution doesn't pick it up automatically:
1. Copy `mystyletau.sty` to `.../texmf/tex/latex/mystyletau/`
2. Copy `mytautwo.ttf` to `.../texmf/fonts/truetype/public/mystyletau/`
3. Update your filename database (run `texhash` and `luaotfload-tool --update` on Terminal).

## License
This work may be distributed and/or modified under the conditions of the LaTeX Project Public License (LPPL), either version 1.3c of this license or (at your option) any later version.
