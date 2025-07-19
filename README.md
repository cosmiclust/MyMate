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
├── README.md
├── requirements.txt
├── main.py                        # Entry point
├── config.py                      # Global configs (paths, model type, etc.)
├── utils/
│   ├── logger.py
│   ├── screen_capture.py          # MSS-based screen grabber
│   ├── ocr_engine.py              # Tesseract wrapper
│   └── prompt_templates.py        # Templates for VLM prompts
├── core/
│   ├── vlm_engine.py              # Vision-language model wrapper (BLIP, LLaVA, etc.)
│   ├── nlp_command_parser.py      # Parse user natural language queries
│   └── agent_controller.py        # Core orchestration logic
├── interface/
│   ├── voice_input.py             # Optional mic input
│   └── gui.py                     # Optional PyQt or Tkinter GUI (future)
├── data/
│   └── screenshots/               # Temp storage for screen captures
└── models/
    └── checkpoints/              # Local VLM/OCR checkpoints if needed
