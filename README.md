# 🕵️‍♂️ eFato: Political Information Verification Backend

> A robust backend developed for real-time fact-checking and political information verification, leveraging Artificial Intelligence (Gemini) and advanced search engines. Developed as part of an information integrity verification project.

[![License](https://img.shields.io/badge/license-ISC-blue)](LICENSE)
[![Tech](https://img.shields.io/badge/Stack-Node.js%20%7C%20Express-green)](https://nodejs.org/)
[![AI](https://img.shields.io/badge/AI-Gemini%20%7C%20Tavily-orange)](https://ai.google.dev/)

---

## 📋 Project Overview

The **eFato Backend** is the processing engine behind the eFato platform, designed to combat political misinformation. The system receives suspicious questions or texts, performs real-time searches in official databases (Chamber of Deputies, Senate) and across the web, and uses state-of-the-art language models to generate critical and well-founded analyses.

### Key Features
* **AI-Powered Fact Analysis:** Integration with Google Gemini for interpreting and checking political claims.
* **Real-Time Search:** Utilization of Tavily Search to capture the latest news and web data.
* **Official Data Integration:** Framework ready for querying government APIs and transparency portals.
* **RAG Pipeline (Retrieval-Augmented Generation):** Intelligent orchestration between data retrieval and text generation for maximum accuracy.

---

## 🛡️ Data Security & Integrity

Since the application handles **Public Interest Information**, data accuracy and traceability are core requirements of this project, ensuring that sources are verifiable and analyses are impartial.

### Implemented Standards:
* **Source Verification:** All data retrieved via Tavily or official APIs is processed to ensure information provenance.
* **Input Sanitization:** Implementation of strict filters to prevent code injection and ensure only valid queries are processed.
* **Audit Logs:** Detailed monitoring of request flow to track AI pipeline behavior.
* **Modular Architecture:** Clear separation between integration, processing, and data delivery layers (LLM).

---

## 🛠️ Tech Stack

* **Backend:** Node.js, Express framework
* **AI & LLM:** Google Generative AI (Gemini SDK)
* **Search & Retrieval:** Tavily API, Axios for REST integrations
* **Data Processing:** xml2js, date-fns

---

## ⚙️ Getting Started (Local Development)

Follow these steps to set up the project environment locally.

### 1. Prerequisites
Ensure you have installed:
* [Git](https://git-scm.com)
* [Node.js](https://nodejs.org/) (v18.0.0 or higher)
* API keys for [Google Gemini](https://ai.google.dev/) and [Tavily](https://tavily.com/)

### 2. Configuration (`.env`)
Create a `.env` file in the root of the `/src` directory and configure the environment variables as shown below:

```env
PORT=3000
GEMINI_API_KEY="your_gemini_key_here"
TAVILY_API_KEY="your_tavily_key_here"
```

### 3. Setup and Execution

**1. Clone the repository**
```bash
git clone https://github.com/LouisyRodrigues7/efato_backend.git
cd efato_backend
```

**2. Install Dependencies**
```bash
npm install
```

**3. Run the Backend**
```bash
# Development mode (with nodemon)
npm run dev

# Production mode
npm start
```

---

## 🚀 Core API Endpoints

| Method | Endpoint | Description | Scope/Context |
| :--- | :--- | :--- | :--- |
| POST | `/api/analyze` | Receives a text or question and returns a detailed analysis. | AI Processing & Search |

---

## 📈 Future Improvements (What We'd Do Next)

If we had more development time, we would plan to implement:

* **Result Caching:** Using Redis to store frequent queries and reduce API costs.
* **Analytics Dashboard:** Data visualization on the most searched political topics.
* **Multi-Model Support:** Integration with other LLMs (such as GPT-4 or Claude) for analysis cross-checking.
* **Advanced Authentication:** Implementation of JWT to protect analysis endpoints against abuse.

---

## 👥 Authors & Project Team

* **Louisy Rodrigues** - Lead Developer & Software Architect 
* **Rihan Cabral** - Front-End Developer & UX/UI Designer
* **Eduardo Henrique** - Front-End Developer
* **Guilherme Jacques** - Process Analyst
* **André Maurilio** - Back-End Developer

**Academic Advisor:** Prof. Rodrigo Rios, Prof. Rafaella Leandra Souza do Nascimento

**Tech English Course Professor:** Prof. Leonardo Trevas
