# Hopscotch Support Chatbot

A Streamlit customer-support chatbot that answers return and refund questions using the policy in `hopscotch_policy.md`. It calls the OpenRouter API using the OpenAI Python SDK.

## Requirements

- Python 3.10 or newer
- An OpenRouter API key

## Setup

Open PowerShell in the project directory and create a virtual environment:

```powershell
py -m venv .venv
.\.venv\Scripts\Activate.ps1
python -m pip install --upgrade pip
pip install -r requirements.txt
```

Create a file named `.env` in the project directory and add your API key:

```text
OPENROUTER_API_KEY=your_openrouter_api_key
```

Keep the key private. `.env` is excluded from Git.

## Run

With the virtual environment active, start the app:

```powershell
streamlit run app.py
```

Streamlit will open the app in your browser, usually at `http://localhost:8501`. Press `Ctrl+C` in the terminal to stop it.

Keep `hopscotch_policy.md` in the same directory as `app.py`; the app reads it at startup. If the app reports that `OPENROUTER_API_KEY` is missing, verify that `.env` is in the project directory and restart Streamlit.
