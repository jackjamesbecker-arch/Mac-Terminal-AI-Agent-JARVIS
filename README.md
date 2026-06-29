# ⚡ Volt — Terminal AI Agent

Volt is a personal AI agent that lives in your terminal. It's powered by Groq and can control your Mac, search the web, send messages, manage your life, and talk back to you — all from the command line.

---

## Install

### 1. Prerequisites
- Mac (macOS 12+)
- Python 3.10+
- A free [Groq API key](https://console.groq.com)

### 2. Install dependencies
```bash
pip3 install groq SpeechRecognition pyaudio
```

### 3. Set your API key
```bash
echo 'export GROQ_API_KEY=gsk_...' >> ~/.zshrc
source ~/.zshrc
```

### 4. Make `volt` a global command
```bash
sudo bash -c 'printf "#!/bin/bash\npython3 ~/Downloads/agent.py\n" > /usr/local/bin/volt && chmod +x /usr/local/bin/volt'
```

### 5. Launch
```bash
volt
```

---

## Login

Volt requires a personal access code at startup.

| User | Code |
|------|------|
| Jackson | `7474` |
| Jules | `110583` |
| Larry | `8675309` |

---

## What Volt Can Do

### 🌐 Web & Info
- Search the web for anything
- Get current weather
- Check stock and crypto prices
- Summarize any article or webpage by URL
- Check if a website is up or down
- Translate text to any language

### 📅 Productivity
- View today's calendar events
- Add reminders
- Manage a to-do list
- Set countdown timers
- Schedule recurring tasks
- Take screenshots

### 💬 Communication
- Send iMessages by name or number
- Send and receive emails with file attachments
- Look up contacts from your Mac Contacts app

### 🗂 Files & System
- Read, write, and list files
- Run any shell command
- Check battery, WiFi, and disk space
- Search your codebase for any string
- Read and summarize CSV and Excel files
- Start a local web server

### 🎵 Media
- Control Apple Music (play, pause, skip, search)
- Voice input — speak instead of type (`/voice`)
- Voice responses — Volt talks back (`/speak`)

### 🧠 Memory & Notes
- Save and recall notes across sessions
- Persistent memory that carries over every time you launch
- Export everything to a `.md` file on exit

### 🔐 Dev Tools
- Check npm and pip package versions
- Open GitHub repos and check PRs
- Serve a local directory in your browser
- Generate secure passwords

### 🟦 NOVA Integration
- Open NOVA in your browser
- Check NOVA's online status
- Sync data between Volt and NOVA

---

## Slash Commands

| Command | What it does |
|---------|-------------|
| `/voice` | Toggle voice input on/off |
| `/speak` | Toggle voice responses on/off |
| `/volume 0-100` | Set voice response volume |
| `/fast` | Switch to faster model |
| `/smart` | Switch to smarter model |
| `/clear` | Clear the conversation |
| `/history` | Save chat history manually |
| `/todo` | Show your to-do list |
| `/github` | Show your recent GitHub repos |
| `/nova` | Check NOVA's status |
| `/model` | Show current model |
| `exit` | Save, export, and quit |

---

## Optional Setup

### Email (send & receive files)
```bash
echo 'export VOLT_EMAIL=you@gmail.com' >> ~/.zshrc
echo 'export VOLT_EMAIL_PASSWORD=xxxx-xxxx-xxxx-xxxx' >> ~/.zshrc
```
Get an App Password at: myaccount.google.com → Security → App passwords  
Enable IMAP in Gmail settings to receive files.

### GitHub
```bash
echo 'export GITHUB_USERNAME=yourname' >> ~/.zshrc
```

---

## Example Prompts

```
❯ what's on my calendar today
❯ remind me in 30 minutes to call Jules
❯ what's the weather here
❯ text Jules "are you free tonight"
❯ what's AAPL at
❯ translate "good morning" to Japanese
❯ search my code for "fetchUser"
❯ set a 25 minute timer
❯ generate a password for my Netflix account
❯ is github.com down
❯ serve this folder on port 3000
❯ open nova
❯ add task finish the landing page
❯ give me my daily briefing
```

---

## Data & Privacy

All your data stays on your machine at `~/.volt/`:

| File | Contents |
|------|----------|
| `memory.json` | Things Volt remembers |
| `notes.json` | Saved notes |
| `todo.json` | To-do list |
| `schedule.json` | Scheduled tasks |
| `nova_sync.json` | NOVA sync data |
| `history/` | Chat logs |
| `exports/` | Session exports (.md files) |

---

*Built by Jackson Becker · Powered by Groq + Llama 4*
