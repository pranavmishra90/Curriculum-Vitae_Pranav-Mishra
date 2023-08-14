# Curriculum Vitae

[![Publish LaTeX CV as PDF](https://github.com/pranavmishra90/Curriculum-Vitae_Pranav-Mishra/actions/workflows/save_pdf.yml/badge.svg)](https://github.com/pranavmishra90/Curriculum-Vitae_Pranav-Mishra/actions)

These are the [Latex](./pranav_kumar_mishra_cv.tex) sources for my academic CV. It automatically pulls from .tex files in the [/Bibliography](./Bibliography/) directory. Alternatively, it can source all types of citations using the keyword filter in the [cv.bib](./CV.bib).

**Download** the latest compiled PDF:
[pranav_kumar_mishra_cv.pdf](https://github.com/pranavmishra90/Curriculum-Vitae_Pranav-Mishra/raw/pdf/pranav_kumar_mishra_cv.pdf)

## Template

You're free to reuse and modify this template under the terms of the BSD
3-clause License (see `LICENSE.md`). Significant credit goes to [Leonardo Uieda](https://github.com/leouieda) who created the original [repository](https://github.com/leouieda/cv). This repository is a modification on his work for content, style, and LaTex compilation.

## Building

I use [Tectonic](https://tectonic-typesetting.github.io) to build the PDF from
the sources.
It's very convenient, can be installed from
[conda-forge](https://github.com/conda-forge/tectonic-feedstock),
and is faster than using a normal LaTeX compiler.
There are many ways to install it (see their website for instructions).

### Creating a python environment using `mamba` (`conda`)

Create a python environment using:

````sh
# From the root directory of this repository
 mamba env create --file environment.yml --prefix ./env
 mamba activate ./env
````

## Deploying

A PDF is compiled automatically by GitHub Actions with every commit to a `features/*` or `draft` branch and stored as a GitHub Actions Artifact (retention = 5 days). When commits are made to the `main` branch, the PDF file is uploaded to the `pdf` branch and committed there.

This allows for a convenient viewing of draft changes to a CV without crowding up the git history excess PDF files. Once changes are finalized, the PDFs are kept in a dedicated branch. (Note: All changes will be accessible through the git history on the various `.tex` and `.bib` files).

## License

All LaTeX template source code is distributed under the
[BSD 3-clause License](https://opensource.org/licenses/BSD-3-Clause). See [License](./LICENSE.md) for more information.
