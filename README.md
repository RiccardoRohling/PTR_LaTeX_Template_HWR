# LaTeX Template for Academic Papers at HWR Berlin

This repository contains a LaTeX template for academic papers, tailored for students at the Hochschule für Wirtschaft und Recht Berlin (HWR).

## Project Overview

This template provides a structured and pre-configured setup for writing academic papers, including a title page, statement of confidentiality, main text, appendix, and bibliography. It uses the Koma-Script bundle and is configured with common packages for academic writing.

## File Structure

The project is organized into several files, each serving a specific purpose:

- `main.tex`: This is the main file that orchestrates the entire document. It includes all other `.tex` files and sets up the document's preamble.
- `00_statement_of_confidentiality.tex`: Contains the statement of confidentiality.
- `01_frontpage.tex`: Defines the layout and content of the title page.
- `02_maintext.tex`: This file is intended to hold the main content of the paper, such as the introduction, body, and conclusion.
- `04_appendix.tex`: The appendix section of the document.
- `05_statementofacademicintegrity.tex`: Contains the statement of academic integrity.
- `glossar.tex`: Used to define acronyms and glossary terms.
- `hyphenation.tex`: Contains custom hyphenation rules to ensure correct typesetting.
- `citations.bib`: The bibliography file where all references should be stored in BibTeX format.
- `README.md`: This file, providing an overview of the project.

## How to Compile

To compile this LaTeX project and generate the final PDF document, you will need a LaTeX distribution that includes `pdflatex` and `biber`. The recommended compilation sequence is as follows:

1.  **pdflatex:** Run `pdflatex` on `main.tex` to generate the auxiliary files.
2.  **biber:** Run `biber` on `main` to process the bibliography.
3.  **pdflatex:** Run `pdflatex` again to incorporate the bibliography.
4.  **pdflatex:** Run `pdflatex` one final time to ensure all cross-references are correct.

You can use the following commands in your terminal:

```bash
pdflatex main.tex
biber main
pdflatex main.tex
pdflatex main.tex
```

Alternatively, you can use a LaTeX editor with a built-in compilation workflow that handles this sequence automatically.
