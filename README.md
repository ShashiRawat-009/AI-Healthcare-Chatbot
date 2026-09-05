🏥 AI Healthcare Chatbot

An AI-powered healthcare chatbot that uses Large Language Models (LLMs), LangChain, Pinecone, and Flask to provide context-aware responses to medical queries based on a curated medical knowledge base.

⚠️ Disclaimer: This project is intended for educational and informational purposes only. It is not a substitute for professional medical advice, diagnosis, or treatment.

📌 Overview

The AI Healthcare Chatbot is a Retrieval-Augmented Generation (RAG) based application designed to answer healthcare-related questions using information retrieved from a medical knowledge base.

Instead of relying only on the language model's general knowledge, the application retrieves relevant information from the medical knowledge base and uses that context to generate a response.

🔄 How It Works

User Question
      ↓
Flask Web Application
      ↓
Question Processing
      ↓
Pinecone Vector Search
      ↓
Relevant Medical Information
      ↓
LangChain RAG Pipeline
      ↓
Large Language Model
      ↓
Context-Aware Response
      ↓
User

✨ Features

💬 Interactive healthcare chatbot

🧠 Large Language Model integration

🔎 Retrieval-Augmented Generation (RAG)

📚 Medical knowledge-base integration

🗂️ Document embeddings and vector search

⚡ Pinecone vector database

🔗 LangChain-based retrieval pipeline

🌐 Flask web application

🐳 Docker support

☁️ AWS deployment configuration

🔄 GitHub Actions CI/CD workflow

🛠️ Tech Stack

Technology

Purpose

Python

Core programming language

Flask

Web application framework

LangChain

RAG and LLM orchestration

Pinecone

Vector database and similarity search

LLM

Natural-language response generation

HTML/CSS/JavaScript

Frontend interface

Docker

Containerization

AWS EC2

Cloud deployment

Amazon ECR

Docker image registry

GitHub Actions

CI/CD automation

📂 Project Structure

AI-Healthcare-Chatbot/
│
├── .github/
│   └── workflows/
│
├── data/
│   └── medical_chatbot/
│
├── research/
│   └── trials.ipynb
│
├── src/
│   ├── helper.py
│   └── prompt.py
│
├── static/
│
├── templates/
│   └── chat.html
│
├── app.py
├── store_index.py
├── requirements.txt
├── setup.py
├── Dockerfile
├── LICENSE
├── README.md
└── .gitignore

⚙️ Installation & Setup

1. Clone the Repository

git clone https://github.com/ShashiRawat-009/AI-Healthcare-Chatbot.git

Navigate into the project:

cd AI-Healthcare-Chatbot

2. Create a Virtual Environment

You can use Python's built-in virtual environment:

python -m venv venv

Windows

venv\Scripts\activate

Linux / macOS

source venv/bin/activate

3. Install Dependencies

pip install -r requirements.txt

🔐 Environment Variables

Create a .env file in the root directory of the project.

Example:

PINECONE_API_KEY="your_pinecone_api_key"
GROK_API_KEY="your_grok_api_key"

Important: Use the exact environment-variable names required by your application code.

Never commit your .env file to GitHub.

The .gitignore file should prevent environment files and local virtual environments from being uploaded.

🗃️ Create / Store the Vector Index

Before running the chatbot, generate and store the document embeddings in Pinecone:

python store_index.py

This prepares the medical knowledge base for vector-based retrieval.

▶️ Run the Application

Start the Flask application:

python app.py

Then open the local URL shown in your terminal, typically:

http://127.0.0.1:5000

You can then interact with the healthcare chatbot through the web interface.

🧠 RAG Architecture

The project follows a Retrieval-Augmented Generation (RAG) architecture.

1. Knowledge Base

Medical information is stored as source documents.

2. Document Processing

The source documents are processed and prepared for retrieval.

3. Embeddings

The processed document content is converted into vector representations.

4. Pinecone

The vectors are stored in Pinecone, enabling similarity-based searches.

5. Retrieval

When a user asks a question, the system searches the vector database for relevant information.

6. LLM Response

The retrieved context is passed through the LangChain pipeline to help generate the final response.

🐳 Docker

The project includes a Dockerfile for containerizing the application.

Build the Docker image:

docker build -t ai-healthcare-chatbot .

Run the container:

docker run -p 5000:5000 ai-healthcare-chatbot

Then open:

http://localhost:5000

☁️ AWS Deployment

The repository also contains GitHub Actions configuration for deployment-related automation.

The deployment architecture can be summarized as:

GitHub Repository
       ↓
GitHub Actions
       ↓
Build Docker Image
       ↓
Amazon ECR
       ↓
AWS EC2
       ↓
Run Docker Container
       ↓
Healthcare Chatbot

AWS Services

Amazon EC2 — application hosting

Amazon ECR — Docker image storage

IAM — access management

GitHub Actions — CI/CD automation

🔑 GitHub Actions Secrets

Deployment credentials should be configured through GitHub Repository Secrets rather than being written directly into source code.

Typical secrets include:

AWS_ACCESS_KEY_ID
AWS_SECRET_ACCESS_KEY
AWS_DEFAULT_REGION
ECR_REPO
PINECONE_API_KEY
GROK_API_KEY

⚠️ Never publish API keys, AWS credentials, Pinecone credentials, or other secrets directly in the repository.


🚀 Future Improvements

Possible future improvements include:

🔐 User authentication

💾 Conversation history

🧑‍⚕️ Medical-professional integration

📱 Improved responsive design

🎙️ Voice-based interaction

🌍 Multilingual support

📊 Chat analytics

🛡️ Enhanced medical safety and response validation

☁️ Improved cloud deployment and monitoring

📚 Learning Outcomes

Through this project, I explored and implemented:

Retrieval-Augmented Generation (RAG)

Large Language Model integration

Vector databases

Semantic search

LangChain

Flask application development

Docker containerization

AWS deployment concepts

GitHub Actions and CI/CD

Environment and API-key management

👩‍💻 Author

Shashi Rawat

GitHub: ShashiRawat-009

Project Repository: AI Healthcare Chatbot

⚠️ Medical Disclaimer

This chatbot is a software/academic project and is not intended to provide medical diagnosis, treatment, or professional medical advice.

Always consult a qualified healthcare professional for medical concerns.
