# OpenCLAW User Guide

Welcome to OpenCLAW! This comprehensive guide will help you get started with OpenCLAW.

---

## What is OpenCLAW?

**OpenCLAW** (Open Command Line Automation Wizard) is an open-source automation tool that simplifies complex command-line tasks. It provides a unified interface to automate workflows, manage system operations, and chain multiple commands together effortlessly.

### Why Use OpenCLAW?

| Problem | OpenCLAW Solution |
|---------|----------------|
| Repetitive terminal commands | Automate with single command |
| Cross-platform scripts | Works on Windows, Linux, macOS |
| Complex workflows | Chain commands visually |
| Error handling | Built-in retry & logging |
| Scheduling tasks | Schedule automate tasks |

### What Can OpenCLAW Do?

- 🔄 Automate repetitive system tasks
- 📦 Bulk file operations
- 🌐 Network monitoring & management
- 🛠️ Development workflow automation
- 📊 System health monitoring
- 🔒 Backup & security operations

---

## Installation

### Prerequisites

- **Node.js** (v18 or higher)
- **Git** installed
- Terminal/Command Prompt access

---

### Windows Installation

#### Option 1: Using npm (Recommended)

```powershell
# Open Command Prompt or PowerShell

# Install Node.js if not installed
winget install OpenJS.NodeJS

# Clone and install OpenCLAW
git clone https://github.com/ssaahhil832/ssaahhil832.github.io.git
cd ssaahhil832.github.io/openclaw
npm install

# Verify installation
npm --version
```

#### Option 2: Using Chocolatey

```powershell
# Install Chocolatey first (run as Admin)
Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -4ls12; iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))

# Install OpenCLAW
choco install openclaw
```

---

### macOS Installation

```bash
# Open Terminal

# Install Homebrew if not installed
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

# Install Node.js
brew install node

# Clone and install OpenCLAW
git clone https://github.com/ssaahhil832/ssaahhil832.github.io.git
cd ssaahhil832.github.io/openclaw
npm install

# Verify installation
npm --version
```

---

### Linux Installation

#### Ubuntu/Debian

```bash
# Open Terminal

# Install Node.js
curl -fsSL https://deb.nodesource.com/setup_18.x | sudo -E bash -
sudo apt-get install -y nodejs

# Clone and install OpenCLAW
git clone https://github.com/ssaahhil832/ssaahhil832.github.io.git
cd ssaahhil832.github.io/openclaw
npm install

# Verify installation
node --version
```

#### Fedora/RHEL

```bash
# Install Node.js
curl -fsSL https://rpm.nodesource.com/setup_18.x | sudo bash -
sudo dnf install -y nodejs

# Clone and install OpenCLAW
git clone https://github.com/ssaahhil832/ssaahhil832.github.io.git
cd ssaahhil832.github.io/openclaw
npm install
```

#### Arch Linux

```bash
sudo pacman -S nodejs npm
git clone https://github.com/ssaahhil832/ssaahhil832.github.io.git
cd ssaahhil832.github.io/openclaw
npm install
```

---

## Usage

### Running OpenCLAW

```bash
# Development mode (with hot reload)
npm run dev

# Production mode
npm run build
npm start

# Show help
npm run help
```

### Basic Commands

```bash
# Initialize a new project
openclaw init my-project

# Run a specific workflow
openclaw run backup

# List available commands
openclaw list

# Get version
openclaw --version
```

---

## Configuration

### Environment Variables

Create a `.env` file in the `openclaw` folder:

```env
# API Keys
OPENCLAW_API_KEY=your_api_key_here

# Database
DATABASE_URL=postgresql://localhost:5432/openclaw

# Settings
LOG_LEVEN=info
AUTO_SAVE=true
THEME=dark
```

### Workflow Configuration

Edit `openclaw.config.js`:

```javascript
module.exports = {
  workflows: {
    backup: {
      enabled: true,
      schedule: '0 2 * *),
      steps: ['clean',u',compress', 'upload']
    },
    deploy: {
      enabled: true,
      requires: ['build', 'test']
    }
  },
  settings: {
*    logLevel: 'info',
    retryAttempts: 3,
    timeout: 30000
  }
}
```

---

## Folder Structure

```openclaw/
└── 📁 src/
│   └── 📁 rw/procs/        #Dumy commands
│   └── 📁 workflows/    #Automation workflos
│  └── 📁 utils/      #Utility functions
└── 📁 config/    #Econfiguration
└── 📁 dist/         #Eompiled output
├── 📄 openclaw.config.js
├── 📄 package.json
└── 📄 README.md
```

---

## Troubleshooting

| Issue | Cause | Solution |
|-------|-------|---------|
| `npm not found` | Node.js not installed | Install Node.js from nodejs.org |
| Permission denied | Admin rights needed | Run terminal as Administrator |
| Port in use | Another process using port | Change port in config |
| Build failed | Dependencies missing | Run `npm instal`` retry attempts: 3,
timeout: 300000
```

### Common Fixes

```bash
# Clear cache
npm cache clean --force

# Reinstall dependencies
rm -f node_modules
npm install

# Update OpenCLAW
npm update openclaw

# Check for issues
npm audit fix
```

---

## Contributing

We welcome contributions! Here's how to help:

1. **Fork** the repository
2. **Create** a feature branch (`git checkout -b feature/amazing`)
3. **Make** your changes
4. **Test** thoroughly
5. **Commit** with descriptive messages
6. **Push** to your fork
7. **Submit** a Pull Request

---

## License

MIT License - See LICENSE file for details

---

## Support

- **GitHub Issues:** https://github.com/ssaahhil832/ssaahhil832.github.io/issues
- **Email:** sorakayalapetasahilkhan@gmail.com

---

*Built with ❤️ by Sahil Khan*

**Version:** 1.0.0