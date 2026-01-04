# 🕵️ Project Ghost: Forensic AI Engine

**A hackathon tool built for hackers that analyzes failed projects and suggests winning strategies.**

## The Problem

At every hackathon, developers struggle with:
- **Decision Paralysis**: "What tech stack should I use?"
- **Project Validation**: "Is this actually a good idea?"
- **Learning from Failure**: "Why do winning projects win?"

Project Ghost solves this by analyzing any GitHub repository and providing AI-powered insights using a noir detective theme.

## The Solution

### Core Features

1. **Multimodal Analysis**
   - Analyze GitHub repository URLs using Gemini 2.5 Flash
   - Upload UI screenshots for contextual understanding
   - Combines code intelligence + visual design feedback in a single request

2. **Coroner's Report**
   - **Cause of Death**: Why the project failed
   - **Smoking Gun**: Critical technical or UX flaw
   - **Resurrection Plan**: How to win with this idea today

3. **AI-Powered Narration**
   - Text-to-speech via ElevenLabs API (v0.2.15)
   - Dynamic voice selection from available voices
   - Makes analysis engaging and memorable

### Tech Stack

- **Frontend**: Streamlit (rapid development, judges love it)
- **AI Analysis**: Google Gemini 2.5 Flash (multimodal, faster inference)
- **Voice**: ElevenLabs v0.2.15 (natural, professional narration)
- **Cloud**: Vultr Ubuntu 22.04 (live deployment)
- **Environment**: Python 3.10+

## Why This Wins

### ✅ Sponsor Category Coverage
- **Google Gemini**: Full multimodal integration (text + images) using Gemini 2.5 Flash
- **ElevenLabs**: Text-to-speech narration with voice selection
- **Vultr**: Live deployment on Vultr cloud at 207.246.125.6

### ✅ Judging Criteria
- **Innovation**: Novel combination of Gemini + ElevenLabs + Noir theme
- **Execution**: Clean, working code with proper error handling
- **Polish**: Professional UI with dark mode + noir aesthetic
- **Practicality**: Actually useful for analyzing hackathon projects

### ✅ Security & Production Best Practices
- `.env` file for API keys (never committed, gitignored)
- `.env.example` for documentation
- Session state initialization to prevent Streamlit crashes
- Markdown stripping before voice generation for clean narration
- Tested and deployed on production cloud infrastructure

## Setup Instructions

### 1. Clone & Install Dependencies
```bash
git clone https://github.com/yourusername/project-ghost.git
cd project-ghost
python -m venv .venv
source .venv/bin/activate  # On Windows: .venv\Scripts\activate
pip install -r requirements.txt
```

### 2. Configure API Keys
```bash
cp .env.example .env
# Edit .env and add your API keys:
# GEMINI_API_KEY=sk-xxx...
# ELEVENLABS_API_KEY=sk-xxx...
```

### 3. Run the App
```bash
streamlit run app.py
```

Navigate to `http://localhost:8501` and start analyzing projects!

## Usage

1. **Paste a GitHub URL** (e.g., a previous hackathon project)
2. **Optionally upload a screenshot** of the UI
3. **Click "Execute Forensic Autopsy"**
4. **Read the Coroner's Report** and listen to narration
5. **Learn from the failures** to build something better

## API Keys Required

### Google Gemini
- [Get API Key](https://ai.google.dev/tutorials/setup)
- Free tier available with rate limits
- Used for multimodal analysis

### ElevenLabs
- [Get API Key](https://elevenlabs.io)
- Free tier: 10,000 characters/month
- Used for voice narration

## Live Deployment

**Project Ghost is live and running at:** http://207.246.125.6

Judges can test it directly without setting up locally. The app is fully functional with all APIs integrated and tested in production.

## Demo

**Ideal Demo Flow for Judges:**

1. Visit http://207.246.125.6 (no setup required)
2. Paste a GitHub URL (e.g., a previous hackathon project)
3. Optionally upload a screenshot of the UI
4. Click "EXECUTE FORENSIC AUTOPSY"
5. Read the Coroner's Report and listen to narration

**Why this impresses judges:**
- Live demo on production infrastructure (Vultr)
- Real multimodal Gemini 2.5 Flash capability
- Professional voice narration (ElevenLabs)
- Shows end-to-end API integration
- Memorable noir theme execution

## Production Issues Overcome

This project demonstrates real problem-solving under pressure:

- **Pydantic v2 Compatibility**: ElevenLabs SDK conflict resolved by pinning v0.2.15
- **Session State Errors**: Streamlit crashes fixed with explicit session state initialization
- **Model Availability**: Discovered gemini-2.5-flash through iterative testing, documented stable version
- **Voice Output Quality**: Markdown stripping implemented for clean TTS narration
- **Cloud Deployment**: Linux venv setup and Streamlit configuration for public access

Each fix was committed strategically to show problem-solving methodology.

## Future Enhancements

- [ ] Cache results to reduce API calls
- [ ] GitHub OAuth for auto-fetching repo details
- [ ] Batch analysis of multiple repos
- [ ] Custom prompts for different analysis types
- [ ] Dark/Light mode toggle
- [ ] Save reports as PDF

## License

MIT - Built for hackers, shared freely.

---

**Built by Ryan and Bhavya at Hacks for Hackers 2026**

*"Where failed projects become winning ideas."*
