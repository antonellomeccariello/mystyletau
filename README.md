![Descrizione della prima foto](mytau.png)
![Descrizione della seconda foto](mytau2.png)
# mystyletau — Custom Tau glyphs for topology

**Authors:** Antonello Meccariello & Francesco Meccariello 
**Version:** 2.0 (2026-04-05)  
**License:** LPPL 1.3c

## Description
The `mystyletau` package provides two unique graphical variants of the Tau symbol: `\vtau` and `\atau`. 

## Technical Workflow
The custom symbols were first designed in **Inkscape** and saved as `.svg` files (now saved in the \src directory). 
These vectors were then imported into the **IcoMoon App** (https://icomoon.io/app) 
to be converted into high-quality font glyphs and exported as the final 
`mytautwo.ttf` file.

**Major update in v2.0:** The symbols are no longer loaded as external PDF images. They are now implemented as true vector glyphs within a dedicated TrueType font (`mytautwo.ttf`). This allows the symbols to:
- Change color dynamically (compatible with `xcolor`).
- Scale perfectly in all math sizes (subscripts, superscripts).
- Support `\ensuremath` for use in both text and math mode.
- Feature custom kerning for mathematical subscripts (e.g., specific spacing for `\vtau_X`).

## Requirements
- **Engine:** LuaLaTeX or XeLaTeX is **required**. This package will not work with pdfLaTeX because it relies on `fontspec` to load TrueType fonts.
- **Packages:** `fontspec`, `amsmath`.

## Files included
- `mystyletau.sty`: The LaTeX package file.
- `mytautwo.ttf`: The TrueType font file containing the glyphs.
- `mystyletau.pdf`: Package documentation.
- `mystyletau.tex`: Documentation source.
- src/: Directory containing the original SVG source files for the glyphs.

## Installation 1: If you have the latest version of Latex:
it's sufficiente to use: "\usepackage{mystyletau}" in the preamble.
## Installation 2 - MANUAL INSTALLATION, macOS - : If you DON'T have the latest version of Latex 
1. Copy `mystyletau.sty` to `.../texmf/tex/latex/mystyletau/`
2. Copy `mytautwo.ttf` to `.../texmf/fonts/truetype/public/mystyletau/`
3. Update your filename database (run `texhash` and `luaotfload-tool --update`, RUN ON TERMINAL).


## License
This work may be distributed and/or modified under the conditions of the LaTeX Project Public License, either version 1.3c of this license or (at your option) any later version.
