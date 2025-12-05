# CV LaTeX Repository

This repository contains Jonas Carlsson's professional CV/résumé built using the AltaCV LaTeX template. The CV is structured in a modern two-column layout showcasing work experience, skills, education, and certifications.

## About

The CV uses the [AltaCV class](AltaCV_README.md) - a clean and modern LaTeX template designed for creating professional résumés. The main document (`mmayer.tex`) is customized with personal information, work history, and technical skills.

## Prerequisites

- A LaTeX distribution (TeX Live, MiKTeX, or MacTeX)
- **Recommended**: [LaTeX Workshop extension](https://marketplace.visualstudio.com/items?itemName=James-Yu.latex-workshop) for VS Code

## Setup

1. **Install LaTeX Distribution**
   - Windows: [MiKTeX](https://miktex.org/download) or [TeX Live](https://tug.org/texlive/)
   - macOS: [MacTeX](https://www.tug.org/mactex/)
   - Linux: `sudo apt-get install texlive-full` (or equivalent)

2. **Install VS Code Extension** (if using VS Code)
   ```
   ext install James-Yu.latex-workshop
   ```

3. **Required Fonts** (optional, for better results)
   - [Lato](http://www.latofonts.com/lato-free-fonts/)

## Usage

### Compiling to PDF

**In VS Code with LaTeX Workshop:**
- Press `Ctrl+Alt+B` to build
- Press `Ctrl+Alt+V` to view PDF
- Or use Command Palette: `LaTeX Workshop: Build LaTeX project`

**Using command line:**
```powershell
pdflatex mmayer.tex
```

**For XeLaTeX compilation:**
```powershell
xelatex -shell-escape -output-driver="xdvipdfmx -z 0" mmayer.tex
```

### Editing the CV

Edit `mmayer.tex` to customize:
- Personal information in the `\personalinfo{}` section
- Work experience with `\cvevent{}{}{}{}`
- Skills using `\cvtag{}`
- Education, certifications, and other sections as needed

The CV automatically builds to the `build/` directory.

## Repository Structure

```
├── mmayer.tex           # Main CV document
├── altacv.cls          # AltaCV class file
├── profilbild.*        # Profile photo
├── pubs-num.tex        # Bibliography configuration
├── latexmkrc           # Build configuration
└── build/              # Compiled output directory
```

## Further Information

For detailed information about the AltaCV template features and customization options, see [AltaCV_README.md](AltaCV_README.md).