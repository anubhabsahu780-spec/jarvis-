# J.A.R.V.I.S. Desktop — Setup Guide

## ⚡ Quick Start (3 Steps)

### Step 1 — Install Node.js (one time only)
Download and install from: https://nodejs.org  
Choose the **LTS** version. This is free.

### Step 2 — Set up Jarvis
Open a Terminal (Mac/Linux) or Command Prompt (Windows), then run:

```
cd jarvis-desktop
npm install
```

This downloads Electron (~150MB, one time only). Wait for it to finish.

### Step 3 — Launch!
```
npm start
```

Jarvis will open as a native desktop window! 🚀

---

## 🔑 Get Your Free API Key

1. Go to https://console.anthropic.com
2. Sign up for a free account
3. Click "API Keys" → "Create Key"
4. Copy the key (starts with `sk-ant-...`)
5. Paste it into the **API Key** field in Jarvis sidebar

You get **free credits** to start. After that it costs a tiny amount per message.

---

## 🗂 File Structure

```
jarvis-desktop/
├── main.js        ← Electron app window config
├── preload.js     ← Bridge between Electron and webpage
├── index.html     ← The entire Jarvis interface
├── package.json   ← App info & dependencies
└── README.md      ← This file
```

---

## 🚀 What's Built In

| Feature | How to use |
|---------|-----------|
| **AI Chat** | Type anything and press Enter |
| **Web Search** | Say "search the web for..." |
| **Voice Input** | Click the 🎤 mic button (Chrome speech API) |
| **Text-to-Speech** | Jarvis speaks responses automatically |
| **Task Manager** | Add tasks in the left sidebar |
| **Quick Commands** | One-click prompts in left sidebar |
| **Memory** | Chat history stays during session |

---

## 🛠 Next Steps (Optional Upgrades)

### Add auto-start on boot
**Windows:** Add a shortcut to `shell:startup` folder  
**Mac:** System Preferences → Users → Login Items → add the app

### Build a distributable .exe / .app
```
npm install electron-builder --save-dev
npx electron-builder
```

### Add a global hotkey
Install `electron-globalShortcut` to open Jarvis with e.g. Ctrl+Space from anywhere.

---

## ❓ Troubleshooting

| Problem | Fix |
|---------|-----|
| `npm: command not found` | Install Node.js from nodejs.org first |
| App won't open | Make sure you ran `npm install` first |
| AI not responding | Check your API key in the sidebar |
| Voice not working | Works best in Chromium-based environments |

---

Built with Electron + Claude AI 🤖
