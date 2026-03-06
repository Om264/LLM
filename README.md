# ⬡ LLM Universe — Large Language Models Explained

> An interactive educational website about Large Language Models (LLMs), built as a university project.

![LLM Universe](https://img.shields.io/badge/LLM-Universe-00d4ff?style=for-the-badge)
![HTML](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Flask](https://img.shields.io/badge/Flask-000000?style=for-the-badge&logo=flask&logoColor=white)

---

## 🌟 Features

| Feature | Description |
|---|---|
| 🧠 **8 Content Sections** | What is LLM, How It Works, Explainer, History, Models, Applications, Quiz, Ethics |
| 🎬 **Animated Explainer** | 7-scene interactive visual story for non-technical readers |
| 🎯 **15-Question Quiz** | Multiple choice quiz with instant feedback and score ring |
| 🔍 **Live Search** | Search any word across all website content with highlighted results |
| 🌐 **Bilingual** | Full English ↔ Chinese (中文) language switching |
| 🌙 **Dark / Light Mode** | Toggle between dark and light themes |
| 📧 **Email Grade System** | Professor can enter a grade (0–100) and it is emailed automatically |
| 📱 **Responsive** | Works on desktop, tablet, and mobile |

---

## 📁 Project Structure

```
llm-universe/
│
├── index.html        # Frontend — complete single-file website
├── backend.py        # Backend — Flask API server
├── requirements.txt  # Python dependencies
└── README.md         # This file
```

---

## 🚀 Quick Start

### 1. Clone the repository

```bash
git clone https://github.com/YOUR_USERNAME/llm-universe.git
cd llm-universe
```

### 2. Install Python dependencies

```bash
pip install -r requirements.txt
```

### 3. Run the backend

```bash
python backend.py
```

You should see:
```
LLM Universe Backend — Updated
http://localhost:5000
```

### 4. Open the website

Open your browser and go to:
```
http://localhost:5000
```

Or simply open `index.html` directly in your browser (search and explainer work without backend).

---

## 📧 Email Setup (Professor Grade Feature)

The grade email uses **EmailJS** (free service, no server needed).

1. Create a free account at [emailjs.com](https://www.emailjs.com)
2. Add an **Email Service** (e.g. Gmail) → copy the **Service ID**
3. Create an **Email Template** with these variables:
   - `{{grade}}` — the submitted grade
   - `{{feedback}}` — the feedback message
   - `{{project}}` — project name
   - `{{date}}` — submission date
4. Copy your **Public Key** from Account → API Keys
5. In `index.html`, replace these 3 values near the bottom of the `<script>`:

```javascript
emailjs.init("YOUR_PUBLIC_KEY");
const EJS_SERVICE  = "YOUR_SERVICE_ID";
const EJS_TEMPLATE = "YOUR_TEMPLATE_ID";
```

### Alternative: Flask SMTP Email (backend)

Set environment variables before running:

```bash
export SMTP_USER="your_gmail@gmail.com"
export SMTP_PASS="your_gmail_app_password"
python backend.py
```

> ⚠️ Use a **Gmail App Password**, not your main Gmail password.  
> Create one at: Google Account → Security → 2-Step Verification → App Passwords

---

## 🔌 API Endpoints

| Method | Endpoint | Description |
|---|---|---|
| `GET` | `/` | Serve frontend |
| `GET` | `/api/search?q=keyword` | Search content |
| `POST` | `/api/grade` | Submit professor grade + send email |
| `GET` | `/api/grade-log` | View all submitted grades |
| `POST` | `/api/quiz-submit` | Log quiz score |
| `GET` | `/api/stats` | LLM statistics data |
| `GET` | `/api/models` | LLM comparison table |

---

## 🎯 Quiz Questions

The quiz covers 15 topics:

1. Definition of LLMs
2. Transformer architecture
3. Tokenization
4. Text generation task
5. Softmax function
6. Attention mechanism
7. Self-attention equation
8. Pre-training
9. Fine-tuning
10. Known LLMs (GPT)
11. Embeddings
12. Temperature parameter
13. GPT creator (OpenAI)
14. Transformer advantages
15. LLM applications

---

## 🛠️ Technologies Used

**Frontend:**
- HTML5, CSS3, Vanilla JavaScript
- Google Fonts: Syne, IBM Plex Mono, Noto Sans SC
- EmailJS (grade email delivery)

**Backend:**
- Python 3.x
- Flask
- Flask-CORS
- smtplib (SMTP email)

---

## 👥 Created By

| Name |
|---|
| Abdulrahman Al-Harbi |
| Sara Al-Mutairi |
| Mohammed Al-Qahtani |
| Noura Al-Shehri |

---

## 📝 License

This project was created for educational purposes as a university assignment.

© 2025 LLM Universe. All rights reserved.
