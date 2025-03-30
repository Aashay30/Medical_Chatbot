# 🏥 Medical ChatBot using Llama-2 🦙

A powerful **Medical ChatBot** designed to provide accurate medical information to users, built with **Llama-2** and advanced NLP techniques.

## 🛠️ Project Architecture

### 🖥️ Backend
1. **Data Ingestion** 📥: Medical data is ingested from a medical book (PDF file).
2. **Data Extraction** 📝: Extracts and processes data from the PDF.
3. **Text Chunking** 📚: Breaks down large content into smaller, manageable chunks to feed into the model.
4. **Embedding** 🧬: Converts each text chunk into vector representations (embeddings).
5. **Semantic Index Building** 🧠: Builds a semantic index to connect vectors, enhancing the understanding of the context.
6. **Knowledge Base** 🗄️: Stores embeddings in a knowledge base using **Pinecone**, a vector database.

### 🌐 Frontend
1. **User Query Processing** 💬: Converts user questions into query embeddings.
2. **Knowledge Base Lookup** 🔍: Searches the knowledge base using the query embeddings for relevant information.
3. **LLM Model Processing** 🤖: Feeds the ranked results into the **Llama-2** model.
4. **User Answer Generation** 📝: Generates a response for the user based on processed information.

## 🛠️ Tech Stack
- **Language**: Python 🐍
- **Framework**: Langchain 🔗
- **Frontend/Webapp**: Flask, HTML, CSS 🌐
- **LLM**: Meta Llama 2 🦙
- **Vector Database**: Pinecone 🧩

## 📄 Project Description
This project utilizes the **Llama-2** model to build a robust **Medical ChatBot**. It leverages advanced NLP techniques and machine learning to provide precise answers to user queries. With a seamless integration of **LangChain** for the backend and **Flask** for the frontend, it offers a comprehensive solution for AI-driven healthcare information.

### 🚀 Key Features
- Ingests medical data from PDFs 📚
- Creates embeddings and builds a semantic index for deep understanding 🧠
- Utilizes **Pinecone** for vector storage and retrieval 📦
- Provides accurate and context-aware medical answers 🏥

## 📸 Output
![Medical ChatBot Output Screenshot](https://github.com/Aashay30/Medical_Chatbot/blob/main/output.png)

## 🏃‍♂️ How to Run?

### Project Structure

```
Medical-Chatbot/
├── .env                      # Environment variables (to be created by the user)
├── .gitignore                # Git ignore file
├── app.py                    # Main Flask application
├── LICENSE                   # License file
├── README.md                 # Project documentation
├── requirements.txt          # Python dependencies
├── setup.py                  # Setup script for the project
├── store_index.py            # Script to store embeddings in Pinecone
├── template.py               # Script to initialize project structure
├── data/                     # Directory for storing data files
│   └── Medical_book.pdf      # Example medical book for chatbot
├── model/                    # Directory for model files
│   ├── architecture.txt      # Architecture explanation
│   ├── instruction.txt       # Instructions for downloading the model
│   └── llama-2-7b-chat.ggmlv3.q4_0.bin # Llama 2 model file (to be downloaded)
├── research/                 # Directory for research and experiments
│   └── trials.ipynb          # Jupyter notebook for trials
├── src/                      # Source code directory
│   ├── __init__.py           # Package initializer
│   ├── helper.py             # Helper functions for data processing
│   └── prompt.py             # Prompt template for the chatbot
├── static/                   # Static files (CSS, JS, images)
│   └── style.css             # Stylesheet for the chatbot UI
├── templates/                # HTML templates for the Flask app
│   └── chat.html             # Chatbot UI template
```

### 🔧 STEPS:

1. **Clone the Repository** 🛠️:
   ```bash
   git clone https://github.com/your-repo-url
   cd Medical-ChatBot-using-llama-2
   ```

2. **Create a Conda Environment** 🐍:
   ```bash
   conda create -n mchatbot python=3.8 -y
   conda activate mchatbot
    ```

3. **Install Requirements** 📦:
   ```bash
   pip install -r requirements.txt
    ```

4. **Set Up Pinecone Credentials** 🔑:
   Create a .env file in the root directory and add
   ```bash
   PINECONE_API_KEY = "xxxxxxxxxxxxxxxxxxxxxxxxxxxxx"
   PINECONE_API_ENV = "xxxxxxxxxxxxxxxxxxxxxxxxxxxxx"
    ```
5. **Download the Quantized Model** 🎯:

6. **Run the Indexing Script** 🔄:
   ```bash
   python store_index.py
    ```

7. **Start the Application** 🚀:
   ```bash
   python app.py
    ```
