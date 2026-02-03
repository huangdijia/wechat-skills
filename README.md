# WeChat Skill

A Claude Code skill for controlling WeChat on macOS. Send messages and images to contacts or groups through AI conversation.

## Skill Installation

### 1. Clone to Skills Directory

```bash
cd ~/.claude/skills  # Claude Code skills directory
git clone <repository-url> wechat-skill
```

### 2. Install Dependencies

```bash
cd wechat-skill
pip3 install pyautogui pyperclip pyperclipimg
```

### 3. Grant Accessibility Permissions

Claude Code requires accessibility permissions to control keyboard automation:

**macOS Ventura and later (macOS 13+):**
1. Open **System Settings** > **Privacy & Security** > **Accessibility**
2. Click the **+** button
3. Add the application running Claude Code (Terminal, iTerm2, or VS Code)
4. Enable the toggle

**macOS Monterey and earlier (macOS 12-):**
1. Open **System Preferences** > **Security & Privacy** > **Privacy** > **Accessibility**
2. Click the lock icon to make changes
3. Add the application running Claude Code
4. Check the checkbox

## AI Usage Examples

Once installed, you can ask Claude to send WeChat messages:

### Send Text Message
```
给张三发微信说"晚上一起吃饭"
```
```
Send a message to "John Doe" saying "Hello!"
```

### Send Image
```
给李四发送图片 "~/Desktop/photo.png"
```
```
Send the image "./screenshot.png" to "Family Group"
```

### Send Text and Image
```
给王五发消息"看看这个"并附带图片 "~/Downloads/image.jpg"
```
```
Send "Check this out!" with image "./chart.png" to "Project Team"
```

## Requirements

- macOS 12+
- Python 3.7+
- WeChat desktop application (logged in)
- Accessibility permissions enabled for Claude Code's host application

## Important Notes

⚠️ **During execution, do not use your mouse or keyboard** as it will interfere with the automation.

⚠️ **Contact names must match exactly** as they appear in WeChat (case-sensitive).

⚠️ **WeChat window must not be minimized** during execution.

## License

MIT License
