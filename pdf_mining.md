# PDF file mining
## Educational
### Light reads
- [Portable Document Format: An Introduction for Programmers
by Kas Thomas](http://preserve.mactech.com/articles/mactech/Vol.15/15.09/PDFIntro/index.html), a piece of history introducing the technical details of the PDF format
- [Hand-coded PDF tutorial](https://brendanzagaeski.appspot.com/0005.html), basic introduction to the PDF format inspired by the above
- [Notes on the structure of PDF files](https://shreevatsa.github.io/site/pdf-structure.html), and how to convert a PDF file to a nice-looking text file with `mutool`and `qpdf`
- [Inside the PDF File Format](https://commandlinefanatic.com/cgi-bin/showarticle.cgi?article=art019), clear step-by-step introduction to a PDF file structure
- [Adobe®, Introduction to the Insides of PDF](https://www.adobe.com/technology/pdfs/presentations/KingPDFTutorial.pdf), good example-based description of the internal structure of a PDF document and its programming language

### Heavy reads
- [Adobe PDF Reference site](https://www.adobe.com/devnet/pdf/pdf_reference.html)
  - [PDF Reference, version 1.7](https://www.adobe.com/content/dam/acom/en/devnet/pdf/pdf_reference_archive/pdf_reference_1-7.pdf)

## Tools
### Online tools
- [pdf2data](https://pdf2data.online)
### Libraries and utilities
- [Ghostscript](https://www.ghostscript.com/), PS and PDF language interpreter (available also as a library). It can be used for [conversion between formats](https://www.ghostscript.com/doc/current/Use.htm#Output_device), [font embedding](https://www.karlrupp.net/2016/01/embed-all-fonts-in-pdfs-latex-pdflatex/), paper-size adjustments, etc. 
- [xpdf-tools](https://www.xpdfreader.com/), open source project including a PDF viewer along with a collection of command line tools which perform various functions on PDF files: **pdftotext**, pdftops, pdftoppm, pdftopng, pdftohtml, **pdfinfo**, **pdfimages**, **pdffonts**, pdfdetach
- pdftk :grey_question:
- [PyMuPDF](https://github.com/pymupdf/PyMuPDF), Python wrapper for MuPDF
- PyPDF2 :grey_question:

#### Low-level libraries
- [PDFxStream](https://www.snowtide.com/), commercial library featuring text extraction, image extraction, form reading and filling and low level PDF handling capabilities.
- [iText](https://itextpdf.com)
- [MuPDF](https://mupdf.com/)
- [Xpdf]](https://www.glyphandcog.com/)
- libpoppler, Poppler is a PDF rendering library based on the xpdf-3.0 code base
- pdfminer, pure Python PDF parser
- [PDFBox](https://pdfbox.apache.org/), extract texts, split & merge, fill forms, preflight, print, save as image, creation, signing. Used as backend by Apache Tika.
- [qpdf](http://qpdf.sourceforge.net/), program and C++ library to perform content-preserving transformations to PDFs: merge, split, rotate, decompress, decrypt

