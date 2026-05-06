# Document Transformation Benchmark: Traditional vs. AI

This project compares two different approaches for extracting structured data from PDF documents, specifically tailored for parliamentary reports and complex layouts.

## Comparison Engines
1. **PyMuPDF (Fitz)**: A traditional, high-performance engine that extracts plain text based on coordinates and document layers. Extremely fast but lacks structural understanding.
2. **Docling (IBM)**: A next-generation AI-powered engine that understands document structure, tables, and hierarchies, exporting directly to Markdown.

## Project Structure
- `inputs/`: Place your source PDF files here (ignored by git).
- `outputs/`: Generated results in `.txt` and `.md` formats (ignored by git).
- `benchmark_transformation.ipynb`: The main Jupyter Notebook to run the comparison.
- `requirements.txt`: Project dependencies with the stable Docling stack.

## Getting Started

### 1. Prerequisites
Ensure you have a Python environment (3.10+ recommended).

### 2. Installation
Install the required dependencies:
```bash
pip install -r requirements.txt
```

### 3. Usage
1. Place your PDF files in the `inputs/` folder.
2. Open `benchmark_transformation.ipynb` in your preferred editor (VS Code, JupyterLab).
3. Set the `PDF_PATH` variable to your target file.
4. Run the cells to compare performance and output quality.

## Stable Stack Note
To avoid dependency conflicts with Docling's AI motor, this project uses a specific version combination:
- `docling==2.0.0`
- `docling-core==2.0.0`
- `docling-parse==1.6.2`
