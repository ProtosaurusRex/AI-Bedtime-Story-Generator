# Quickstart

Small project demonstrating one way to call the OpenAI Responses API from Python:

- `ST_App.py` — a Streamlit web app that lets a user enter a topic and generates a one-paragraph bedtime story.

## Files

- `ST_App.py` — Streamlit app (web UI) for generating bedtime stories.
- `.env` — environment file containing `OPENAI_API_KEY` (keep private).
- `requirements.txt` — pinned Python dependencies for the venv.

## Prerequisites

- Python 3.10+ (or compatible with the included `venv`).
- A valid OpenAI API key.

## Setup

1) Create and activate a virtual environment (recommended):

PowerShell:

```powershell
python -m venv .venv
& .\.venv\Scripts\Activate.ps1
```

cmd.exe:

```bat
python -m venv .venv
.venv\Scripts\activate.bat
```

2) Install dependencies:

```powershell
pip install -r requirements.txt
```

3. Create a `.env` file in this directory with your API key:

```
OPENAI_API_KEY=sk-...your-api-key...
```

`ST_App.py` calls `load_dotenv()` so the key in `.env` will be read at runtime.

## Running

- Run the Streamlit app (open http://localhost:8501 in your browser):

```powershell
streamlit run ST_App.py
```

The Streamlit app uses `ST_App.py` which:

- Loads environment variables via `python-dotenv`.
- Initializes the OpenAI client once at startup (`client = OpenAI()`).
- Displays a text input for a story topic and a `Generate story` button.
- On click, it calls `client.responses.create(model="gpt-5-nano", input=...)` and shows the returned `response.output_text`.

## Notes

- Model: `ST_App.py` uses `gpt-5-nano` in the example; change the `model` parameter if needed.
- Never commit your API key to source control. Add `.env` to `.gitignore`.
- If imports are unresolved in VS Code, set the workspace interpreter to `./venv/Scripts/python.exe`.

## License

This project contains example code; adapt and reuse as you like.

