# 🎓 Scholar AI

## 📖 About
**Scholar AI** is an advanced, AI-powered study companion designed to streamline the learning process. By leveraging Google's Gemini 1.5 Flash models, it transforms raw study materials—PDFs, Word documents, and audio recordings—into structured, actionable learning aids.

## ✨ Core Features
- **Smart Summarization:** Instantly distills complex documents into concise, markdown-formatted summaries with key points highlighted.
- **Automated Flashcards:** Generates Q&A flashcards from uploaded content to aid active recall.
- **Interactive Quizzes:** Creates multiple-choice quizzes to test comprehension and retention.
- **Multi-Format Support:** Handles PDF, DOCX, TXT, and Audio (MP3/WAV) inputs seamlessly.
- **Export Capabilities:** precision-formatted DOCX exports for offline study.

---

## 🛠️ Technology Stack

### **Frontend**
- **Framework:** Angular 18+ (Standalone Architecture)
- **Design:** Custom SCSS with Glassmorphism aesthetic & Dark Mode
- **Authentication:** Firebase Auth (Secure Email & Google Sign-In)
- **Deployment:** Vercel / Firebase Hosting

### **Backend**
- **Runtime:** Python 3.11+ (Flask)
- **AI Engine:** Google Gemini 1.5 Flash (Optimized for low-latency single-shot generation)
- **Speech Processing:** Google Cloud Speech-to-Text & Mutagen
- **Infrastructure:** Vercel Serverless Functions / Google Cloud Run

---

## 🚀 Setup & Deployment

### **Prerequisites**
- Node.js 18+
- Python 3.11+
- Google Cloud Project (with Gemini API enabled)
- Firebase Project

### **Environment Variables**
Create a `.env` file in `backend-functions/` or configure in your deployment dashboard:
```bash
GEMINI_API_KEY=your_api_key_here
GOOGLE_APPLICATION_CREDENTIALS=path/to/credentials.json # Optional for GCS
```

### **1. Vercel Deployment (Recommended)**
Scholar AI is optimized for Vercel. 
1. Import this repository into Vercel.
2. Add `GEMINI_API_KEY` to Environment Variables.
3. Deploy.
*(The included `vercel.json` handles all build & route configuration automatically)*

### **2. Local Development**
**Frontend:**
```bash
cd frontend-angular
npm install
npm start -- --port 4200
```
**Backend:**
```bash
cd backend-functions
pip install -r requirements.txt
python main.py
```
*(Access the app at http://localhost:4200)*

---

## 📂 Project Structure
- `frontend-angular/`: The complete Angular client application.
- `backend-functions/`: The Flask API server handling AI processing and file intake.
- `deploy.sh`: Utility script for Google Cloud deployments.
- `vercel.json`: Configuration for Vercel Serverless deployment.

---

**Developed by Devansh V Purohit**
