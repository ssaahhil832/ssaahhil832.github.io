# 🚀 OpenCLAW User Guide

<p align="center">
  <img src="https://img.shields.io/badge/Version-1.0.0-blue?style=for-the-badge&logo=version&color=00D4FF" alt="Version">
  <img src="https://img.shields.io/badge/License-MIT-green?style=for-the-badge&color=22C55E" alt="License">
  <img src="https://img.shields.io/badge/Platform-Windows%20%7C%20macOS%20%7C%20Linux-purple?style=for-the-badge&color=8B5CF6" alt="Platform">
  <img src="https://img.shields.io/badge/Open%20Source-100%25-orange?style=for-the-badge&color=FF6B00" alt="Open Source">
</p>

---

> **OpenCLAW** (Open Command Line Automation Wizard) — Built on [OpenClaw](https://github.com/openclaw/openclaw), the personal AI assistant that runs on your own devices.

---

## 📋 Table of Contents

1. [Prerequisites](#prerequisites)
2. [Universal Installation](#universal-installation)
3. [Platform-Specific Setup](#platform-specific-setup)
4. [Common Errors](#common-errors)
5. [Optional: Ollama Setup](#optional-ollama-setup)
6. [Troubleshooting](#troubleshooting)
7. [Contributing](#contributing)

---

## ✅ Prerequisites

Before installing, make sure you have:

| Tool | Version | Required |
|:-----|:--------|:---------|
| **Node.js** | v20+ recommended | ✅ Yes |
| **Git** | Latest | ✅ Yes |
| **pnpm** | Latest | ✅ Yes (IMPORTANT) |

---

## 🔥 UNIVERSAL METHOD (Works on All Platforms)

### Step 1: Clone the repo

```bash
git clone https://github.com/openclaw/openclaw.git
cd openclaw
```

### Step 2: Install pnpm globally

```bash
npm install -g pnpm
```

### Step 3: Install dependencies

```bash
pnpm install
```

### Step 4: Run the project

```bash
pnpm dev
```

---

## 🪟 Platform-Specific Setup

### ⚠️ IMPORTANT: Choose Your Method

| Method | Status | Notes |
|:-------|:-------|:------|
| Windows CMD | 😐 Unstable | Not recommended for heavy builds |
| **Windows + WSL** | ✅ BEST | Recommended for Windows users |
| **Linux** | ✅ BEST | Full support |
| **macOS** | ✅ BEST | Full support |

---

### 🪟 Windows (NOT Recommended)

> ❌ **Problems with Windows CMD:**
> - Build stuck (tsdown issue)
> - File linking issues  
> - Slow node_modules

**If you MUST use Windows CMD:**

```powershell
# Clone the repo
git clone https://github.com/openclaw/openclaw.git
cd openclaw

# Install pnpm
npm install -g pnpm

# Install dependencies
pnpm install

# Build
pnpm build

# Run
pnpm dev
```

**⚠️ If stuck, try:**

```powershell
set TS_NODE_TRANSPILE_ONLY=1
pnpm dev
```

---

### ✅ Windows + WSL (BEST for Windows) 🔥

#### Step 1: Install WSL

```powershell
wsl --install
```

#### Step 2: Open Ubuntu terminal

#### Step 3: Install Node.js

```bash
sudo apt update
sudo apt install nodejs npm -y
```

**Upgrade to Node.js v20:**

```bash
sudo npm install -g n
sudo n 20
```

#### Step 4: Install pnpm

```bash
npm install -g pnpm
```

#### Step 5: Clone repo INSIDE WSL

```bash
cd ~
git clone https://github.com/openclaw/openclaw.git
cd openclaw
```

#### Step 6: Install & Run

```bash
pnpm install
pnpm dev
```

---

### 🐧 Linux (Ubuntu / Debian)

#### Step 1: Install dependencies

```bash
sudo apt update
sudo apt install git nodejs npm -y
```

**Upgrade to Node.js v20:**

```bash
sudo npm install -g n
sudo n 20
```

#### Step 2: Install pnpm

```bash
npm install -g pnpm
```

#### Step 3: Clone & Run

```bash
git clone https://github.com/openclaw/openclaw.git
cd openclaw

pnpm install
pnpm dev
```

---

### 🍎 macOS

#### Step 1: Install Homebrew

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

#### Step 2: Install Node.js & Git

```bash
brew install node git
```

#### Step 3: Install pnpm

```bash
npm install -g pnpm
```

#### Step 4: Clone & Run

```bash
git clone https://github.com/openclaw/openclaw.git
cd openclaw

pnpm install
pnpm dev
```

---

## 🔗 Optional: Ollama Setup (Local AI)

Ollama provides local AI capabilities for OpenClaw.

### Install Ollama

```bash
# For macOS/Linux
curl -fsSL https://ollama.ai/install.sh | sh

# For Windows (WSL)
wsl -s
curl -fsSL https://ollama.ai/install.sh | sh
```

### Use Ollama with OpenClaw

```bash
# Run a model
ollama run llama3

# Connect in OpenClaw config
```

---

## 🧨 Common Errors & Solutions

| Error | Cause | Solution |
|:------|:------|:--------|
| `node not found` | Node.js not installed | Install Node.js v20+ |
| `json5 missing` | npm install incomplete | Use `pnpm install` instead |
| Build stuck (`tsdown`) | Windows issue | Use WSL |
| Slow copy | Copying node_modules | Don't copy node_modules, run pnpm install |

### Quick Fix Commands

```bash
# Fix pnpm issues
pnpm store clean

# Reinstall everything
rm -rf node_modules
pnpm install

# If stuck on Windows
set TS_NODE_TRANSPILE_ONLY=1
pnpm dev
```

---

## 📊 Recommended Setup Summary

| Your Platform | Use This |
|:-------------|:---------|
| Windows 10/11 | **WSL + Ubuntu** |
| Linux (any) | Direct terminal |
| macOS | Terminal |
| Windows 11 + Docker | Docker container |

---

## 🎯 My Recommendation

> **Use: Windows + WSL + pnpm**
> 
> This is how professional developers run this type of project. WSL gives you Linux power while keeping Windows.

---

## 🤝 Contributing

1. 🍴 **Fork** the [repository](https://github.com/openclaw/openclaw)
2. 🌿 **Create** a feature branch (`git checkout -b feature/amazing`)
3. 🔨 **Make** your changes
4. ✅ **Test** thoroughly
5. 📝 **Commit** with descriptive messages
6. 🚀 **Push** to your fork
7. 📥 **Submit** a Pull Request

---

## 📄 License

MIT Licensed

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