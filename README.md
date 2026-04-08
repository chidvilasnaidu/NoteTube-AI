# 🎬 NoteTube AI

> **Turn any YouTube video into clean, structured notes — instantly.**

NoteTube AI extracts transcripts from YouTube videos and uses Google Gemini AI to generate well-organized, readable notes in seconds. No more rewatching. No more manual note-taking.

---

## ✨ Features

- 🎥 **Transcript Extraction** — Pulls captions from any public YouTube video automatically
- 🤖 **AI-Powered Notes** — Google Gemini generates structured notes with key points, summary & takeaways
- 📋 **Copy to Clipboard** — One-click copy of your generated notes
- ⬇️ **Download as TXT** — Save notes as a `.txt` file instantly
- 🔄 **Smart Retry Logic** — Auto-retries with fallback models if Gemini is overloaded
- 🎨 **Glassmorphism UI** — Sleek dark-themed interface with red accents
- 📄 **Multi-page Navigation** — Home, About, and Contact pages

---

## 🚀 Getting Started

### Prerequisites

- Python 3.9+
- A [Google Gemini API Key](https://makersuite.google.com/app/apikey)

### Installation

```bash
# 1. Clone the repository
git clone https://github.com/yourusername/notetube-ai.git
cd notetube-ai

# 2. Install dependencies
pip install -r requirements.txt

# 3. Create your .env file
cp .env.example .env
# Add your API key inside .env

# 4. Run the app
streamlit run main.py
```

### Environment Variables

Create a `.env` file in the root directory:

```env
GOOGLE_API_KEY=your_gemini_api_key_here
MODEL_NAME=gemini-1.5-flash
```

---

## 📦 Dependencies

```txt
streamlit
python-dotenv
google-genai
youtube-transcript-api
```

Install all at once:

```bash
pip install streamlit python-dotenv google-genai youtube-transcript-api
```

---

## 🛠️ How It Works

```
YouTube URL
    ↓
Extract Transcript (youtube-transcript-api)
    ↓
Send to Google Gemini AI with structured prompt
    ↓
Get formatted notes: Key Topics · Summary · Key Points · Takeaways
    ↓
Display · Copy · Download
```

---

## 📁 Project Structure

```
notetube-ai/
│
├── main.py              # Main Streamlit application
├── .env                 # API keys (not committed)
├── .env.example         # Template for environment variables
├── requirements.txt     # Python dependencies
├── IMGs/
│   └── BG.jpg           # Background image
└── README.md
```

---

## ⚙️ Fallback Model Chain

If the primary model is overloaded (503 error), NoteTube AI automatically retries with fallback models:

1. `gemini-1.5-flash` *(default)*
2. `gemini-1.5-flash-8b`
3. `gemini-2.0-flash`
4. `gemini-2.0-flash-lite`

---

## 🖼️ Screenshots

> Home page with YouTube URL input, thumbnail preview, and AI-generated notes panel.

---

## ⚠️ Limitations

- Only works with videos that have **captions/subtitles** enabled
- Very long videos may have transcripts **truncated at 50,000 characters**
- Requires a valid **Google Gemini API key**

---

## 🤝 Contributing

Pull requests are welcome! For major changes, please open an issue first.

1. Fork the repo
2. Create your branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

---

## 📄 License

MIT License © 2026 NoteTube AI

---

## 👨‍💻 Author

Built with ❤️ using Streamlit + Google Gemini AI
