📌 E-KYC Automation System

A fully automated e-KYC (Electronic Know Your Customer) system built using Computer Vision, Deep Learning, OCR, and Streamlit.
This application extracts information from government ID cards (Aadhaar/PAN), verifies the user’s face against the ID card photo, and stores verified data securely in a MySQL database.

🚀 Features
Feature	Description
🧠 OCR-Based Text Extraction	Uses EasyOCR to extract Name, DOB, Father's name, and ID number.
👤 Face Verification	Uses DeepFace + HaarCascade to compare uploaded face image with ID card photo.
🗄️ Database Storage	Stores extracted information and face embeddings in MySQL.
🔁 Duplicate Detection	Automatically detects if a user is already registered.
🧩 Modular Code Structure	Easy to extend for other identity documents.
💻 Streamlit UI	Simple upload-based interface. No manual entry required.

🏗️ System Workflow
User → Uploads ID Card + Face Image  
     → OCR + Face Extraction  
     → Face Verification  
         ├── ❌ Failed → Stop  
         └── ✅ Passed → Extract Data + Generate Embeddings  
 → Check Duplicacy  
         ├── Found → Return Existing Record  
         └── Not Found → Save to MySQL  
🛠️ Technologies Used
Category	Tools/Frameworks
UI	Streamlit
OCR	EasyOCR
Face Recognition	DeepFace (FaceNet), Haarcascade
Backend	Python
Database	MySQL
ML Tools	OpenCV, NumPy, TensorFlow/Keras

