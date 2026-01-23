# CV / Curriculum Vitae

This repository contains my CV in both English and Spanish, with automated PDF generation via GitHub Actions.

## Files

- `cv-en.tex` - English version of the CV
- `cv-es.tex` - Spanish version of the CV (Versión en español del CV)
- `.github/workflows/build-cv.yml` - GitHub Actions workflow for automatic PDF compilation

## Features

- **Multi-language support**: English and Spanish versions
- **Automatic PDF generation**: Every push to master triggers PDF compilation
- **No local LaTeX installation required**: All compilation happens in GitHub Actions
- **Professional template**: Clean, modern CV layout using LaTeX

## Usage

### Editing the CV

1. Edit `cv-en.tex` for the English version
2. Edit `cv-es.tex` for the Spanish version
3. Commit and push your changes

### Getting the PDFs

After pushing changes to the `master` branch:

1. Go to the "Actions" tab in your GitHub repository
2. Click on the latest workflow run
3. Download the artifacts:
   - `cv-english` - Contains `cv-en.pdf`
   - `cv-spanish` - Contains `cv-es.pdf`

### Creating a Release

To create a release with attached PDF files:

```bash
git tag -a v1.0 -m "Release version 1.0"
git push origin v1.0
```

The PDFs will be automatically attached to the release.

## Compiling Locally (Optional)

If you want to compile the PDFs locally, you'll need a LaTeX distribution installed:

### On macOS:
```bash
brew install --cask mactex
```

### On Ubuntu/Debian:
```bash
sudo apt-get install texlive-full
```

### On Windows:
Download and install [MiKTeX](https://miktex.org/) or [TeX Live](https://tug.org/texlive/)

Then compile with:
```bash
pdflatex cv-en.tex
pdflatex cv-es.tex
```

## Template Customization

The CV template includes:
- Professional header with contact information
- Sections for: Professional Summary, Work Experience, Education, Technical Skills, Projects, Languages
- Font Awesome icons for contact details
- Clean, modern design with blue accents

Feel free to customize colors, fonts, and layout by modifying the LaTeX preamble in the `.tex` files.

## License

This CV template is provided as-is for personal use.
