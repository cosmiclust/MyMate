# MyMate
your real-time, privacy-first screen assistant.



**What it does:**

"A voice-first AI assistant that lets users control their laptop screen, apps, and tasks — just like a teammate guiding you."

**Who it's for:**

Coders, non-tech users, small-town learners, students, travelers, workers — everyone

**Why it matters:**

It removes the need to type, click, or even understand tech. It democratizes help.

*Apps don’t expose APIs?*  Doesn’t matter — you read screen pixels.

*No login/OAuth needed?* Doesn’t matter — you don’t need user data from them.

*Privacy?* Everything is local — no data shared unless user consents.

*Scalable trust model* — Everyone can have their own local agent. No one needs to “give” their data._


mymate/
├── README.md               # Project overview and instructions
├── main.py                 # Entry point for running MyMate
├── requirements.txt        # List of dependencies
├── config/
│   └── settings.py         # Central configuration for paths, model, app settings
├── core/
│   ├── agent.py            # Agent logic for deciding actions based on vision + text
│   ├── pipeline.py         # Orchestration of screen input, OCR, VLM, and response
│   └── utils.py            # Shared utility functions (e.g., timers, logging)
├── screen/
│   ├── screen_capture.py   # Real-time screen grabbing using MSS
│   └── ocr.py              # OCR using Tesseract or any chosen engine
├── vision/
│   ├── analyzer.py         # Visual understanding using VLMs (BLIP2, LLaVA, etc.)
│   └── models/             # Optional folder for loading/storing local model weights
├── audio/ (optional)       
│   ├── mic_input.py        # Capture voice commands
│   └── tts.py              # Text-to-speech responses (if voice output needed)
├── gui/ (optional)
│   └── interface.py        # GUI for MyMate using Tkinter, PyQt, or web UI
└── tests/
    ├── test_pipeline.py    # Unit tests for the core pipeline
    └── test_agent.py       # Tests for the agent's decision logic

