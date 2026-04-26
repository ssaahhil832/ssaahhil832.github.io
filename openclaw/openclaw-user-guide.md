# 🚀 OpenCLAW User Guide

<p align="center">
  <img src="https://img.shields.io/badge/Version-1.0.0-blue?style=for-the-badge&logo=version&color=00D4FF" alt="Version">
  <img src="https://img.shields.io/badge/License-MIT-green?style=for-the-badge&color=22C55E" alt="License">
  <img src="https://img.shields.io/badge/Platform-Windows%20%7C%20macOS%20%7C%20Linux-purple?style=for-the-badge&color=8B5CF6" alt="Platform">
  <img src="https://img.shields.io/badge/Open%20Source-100%25-orange?style=for-the-badge&color=FF6B00" alt="Open Source">
</p>

---

> **OpenCLAW** (Open Command Line Automation Wizard) — Your ultimate automation companion for command-line workflows, powered by [OpenClaw](https://github.com/openclaw/openclaw).

---

## 📋 Table of Contents

1. [What is OpenCLAW?](#what-is-openclaw)
2. [Why Use OpenCLAW?](#why-use-openclaw)
3. [Features](#features)
4. [Installation](#installation)
5. [Usage](#usage)
6. [Configuration](#configuration)
7. [Folder Structure](#folder-structure)
8. [Troubleshooting](#troubleshooting)
9. [Contributing](#contributing)
10. [License](#license)

---

## 🤖 What is OpenCLAW?

**OpenCLAW** is an **open-source automation tool** built on top of [OpenClaw](https://github.com/openclaw/openclaw) — a personal AI assistant. It simplifies complex command-line tasks and provides:

- 🔄 Automate repetitive workflows
- 🛠️ Manage system operations effortlessly  
- ⛓️ Chain multiple commands together
- 🤖 AI-powered automation using OpenClaw skills

```javascript
// Example: AI-powered automation
const openclaw = require('openclaw');

await openclaw.init({
  skill: 'automation-expert',
  task: 'backup-files',
  onComplete: (result) => console.log('✅ Done!')
});
```

---

## ❓ Why Use OpenCLAW?

| Problem | OpenCLAW Solution |
|:------|:---------------|
| 🤯 Repetitive terminal commands | ⚡ Automate with AI assistance |
| 🌍 Cross-platform scripts | 🪟 Works on Windows, macOS, Linux |
| 📈 Complex workflows | 🎯 OpenClaw skill integration |
| 🐛 Error handling | 🛡️ Built-in retry & logging |
| ⏰ Scheduling tasks | 📅 Schedule automations easily |

---

## ✨ Features

<div align="center">

| Feature | Description |
|:--------|:-----------|
| 🔄 **Workflow Automation** | Automate tasks with AI power |
| 📦 **Bulk Operations** | Process multiple files simultaneously |
| 🌐 **Channel Integrations** | Works with WhatsApp, Telegram, Discord, Slack & more |
| 🛠️ **Dev Workflows** | Streamline development processes |
| 📊 **System Monitoring** | Real-time health dashboards |
| 🔒 **Security** | Automated backup & security ops |

</div>

---

## 📦 Installation

### Prerequisites

- ✅ **Node.js** (v18 or higher)
- ✅ **Git** installed
- ✅ Terminal/Command Prompt access

---

### 🪟 Windows

#### Option 1: Using npm (Recommended)

```powershell
# 1. Install Node.js
winget install OpenJS.NodeJS

# 2. Clone the OpenClaw repository
git clone https://github.com/openclaw/openclaw.git
cd openclaw

# 3. Install dependencies (pnpm recommended)
npm install
# OR use pnpm
npm install -g pnpm
pnpm install

# 4. Build the project
pnpm build

# 5. Start OpenClaw
pnpm openclaw onboard --install-daemon
```

#### Option 2: Using PowerShell

```powershell
# Run as Administrator
Set-ExecutionPolicy Bypass -Scope Process -Force

# Quick install
iwr https:// Install.ps1 -useb | iex
```

---

### 🍎 macOS

```bash
# 1. Install Homebrew (if needed)
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

# 2. Install Node.js
brew install node
# OR use pnpm
brew install pnpm

# 3. Clone & setup
git clone https://github.com/openclaw/openclaw.git
cd openclaw
pnpm install
pnpm build

# 4. Initialize
pnpm openclaw onboard --install-daemon
```

---

### 🐧 Linux

#### Ubuntu/Debian

```bash
# Install Node.js
curl -fsSL https://deb.nodesource.com/setup_18.x | sudo -E bash -
sudo apt-get install -y nodejs

# Install pnpm
npm install -g pnpm

# Clone & setup
git clone https://github.com/openclaw/openclaw.git
cd openclaw
pnpm install
pnpm build
```

#### Fedora/RHEL

```bash
curl -fsSL https://rpm.nodesource.com/setup_18.x | sudo bash -
sudo dnf install -y nodejs

npm install -g pnpm
git clone https://github.com/openclaw/openclaw.git
cd openclaw
pnpm install
pnpm build
```

#### Arch Linux

```bash
sudo pacman -S nodejs pnpm
git clone https://github.com/openclaw/openclaw.git
cd openclaw
pnpm install
pnpm build
```

---

## 🚦 Usage

### Quick Start

```bash
# Clone the repo
git clone https://github.com/openclaw/openclaw.git
cd openclaw

# Install dependencies
pnpm install

# Build
pnpm build

# Initialize (recommended)
pnpm openclaw onboard --install-daemon

# Start the daemon
pnpm start
```

### Basic Commands

```bash
# Development mode (hot reload)
pnpm dev

# Production mode
pnpm build
pnpm start

# List available skills
openclaw skills list

# Use a skill
openclaw run backup

# Check status
openclaw status

# Get version
openclaw --version
```

---

## ⚙️ Configuration

### Environment Variables

Create a `.env` file in the openclaw folder:

```env
# OpenClaw Configuration
OPENCLAW_API_KEY=your_api_key_here

# Database
DATABASE_URL=postgresql://localhost:5432/openclaw

# Settings
LOG_LEVEL=info
AUTO_SAVE=true
THEME=dark
```

### Skill Configuration

Edit `skills.config.js`:

```javascript
module.exports = {
  skills: {
    automation: {
      enabled: true,
      schedule: '0 2 * * *',
      actions: ['clean', 'compress', 'upload']
    },
    deploy: {
      enabled: true,
      requires: ['build', 'test']
    }
  },
  settings: {
    logLevel: 'info',
    retryAttempts: 3,
    timeout: 30000
  }
}
```

---

## 📂 Folder Structure

```
openclaw/
├── 📁 src/              # Core agent code
├── 📁 extensions/       # Channel plugins
├── 📁 skills/           # Automation skills
├── 📁 docs/             # Documentation
├── 📁 packages/         # Shared packages
├── 📄 openclaw.config.js
├── 📄 package.json
└── 📄 README.md
```

---

## 🔧 Troubleshooting

| Issue | Cause | Solution |
|:-----|:------|:--------|
| `pnpm not found` | pnpm not installed | `npm install -g pnpm` |
| Permission denied | Admin rights needed | Run terminal as Administrator |
| Port in use | Another process | Change port in config |
| Build failed | Dependencies missing | Run `pnpm install` |

### Quick Fixes

```bash
# Clear cache
pnpm store clean

# Reinstall
rm -rf node_modules
pnpm install

# Update OpenClaw
pnpm update openclaw
```

---

## 🤝 Contributing

We welcome contributions! Here's how to help:

1. 🍴 **Fork** the [repository](https://github.com/openclaw/openclaw)
2. 🌿 **Create** a feature branch (`git checkout -b feature/amazing`)
3. 🔨 **Make** your changes
4. ✅ **Test** thoroughly
5. 📝 **Commit** with descriptive messages
6. 🚀 **Push** to your fork
7. 📥 **Submit** a Pull Request

---

## 📄 License

MIT Licensed — See [LICENSE](LICENSE) file for details.

---

## 🆘 Support

<p align="center">

[![GitHub Issues](https://img.shields.io/badge/Issues-Open-blue?style=for-the-badge&logo=github)](https://github.com/openclaw/openclaw/issues)
[![Discord](https://img.shields.io/badge/Join-Discord-5865F2?style=for-the-badge&logo=discord)](https://discord.gg/openclaw)
[![Website](https://img.shields.io/badge/Website-Visit-green?style=for-the-badge&logo=globe)](https://openclaw.ai)

</p>

---

<p align="center">
  <strong>Built with ❤️ by <a href="https://github.com/ssaahhil832">Sahil Khan</a> using <a href="https://github.com/openclaw/openclaw">OpenClaw</a></strong>
</p>

<p align="center">
  <img src="https://komarev.com/pills/?repo=openclaw&style=flat-square&color=00D4FF" alt="Profile views">
</p>