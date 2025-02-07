# RAG-based Chat with PDF

## Overview

RAG-based Chat with PDF is an interactive application that allows users to engage in conversational interactions with the content of uploaded PDF files. Utilizing the power of Retrieval-Augmented Generation (RAG), the system efficiently retrieves and generates responses to user queries based on the information present in the uploaded documents.

This project leverages advanced AI technologies, including Natural Language Processing (NLP) and vector-based search, to enhance user experience and ensure accurate, context-aware responses.

## Features

### 🔹 PDF Upload
- Supports uploading one or multiple PDF files.
- Securely handles file processing.

### 🔹 Text Extraction
- Extracts textual content from uploaded PDFs for further analysis.
- Uses **PyPDF2** for parsing PDFs.

### 🔹 Text Chunking
- Splits extracted text into manageable chunks to optimize retrieval.
- Improves search accuracy and performance.

### 🔹 Vector Store Creation
- Utilizes **FAISS** (Facebook AI Similarity Search) for vector storage.
- Enables fast and efficient retrieval of relevant information.

### 🔹 Conversational Interface
- Employs a **RAG model** for intelligent response generation.
- Seamlessly integrates with **Claude-3 Sonnet LLM** via Anthropic API.

## Tech Stack

| Technology  | Purpose |
|-------------|---------|
| **Python** | Core programming language for backend processing. |
| **Streamlit** | Web framework for building an interactive UI. |
| **PyPDF2** | Library for extracting text from PDFs. |
| **LangChain** | Framework for developing LLM-powered applications. |
| **FAISS** | Vector search library for fast and efficient retrieval. |
| **Anthropic API** | Provides access to the **Claude-3 Sonnet** model. |
| **dotenv** | Manages environment variables securely. |

## Installation

### Prerequisites
- **Python 3.7+** installed on your machine.
- **Anthropic API key** for accessing Claude-3 Sonnet.

### Setup Steps


1. **Create a Virtual Environment (Recommended)**
   ```bash
   python -m venv env
   source env/bin/activate   # On macOS/Linux
   env\Scripts\activate      # On Windows
   ```

2. **Install Dependencies**
   ```bash
   pip install -r requirements.txt
   ```

3. **Set Up Environment Variables**
   - Create a `.env` file in the project root.
   - Add the following content:
     ```ini
     ANTHROPIC_API_KEY=your_api_key_here
     ```
   - Replace `your_api_key_here` with your actual Anthropic API key.

4. **Run the Application**
   ```bash
   streamlit run rag_pdf.py
   ```

## Usage Guide

1. **Upload PDFs**: Click the **Upload** button and select one or more PDF files.
2. **Process PDFs**: Click **Submit & Process** to extract and chunk the text.
3. **Ask Questions**: Type your query in the input field and receive an AI-generated response based on the uploaded content.

## Example Workflow

1. Upload `research_paper.pdf`
2. Ask: *"What are the key findings of this research?"*
3. The system retrieves relevant content and generates an accurate answer.

## Deployment

You can deploy this application on various cloud platforms like:
- **Streamlit Community Cloud**
- **Google Cloud Run**
- **Heroku**
- **AWS Lambda + API Gateway**

## Troubleshooting

- **Issue**: *Application crashes on startup.*
  - **Solution**: Ensure Python 3.8+ is installed and all dependencies are properly installed.

- **Issue**: *API key error.*
  - **Solution**: Verify the API key is correctly set in the `.env` file.


## License

This project is licensed under the **MIT License**. See the [LICENSE](LICENSE) file for more details.


