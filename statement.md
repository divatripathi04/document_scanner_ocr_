# Project Statement

## Document Scanner Using OCR

*Name:* Diva Tripathi  
*Registration No.:* 24BAI10692  
*Domain:* Computer Vision

## Problem Statement

Images captured using a phone or camera can contain tilted documents, unwanted background areas, uneven lighting, and perspective distortion. These problems can reduce the readability of the document and make text extraction more difficult.

The objective of this project is to create a simple document scanner that identifies a document from an image, corrects its perspective, improves its appearance, and extracts the text using OCR.

## Proposed Solution

The project is developed in Python using OpenCV and EasyOCR and is organized into three main modules.

### Module 1 — Preprocessing

The input image is validated and processed to identify document edges and boundaries. The document corners are detected, perspective distortion is corrected, and the resulting scan is enhanced for better readability.

### Module 2 — OCR

The processed document is given to EasyOCR for text recognition. The extracted text is stored along with confidence values, allowing low-confidence results to be filtered using a selected threshold.

### Module 3 — Export

The processed scan and extracted OCR results can be saved in PNG, TXT, JSON, and PDF formats. The application also records important pipeline events through logging.

## Functional Requirements

1. The system should accept and validate supported image files.
2. It should identify and straighten the document using Computer Vision techniques.
3. It should extract text from the processed document using EasyOCR.
4. It should provide an option to filter OCR results based on confidence.
5. It should save the processed results in different formats.
6. It should provide clear handling of common processing errors.

## Non-Functional Requirements

- *Performance:* Process normal document images within a reasonable time.
- *Reliability:* Handle invalid inputs and processing failures appropriately.
- *Usability:* Provide simple command-line options and understandable messages.
- *Maintainability:* Separate preprocessing, OCR, exporting, and utility functions into modules.
- *Testing:* Use automated tests to verify important project functionality.
- *Logging:* Maintain records of significant pipeline operations.

## Technology Stack

- Python
- OpenCV
- NumPy
- EasyOCR
- FPDF2
- pytest

## Testing

The project includes automated tests covering preprocessing and OCR functionality. The current test suite contains *13 tests*, and the development test run completed with:

```text
13 passed
