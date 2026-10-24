# Compile the English report

Report-only ZIP: upload to Overleaf, select `main.tex`, and use pdfLaTeX. Keep `figures/` beside the source. No custom fonts or bibliography processor are required; references are embedded in the source.

Complete repository ZIP: select the nested `report/main.tex` as the main document.

Locally, from the repository root:

```bash
cd report
pdflatex -interaction=nonstopmode -halt-on-error main.tex
pdflatex -interaction=nonstopmode -halt-on-error main.tex
```

The document uses standard LaTeX packages and Latin Modern fonts. TikZ creates the English geometry schematic. No Abaqus installation, code, videos, or external data are required to compile the report.
