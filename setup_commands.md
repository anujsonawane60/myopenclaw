# OpenClaw Setup Guide

A step-by-step guide to setting up [OpenClaw](https://openclaw.ai/) on an AWS EC2 instance.

---

## 1. Setup AWS EC2

1. Go to the [AWS Console](https://console.aws.amazon.com/) and navigate to **EC2**.
2. Launch a new instance with the following settings:

| Setting | Value |
|---|---|
| **Name** | `openclaw_test` |
| **OS** | Ubuntu |
| **Instance Type** | `m7i-flex.large` |
| **Key Pair** | `openclaw_test_aiwithhassan.pem` |
| **Storage** | `30 GiB` |

> ⚠️ **Keep your `.pem` key file safe** — you'll need it to SSH into the instance.

3. Update the system packages:

```bash
sudo apt update && sudo apt upgrade -y
```

---

## 2. Install OpenClaw

Website: [https://openclaw.ai/](https://openclaw.ai/)

**🐧 Linux / 🍎 Mac:**

```bash
curl -fsSL https://openclaw.ai/install.sh | bash
source ~/.bashrc
```

**🪟 Windows (PowerShell as Administrator):**

```powershell
irm https://openclaw.ai/install.ps1 | iex
# Or using curl:
curl -fsSL https://openclaw.ai/install.sh | bash   # (via WSL)
```

> 💡 Press `Ctrl + C` to cancel if it starts running in the terminal after install.

---

## 3. Setup OpenRouter

1. Go to [OpenRouter](https://openrouter.ai/) and create an account.
2. Generate an **API key** from the dashboard.
3. Keep the key handy — you'll use it during OpenClaw onboarding.

---

## 4. Setup ElevenLabs

1. Go to [ElevenLabs](https://elevenlabs.io/) and create an account.
2. Generate an **API key** from the dashboard.

---

## 5. Onboard OpenClaw

Run the onboarding wizard to configure your OpenClaw instance:

**🐧 Linux / 🍎 Mac / 🪟 Windows:**

```bash
openclaw onboard
```

> This walks you through setting your name, AI persona, API keys, and preferences.

### Suggested First Message

Use something like this as your initial prompt to personalize OpenClaw:

> Hi, my name is **[Your Name]**. I am a **[Your Profession/Role]**. Your name is **[AI Name]**. I like to stay updated on **[Your Interests, e.g., AI, tech, finance]**. Our relationship vibe should be **[e.g., professional yet friendly]**. I think of you as my personal assistant who helps me stay organized, informed, and productive throughout the day. Add much information here as possible (DONT SHARE SECRET INFORMATION)

---

## 6. Setup Telegram Bot

### Install Telegram

- [Android (Google Play)](https://play.google.com/store/apps/details?id=org.telegram.messenger)
- [iOS (App Store)](https://apps.apple.com/app/telegram-messenger/id686449807)
- [Windows / Mac / Linux (Desktop)](https://desktop.telegram.org/)

### Create a Bot

1. Open Telegram and search for [@BotFather](https://t.me/BotFather).
2. Send `/start`, then `/newbot`.
3. Give your bot a **name** and a **username**.
4. Copy the bot token provided by BotFather. 

### Connect Bot to OpenClaw

**🐧 Linux / 🍎 Mac / 🪟 Windows:**

```bash
openclaw pairing approve telegram <your-bot-username>
```

---

## 7. Setup Brave Search API

1. Go to [Brave Search API](https://brave.com/search/api/) and create an account.
2. Generate an API key and add it to your OpenClaw configuration.

---

## 8. Setup ZAI API

1. Go to the [ZAI API Portal](https://zai.com/) and generate an API key.

---

## 9. Connect to EC2

### Via SSH (Terminal)

**🐧 Linux / 🍎 Mac:**

```bash
# Set correct permissions on your key file
chmod 400 <path-to-pem-file>

# Connect to the instance
ssh -i <path-to-pem-file> ubuntu@<public-ip-of-ec2>
```

**🪟 Windows (PowerShell):**

```powershell
# Set correct permissions on your key file
icacls <path-to-pem-file> /inheritance:r /grant:r "%USERNAME%:R"

# Connect to the instance
ssh -i <path-to-pem-file> ubuntu@<public-ip-of-ec2>
```

**🪟 Windows (Command Prompt):**

```cmd
# Connect to the instance (use PuTTY or OpenSSH)
ssh -i <path-to-pem-file> ubuntu@<public-ip-of-ec2>
```

### Via Browser (Port Forwarding)

**🐧 Linux / 🍎 Mac:**

```bash
ssh -i <path-to-pem-file> -N -L 18789:127.0.0.1:18789 ubuntu@<public-ip-of-ec2>
```

**🪟 Windows (PowerShell / CMD):**

```powershell
ssh -i <path-to-pem-file> -N -L 18789:127.0.0.1:18789 ubuntu@<public-ip-of-ec2>
```

Then open `http://localhost:18789` in your browser.

---

## 10. OpenClaw Commands Reference

All commands work the same on **Linux**, **Mac**, and **Windows**.

| Command | Description |
|---|---|
| `openclaw onboard` | Run the onboarding/setup wizard |
| `openclaw tui` | Launch the terminal UI |
| `openclaw gateway` | Start the API gateway |
| `openclaw model configure` | Configure AI models |
| `openclaw skills` | Manage and view available skills |

### Run with Ollama (Local Models)

**🐧 Linux / 🍎 Mac:**

```bash
ollama serve
ollama run <model-name>
```

**🪟 Windows (PowerShell / CMD):**

```powershell
ollama serve
ollama run <model-name>
```

---

## 11. Uninstall OpenClaw

**🐧 Linux / 🍎 Mac:**

```bash
npm uninstall -g openclaw
```

**🪟 Windows (PowerShell / CMD):**

```powershell
npm uninstall -g openclaw
```

---

## 🙌 Shoutouts

A huge thanks to the amazing community and creators pushing the boundaries with OpenClaw!

 ### 🌟 Community Highlights

| Who | What They Built | Link |
|---|---|---|
| 🧠 OpenClaw Team | The core platform powering personal AI agents | [openclaw.ai](https://openclaw.ai/) |
| 🎥 AI With Hassan | Tutorials & walkthroughs for setting up OpenClaw | [YouTube](https://youtube.com/@aiwithhassan) |

### 🔗 Useful Resources

- 📖 [OpenClaw Documentation](https://openclaw.ai/docs)
- 💬 [OpenClaw Community / Discord](https://openclaw.ai/community)
- 🐦 [OpenClaw on Twitter/X](https://x.com/openclaw)
- 🌐 [Community Shoutouts Page](https://openclaw.ai/shoutouts)

---

> ⭐ **If you found this guide helpful, give it a star and share it with others!**
