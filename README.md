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

## Recommended Software Setup

For the best experience on Windows, the following setup is recommended:

  * **IDE**: **Visual Studio Code** is a powerful and highly customizable code editor.
      * [Download VS Code](https://code.visualstudio.com/download)
  * **LaTeX Distribution**: **MiKTeX** is a modern TeX distribution for Windows that installs packages on-the-fly.
      * [Download MiKTeX](https://miktex.org/download)
  * **VS Code Extension**: **LaTeX Workshop** is an extension for VS Code that provides an all-in-one environment for LaTeX development, including compiling, previewing, and syntax highlighting.
      * [Install LaTeX Workshop](https://marketplace.visualstudio.com/items?itemName=James-Yu.latex-workshop)
  * **Perl**: Some LaTeX scripts and packages (like the one used for the glossary) require a Perl interpreter. **Strawberry Perl** is a good option for Windows.
      * [Download Strawberry Perl](http://strawberryperl.com/)

## Reference Management with Zotero

Manually managing your `citations.bib` file can be tedious. A highly recommended workflow is to use **Zotero**, a free and open-source reference management tool, along with the **Better BibTeX for Zotero** extension. This setup allows you to automatically keep your `citations.bib` file synchronized with your Zotero library.

### How to Set It Up:

1.  **Install Zotero**: Download and install the Zotero desktop application.
      * [Download Zotero](https://www.zotero.org/download/)
2.  **Install Better BibTeX**: Download the Better BibTeX for Zotero (`.xpi`) file from the latest release page and install it in Zotero by going to `Tools -> Add-ons -> Gear Icon ⚙️ -> Install Add-on From File...`.
      * [Download Better BibTeX](https://github.com/retorquere/zotero-better-bibtex/releases)
3.  **Enable Auto-Export**:
      * In Zotero, select the collection of references you want to export for your paper.
      * Right-click the collection and choose `Export Collection...`.
      * Select `Better BibLaTeX` as the format. **Crucially, check the "Keep updated" box.**
      * Save the file directly as `citations.bib` inside your project folder, overwriting the existing file.

Now, whenever you add, remove, or modify a reference in that Zotero collection, your `citations.bib` file will be automatically updated in the background. This streamlines the citation process and ensures your bibliography is always current.

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
