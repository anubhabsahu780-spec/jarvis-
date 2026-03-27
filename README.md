
# 🦾 J.A.R.V.I.S. Personal AI Assistant - Desktop App

Welcome to **J.A.R.V.I.S.**, a futuristic, desktop-native AI assistant inspired by Iron Man. Powered by **Electron** and **Anthropic's Claude AI**, this application brings a highly capable, voice-interactive, and visually stunning AI directly to your desktop.

![J.A.R.V.I.S UI Concept](https://img.shields.io/badge/UI-Sci--Fi_Cyberpunk-00c8ff?style=for-the-badge)
![Electron Version](https://img.shields.io/badge/Electron-^28.0.0-47848f?style=for-the-badge&logo=electron)
![AI Model](https://img.shields.io/badge/AI-Claude_3.5_Sonnet-d97757?style=for-the-badge&logo=anthropic)

## ✨ Core Features

- **🧠 Advanced AI Core**: Powered by Anthropic's Claude API, capable of complex reasoning, formatting, and coding.
- **🎙️ Voice Interaction**: 
  - **Speech-to-Text**: Click the mic to speak to Jarvis natively using the built-in browser Web Speech API.
  - **Text-to-Speech**: Jarvis responds audibly with a sophisticated voice automatically.
- **🛜 Live Web Search**: Ask Jarvis to `search the web for...` and it will securely fetch live information using the built-in tool use capability.
- **✅ Built-in Task Manager**: Track your daily objectives with a local, persistent to-do list integrated into the UI.
- **⚡ Quick Commands**: One-click prompts for daily briefings, motivational quotes, and productivity tips.
- **🖥️ Frameless Sci-Fi UI**: Custom draggable title bar, glassmorphism-inspired dark mode, glowing accents, and `Orbitron` typography.

## 🗂️ Project Architecture

This application is built using standard web technologies wrapped in Electron for native desktop functionality.

- **`main.js`**: The Electron main process. It creates a frameless `BrowserWindow`, sets strict security preferences (`nodeIntegration: false`, `contextIsolation: true`), routes IPC messages for window controls (minimize, maximize, close), and forces external links to open in your default system browser.
- **`preload.js`**: The secure bridge (Context Bridge) exposing limited IPC capabilities (`electronAPI`) to the renderer process, ensuring UI controls can interact with the OS without exposing full Node.js APIs directly to the frontend.
- **`index.html`**: The entire frontend. It contains the HTML layout, a standalone CSS block for the futuristic UI, and vanilla JavaScript handling Anthropic API calls, state management (localStorage), chat history, tasks, and Speech Recognition.
- **`package.json`**: Defines scripts and the `electron@^28.0.0` dependency.

## 🚀 Installation & Setup

### 1. Prerequisites
Ensure you have [Node.js](https://nodejs.org/) installed.

### 2. Install Dependencies
```bash
# Navigate to the project directory
cd jarvis-desktop

# Install packages (Electron)
npm install
```

### 3. Launch the Assistant
```bash
# Start the Electron application
npm start
```
