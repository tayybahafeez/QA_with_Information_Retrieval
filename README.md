# Project Name: LLama_Index Chatbox with PDF Integration

## Overview

This project demonstrates the integration of a generative AI model with PDF document data ingestion. It uses Streamlit to provide a simple user interface (UI) for querying information from PDF files via a chatbox. The backend uses the **Llama Index**, which leverages generative AI models to process the data and answer queries.

## Features

- **PDF Document Ingestion**: Upload and read PDFs using Streamlit.
- **Data Indexing**: Process and index PDF data using Llama Index.
- **Generative AI Model**: Use Google Gemini and OpenAI models to answer questions based on the indexed PDF data.
- **Chat Interface**: Query the AI model to retrieve information from the PDFs via a Streamlit-powered chat interface.

## Requirements

- **Python 3.x** (recommended: version 3.7 or higher)
- **Streamlit**
- **Llama Index**
- **Google Gemini or OpenAI API** (for AI model integration)
- **Google API Key** (for Gemini)
- Other Python Dependencies: Install necessary libraries from `requirements.txt`.

## Setup Instructions

1. **Clone the Repository**:
    ```bash
    git clone https://github.com/tayybahafeez/QA_with_Information_Retrieval.git
    cd QA_with_Information_Retrieval
    ```

2. **Create a Virtual Environment**:
    ```bash
    python -m venv venv
    ```

3. **Activate the Virtual Environment**:
    - On Windows:
      ```bash
      .\venv\Scripts\activate
      ```
    - On macOS/Linux:
      ```bash
      source venv/bin/activate
      ```

4. **Install Dependencies**:
    ```bash
    pip install -r requirements.txt
    ```

5. **Set Up API Keys**:
   - For **Google Gemini**, create and get your API key from the [Google Cloud Console](https://console.cloud.google.com/).
   - Set the API key in your environment:
     - On Windows:
       ```bash
       set GOOGLE_API_KEY=your_api_key_here
       ```
     - On macOS/Linux:
       ```bash
       export GOOGLE_API_KEY=your_api_key_here
       ```
   Alternatively, you can create a `.env` file and store your API keys there:
   ```env
   GOOGLE_API_KEY=your_api_key_here


Run the Application:

bash
```
streamlit run yourscript.py
```
This will launch a web-based interface where you can interact with the chatbot, upload PDFs, and query them.

##### How It Works
* PDF Data Ingestion: Upload PDF files via the UI.
* Data Processing and Indexing: The files are read, processed, and indexed using the SimpleDirectoryReader and VectorStoreIndex from Llama Index.
* Generative AI Querying: After indexing, the AI model (Google Gemini or OpenAI) is used to generate answers based on the documents.
* Querying via Chat: Interact with the model via a Streamlit chat interface to ask questions about the contents of the PDFs.
##### Directory Structure
bash
```
/project-root
│
├── QASYSTEM/
│   └── data_ingestion.py       # Script for processing and indexing data from PDF
│
├── exception.py                # Custom exception handling
│
├── yourscript.py               # Main Streamlit application script
│
├── requirements.txt            # List of Python dependencies
│
├── README.md                  # Project documentation
│
└── .env                        # Environment variables (for API keys)
```
#### Troubleshooting
* No API Key Found: Ensure that your API key is correctly set in your environment or .env file.

* Rate Limiting Error: If you are using an OpenAI API or Gemini API, you may hit a rate limit. Ensure that you are within your quota and consider upgrading if necessary.

* Module Import Errors: Ensure that all dependencies are installed correctly using
```
pip install -r requirements.txt.
```

