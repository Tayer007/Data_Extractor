# Document Data Extractor

A powerful tool for extracting text, tables, and images from PDF documents, Word files, and PowerPoint presentations.

![Document Data Extractor Screenshot](screenshots/main-interface.png)

## Features

- **Extract text** from PDF, DOCX, and PPTX files
- **Extract tables** and save them as CSV files
- **Extract images** embedded in documents
- **User-friendly GUI** with preview capabilities
- **Multilingual support** for text extraction

## Installation

### Option 1: Install from Release (Recommended)

1. Download the latest installer from the [Releases](https://github.com/yourusername/document-data-extractor/releases) page
2. Run `DocumentDataExtractor_Setup.exe` from the downloaded files
3. Follow the installation wizard to complete the setup
4. When first launching the application, you'll be prompted for a password
   - Use the password provided to you separately
   - This password is needed only for the first run

![Installation Screenshot](screenshots/installer.png)

### Option 2: Manual Installation (For Developers)

1. Clone the repository:
   ```
   git clone https://github.com/yourusername/document-data-extractor.git
   cd document-data-extractor
   ```

2. Install dependencies:
   ```
   pip install -r requirements.txt
   ```

3. Run the application:
   ```
   python main.py
   ```

## How to Use

1. **Launch the application** from your Start Menu or Desktop shortcut
2. **Select a document** by clicking the "Browse..." button
   - Supported formats: PDF, DOCX, PPTX
3. **Choose an output folder** where extracted data will be saved
4. **Select extraction options**:
   - Text extraction
   - Table extraction
   - Image extraction
5. **Click "Extract Data"** to begin the process
6. **View the results** in the preview tabs or open the output folder

![Extraction Process](screenshots/extraction-process.png)

## Output Structure

The program creates a structured output with the following organization:

```
output_directory/
├── extracted_text.txt         # All extracted text
├── tables/                    # Directory containing CSV files
│   ├── filename_page1_table0.csv
│   ├── filename_page2_table0.csv
│   └── ...
└── images/                    # Directory containing extracted images
    ├── page1_img1.png
    ├── page1_img2.jpg
    └── ...
```

## Applications

Document Data Extractor is useful for:

- **Data analysis** - Extract data from PDFs into CSV for analysis
- **Content migration** - Move content from documents to other systems
- **Text mining** - Extract large volumes of text for processing
- **Image collection** - Extract embedded images for reuse
- **Document archiving** - Extract and store content in accessible formats

## Limitations

- PDF extraction may not work perfectly with heavily formatted or scanned PDFs
- Complex tables might not maintain all formatting when extracted
- For scanned PDFs, OCR functionality is not included in this version

## Troubleshooting

### Common Issues

1. **Password prompt appears every time**
   - This indicates the password is incorrect
   - Contact your administrator for the correct password

2. **No tables extracted from PDF**
   - Some PDFs use images for tables, which cannot be extracted as structured data
   - Try using a PDF with proper table structures

3. **Missing images in output**
   - Some document formats embed images in ways that make extraction difficult
   - Try a different document or format

### Getting Help

If you encounter any issues or have questions:
- Check the [GitHub Issues](https://github.com/yourusername/document-data-extractor/issues) page
- Submit a new issue with details about your problem
- Include information about your document format and operating system

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

- PDF extraction powered by PyPDF2 and pdfplumber
- Word document extraction via python-docx
- PowerPoint extraction using python-pptx
- Image processing with PyMuPDF and Pillow
