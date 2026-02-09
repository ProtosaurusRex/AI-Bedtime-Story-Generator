# Quickstart

Simple example demonstrating the OpenAI Python client in a small Quickstart project.

## What this is

- Minimal project showing how to call the OpenAI Responses API from Python.
- Includes `example.py` which loads an API key from a local `.env` file and sends a prompt.

## Files

- `example.py` — example script that initializes the client and requests a response.
- `.env` — environment file containing `OPENAI_API_KEY` (not committed to source control).
- `venv/` — project virtual environment (local to this folder).

## Prerequisites

- Python 3.10+ (or whichever your virtual environment uses).
- A valid OpenAI API key.

## Setup

1. Activate the included virtual environment (Windows PowerShell):

```powershell
& .\venv\Scripts\Activate.ps1
```

Or (cmd):

```bat
venv\Scripts\activate.bat
```

2. Install dependencies (if not already installed):

```powershell
pip install -r requirements.txt
```

3. Create a `.env` file in this directory with the `OPENAI_API_KEY` variable (if not present):

```
OPENAI_API_KEY=sk-...your-api-key...
```

`example.py` uses `python-dotenv` to load the `.env` file automatically.

## Run the example

With the venv active:

```powershell
python example.py
```

You should see a short generated response printed to stdout.

## Notes

- Never commit your API key to source control. Keep it in `.env` and add `.env` to `.gitignore`.
- If VS Code doesn't resolve imports, ensure the workspace Python interpreter is set to `./venv/Scripts/python.exe`.

## License

This project contains example code; adapt and reuse as you like.
