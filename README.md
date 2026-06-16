# Medical-Chatbot : 🩺 AI-Powered Medical Chatbot

An intelligent, conversational medical assistant built using Large Language Models (LLMs) and Retrieval-Augmented Generation (RAG). This chatbot processes medical documents, generates vector embeddings, and retrieves highly relevant context to answer user queries accurately. 

Designed with a lightweight Flask backend and optimized for cloud deployment.

## 🚀 Tech Stack

* **Framework:** Flask, Gunicorn (Production Server)
* **AI & Orchestration:** LangChain (Core, Community, Pinecone, Groq integrations)
* **Vector Database:** Pinecone
* **Embeddings:** HuggingFace `sentence-transformers`
* **Document Processing:** `pypdf`, LangChain Text Splitters
* **Language:** Python 3.11

## ✨ Features

* **Retrieval-Augmented Generation (RAG):** Grounds LLM responses in factual medical data to reduce hallucinations.
* **Semantic Search:** Uses Pinecone vector database for lightning-fast, highly relevant context retrieval.
* **Document Ingestion:** Automatically parses and splits complex medical PDFs into digestible chunks for embedding.
* **Production-Ready:** Configured with Gunicorn and optimized dependency resolution for seamless deployment on platforms like Render.

## 🛠️ Local Setup

### STEPS:
Clone the repository

```bash
git clone https://github.com/shreyavni/Medical-Chatbot.git
```


### STEP 01. Create the virtual environment and activate the environment
```bash
python -m venv medibot
source medibot/Scripts/activate
```


### STEP 02- install the requirements
```bash
pip install -r requirements.txt
```


### STEP 03- Create a `.env` file in the root directory and add your Pinecone & openai credentials as follows:
```bash
PINECONE_API_KEY = "xxxxxxxxxxxxxxxxxxxxxxxxxxxxx"
OPENAI_API_KEY = "xxxxxxxxxxxxxxxxxxxxxxxxxxxxx"
```


### STEP 04- Run the application
```bash
python app.py
```

*The app will be available at http://127.0.0.1:5000/*

## 🌐 Deployment
This project is fully configured for deployment on Render.

1. Connect the repository to a new Render Web Service.
2. Set the Environment to Python 3.
3. Under Environment Variables, set PYTHON_VERSION to 3.11.0.
4. Build Command: pip install -r requirements.txt
5. Start Command: gunicorn app:app (Adjust app:app if your main file is named differently).
6. Add your GROQ_API_KEY and PINECONE_API_KEY to Render's environment variables.

## 🤝 Contributing
Contributions, issues, and feature requests are welcome! Feel free to check the issues page.

***Developed by Avni Shukla***
