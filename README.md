# InsureLLM RAG Chatbot 🤖
<img width="1920" height="1080" alt="Screenshot (428)" src="https://github.com/user-attachments/assets/6da0a1ab-68c2-4194-8558-820b31c787ff" />

This repository contains the code for an intelligent chatbot built to answer questions about the internal knowledge base of a demo company, **InsureLLM**. It uses a Retrieval-Augmented Generation (RAG) architecture powered by **Google's Gemini Pro** and a local **ChromaDB** vector store to deliver accurate, context-aware answers from private company documents.

## 🧠 Problem Statement

As InsureLLM grows, its internal knowledge—spread across folders for company info, employees, products, and contracts—becomes harder to navigate. Manually searching for details like the CEO's background or product specs is inefficient. This chatbot solves that by offering a centralized, conversational AI assistant that instantly retrieves and synthesizes relevant information.

## ✨ Features

- **Conversational Q&A**: Ask questions in natural language and get direct answers.
- **Context-Aware**: Remembers conversation history for follow-up questions.
- **Fact-Based Generation**: Generates answers strictly from provided documents.
- **Local & Private**: All data and vector DB are stored locally for privacy.
- **Interactive UI**: Simple web interface built with Gradio.

## 🛠️ Tech Stack

| Component            | Technology               |
|---------------------|--------------------------|
| LLM                 | Google Gemini 1.5 Flash  |
| Framework           | LangChain                |
| Vector Database     | ChromaDB                 |
| Embeddings Model    | Google embedding-001     |
| UI                  | Gradio                   |
| Environment         | Jupyter Notebook         |

## 📁 Project Structure
To run this project, you must have your knowledge base organized in the following folder structure:
```
your-project-folder/
├── Untitled.ipynb             # The main Jupyter Notebook with the code
├── vector_db/                 # This folder will be created automatically
└── knowledge-base/
    ├── company/
    │   └── about_us.md
    ├── employee/
    │   └── avery_lancaster_ceo.md
    ├── product/
    │   └── policyguard_pro.md
    └── contract/
        └── standard_terms.md
```
## Install Dependencies
Install all the required Python libraries.

```pip install langchain google-generativeai chromadb gradio``` 

## Set Up Your API Key
Open Untitled.ipynb and replace "YOUR_API_KEY_HERE" with your actual Gemini API key:

```python
# Cell 2
os.environ["GOOGLE_API_KEY"] = "YOUR_API_KEY_HERE"
```

## Add Your Knowledge Base
Create the knowledge-base directory and populate it with .md files in the appropriate subfolders.

## 🧾 Example Conversation
```text
You: Who is the CEO of InsureLLM?

Bot: The CEO of InsureLLM is Avery Lancaster.

You: What was their experience before joining?

Bot: Before founding InsureLLM..............
```

credit:- Thankyou ed donner for you exceptional teaching and providing material for this project 
