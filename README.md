DEPLOY LINK : https://replyforge-aigit-frclhaa3crfprjuug5772f.streamlit.app/

<div align="center">

<br/>

```
 ███████╗███╗   ███╗ █████╗ ██╗██╗      █████╗ ███████╗███████╗██╗███████╗████████╗ █████╗ ███╗   ██╗████████╗
 ██╔════╝████╗ ████║██╔══██╗██║██║     ██╔══██╗██╔════╝██╔════╝██║██╔════╝╚══██╔══╝██╔══██╗████╗  ██║╚══██╔══╝
 █████╗  ██╔████╔██║███████║██║██║     ███████║███████╗███████╗██║███████╗   ██║   ███████║██╔██╗ ██║   ██║   
 ██╔══╝  ██║╚██╔╝██║██╔══██║██║██║     ██╔══██║╚════██║╚════██║██║╚════██║   ██║   ██╔══██║██║╚██╗██║   ██║   
 ███████╗██║ ╚═╝ ██║██║  ██║██║███████╗██║  ██║███████║███████║██║███████║   ██║   ██║  ██║██║ ╚████║   ██║   
 ╚══════╝╚═╝     ╚═╝╚═╝  ╚═╝╚═╝╚══════╝╚═╝  ╚═╝╚══════╝╚══════╝╚═╝╚══════╝   ╚═╝   ╚═╝  ╚═╝╚═╝  ╚═══╝   ╚═╝   
```

<h3>⚡ AI-Powered Email Response Engine — Built with Streamlit × Groq × LLaMA 3.3</h3>

<br/>

![Python](https://img.shields.io/badge/Python-3.9%2B-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Streamlit](https://img.shields.io/badge/Streamlit-1.x-FF4B4B?style=for-the-badge&logo=streamlit&logoColor=white)
![Groq](https://img.shields.io/badge/Groq-API-F55036?style=for-the-badge&logoColor=white)
![LLaMA](https://img.shields.io/badge/LLaMA-3.3_70B-0467DF?style=for-the-badge&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-22c55e?style=for-the-badge)

<br/>

> **Paste an email. Get instant AI analysis. Generate a perfectly-toned, context-aware reply — in seconds.**

<br/>

</div>

---

## 📋 Table of Contents

- [Overview](#-overview)
- [Live Demo](#-live-demo)
- [Features](#-features)
- [Themes & UI Design](#-themes--ui-design)
- [Architecture](#-architecture)
- [AI Models](#-ai-models)
- [Tech Stack](#-tech-stack)
- [Getting Started](#-getting-started)
- [Environment Variables](#-environment-variables)
- [Usage Guide](#-usage-guide)
- [Project Structure](#-project-structure)
- [Design Philosophy](#-design-philosophy)
- [Contributing](#-contributing)
- [License](#-license)

---

## 🔍 Overview

**Email Assistant** is a sleek, dark-themed Streamlit web application that uses the **Groq API** with **LLaMA 3.3 70B** to analyze incoming emails and generate professional, context-aware replies in seconds.

Instead of staring at a blank compose window, you paste the email you received, describe *why* you want to respond the way you do, and let the AI handle the writing. The assistant first analyzes the email's intent, tone, urgency, and decision requirements — then generates a complete, ready-to-send response based on your instructions.

It is designed to feel less like a chatbot and more like a **command center** — purpose-built, fast, and unapologetically beautiful.

---

## 🚀 Live Demo

> Coming soon — deploy your own instance using the setup instructions below.

---

## ✨ Features

### 🧠 Dual-Agent AI Pipeline

The app implements a two-stage AI processing pipeline:

| Stage | Agent | Responsibility |
|-------|-------|----------------|
| **Agent 1** | Intent Analyzer | Reads the email, returns structured JSON: type, urgency, tone, decision needed, possible paths, summary, and key points |
| **Agent 2** | Response Generator | Takes the analysis + your reasoning + chosen scenario + tone preference, and writes the complete reply |

### 📊 Smart Intent Analysis

Automatically extracts and displays:
- **Email Type** — Invitation, Meeting Request, Task, Question, Newsletter, etc.
- **Urgency Level** — High / Medium / Low (color-coded)
- **Tone Detected** — Friendly, Formal, Urgent, Professional, Neutral
- **Decision Needed** — Yes / No
- **Possible Paths** — Dynamic action pills (Accept, Decline, Delay, Ask Clarification, etc.)
- **One-Line Summary** — A concise italic summary of the email's purpose

### ✍️ Contextual Response Generation

- **Scenario Selection** — Choose from AI-suggested response paths
- **Tone Override** — Formal | Friendly | Professional | Assertive | Neutral
- **Role Selector** — Set sender context: Client, Colleague, Manager, Team Lead, Vendor, Partner
- **Reasoning Input** — Tell the AI *why* you're responding this way for a more natural output
- **Regenerate** — Get a fresh response variation without re-analyzing
- **Edit Mode** — Inline editing of the generated response before you send
- **Copy to Clipboard** — One-click copy

### 🎨 7 Handcrafted Themes

Full UI theme switching with live re-render, no page reload.

### 🔒 Secure API Key Management

API keys are loaded from `.env` or injected at runtime via the sidebar input — never hardcoded.

---

## 🎨 Themes & UI Design

The app ships with **7 meticulously crafted dark themes**, each with its own color palette, font pairing, border radius, and glow effects:

| Theme | Primary Accent | Vibe |
|-------|---------------|------|
| 🌌 **Cyber Dark** | `#6c63ff` Violet | Futuristic hacker terminal |
| 🌲 **Forest** | `#4ade80` Green | Calm, natural depth |
| 🌊 **Ocean Depth** | `#00b4d8` Cyan | Deep-sea command center |
| 🌅 **Sunset Gold** | `#f59e0b` Amber | Warm, editorial luxury |
| 🔮 **Neon Noir** | `#f700ff` Magenta | Cyberpunk maximalism |
| ❄️ **Ice Nord** | `#88c0d0` Ice Blue | Nordic, minimal clarity |
| 🌋 **Lava** | `#ff4444` Crimson | Intense, high-energy |

### Design Tokens

Each theme exposes a set of CSS custom properties injected dynamically at runtime:

```css
--bg          /* Page background */
--surface     /* Card / panel background */
--surface2    /* Elevated surface (panel headers) */
--border      /* Subtle border color */
--accent      /* Primary accent */
--accent2     /* Secondary accent */
--accent3     /* Alert / error accent */
--text        /* Primary text */
--muted       /* Secondary / label text */
--glow        /* Ambient glow for hover/focus states */
--btn-p       /* Primary button gradient */
--btn-g       /* Secondary button gradient */
--font        /* UI font family */
--mono        /* Monospace font for labels/code */
--r           /* Global border radius */
```

### Typography

Each theme pairs a **display font** with a **monospace font**:

| Theme | Display Font | Mono Font |
|-------|-------------|-----------|
| Cyber Dark | Syne 800 | Space Mono |
| Forest | DM Sans | JetBrains Mono |
| Ocean Depth | Syne | JetBrains Mono |
| Sunset Gold | Syne | Space Mono |
| Neon Noir | Syne | JetBrains Mono |
| Ice Nord | DM Sans | JetBrains Mono |
| Lava | Syne | Space Mono |

All fonts are loaded from Google Fonts: `Syne`, `DM Sans`, `Space Mono`, `JetBrains Mono`, `Playfair Display`.

### Visual Details

- **Background Grid** — Subtle CSS dot/line grid using `background-image: linear-gradient` overlaid via `::before` pseudo-element, creating depth without distraction
- **Glowing Focus Rings** — `box-shadow: 0 0 0 3px var(--glow)` on text inputs and textareas
- **Hover Lift** — Buttons lift 2px on hover with a gradient glow shadow
- **Live Dot Animation** — Pulsing dot on the model badge, indicating active AI connection
- **Smooth Transitions** — All theme switches animate via CSS `transition: background-color .35s ease`
- **Panel Hover Borders** — Cards highlight their accent border on hover

---

## 🏗️ Architecture

```
┌─────────────────────────────────────────────────────────────┐
│                      STREAMLIT FRONTEND                      │
│                                                             │
│   ┌──────────────┐         ┌──────────────────────────┐    │
│   │  Email Input │         │    Intent Analysis Panel  │    │
│   │  + Context   │         │  (Type, Urgency, Paths)   │    │
│   └──────┬───────┘         └──────────────┬───────────┘    │
│          │  Analyze Click                  │                 │
│          ▼                                 ▼                 │
│   ┌──────────────────────────────────────────────────────┐  │
│   │                  Session State Store                  │  │
│   │  email_content │ analysis_result │ generated_response│  │
│   │  reasoning     │ selected_scenario│ selected_tone    │  │
│   │  model_choice  │ theme            │ edit_mode        │  │
│   └──────────────────────┬───────────────────────────────┘  │
│                           │                                  │
└───────────────────────────┼──────────────────────────────────┘
                            │
              ┌─────────────▼─────────────┐
              │       call_groq()          │
              │   POST /v1/chat/completions│
              │   Bearer: GROQ_API_KEY     │
              └─────────────┬─────────────┘
                            │
              ┌─────────────▼─────────────┐
              │         GROQ API          │
              │                           │
              │  ┌─────────────────────┐  │
              │  │  Agent 1 — Analyzer │  │
              │  │  temp=0.2, json out │  │
              │  └──────────┬──────────┘  │
              │             │             │
              │  ┌──────────▼──────────┐  │
              │  │  Agent 2 — Writer   │  │
              │  │  temp=0.4, prose out│  │
              │  └─────────────────────┘  │
              └───────────────────────────┘
```

### Data Flow

1. **User pastes email** → stored in `email_input_area` widget
2. **Analyze Email** clicked → `analyze_email_intent()` called → Groq returns JSON → `st.session_state.analysis_result` updated → UI re-renders intent panel
3. **User provides reasoning** → selects scenario & tone
4. **Generate** clicked → `generate_email_response()` called → Groq returns draft → stored in `st.session_state.generated_response`
5. **User edits / copies / regenerates** response as needed

### State Management

All application state lives in `st.session_state`, making the app fully reactive without any external database:

```python
st.session_state.email_content        # Raw email text
st.session_state.analysis_result      # Dict from Agent 1 (JSON)
st.session_state.generated_response   # String from Agent 2
st.session_state.reasoning            # User's decision context
st.session_state.selected_scenario    # Accept / Decline / Delay / etc.
st.session_state.selected_tone        # Formal / Friendly / etc.
st.session_state.model_choice         # Active LLM model ID
st.session_state.theme                # Active UI theme name
st.session_state.edit_mode            # Boolean: inline edit toggle
st.session_state.edited_response      # Edited draft before save
```

---

## 🤖 AI Models

Three Groq-hosted models are available, switchable per session:

| Model ID | Display Name | Best For |
|----------|-------------|----------|
| `llama-3.3-70b-versatile` | **Llama 3.3 70B** | Highest quality, nuanced responses |
| `llama-3.1-8b-instant` | **Llama 3.1 8B** | Fastest responses, simple emails |
| `mixtral-8x7b-32768` | **Mixtral 8x7B** | Good balance of speed and quality |

### Prompt Design

**Agent 1 — Intent Analyzer** (`temperature=0.2`, low creativity for reliable JSON):
```
System: "You are an expert email analyst. Analyze the email and return a structured analysis..."
Output: { email_type, action_needed, urgency, tone_detected, decision_needed, possible_paths, summary, key_points }
```

**Agent 2 — Response Writer** (`temperature=0.4`, moderate creativity for natural prose):
```
System: "You are an expert email writer. Generate a personalized email response with {tone} tone.
         The user has chosen to: {SCENARIO}. Their reasoning: {reasoning}..."
Output: Full email response with subject line suggestion
```

---

## 🛠️ Tech Stack

| Layer | Technology |
|-------|-----------|
| **Frontend Framework** | [Streamlit](https://streamlit.io/) |
| **AI Inference** | [Groq API](https://groq.com/) |
| **Language Model** | Meta LLaMA 3.3 70B / 3.1 8B, Mixtral 8x7B |
| **HTTP Client** | `requests` |
| **Styling** | Custom CSS injected via `st.markdown(unsafe_allow_html=True)` |
| **Fonts** | Google Fonts (Syne, DM Sans, Space Mono, JetBrains Mono) |
| **Config** | `python-dotenv` |
| **Language** | Python 3.9+ |

---

## 🚀 Getting Started

### Prerequisites

- Python 3.9 or higher
- A [Groq API Key](https://console.groq.com/) (free tier available)

### Installation

**1. Clone the repository**

```bash
git clone https://github.com/yourusername/email-assistant.git
cd email-assistant
```

**2. Create a virtual environment**

```bash
python -m venv venv
source venv/bin/activate       # Linux / macOS
venv\Scripts\activate          # Windows
```

**3. Install dependencies**

```bash
pip install -r requirements.txt
```

**4. Configure your API key**

```bash
cp .env.example .env
# Then edit .env and add your GROQ_API_KEY
```

**5. Run the app**

```bash
streamlit run app.py
```

The app will open at `http://localhost:8501`

### requirements.txt

```txt
streamlit>=1.32.0
requests>=2.31.0
python-dotenv>=1.0.0
```

---

## 🔐 Environment Variables

Create a `.env` file in the project root:

```env
GROQ_API_KEY=your_groq_api_key_here
```

| Variable | Required | Description |
|----------|----------|-------------|
| `GROQ_API_KEY` | ✅ Yes | Your Groq API key from [console.groq.com](https://console.groq.com) |

> **Note:** The API key can also be entered directly in the app sidebar at runtime if you prefer not to use a `.env` file.

---

## 📖 Usage Guide

### Step-by-Step Workflow

```
1. PASTE EMAIL ──────► Paste the email you received into the left panel
                       Add optional one-line context (e.g. "This is from a key client")

2. SET PREFERENCES ──► Choose the sender's Role (Client, Manager, Vendor, etc.)
                       Select your preferred tone for input

3. ANALYZE ──────────► Click "Analyze Email"
                       AI reads the email and populates:
                       - Email type, urgency, detected tone
                       - Decision needed, possible response paths
                       - One-line summary

4. YOUR REASONING ───► In the context panel, type WHY you want to respond this way
                       e.g. "I need to decline but keep the relationship warm"

5. CHOOSE SCENARIO ──► Select a path from the AI-suggested options
                       (Accept / Decline / Delay / Ask Clarification / custom)

6. TONE OVERRIDE ────► Fine-tune the response tone: Formal, Friendly, Professional,
                       Assertive, or Neutral

7. GENERATE ─────────► Click "Generate"
                       AI writes the complete email response

8. REFINE ───────────► Use "Edit" to tweak inline
                       Use "Regenerate" for a fresh variation
                       Use "Copy" to copy to clipboard
```

### Tips for Best Results

- The more specific your **reasoning**, the more natural the response
- Use **context input** to give background the email doesn't contain (e.g. "we already spoke on the phone")
- Try **Regenerate** 2-3 times to get different stylistic variations
- Switch models mid-session: 8B for quick drafts, 70B for final polish

---

## 📁 Project Structure

```
email-assistant/
│
├── app.py                  # Main application (single-file architecture)
│   ├── CONFIGURATION       # Streamlit page config
│   ├── THEMES              # 7 theme definitions
│   ├── SESSION STATE       # State initialization
│   ├── API CONFIG          # Model list, API URL
│   ├── API HELPERS         # call_groq(), analyze_email_intent(), generate_email_response()
│   ├── DYNAMIC CSS         # get_css(theme) — full CSS string generator
│   ├── SIDEBAR             # (minimal, for future expansion)
│   └── MAIN APP            # UI layout, widgets, event handlers
│
├── .env                    # Environment variables (gitignored)
├── .env.example            # Template for environment setup
├── requirements.txt        # Python dependencies
└── README.md               # This file
```

---

## 🎨 Design Philosophy

This app was built around a core principle: **tools should feel good to use.**

Most productivity apps are functional but visually uninspiring. Email Assistant takes the opposite approach — dark, tactile, high-contrast UI with micro-animations, glowing accents, and monospace labels that make every interaction feel intentional.

Key design decisions:

**Single-page, no navigation** — Everything you need is visible at once. No tabs, no modals, no buried settings.

**Theme as personality** — The 7 themes aren't just color swaps. Each has its own typographic identity, glow warmth, and border radius — giving the app a distinct personality per theme.

**Minimal Streamlit chrome** — The default Streamlit header, footer, and deploy button are hidden via CSS. The layout breathes.

**Monospace for metadata, humanist for content** — Labels, tags, and badges use monospace fonts for a terminal-like precision feel. The main UI uses Syne or DM Sans for readability.

**Dynamic CSS injection** — Rather than static stylesheets, CSS is generated as a Python f-string at runtime using the active theme's token dictionary. This means zero class name conflicts and perfectly scoped theming.

---

## 🤝 Contributing

Contributions are welcome! Here's how to get involved:

1. Fork the repository
2. Create your feature branch: `git checkout -b feature/amazing-feature`
3. Commit your changes: `git commit -m 'Add amazing feature'`
4. Push to the branch: `git push origin feature/amazing-feature`
5. Open a Pull Request

### Ideas for Contribution

- [ ] Add email history / conversation threading
- [ ] Export responses as `.eml` or `.txt`
- [ ] Add more themes (Rosé Pine, Dracula, Tokyo Night)
- [ ] Calendar invite parsing for meeting requests
- [ ] Multi-language response generation
- [ ] Streamlit Cloud deployment button
- [ ] Unit tests for API helper functions

---

## 📄 License

This project is licensed under the **MIT License** — see the [LICENSE](LICENSE) file for details.

---

<div align="center">

**Built with ⚡ by [Your Name]**

Powered by [Groq](https://groq.com) · [Meta LLaMA](https://llama.meta.com/) · [Streamlit](https://streamlit.io)

<br/>

*If this project helped you, consider giving it a ⭐ on GitHub*

</div>
