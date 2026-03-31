# Math Olympiad Club Zurich

A Flask-based website for the Math Olympiad Club Zurich.

## Non-Website Files

The following files are **not directly used by the website** but serve auxiliary purposes:

### `compile_and_clean.py`
A utility script for compiling LaTeX `.tex` files into PDFs. It:
- Automatically installs required LaTeX packages from `preamble.tex` using `tlmgr`
- Copies the shared preamble into each folder containing `.tex` files
- Compiles all `.tex` files to PDF using `latexmk`
- Cleans up auxiliary files, leaving only the PDFs

This is used offline to generate PDF problem sheets that are then served by the website.

### `preamble.tex`
A shared LaTeX preamble containing common packages, custom commands, and theorem environments used across all math problem documents. It includes:
- Math packages (amsmath, amssymb, tikz, etc.)
- Custom `\problem` and `\solution` commands
- Theorem environments (theorem, lemma, remark)
- Consistent styling and formatting

This file is copied into problem directories by `compile_and_clean.py` during compilation.
