# CodeCoach AI — CodeSentinels

A beginner-friendly AI programming coach that reviews C++ and Python code, explains likely bugs, provides progressive hints, suggests a correction, and proposes test cases.

## Features
- C++ and Python code input
- Optional compiler/runtime error and expected-behaviour fields
- Gemini-powered code review
- Baseline, structured, refined and final prompt selection for experiments
- Beginner-friendly explanations and progressive hints
- Suggested fix and test-case ideas
- Downloadable Markdown review

## Requirements
- Python 3.10 or newer (Python 3.11 recommended)
- Google Gemini API key
- Internet connection

## Run locally on Windows

1. Install Python and VS Code.
2. Open this folder in VS Code.
3. Open Terminal → New Terminal.
4. Create and activate a virtual environment:

   ```powershell
   python -m venv venv
   .\venv\Scripts\Activate.ps1
   ```

   If PowerShell blocks activation, run this once in the current terminal:

   ```powershell
   Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass
   .\venv\Scripts\Activate.ps1
   ```

5. Install dependencies:

   ```powershell
   python -m pip install --upgrade pip
   pip install -r requirements.txt
   ```

6. Create a file named `.env` in the same folder as `app.py`. Copy the format from `.env.example` and add your own key:

   ```text
   GEMINI_API_KEY=your_actual_key
   GEMINI_MODEL=gemini-2.5-flash
   ```

7. Start the app:

   ```powershell
   streamlit run app.py
   ```

8. Open the local URL printed in the terminal, normally http://localhost:8501.

## Project structure

```text
CodeCoach-AI/
├── app.py
├── requirements.txt
├── .env.example
├── .gitignore
├── prompts/
│   ├── v1/baseline.txt
│   ├── v2/structured.txt
│   ├── v3/refined.txt
│   └── final/P1_CodeReview.txt
├── test-data/test_inputs.json
├── docs/
└── CHANGELOG.md
```

## Prompt experiments

Choose V1, V2, V3 or Final (P1) in the app. Use the same code inputs for each version and record the actual outputs. Do not invent experiment results. The final application prompt is P1.

## Security
- Never commit `.env`, API keys, passwords or private credentials.
- `.gitignore` excludes `.env`.
- AI output may be incorrect. Review and test suggested code independently.
- The app does not execute or compile submitted code; it asks the model to inspect the code.

## Current scope and limitations
- AI-based static review only; no actual compiler or runtime execution.
- Only C++ and Python are offered in the interface.
- Model availability, API quotas and network access can affect responses.
- Long or complex programs may need to be divided into smaller sections.

## Team
- CodeSentinels
- Project: CodeCoach AI
- Team member names and enrollment numbers: add verified details before submission.
