# Lottery Number Checker

This is an OCR pipeline to check lotto max ticket(s)

  - Inputs: Image of lotto max ticket(s)
  - Outputs: ticket_results.csv 


You will need both python 3 and tesseract installed:

- Python 3: https://www.python.org/downloads/
 - Tesseract: https://tesseractocr.org/
 - Tesseract Git (for windows): https://github.com/UB-Mannheim/tesseract/wiki

You will also need an API key with https://dashboard.apiverve.com/

Sign up for a free account, go to api keys (below link) and copy that api for when the prompt asks for it (step 3)

https://dashboard.apiverve.com/apikey

## Requirements

| Package | Purpose | pip install |
| --- | --- | --- |
| os | Provides a way to interact with the operating system | N/A |
| cv2 | Provides computer vision functions for image processing | pip install opencv-python |
| numpy | Provides support for arrays and mathematical functions | pip install numpy |
| pytesseract | Provides a Python wrapper for the Tesseract OCR engine | pip install pytesseract |
| pandas | Provides support for data manipulation and analysis | pip install pandas |
| PIL | Provides support for opening, manipulating, and saving many different image file formats | pip install
pillow |
| requests | Provides support for making HTTP requests to websites | pip install requests |

## Steps

### 1. Check for latest image in image folder

  1. Import packages and read files
  2. Organize folders and find the latest images
  3. Check on tesseract installation for OCR operations

### 2. Read image text w/Manual Steps

  1. Crop Image w/MS Paint
      - process will open MS Pain, crop then save/close
  2. Apply Green Dots on outer corners of #s
      - must be pure green RGB (0,255,0) and use 5 pixel width and the brush tool
      - process will open MS Paint, crop then save/close
  3. Image will be processed for maximal readibility (color + perspective correction)
### 3. Connect to Lotto Max Website and check the latest draw
### 4. Bonus: Max-Millions & Max-Plus
- If max millions (jackpot > $50MM) - check (no API)
- Copy and paste the max million #s from:
https://www.olg.ca/en/lottery/play-lotto-max-encore/hub.html
    - Run the checker, export maxmillion_results.csv
- Copy and paste the max plus #s from:
https://www.olg.ca/en/lottery/play-lotto-max-encore/hub.html