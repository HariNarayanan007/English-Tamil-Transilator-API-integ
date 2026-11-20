# English to Tamil AI Translator

An AI-powered English-to-Tamil translation web application built using Google's Gemini LLM, Python FastAPI, and HTML, CSS, and JavaScript.

The application uses Generative AI to understand the context of English text and generate natural Tamil translations.

## About the Project

This project aims to provide an easy-to-use English-to-Tamil translation platform powered by a Large Language Model (LLM).

Unlike traditional dictionary-based translation systems, this application uses Google's Gemini API to generate context-aware Tamil translations.

Users can enter English text through a web interface, submit it to the backend, and receive the Tamil translation.

## Technologies Used

- **Programming Language:** Python
- **AI Model:** Google Gemini Flash
- **AI Approach:** Generative AI and Large Language Models (LLMs)
- **Backend:** FastAPI
- **AI Integration:** Google Gen AI Python SDK
- **Frontend:** HTML, CSS, JavaScript
- **Communication:** REST API and JSON
- **Deployment Target:** Vercel
- **Version Control:** Git and GitHub

## Features

- English text input
- AI-powered English-to-Tamil translation
- Context-aware translation using Gemini
- Natural Tamil text generation
- Real-time API-based communication
- Character count and input validation
- Copy translated text
- Download Tamil translation as a text file
- Responsive web interface
- Backend API error handling

## Project Architecture

The application follows a frontend-backend architecture.

1. The user enters English text in the frontend.
2. JavaScript sends the text to the FastAPI backend through a REST API request.
3. FastAPI validates the input.
4. The backend sends the text to Google's Gemini model using the Google Gen AI SDK.
5. Gemini generates the Tamil translation.
6. FastAPI returns the translated text as a JSON response.
7. The frontend displays the Tamil translation.

## Project Structure

```text
English-Tamil-Translator/
│
├── app.py
├── public/
│   └── index.html
│
├── requirements.txt
├── .python-version
├── .gitignore
├── .env
└── README.md
```

**Note:** The `.env` file and virtual environment are local development files and should not be uploaded to GitHub.

## Installation and Setup

### 1. Clone the Repository

```bash
git clone https://github.com/HariNarayanan007/English-Tamil-Transilator-API-integ.git
```

### 2. Navigate to the Project

```bash
cd English-Tamil-Transilator-API-integ
```

### 3. Create a Virtual Environment

```bash
python -m venv venv
```

Activate it on Windows:

```powershell
.\venv\Scripts\Activate.ps1
```

### 4. Install Dependencies

```bash
python -m pip install --upgrade pip
pip install -r requirements.txt
```

### 5. Configure Gemini API Key

Create a `.env` file in the project root:

```env
GEMINI_API_KEY=your_gemini_api_key
```

Obtain an API key from Google AI Studio:

https://aistudio.google.com/app/apikey

**Important:** Never upload your API key to GitHub or expose it in frontend JavaScript.

### 6. Run the Application

```bash
uvicorn app:app --reload
```

Open the application in your browser:

```text
http://127.0.0.1:8000
```

API health check:

```text
http://127.0.0.1:8000/api/health
```

## AI Mechanism

The application uses a pretrained Transformer-based Large Language Model (LLM) through Google's Gemini API.

The translation process involves:

- Tokenization of input text.
- Contextual language understanding.
- Attention-based processing within the pretrained model.
- Generative inference to produce Tamil output.
- Context-aware translation instead of simple word substitution.

The model is accessed through an API; this project does not train a new language model from scratch.

## API Endpoint

### POST `/api/translate`

Accepts English text and returns its Tamil translation.

Example request:

```json
{
  "text": "Hello, how are you?"
}
```

Example response structure:

```json
{
  "translation": "வணக்கம், நீங்கள் எப்படி இருக்கிறீர்கள்?",
  "model": "Gemini Flash",
  "status": "success"
}
```

The exact model identifier and response fields depend on the backend configuration.

## Security

- Gemini API keys are stored in environment variables.
- API credentials are not exposed in frontend code.
- Input validation is performed on the backend.
- Sensitive environment files are excluded from Git.

## Future Improvements

- Support for multiple Indian languages.
- PDF and document translation.
- Translation history.
- Speech-to-text and text-to-speech.
- Improved long-text handling.
- User authentication.
- Translation quality evaluation.
- Rate limiting and API abuse protection.

## Author

**Hari Narayanan**

GitHub: https://github.com/HariNarayanan007