# Fact Check Agent

A small Streamlit web app for checking factual claims from PDF files.

## What it does

The app reads a PDF, finds claim-like sentences, searches the web for evidence, and gives a simple status:

- Verified
- Inaccurate
- False

This is built for quick review of marketing and product documents where numbers, dates, or market claims may be outdated.

## Tech used

- Python
- Streamlit
- pdfplumber
- Serper API

## Run locally

```bash
python -m venv .venv
.venv\Scripts\activate
pip install -r requirements.txt
python -m streamlit run app.py
```

## API key setup

Create this file:

```text
.streamlit/secrets.toml
```

Add:

```toml
SERPER_API_KEY = "your_key_here"
```

## Deployment

This app can be deployed on Streamlit Cloud.

1. Push the project to GitHub
2. Go to Streamlit Cloud
3. Select the repo
4. Add `SERPER_API_KEY` in app secrets
5. Deploy

## Note

The app uses web search results to estimate whether a claim is supported. Final business use should include manual review of sources.
