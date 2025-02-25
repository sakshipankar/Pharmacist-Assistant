# Pharmacist-Assistant
1. Project Overview
This project uses Optical Character Recognition (OCR) and Natural Language Processing (NLP) to extract medicine names from handwritten prescriptions and match them with a pharmacy’s stock database.

Key Features:

Extracts text from handwritten prescriptions using Tesseract OCR.
Matches extracted medicines with pharmacy stock.
Automatically generates medicine orders.
Flask API for easy integration into pharmacy systems.
2. Environment Setup & Installation
Step 1: Clone the Repository
Open a terminal or command prompt.
Run the following command:
git clone https://github.com/your-username/pharmacist-assistant.git
Navigate to the project directory:
cd pharmacist-assistant
Step 2: Set Up a Virtual Environment
To keep dependencies organized, create and activate a virtual environment.

For Windows:

Run python -m venv venv
Activate the virtual environment: venv\Scripts\activate
For macOS/Linux:

Run python3 -m venv venv
Activate the virtual environment: source venv/bin/activate
Step 3: Install Dependencies
Run the following command to install required libraries:
pip install -r requirements.txt

If requirements.txt is missing, install manually:
pip install opencv-python pytesseract flask numpy pandas

Step 4: Install Tesseract OCR
Tesseract is required for text extraction.

For Windows:

Download Tesseract OCR from the official website: https://github.com/UB-Mannheim/tesseract/wiki
Install it and note the installation path (e.g., C:\Program Files\Tesseract-OCR).
For Linux (Ubuntu/Debian):
Run the following command:
sudo apt install tesseract-ocr

For macOS:
Run the following command:
brew install tesseract

After installation, set the Tesseract path (Windows only):
setx TESSDATA_PREFIX "C:\Program Files\Tesseract-OCR\tessdata"

3. Running the Code
Step 5: Start the Flask API
Run the following command:
python src/main.py

The API will start at: http://127.0.0.1:5000

Step 6: Testing the OCR Module
To check if OCR is working correctly, run:
python src/ocr_module.py --image sample_prescription.jpg

This will extract text from the sample prescription and display it.

4. Project Workflow
Upload Prescription: The user uploads a handwritten prescription image.
OCR Processing: The system extracts text from the image using Tesseract OCR.
NLP-Based Text Cleaning: The extracted text is cleaned and filtered using NLP techniques.
Medicine Matching with Stock Database: The cleaned text is matched against the pharmacy’s database.
Automatic Order Generation: The system generates an order with available medicines and suggests alternatives for unavailable ones.
