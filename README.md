# 🤖 AI Personal Assistant

An **AI-powered Personal Assistant** built with **Python, Flask, Google Gemini API, and RAG (Retrieval-Augmented Generation)**.

The application provides an interactive web interface where users can ask questions, get AI-generated responses, and summarize emails. The project is designed to be extended with document-based question answering using a RAG pipeline.

## 🚀 Features

* 🤖 AI-powered personal assistant
* 💬 Ask questions and receive intelligent responses
* 🧠 Google Gemini API integration
* 📚 RAG (Retrieval-Augmented Generation) pipeline
* 📄 Document-based information retrieval
* ✉️ Email summarization
* 🌐 Flask web application
* 🎨 HTML/CSS frontend
* 🔐 Environment variables for API key security
* 🔌 REST API endpoints
* ⚡ JSON responses for frontend integration

## 🧠 AI Capabilities

### 1. Personal Assistant

Users can send questions through the web interface.

The Flask backend sends the question to the Gemini model with a system instruction to behave as a helpful personal assistant.

### 2. Email Summarization

The application accepts email text and generates a concise **2–3 sentence summary** using Gemini.

This can be useful for quickly understanding long emails.

### 3. RAG Pipeline

The project also includes a **Retrieval-Augmented Generation (RAG)** pipeline.

The RAG architecture can be used to:

```text
User Question
      ↓
Query Processing
      ↓
Embedding Generation
      ↓
Vector Database
      ↓
Similarity Search
      ↓
Relevant Documents
      ↓
Gemini
      ↓
Generated Answer
```

RAG allows the assistant to generate answers based on information retrieved from your own documents instead of relying only on the model's built-in knowledge.

## 🛠️ Technologies Used

| Technology        | Purpose                                |
| ----------------- | -------------------------------------- |
| Python            | Backend programming                    |
| Flask             | Web framework                          |
| Google Gemini API | AI text generation                     |
| Google GenAI SDK  | Gemini API integration                 |
| RAG               | Retrieval-augmented question answering |
| Vector Database   | Document/vector retrieval              |
| HTML5             | Frontend structure                     |
| CSS3              | Frontend styling                       |
| Jinja2            | Flask templating                       |
| python-dotenv     | Environment variable management        |
| Git               | Version control                        |
| GitHub            | Source code hosting                    |

## 📂 Project Structure

```text
AI-Assistant/
│
├── main.py
│
├── templates/
│   └── index.html
│
├── static/
│   └── style.css
│
├── .gitignore
│
└── README.md
```

> Additional RAG-related files and modules can be added as the project grows.

## 🔌 API Endpoints

### Home

```http
GET /
```

Loads the AI Assistant web interface.

### Ask Assistant

```http
POST /ask
```

Accepts a question and returns an AI-generated response.

Example form data:

```text
question=What is machine learning?
```

Example response:

```json
{
    "response": "Machine learning is a branch of artificial intelligence..."
}
```

### Summarize Email

```http
POST /summarize
```

Accepts email text and returns a concise summary.

Example form data:

```text
email=Your email content here...
```

Example response:

```json
{
    "response": "The email discusses..."
}
```

## 🔐 Environment Variables

The Gemini API key is loaded using `python-dotenv`.

Create a `.env` file in the project root:

```env
GEMINI_API_KEY=your_gemini_api_key_here
```

The application loads the key using:

```python
from dotenv import load_dotenv
import os

load_dotenv()

api_key = os.getenv("GEMINI_API_KEY")
```

### ⚠️ Security

**Never upload your `.env` file or API keys to GitHub.**

The project `.gitignore` already includes:

```text
.env
```

## ⚙️ Installation

### 1. Clone the repository

```bash
git clone https://github.com/mujammilkurundwad/AI-Assistant.git
```

### 2. Enter the project directory

```bash
cd AI-Assistant
```

### 3. Create a virtual environment

Windows:

```bash
python -m venv venv
```

### 4. Activate the virtual environment

```bash
venv\Scripts\activate
```

### 5. Install dependencies

```bash
pip install flask python-dotenv google-genai
```

Install any additional packages required by your RAG pipeline separately.

## ▶️ Run the Application

Start the Flask server:

```bash
python main.py
```

The application will be available at:

```text
http://127.0.0.1:5000/
```

Open the URL in your browser.

## 🔄 Application Flow

The basic assistant flow is:

```text
User
 ↓
Web Interface
 ↓
Flask
 ↓
/ask endpoint
 ↓
Gemini API
 ↓
AI Response
 ↓
Frontend
```

The email summarization flow:

```text
Email Text
 ↓
Flask /summarize
 ↓
Gemini API
 ↓
Email Summary
 ↓
Frontend
```

The RAG flow:

```text
Documents
 ↓
Document Loading
 ↓
Text Splitting
 ↓
Embeddings
 ↓
Vector Store
 ↓
Similarity Search
 ↓
Relevant Context
 ↓
Gemini
 ↓
Final Answer
```

## 📈 Future Improvements

* [ ] Complete RAG integration with the Flask interface
* [ ] Upload PDF and text documents
* [ ] Add conversational chat history
* [ ] Add voice input
* [ ] Add text-to-speech
* [ ] Add document question answering
* [ ] Add user authentication
* [ ] Add conversation memory
* [ ] Improve frontend UI/UX
* [ ] Add streaming AI responses
* [ ] Add error handling and API rate-limit handling
* [ ] Deploy the application online
* [ ] Add Docker support
* [ ] Add production WSGI server

## 🚧 Project Status

**In Development**

This project is being developed as a personal AI assistant that combines:

* Flask web development
* Generative AI
* Google Gemini API
* RAG
* Vector search
* Document processing
* Email summarization

## 👨‍💻 Author

**Mujjamil Kurundwad**

GitHub:
https://github.com/mujammilkurundwad

---

⭐ If you find this project interesting, consider giving the repository a star!
