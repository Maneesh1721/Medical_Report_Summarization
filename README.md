# 🚀 **MedScribeAI: Medical Report Summarization System** 🚀

## 🩺 **Overview**
Welcome to **MedScribeAI**, your advanced, web-based platform for seamless medical report summarization. Powered by **Flask**, **MongoDB**, **LangChain**, and **HuggingFace**, MedScribeAI is designed to streamline medical documentation, offering AI-powered summaries that make manual data extraction a thing of the past.

## 🧩 **Project Components**

### 🎨 **User Interface (UI)**
- **🔑 Login Page:**
  - **Purpose:** Authenticates users and directs them to the appropriate report upload sections based on credentials.
  - **Tech Stack:** HTML, CSS, JavaScript, Flask templates.

- **📤 Upload Pages:**
  - **Purpose:** Facilitates the upload of various medical reports such as doctor notes, scan results, and blood tests.
  - **Tech Stack:** HTML, CSS, JavaScript, Flask templates.

- **🖥️ Summary Display Page:**
  - **Purpose:** Displays AI-generated summaries with an option to download them as PDFs.
  - **Tech Stack:** HTML, CSS, JavaScript, Flask templates.

### 🛠️ **Application Logic (Flask Backend)**
- **🗂️ Flask Application:**
  - Manages routing, form submissions, and database interactions smoothly.
  - **Key Routes:**
    - `/`: Renders the login page.
    - `/login`: Authenticates users and redirects them based on their role.
    - `/upload_doctor_report`, `/upload_scan_report`, `/upload_blood_report`: Handles different report uploads.
    - `/create_patient`: Allows the creation of new patient records.
    - `/index`: The main dashboard for report uploads and processing.
    - `/upload`: Processes uploaded reports, generates summaries, and displays them.
    - `/download`: Downloads the summary as a professional PDF.

### 🗄️ **Data Storage**
- **💾 MongoDB:**
  - Serves as the central repository for patient details and uploaded report file paths.
  - Supports efficient data retrieval and updates.

- **📚 ChromaDB:**
  - Stores vectorized document representations for rapid retrieval during summarization.
  - Ensures precise search capabilities for summaries.

### 🔍 **Data Processing**
- **📄 PDF Handling:**
  - **Text Extraction:**
    - Extracts text from uploaded PDFs using `pdfplumber` and `PyPDFLoader`.
    - Prepares content for AI-driven summarization.

- **📝 Summarization Logic:**
  - **LangChain Integration:**
    - Utilizes the `Mistral-7B-Instruct-v0.3` model to generate structured and insightful summaries.
    - Processes extracted text with a finely-tuned prompt template.

### 🧠 **Model Integration**
- **🤖 HuggingFace Model:**
  - **Mistral-7B-Instruct-v0.3:**
    - A cutting-edge AI model that transforms raw text into coherent and accurate summaries.
    - Ensures patient reports are not only precise but also easy to understand.

### 📂 **File Handling**
- **🗄️ File Storage:**
  - Manages the upload, storage, and retrieval of report files and generated summaries.
  - Leverages Flask’s file handling to manage server-side files efficiently.

- **📝 PDF Generation:**
  - **PDF Creation:**
    - Converts AI-generated summaries into polished, downloadable PDF files using the `pdf_generator.py` script.
    - Delivers professional-grade summaries that are easy to distribute and review.

### 🛡️ **Logging and Error Handling**
- **📊 Logging:**
  - Tracks every step of the application using Python’s `logging` module.
  - Facilitates issue diagnosis and performance monitoring.

- **⚠️ Error Handling:**
  - Provides graceful exception handling with user-friendly error messages.
  - Logs errors for debugging and future reference, ensuring smooth application performance.

### 🌐 **Integration and Deployment**
- **🚀 Flask Server:**
  - Handles all HTTP requests efficiently, whether locally or on a web server.
  - Ensures minimal downtime and robust service delivery.

- **🌍 Deployment:**
  - Deployed for accessibility, scalability, and ease of maintenance.

## 📊 **Data Flow Overview**
1. **🔐 User Authentication:** Users log in and are directed to the appropriate report upload section based on their role.
2. **📥 Report Upload:** Medical reports are uploaded, stored, and linked to patient records in MongoDB.
3. **🔄 Text Extraction and Summarization:** Extracted text is processed and summarized using the AI model, then stored and displayed.
4. **📤 Summary Generation and Download:** Summaries are presented to users, who can download them as professional PDFs.

### 🤝 **Contribution and Contact**
We welcome contributions! Whether it’s a bug fix, a feature enhancement, or a new idea, feel free to open an issue or submit a pull request. Have questions? Reach out via [your-email@example.com](mailto:your-email@example.com).

### 📄 **License**
This project is licensed under the MIT License. See the LICENSE file for more details.
