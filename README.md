# Template_HKUST-GZ_Thesis_Variant-LYC

HKUST (GZ) thesis template, LYC's variant.

# Preparation (With VSCode - LaTeX Workshop)

- Integrate the following items into your VS Code `settings.json`.

```json
{
    "latex-workshop.latex.tools": [
        {
            "name": "xelatex",
            "command": "xelatex",
            "args": [
                "-synctex=1",
                "-interaction=nonstopmode",
                "-file-line-error",
                "%DOCFILE%"
            ]
        },
        {
            "name": "pdflatex",
            "command": "pdflatex",
            "args": [
                "-synctex=1",
                "-interaction=nonstopmode",
                "-file-line-error",
                "%DOCFILE%"
            ]
        },
        {
            "name": "latexmk",
            "command": "latexmk",
            "args": [
                "-synctex=1",
                "-interaction=nonstopmode",
                "-file-line-error",
                "-pdf",
                "-outdir=%OUTDIR%",
                "%DOCFILE%"
            ]
        },
        {
            "name": "bibtex",
            "command": "bibtex",
            "args": [
                "%DOCFILE%"
            ]
        },
        {
            "name": "makeglossaries",
            "command": "makeglossaries",
            "args": [
              "%DOCFILE%"
            ]
        },
    ],
    "latex-workshop.latex.recipes": [
        {
            "name": "XeLaTeX",
            "tools": [
                "xelatex"
            ]
        },
        {
            "name": "PDFLaTeX",
            "tools": [
                "pdflatex"
            ]
        },
        {
            "name": "BibTeX",
            "tools": [
                "bibtex"
            ]
        },
        {
            "name": "LaTeXmk",
            "tools": [
                "latexmk"
            ]
        },
        {
            "name": "xelatex, biblatex, xelatex * 2",
            "tools": [
                "xelatex",
                "bibtex",
                "xelatex",
                "xelatex"
            ]
        },
        {
            "name": "pdflatex, biblatex, pdflatex * 2",
            "tools": [
                "pdflatex",
                "bibtex",
                "pdflatex",
                "pdflatex"
            ]
        },
        {
            "name": "xelatex, biblatex, xelatex, makeglossaries, xelatex * 2",
            "tools": [
                "xelatex",
                "makeglossaries",
                "xelatex",
                "bibtex",
                "xelatex",
                "xelatex"
            ]
        },
        {
            "name": "pdflatex, biblatex, pdflatex, makeglossaries, pdflatex * 2",
            "tools": [
                "pdflatex",
                "makeglossaries",
                "pdflatex",
                "bibtex",
                "pdflatex",
                "pdflatex"
            ]
        },
    ]
}
```

- You can use the Command Palette (Ctrl+Shift+P) to access your `settings.json`.

# Compilation

- Go to the [thesis](./thesis/) folder.
- Use the `xelatex, biblatex, xelatex, makeglossaries, xelatex * 2` compilation recipe.
- Compile [0_0_thesis.tex](./thesis/0_0_thesis.tex).

# References - TeX Template

- [@luckyfan-cs, Template-of-HKUST-GZ-Thesis](https://github.com/luckyfan-cs/Template-of-HKUST-GZ-Thesis)
  - Permitted to use under the [MIT License](https://www.mit.edu/~amini/LICENSE.md).

# Copyright
## Textual and Code Contents

```
Copyright (C) 2024-2026 Yucheng Liu. Under the AGPL 3.0 License.
AGPL 3.0 License: https://www.gnu.org/licenses/agpl-3.0.txt .
```

- [The AGPL 3.0 License.](./license)

## Non-textual or Non-code Contents

```
Copyright (C) 2024-2026 Yucheng Liu. Under the CC-BY-SA 4.0 License.
CC-BY-SA 4.0 License: https://creativecommons.org/licenses/by-sa/4.0/legalcode.txt .
```

- [The CC-BY-SA 4.0 License.](./license-2)
