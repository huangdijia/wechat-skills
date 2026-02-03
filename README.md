# WeChat Skill

Agent Skill for sending WeChat messages on macOS. Control WeChat via AI conversation to send text and images to contacts or groups.

This skill follows the [Agent Skills specification](https://agentskills.io/specification) so it can be used by any skills-compatible agent, including Claude Code and Codex CLI.

## Installation

### Marketplace

Add this skill to your project:

```bash
/plugin marketplace add huangdijia/wechat-skills
/plugin install wechat@wechat-skills
```

Or manually clone to your project's `.claude/skills` directory:

```bash
cd .claude/skills
git clone https://github.com/huangdijia/wechat-skills wechat-skill
```

### Codex CLI

Copy the skills/ directory into your Codex skills path (typically ~/.codex/skills). See the Agent Skills specification for the standard skill format.

## Requirements

- macOS 12+
- Python 3.7+
- WeChat desktop application (logged in)
- Accessibility permissions enabled for your terminal/IDE

Grant accessibility permissions:

1. Open **System Settings** > **Privacy & Security** > **Accessibility**
2. Add your terminal application (Terminal, iTerm2, or VS Code)
3. Enable the toggle

## Capabilities

- **Send text messages** to contacts or groups by name
- **Send images** from local file paths
- **Combine text and images** in a single message

## Examples

Send a text message:

```
给张三发微信说"晚上一起吃饭"
Send a message to "John Doe" saying "Hello!"
```

Send an image:

```
给李四发送图片 ~/Desktop/photo.png
Send image ./screenshot.png to "Family Group"
```

Send both text and image:

```
给王五发消息"看看这个"并附带图片 ~/Downloads/image.jpg
Send "Check this out!" with image ./chart.png to "Project Team"
```

## Notes

Contact names must match exactly as they appear in WeChat (case-sensitive). During execution, do not use your mouse or keyboard as it will interfere with the automation.
