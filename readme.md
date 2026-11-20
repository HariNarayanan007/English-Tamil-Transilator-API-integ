
# English to Tamil Local AI Translator

## About the Project

This project is an AI-powered English-to-Tamil text translator.

It uses a locally running Large Language Model (LLM) to translate English text into Tamil without depending on external AI APIs.

## Technologies Used

- Python
- Ollama
- Qwen3:4B
- Streamlit

## Features

- English text input
- Automatic Tamil translation
- Local AI model processing
- No external AI API required
- Simple web-based interface
- Offline translation after model download

## Project Structure

English-Tamil-Translator/

    app.py
    requirements.txt
    README.md

## Installation

### 1. Install Ollama

Download Ollama from:

https://ollama.com/download

### 2. Download the AI model

Open PowerShell and execute:

    ollama pull qwen3:4b

### 3. Clone or open the project

Open the project folder in VS Code.

### 4. Create a virtual environment

    python -m venv venv

Activate it on Windows:

    .\venv\Scripts\Activate.ps1

### 5. Install dependencies

    pip install -r requirements.txt

### 6. Run the application

    streamlit run app.py

The application will open in your browser.

## How It Works

1. User enters English text.
2. Python receives the input.
3. Ollama sends the request to the local Qwen3 model.
4. Qwen3 translates the English text into Tamil.
5. Streamlit displays the translated output.

## Future Improvements

- Translation history
- Copy translation button
- Document translation
- Multiple Indian languages
- Improved translation accuracy

## Author

English to Tamil Local AI Translator Project
