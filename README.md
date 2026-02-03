# WeChat Skill

A Python automation tool for controlling WeChat on macOS using pyautogui. Send messages and images to contacts or groups programmatically.

## Features

- **Open WeChat** - Launch WeChat via Spotlight search
- **Search Contacts** - Find contacts or groups by name
- **Send Text Messages** - Type and send text messages
- **Send Images** - Send image files from local storage
- **Combine Messages** - Send both text and images in one command

## Requirements

- macOS (tested on macOS 12+)
- Python 3.7+
- WeChat desktop application
- Accessibility permissions enabled for your terminal/IDE

## Installation

1. Clone or download this repository:

```bash
git clone <repository-url>
cd wechat-skill
```

1. Install dependencies:

```bash
pip install pyautogui pyperclip pyperclipimg
```

1. Grant accessibility permissions:
   - Open **System Settings** > **Privacy & Security** > **Accessibility**
   - Add your terminal application (e.g., Terminal, iTerm2, VS Code)
   - Ensure the toggle is enabled

## Quick Start

```bash
cd scripts

# Send a text message
python3 wechat_send.py --name "John Doe" --message "Hello!"

# Send an image
python3 wechat_send.py --name "Family Group" --image_path="./photo.png"

# Send both message and image
python3 wechat_send.py --name "John Doe" --message "Check this out!" --image_path="./screenshot.png"
```

## Command Line Arguments

| Argument | Required | Description |
|----------|----------|-------------|
| `--name` | Yes | Contact or group name (must match exactly as shown in WeChat) |
| `--message` | At least one | Text message content to send |
| `--image_path` | At least one | Path to the image file to send |

**Note:** At least one of `--message` or `--image_path` must be provided.

## How It Works

This tool uses `pyautogui` to simulate keyboard actions:

1. **Open WeChat** (`Cmd+Space` → type "微信" → `Enter`)
2. **Search Contact** (`Cmd+F` → paste name → `Enter`)
3. **Send Content** (copy to clipboard → paste → `Enter`)

## Project Structure

```
wechat-skill/
├── README.md              # Project documentation
├── SKILL.md               # Detailed skill/usage guide
├── scripts/
│   └── wechat_send.py     # Main automation script
└── test.png               # Example image for testing
```

## Important Notes

⚠️ **During execution, do not use your mouse or keyboard** as it will interfere with the automation.

⚠️ **WeChat must be logged in** before running the script.

⚠️ **Contact names must match exactly** as they appear in WeChat (case-sensitive).

⚠️ **Accessibility permission is required** for pyautogui to control your system.

## Troubleshooting

### WeChat doesn't open

- Ensure WeChat is installed in `/Applications/WeChat.app`
- Try manually opening WeChat first to ensure it's properly logged in

### Contact not found

- Make sure the contact name matches exactly (including spaces and capitalization)
- For groups, ensure you're already a member of the group

### Permission denied

- Check System Settings > Privacy & Security > Accessibility
- Add and enable your terminal application

### Message not sent

- Ensure WeChat window is not minimized during execution
- Try increasing the sleep delays in the script if your system is slower

## Limitations

- macOS only (uses macOS-specific keyboard shortcuts)
- Requires WeChat to be in the foreground during execution
- Cannot send to contacts not in your WeChat address book
- Image sending requires `pyperclipimg` which has limited format support (PNG, JPEG)

## Safety

This tool is intended for personal automation and productivity purposes only. Please:

- Respect WeChat's Terms of Service
- Do not use for spam or automated harassment
- Use responsibly and in moderation

## License

MIT License - Feel free to use and modify for personal use.

## Contributing

Contributions are welcome! Please ensure your changes:

- Work on macOS with the latest WeChat version
- Include appropriate error handling
- Update documentation as needed
