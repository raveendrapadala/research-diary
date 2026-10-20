# Research Journal Diary & Lab Notebook 📝

An organized repository for tracking daily/weekly research progress, literature reviews, methodology notes, and experimental logs, written entirely in LaTeX.

---

## 📁 Repository Structure

```text
├── .gitignore          # Ignores LaTeX build/auxiliary files
├── README.md           # This file
├── main.tex            # The master layout file (inputs entries)
├── references.bib      # Centralized bibliography database
├── assets/             # Images, diagrams, and data plots
└── entries/            # Modular research logs organized by date/topic
    ├── 2026-10-20.tex
    └── literature-review.tex
```

---

## 🚀 How to Compile

This project relies on a modular structure where individual entries are included in `main.tex`. 

### Local Compilation (Command Line)
The recommended way to compile this document locally is using **`latexmk`**, which automatically handles bibliography and auxiliary generation:

```bash
latexmk -pdf -synctex=1 main.tex
```

To clean up the temporary directory after building:
```bash
latexmk -c
```

### Preferred Editors
* **Overleaf:** Connect this repository directly to Overleaf via the GitHub integration. Set `main.tex` as the root file.
* **VS Code:** Install the **LaTeX Workshop** extension. It will automatically build the project on save using your configured recipes.

---

## ✍️ Workflow: Adding a New Entry

To keep the project maintainable over time, follow this workflow:

1. **Create a new entry file** inside the `entries/` directory using a standardized date format (e.g., `entries/YYYY-MM-DD-topic.tex`).
2. **Write your content** without document preambles (just start with `\section{...}`).
3. **Include the entry** in the main workflow file (`main.tex`) using the input command:
   ```latex
   \(\input{entries/YYYY-MM-DD-topic.tex} \%\%\)MAGIT_PARSER_PROTECT%%   ```
4. **Commit and push** your source code regularly. 

*Note: Compiled PDFs are ignored by version control to avoid git bloat. Generate them locally or view them via your editor.*

---

## 🛡️ License & Access Notice

* **Visibility:** Strictly **Private** until relevant papers are formally published. 
* **License:** Distributed under the **MIT License**. See the `LICENSE` file in this repository for full details.

*Note: While the codebase is licensed under MIT to allow open sharing in the future, this repository remains strictly private until the associated research is officially published.*
