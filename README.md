# English Tutor MVP 🎓

An AI-powered English conversation practice application with real-time voice interaction and intelligent feedback.

## 🌟 Features

- **Free Talk Mode**: Natural conversation practice with an AI tutor
- **Real-time Voice Interaction**: Speech-to-text input and text-to-speech output
- **Intelligent Feedback**: Get corrections on grammar and phrasing
- **Session Management**: Conversation context preservation
- **Modern UI**: Sleek, futuristic interface with visual feedback

## 🛠️ Tech Stack

- **Backend**: FastAPI (Python 3.10+)
- **AI**: OpenAI GPT-4o-mini & TTS-1
- **Frontend**: Vanilla HTML/CSS/JavaScript
- **Speech Recognition**: Web Speech API

## 📋 Prerequisites

- Python 3.10 or higher
- OpenAI API key
- Chrome browser (recommended for speech recognition)

## 🚀 Quick Start

### 1. Clone the repository
```bash
git clone https://github.com/Darkunquie/ENGLISH_Tutor.git
cd ENGLISH_Tutor
```

### 2. Install dependencies
```bash
pip install -r requirements.txt
```

### 3. Set up environment variable
**Windows (PowerShell)**:
```powershell
setx OPENAI_API_KEY "your-api-key-here"
```
Then close and reopen your terminal.

**Linux/Mac**:
```bash
export OPENAI_API_KEY="your-api-key-here"
```

### 4. Run the application
**Option A - Using the batch file (Windows)**:
```bash
run.bat
```

**Option B - Direct command**:
```bash
uvicorn main:app --reload --host 127.0.0.1 --port 8000
```

### 5. Access the application
Open your browser and navigate to:
```
http://127.0.0.1:8000
```

## 🎯 How to Use

1. **Start a Conversation**: Click the microphone button or type a message
2. **Speak or Type**: Use voice input (Chrome) or type your response
3. **Get Feedback**: The AI tutor responds with natural conversation and corrections
4. **Toggle Voice**: Use the voice toggle switch to enable/disable TTS output

## 📁 Project Structure

```
english-tutor-mvp/
├── main.py              # FastAPI backend application
├── static/
│   └── index.html       # Frontend UI
├── requirements.txt     # Python dependencies
├── run.bat             # Windows startup script
└── README.md           # This file
```

## 🔌 API Endpoints

- `GET /` - Serve the frontend
- `POST /api/session/create` - Create a new conversation session
- `POST /api/chat` - Send a message and get AI response
- `POST /api/tts` - Convert text to speech
- `GET /api/health` - Health check endpoint

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📝 License

This project is open source and available under the MIT License.

## ⚠️ Notes

- The application uses in-memory session storage (not persistent)
- Sessions expire after 120 minutes of inactivity
- Maximum conversation history is limited to 30 messages per session
- For production use, consider implementing persistent storage (Redis/Database)

## 🙏 Acknowledgments

- OpenAI for GPT and TTS APIs
- FastAPI framework
- Web Speech API

---

**Happy Learning! 🚀**
