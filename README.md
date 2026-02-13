# Seminar Template for Typst

A Typst template for writing seminar papers in the ACM conference paper format, based on the [clean-acmart](https://typst.app/universe/package/clean-acmart/) package.

## Overview

This template provides a ready-to-use structure for writing academic papers following the ACM conference paper format. It includes all necessary components for a complete seminar paper, including abstract, paper body, bibliography, and artifact appendix sections.

## Prerequisites

To use this template, you need to have Typst installed on your system. Typst is a modern markup-based typesetting system.

### Installing Typst

You can install Typst in several ways:

- **Using cargo** (Rust package manager):
  ```bash
  cargo install typst-cli
  ```

- **Using a package manager**:
  - **macOS**: `brew install typst`
  - **Arch Linux**: `pacman -S typst`
  - **Windows**: Download from the [official releases](https://github.com/typst/typst/releases)

- **From source**: See the [Typst repository](https://github.com/typst/typst) for instructions

For more installation options, visit the [official Typst documentation](https://github.com/typst/typst#installation).

## Quick Start

1. Clone this repository:
   ```bash
   git clone https://github.com/ds-ukassel/seminar-template-typst.git
   cd seminar-template-typst
   ```

2. Edit the paper metadata in `main.typ`:
   - Update `title`, `authors`, `affiliations`, and `conference` details
   - Modify the CCS categories and keywords

3. Write your content in the text files:
   - `text/abstract.typ` - Your paper's abstract
   - `text/paper.typ` - Main content of your paper

4. Add your references to `refs.bib` in BibTeX format

5. Compile the document:
   ```bash
   typst compile main.typ
   ```
   This will generate a PDF file named `main.pdf`

## Project Structure

```
.
├── main.typ          # Main document file with metadata and structure
├── refs.bib          # Bibliography file in BibTeX format
└── text/
    ├── abstract.typ  # Abstract content
    └── paper.typ     # Main paper content
```

## Configuration

### Document Metadata

Edit the following sections in `main.typ`:

- **Title**: Define your paper title
- **Authors**: List of authors with their emails
- **Affiliations**: Institution details (name, department, city)
- **Conference**: Conference name, short name, year, date, and venue
- **DOI**: Digital Object Identifier (if available)
- **CCS Categories**: ACM Computing Classification System categories
- **Keywords**: List of keywords for your paper

### Review Mode

For the review process, uncomment the review line in `main.typ`:
```typst
review: [\#001],  // Submission ID
```

Set it to `none` for the final version.

## Usage

### Compiling the Document

To compile your document to PDF:
```bash
typst compile main.typ
```

To compile with a custom output name:
```bash
typst compile main.typ output.pdf
```

### Watch Mode

For automatic recompilation on file changes:
```bash
typst watch main.typ
```

### Writing Content

- Use standard Typst markup for formatting your text
- Include figures, tables, and equations as shown in the example
- Reference figures, tables, and equations using labels (e.g., `@fig:sun`, `@tab:planets`, `@eq:gamma`)
- Cite references using `@citation-key` format

### Example Elements

The template includes examples of:
- Figures with captions
- Tables with styling
- Equations with numbering
- Cross-references
- Citations

## Bibliography

Add your references to `refs.bib` in standard BibTeX format. The template uses the ACM bibliography style.

Example entry:
```bibtex
@article{key2024,
  title={Your Article Title},
  author={Author, First and Author, Second},
  journal={Journal Name},
  volume={1},
  pages={1--10},
  year={2024},
  publisher={Publisher Name}
}
```

## Features

- ✅ ACM conference paper format
- ✅ Clean and professional layout
- ✅ Automatic formatting of authors and affiliations
- ✅ ACM CCS categories and keywords support
- ✅ Bibliography with ACM citation style
- ✅ Artifact appendix section
- ✅ Support for figures, tables, and equations
- ✅ Cross-referencing support

## Customization

The template uses the `clean-acmart` package. For advanced customization options, refer to the [clean-acmart documentation](https://typst.app/universe/package/clean-acmart/).

## Contributing

Contributions are welcome! If you find any issues or have suggestions for improvements:

1. Fork the repository
2. Create a new branch for your changes
3. Make your changes and commit them
4. Submit a pull request

## License

This template is maintained by the University of Kassel. Please check with the repository maintainers for specific license information.

## Resources

- [Typst Documentation](https://typst.app/docs/)
- [Typst Universe](https://typst.app/universe/) - Package repository
- [clean-acmart Package](https://typst.app/universe/package/clean-acmart/)
- [ACM Style Guide](https://www.acm.org/publications/authors/reference-formatting)

## Support

For issues or questions about this template, please open an issue in the [GitHub repository](https://github.com/ds-ukassel/seminar-template-typst/issues).
