# 🤖 AI Influencer Studio (OpenClaw Skill)

[![OpenClaw Skill](https://img.shields.io/badge/OpenClaw-Skill-06B6D4?style=flat-square)](https://openclaw.ai)
[![Python 3.11+](https://img.shields.io/badge/python-3.11+-blue.svg?style=flat-square)](https://www.python.org/downloads/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=flat-square)](https://opensource.org/licenses/MIT)

A complete automated pipeline to design, generate, and operate 24/7 character-consistent virtual personas on X (Twitter). Built natively as an [OpenClaw](https://openclaw.ai) Skill.

This system takes you from zero to a fully autonomous AI influencer. It manages long-term persona memory, generates 100% face-consistent photos using Gemini models, schedules content, posts via the X API, and autonomously replies to fans in character.

## ✨ Features

- **🧠 Persona Design Engine:** Create rich, consistent backstories, tone-of-voice rules, and locked visual DNA.
- **📸 Consistent Image Generation:** Lock facial features and styling using Gemini (Nano Banana Pro) with fixed seeds.
- **📅 Automated Content Calendar:** Draft 30-day content pillars and daily posts mapped to your persona's niche.
- **🚀 Auto-Posting Pipeline:** Push text and generated images to X automatically using `tweepy`.
- **💬 Autonomous Fan Engagement:** Cron-triggered sweep script to reply to `@mentions` without breaking character.

## 📂 Repository Structure

```text
ai-influencer/
├── SKILL.md                 # Core OpenClaw instruction and prompt file
├── requirements.txt         # Python dependencies
├── scripts/
│   ├── 04_consistent_generator.py # Image generator (locks face & seed)
│   ├── 05_post_to_x.py            # Posts a single tweet + image
│   ├── 06_auto_reply.py           # Sweeps mentions and replies in character
│   ├── generate_calendar.py       # Drafts a 30-day content CSV
│   └── generate_x_post.py         # Drafts a single post text + image prompt
├── references/
│   ├── persona_design_workflow.md # Guide for creating the initial identity
│   ├── full_setup_workflow.md     # Step-by-step setup checklist
│   ├── persona_template.md        # Blank JSON/MD template for new personas
│   └── model_guide.md             # Image model selection guide
└── assets/
    └── alex_persona.md            # Example deployed persona
```

## ⚙️ Quick Start

### 1. Install the Skill
Clone this repository into your OpenClaw skills directory:
```bash
git clone https://github.com/YOUR_USERNAME/ai-influencer-skill.git ~/.openclaw/skills/ai-influencer
```

### 2. Set Up Environment
Create a Python virtual environment and install dependencies:
```bash
cd ~/.openclaw/skills/ai-influencer
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
```

### 3. Configure API Keys
Create a `.env` file in your workspace root (`~/.openclaw/workspace/.env`) and add your keys:
```env
# Google Gemini API (for text & image generation)
GEMINI_API_KEY="your_gemini_api_key"

# X (Twitter) Developer API (Read & Write permissions required)
X_CONSUMER_KEY="your_consumer_key"
X_CONSUMER_SECRET="your_consumer_secret"
X_ACCESS_TOKEN="your_access_token"
X_ACCESS_TOKEN_SECRET="your_access_token_secret"
```

## 🛠️ Usage

Once installed, simply chat with OpenClaw:
> *"Create a new AI influencer who is a 68-year-old wealth advisor."*

OpenClaw will automatically read the `SKILL.md` file and guide you through the 5-phase creation process.

## 🤝 Contributing
Contributions, issues, and feature requests are welcome! Feel free to check the [issues page](issues).

## 📝 License
This project is [MIT](LICENSE) licensed.
# aiinfluencer2
