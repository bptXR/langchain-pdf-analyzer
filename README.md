# Langchain PDF Analyzer
This is a Python-based application designed to facilitate interactions with PDFs using natural language inquiries. Leveraging a Language Model (LLM), it generates responses pertaining to your PDF. Please note that the LLM is focused on the content of the document, hence it won't provide answers to queries not related to the PDF.

## How it works
This application processes the content of the PDF by segmenting the text into manageable portions suitable for the Language Model (LLM). Utilizing OpenAI's embeddings, it transforms these text segments into vector representations. The application identifies the segments that share semantic similarities with the user's query, and these selected portions are then inputted into the LLM to formulate a response.

The user interface of the application is designed using Streamlit, while Langchain is employed for managing the LLM operations.

### Example
Upload your PDF and ask it any question! E.g. you have questions about your work contract but dont want to read through 30 pages of a PDF. Just upload it and ask questions like: "How is my bonus composed?". Assuming your working contract specifies how your bonus is composed it will give you exactly the information you need just like asking ChatGPT for any general information it was trained on.

## Setup Guide
To install the repository, clone it and install the requirements:

```python
pip install -r requirements.txt
```

You will also need to add your OpenAI API key to the .env file.

## Run the app
To run the application on your localhost run app.py with streamlit:

```python
streamlit run app.py
```