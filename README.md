# 📄 PDF Text Extractor & Metadata Viewer

This Python script allows you to extract and view text content from PDF files and also displays basic metadata like number of pages and document language. It supports saving the extracted text as either a `.txt` or `.docx` file.

---

## 📚 Features

- ✅ Lists all available PDFs in the current directory
- ✅ Lets you select a PDF interactively via terminal
- ✅ Extracts text using `pdfminer`
- ✅ Displays metadata: number of pages and detected language (if available)
- ✅ Allows saving extracted text as:
  - `.txt` file
  - `.docx` file (cleaned of control characters)
- ✅ Supports Unicode content

---

## ⚙️ Requirements

Install the required libraries:

```bash
pip install pdfminer.six python-docx
```

> `re` and `os` are standard libraries and come preinstalled with Python.

---

## 🚀 How to Use

1. **Place all your PDFs in the script directory.**
2. **Run the script:**

```bash
python main.py
```

3. **Select a PDF by its number from the list.**
4. **The script will:**
   - Display number of pages and language
   - Print extracted text
   - Ask how you want to save the extracted content

5. **Choose how to save:**
   - Option 1: Save as `.txt`
   - Option 2: Save as `.docx`
   - Option 3: Don't save (just view)

---

## 📝 Output Files

Saved output files are named using this format:

```
original_filename_extracted.txt
original_filename_extracted.docx
```

They will be saved in the same directory as the script.

---

## 🔧 Code Structure Overview

### `list_pdfs_in_directory(directory)`
Lists all PDF files in the current directory.

### `extract_text_from_pdf(pdf_path)`
Extracts plain text from the selected PDF using `pdfminer`.

### `get_pdf_metadata(pdf_path)`
Extracts:
- Number of pages
- Language (if available in metadata)

### `save_extracted_text(text, filename, file_format)`
Saves the extracted text to `.txt` or `.docx`. For `.docx`, it also:
- Cleans control characters
- Writes paragraphs using `python-docx`

### `get_save_option()`
Prompts the user to choose the desired output format interactively.

---

## ⚠️ Notes

- Extraction quality depends on the structure of the PDF. Some PDFs (like scanned images) may not extract text unless OCR is applied.
- Make sure `pdfminer.six` and `python-docx` are installed.
- The script does not yet handle encrypted PDFs.

---

## 👨‍💻 Author

**Wolfie Crypto**  
Lightweight PDF reader and extractor script designed for accessibility and quick use.

---

## 📃 License

This project is available under the **MIT License**.

---

Enjoy the simplicity of extracting and working with PDF content from your terminal!
