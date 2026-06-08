# Project development Log

## Day 1
Decided the project Document QA

## Day 2
- Functional Requirements and Non functional Requirements are gathered
- Collected Reference papers

## Day 3
- fastapi
We need a web server in Python so React can send requests to it. FastAPI is a modern, beginner-friendly framework for building APIs. It's what turns your Python file into a server.

- uvicorn
FastAPI alone can't run — it needs a server to actually start and listen for requests. Uvicorn is that server. Think of FastAPI as the engine and Uvicorn as the ignition.

- python-multipart
When the user uploads a PDF file from React, it comes as multipart/form-data (that's how browsers send files). Without this package, FastAPI can't read uploaded files at all.

- pymupdf
The uploaded files are PDFs. Python can't read PDF content by default — it's a binary format. PyMuPDF lets us open a PDF and extract the text from each page.

- openai
Groq's API follows the exact same structure as OpenAI's API. So instead of Groq making their own library, they just said "use the OpenAI library, just change the base URL." That's why we install this.

- python-dotenv
Your Groq API key should never be hardcoded in your Python file. We store it in a .env file and this package loads it into your code securely.
