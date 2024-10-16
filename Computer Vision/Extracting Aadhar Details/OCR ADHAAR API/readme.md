# Flask OCR and Aadhaar Information Extraction API

This project is a Flask-based API that extracts relevant information (like Name, Gender, Date of Birth, and Aadhaar number) from images of Aadhaar cards using the `EasyOCR` library. The API supports both **English** and **Hindi** text extraction.

---

## Features

- **Optical Character Recognition (OCR)**: Uses `EasyOCR` to read text from Aadhaar card images.
- **Multi-language Support**: Supports both **English** and **Hindi** text extraction.
- **Regex Matching**: Uses regular expressions to identify key pieces of information such as:
  - First, Middle, and Last Names
  - Gender
  - Date of Birth (DOB)
  - Year of Birth (YOB)
  - Aadhaar Number
- **REST API**: Provides a `/extract` POST endpoint to process Aadhaar card images.

---

## How It Works

1. **User sends an Aadhaar card image** to the `/extract` endpoint via a POST request.
2. The **EasyOCR** library reads the image and extracts the text in **English** and **Hindi**.
3. The text is processed to extract important details such as:
   - First Name, Middle Name, Last Name
   - Gender
   - Date of Birth or Year of Birth
   - Aadhaar Number
4. The extracted information is returned in JSON format.

---

## Install Required Libraries
Install all required Python libraries using the requirements.txt file:


`pip install -r requirements.txt`

This will install:

 - Flask (For creating the API server)
 - EasyOCR (For extracting text from images)
 - regex (For pattern matching in the text)

## How to Run the API
Once you’ve installed all the necessary libraries, follow these steps to run the Flask application:

Start the Flask development server:

`python app.py`

The Flask API will be running on http://127.0.0.1:5000/.
