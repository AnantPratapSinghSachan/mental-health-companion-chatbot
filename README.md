Student Mental Health Companion (Streamlit + Gemini)
A professional, supportive mental health companion for students, powered by Google Gemini and Streamlit. Includes quick prompts, basic crisis guidance, session-only mood check-ins, and a small statistics visualization.

Features
Chatbot guidance for stress, anxiety, academic pressure, sleep, and self-care
Crisis awareness: highlights resources if risky keywords are detected
Quick prompts for common student concerns
Session-only mood check-in and simple trend chart
Statistics section (WHO and CDC YRBS examples) with an Altair chart
Important
This app is not a substitute for professional help. If you're in immediate danger or considering harming yourself:

United States: Call or text 988 (Suicide & Crisis Lifeline)
International: Visit https://findahelpline.com or contact your local emergency services
Prerequisites
Python 3.9+
A Google API key with access to the Gemini API
Setup
Create and activate a virtual environment (recommended)

PowerShell (Windows):

python -m venv .venv
.\.venv\Scripts\Activate.ps1
Install dependencies

pip install -r requirements.txt
Provide your Google API Key (choose one):

Option A: Environment variable (persists across sessions after restart)
setx GOOGLE_API_KEY "{{YOUR_GOOGLE_API_KEY}}"
# Restart the terminal after this
Option B: Streamlit secrets (per project) Create a file .streamlit/secrets.toml and add:
GOOGLE_API_KEY = "{{YOUR_GOOGLE_API_KEY}}"
Option C: Paste your key into the sidebar field when the app runs (temporary for the session)
Run the app

streamlit run app.py
Model selection
The sidebar lets you choose between gemini-1.5-pro (higher quality) and gemini-1.5-flash (faster, cost-efficient). You can change this at runtime.

Notes on data and privacy
Conversations are kept only in the current session unless you export or persist them yourself.
