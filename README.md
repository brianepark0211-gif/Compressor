# PDF Consolidator

Convert a folder of `.ppt`, `.pptx`, and `.pdf` files into one compressed
`consolidated.pdf`.

## Requirements

- Python 3.10+
- LibreOffice available on `PATH` as `libreoffice` or `soffice`
- Ghostscript available on `PATH` as `gswin64c`, `gswin32c`, or `gs`

Install the Python dependency:

```powershell
pip install -r requirements.txt
```

## Usage

```powershell
python .\pdf_consolidator.py "C:\path\to\folder"
```

By default, the tool writes `consolidated.pdf` in the current directory. Files
are processed in case-insensitive filename order. PowerPoint files are converted
to temporary PDFs with LibreOffice, all PDFs are merged, and Ghostscript
compresses the merged PDF.

Common options:

```powershell
python .\pdf_consolidator.py "C:\path\to\folder" --overwrite
python .\pdf_consolidator.py "C:\path\to\folder" -o "C:\path\out.pdf"
python .\pdf_consolidator.py "C:\path\to\folder" --quality screen --verbose
```
