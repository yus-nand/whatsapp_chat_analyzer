# WhatsApp Chat Analyzer (Streamlit)

This is a Streamlit app that analyzes exported WhatsApp chats (messages, timelines, active users, wordcloud, emojis, links).

## Run locally

```bash
python -m venv .venv
.venv\Scripts\activate
python -m pip install -r requirements.txt
streamlit run app.py
```

Then upload your exported WhatsApp `.txt` file in the sidebar.

## Deploy (recommended: Streamlit Community Cloud)

1. Push this folder to a **GitHub** repo.
2. Go to https://share.streamlit.io
3. Click **New app**
4. Select your repo + branch
5. Set **Main file path** to `app.py`
6. Deploy

Streamlit Cloud will install dependencies from `requirements.txt` automatically.

### Important

- Don’t commit personal chat exports. This repo’s `.gitignore` ignores `WhatsApp Chat*.txt`.
- Keep `stop_hinglish.txt` in the repo (the app uses it for filtering words).

## Deploy (alternative: Render)

- Create a new **Web Service** from your GitHub repo.
- Build command: `pip install -r requirements.txt`
- Start command: `streamlit run app.py --server.port $PORT --server.address 0.0.0.0`
