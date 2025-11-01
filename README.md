# 🧾 OCR Images to Excel

This project extracts text from images using **Tesseract OCR** and exports the recognized text into an **Excel file** for easy data analysis and manipulation.

---

## 🚀 Features

- 🖼️ Extracts text from image files (`.jpg`, `.png`, etc.)
- 🧠 Uses **Tesseract OCR** for accurate text recognition
- 🧹 Supports preprocessing to improve OCR results
- 📊 Automatically saves extracted text into an Excel file (`.xlsx`)
- 💬 Supports multiple languages (English, French, etc.)

---

## ⚙️ Installation

### 1. Clone the repository

```
git clone git@github.com:MadaniRiad/OCR_images_to_Excel.git
cd OCR_images_to_Excel
```

### 2. Create and activate a Conda environment
```
conda create -n ocr_env python=3.12
conda activate ocr_env
```
### 3. Install dependencies
```
conda install -c conda-forge tesseract pytesseract pillow pandas openpyxl
```

If you haven’t installed Tesseract system-wide yet:

- Linux: sudo apt-get install tesseract-ocr
- macOS: brew install tesseract
- Windows: Download from Tesseract GitHub


### 🧠 Example Code Snippet
```
from PIL import Image
import pytesseract
import pandas as pd

image_path = "image_exemple.jpg"
image = Image.open(image_path)

# Extract text
texte = pytesseract.image_to_string(image, lang='fra')

# Save to Excel
df = pd.DataFrame({"Texte_extrait": [texte]})
df.to_excel("texte_extrait.xlsx", index=False)

print("✅ Texte extrait et enregistré dans texte_extrait.xlsx")
```

### 🧩 Project Structure
```
OCR_images_to_Excel/
│
├── ocr_to_excel.py        # Main script for text extraction
├── requirements.txt        # (Optional) Dependencies
├── image_exemple.jpg       # Sample image
├── texte_extrait.xlsx      # Generated output
└── README.md               # Project documentation
```

### 📚 Requirements

- Python ≥ 3.8
- Tesseract OCR installed
- Conda or pip environment
- Internet connection (for package installation)

### 🤝 Contributing

Contributions are welcome!
Feel free to fork this repo, create a branch, and submit a pull request.



