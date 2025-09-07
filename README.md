# Production Order Release Agent in SAP S/4HANA Public Cloud Edition

**Interdisciplinary Project (IDP) Master's of Informatics**  
**Technical University of Munich (TUM)**

**Authors:** Chaeeun (Joy) Lee, Duc Trung Nguyen  
**Supervisor:** Philipp Landler  
**Examiner:** Prof. Dr. Helmut Krcmar  
**Submission Date:** September 30, 2025

## Project Overview

This repository contains the LaTeX source code for a thesis project focused on developing an AI-powered Production Order Release Agent for SAP S/4HANA Public Cloud Edition. The project explores the integration of SAP Joule, SAP Agent Builder, and OData APIs to automate and optimize production order release processes in manufacturing environments.

## Repository Structure

```
├── main.tex                    # Main LaTeX document
├── literature.bib              # Bibliography database
├── Makefile                    # Build automation
├── tum-*.sty                   # TUM Corporate Design styles
├── tum-*.cls                   # TUM document class
├── chapters/                   # Individual chapter files
│   ├── 00_Abstract.tex
│   ├── 01_Introduction.tex
│   ├── 02_Related_Work.tex
│   ├── 03_Solution_Design.tex
│   ├── 04_Implementation.tex
│   ├── 05_Evaluation.tex
│   ├── 06_Discussion.tex
│   ├── 07_Conclusion.tex
│   └── 99_Appendix.tex
└── tum-resources/              # TUM branding assets
    └── images/
        ├── TUM_Uhrenturm.png
        ├── Universitaet_Logo_RGB.pdf
        └── Universitaet_Flaggen.jpg
```

## Prerequisites

### Required Software

- **LaTeX Distribution:** MacTeX (macOS), TeX Live (Linux), or MiKTeX (Windows)
- **Bibliography Tool:** Biber (included with modern LaTeX distributions)
- **Make:** GNU Make (for build automation)

### Package Dependencies

The document uses several LaTeX packages that should be included in a full LaTeX distribution:

- `biblatex` with `biblatex-ieee` style
- `tikz` and `pgfplots` for diagrams
- `algorithm2e` for algorithms
- `listings` for code blocks
- `hyperref` for PDF links
- `cleveref` for smart references

## Installation Instructions

### macOS

1. **Install Homebrew** (if not already installed):

   ```bash
   /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
   ```

2. **Install MacTeX**:

   ```bash
   brew install --cask mactex
   ```

3. **Update PATH** (restart terminal or run):
   ```bash
   eval "$(/usr/libexec/path_helper)"
   ```

### Linux (Ubuntu/Debian)

1. **Install TeX Live**:

   ```bash
   sudo apt update
   sudo apt install texlive-full
   ```

2. **Install additional packages** (if needed):
   ```bash
   sudo apt install texlive-bibtex-extra biber
   ```

### Linux (Fedora/RHEL)

1. **Install TeX Live**:

   ```bash
   sudo dnf install texlive-scheme-full
   ```

2. **Or use the Makefile target**:
   ```bash
   make fedora-install
   ```

### Windows

1. **Download and install MiKTeX** from: https://miktex.org/download
2. **Install Biber** (usually included with MiKTeX)
3. **Install Make** (e.g., via Chocolatey: `choco install make`)

## Compilation Instructions

### Quick Start

1. **Clone or download** this repository
2. **Navigate** to the project directory
3. **Compile** the document:

   ```bash
   make pdf
   ```

### Available Make Targets

| Command      | Description                  |
| ------------ | ---------------------------- |
| `make pdf`   | Compile to PDF (recommended) |
| `make clean` | Remove auxiliary files       |
| `make force` | Force recompilation          |
| `make bib`   | Process bibliography only    |
| `make all`   | Compile all targets          |
| `make view`  | Open PDF in default viewer   |

### Manual Compilation

If you prefer to compile manually or if Make is not available:

1. **First pass** (processes document structure):

   ```bash
   pdflatex main.tex
   ```

2. **Process bibliography**:

   ```bash
   biber main
   ```

3. **Second pass** (resolves references):

   ```bash
   pdflatex main.tex
   ```

4. **Third pass** (finalizes cross-references):
   ```bash
   pdflatex main.tex
   ```

### Troubleshooting

#### Common Issues

1. **"pdflatex: command not found"**

   - Ensure LaTeX is properly installed and in your PATH
   - Restart your terminal after installation

2. **"biber: command not found"**

   - Install Biber separately or use a full LaTeX distribution
   - On macOS: `brew install biber`

3. **Missing packages**

   - Install missing packages through your LaTeX distribution's package manager
   - For TeX Live: `tlmgr install <package-name>`

4. **Font warnings**
   - These are usually non-critical and don't affect compilation
   - The document will still compile successfully

#### Clean Build

If you encounter persistent issues:

```bash
make clean
make pdf
```

## Project Content

### Current Status

- **Abstract**: Placeholder content (Lorem ipsum)
- **Introduction**: Detailed structure with guidance comments
- **Related Work**: ✅ Complete content on SAP S/4HANA, SAP Joule, and SAP Agent Builder
- **Solution Design**: Structure ready for content
- **Implementation**: Structure ready for content
- **Evaluation**: Structure ready for content
- **Discussion**: Structure ready for content
- **Conclusion**: Structure ready for content
- **Appendix**: Structure ready for content

### Adding Content

To add content to chapters:

1. **Edit** the corresponding `.tex` file in the `chapters/` directory
2. **Recompile** using `make pdf`
3. **Check** the output in `main.pdf`

### Bibliography

- **Add references** to `literature.bib` using BibTeX format
- **Cite references** in your text using `\cite{key}`
- **Process bibliography** with `make bib` or `biber main`

## Development Workflow

1. **Edit** chapter files in `chapters/`
2. **Compile** with `make pdf`
3. **Review** output in `main.pdf`
4. **Repeat** as needed

## Output

The compilation produces:

- `main.pdf` - The final thesis document
- Various auxiliary files (`.aux`, `.log`, `.toc`, etc.)

## Contributing

This is an academic thesis project. If you need to modify the template or structure:

1. **Backup** your work
2. **Test** changes with `make clean && make pdf`
3. **Verify** the output meets TUM requirements

## License

This project uses the TUM Corporate Design template. Please refer to the LICENSE file for details.

## Support

For LaTeX compilation issues:

- Check the `main.log` file for detailed error messages
- Ensure all required packages are installed
- Verify file paths and names are correct

For TUM-specific formatting:

- Refer to the TUM Corporate Design guidelines
- Check the `tum-*.sty` and `tum-*.cls` files for available options

---

**Note:** This README assumes basic familiarity with LaTeX. For beginners, consider starting with a LaTeX tutorial before working with this template.
