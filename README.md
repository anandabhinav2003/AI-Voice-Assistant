🎙️ AI Voice Bot Project
Intelligent Wake-Word Activated Voice Assistant with NLP + Dashboard

<img width="466" height="548" alt="Screenshot 2025-11-22 at 11 19 37 AM" src="https://github.com/user-attachments/assets/c0ebe885-8ac7-4c68-b6b0-7f865e943c3c" />


🚀 Overview

This project is an AI-powered Voice Assistant designed to behave like a smart speaker:

Always listening for the wake-word “Jarvis”

Converts speech → text using Whisper

Understands intent using NLU

Generates meaningful responses

Speaks back using Text-to-Speech

Logs every interaction in a database

Provides a beautiful analytics dashboard (Simplotel-style)

This is a complete Voice Bot System with:

✔ Wake Word
✔ STT
✔ NLU
✔ TTS
✔ GUI (Tkinter)
✔ Analytics Dashboard (Streamlit)
✔ Database Logging
✔ Hotel Support Use Case

✨ Features

| Feature                           | Description                                                          |
| --------------------------------- | -------------------------------------------------------------------- |
| 🎤 Wake-Word Detection            | Uses Porcupine (Picovoice) to detect the command **"Jarvis"**        |
| 🔊 Speech-to-Text                 | Whisper converts user speech to accurate text                        |
| 🧠 Natural Language Understanding | Detects intents: refund policy, booking, greetings, small-talk, exit |
| 🤖 Response Engine                | Rule-based + fallback responses                                      |
| 🔈 Text-to-Speech                 | Speaks responses naturally using pyttsx3                             |
| 🪟 GUI Interface                  | Clean chat interface using Tkinter                                   |
| 🗄 Database Logging               | Stores timestamp, query, intent, response, success flag              |
| 📊 Analytics Dashboard            | Simplotel-style dashboard built with Streamlit                       |
| 🛠 Modular Architecture           | Every component is independent and cleanly structured                |

🏗 Architecture Diagram

<img width="510" height="638" alt="Screenshot 2025-11-22 at 10 55 49 AM" src="https://github.com/user-attachments/assets/02e4ca47-1294-4fad-b5e5-f20a21b7392d" /> 


📂 Folder Structure

```
voice_bot_project/
│
├── main.py                     # Terminal bot (runs the voice assistant)
├── voice_ui.py                 # GUI interface for the assistant
├── wakeword_porcupine.py       # Wake-word detection (Porcupine)
├── stt.py                      # Speech-to-Text using Whisper
├── tts.py                      # Text-to-Speech with speaking lock
├── nlu.py                      # Natural Language Understanding (intent detection)
├── response_generator.py       # Generates responses based on intent
├── backend.py                  # DB storage + list of intents & FAQs
├── dashboard.py                # Streamlit analytics dashboard
│
├── models/                     # STT model files
│   └── (Whisper model files here)
│
├── requirements.txt
└── .env                        # Picovoice API Key
```



⚙️ Installation

1️⃣ Clone the Repo
git clone https://github.com/vishalrox/voice_bot_project.git
cd voice_bot_project

2️⃣ Create Python 3.10 Virtual Environment
python3.10 -m venv venv
source venv/bin/activate

3️⃣ Install Dependencies
pip install -r requirements.txt

4️⃣ Add Your Picovoice Wake-Word Key
Create .env:
PORCUPINE_ACCESS_KEY="your_key_here"

🚀 Running the Project
▶ Run GUI Voice Assistant
source venv/bin/activate
python3.10 voice_ui.py

It will show:

👂 Waiting for wake word: 'Jarvis'...

Say:

“Jarvis” → Ask a question → Bot responds.

▶ Run Terminal-Only Bot

python3.10 main.py

▶ Run Analytics Dashboard (in a new terminal)

source venv/bin/activate
streamlit run dashboard.py

Web dashboard opens at:

👉 http://localhost:85xx


📊 Dashboard Preview

Total interactions

Successful Response 

Success rate 

Active intents 

Intent distribution 

Response quality 

Recent queries 

Performance metrics

<img width="1440" height="900" alt="Screenshot 2025-11-22 at 12 23 10 AM" src="https://github.com/user-attachments/assets/597cc4ab-e116-4a07-a7c9-c274bb2dd977" />




🧠 Supported Intents

| Intent             | Example Utterances         |
| ------------------ | -------------------------- |
| refund_policy      | “What is refund policy?”   |
| hotel_booking_help | “How to book a room?”      |
| greeting           | “Hello”, “Hey”             |
| bot_feeling        | “How are you?”             |
| goodbye            | “Goodbye”, “Thanks Jarvis” |
| fallback           | Unknown queries            |

🔮 Future Improvements

Replace TTS with Azure or Google TTS

Add LLM-powered response generation

Add emotion detection

Add multilingual support

Add user authentication

Deploy dashboard online

Add call center mode

🙌 Author

Abhinav Anand
AI/ML Developer
