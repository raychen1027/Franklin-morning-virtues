# 🌅 富兰克林晨间准则 Franklin Morning Virtues

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Platform: Claude Code](https://img.shields.io/badge/Platform-Claude%20Code-blue)](https://claude.ai/code)
[![Platform: OpenClaw](https://img.shields.io/badge/Platform-OpenClaw-green)](https://github.com/topics/openclaw)

> 每日清晨，以富兰克林13条道德准则开启智慧一天
> Start your day with Benjamin Franklin's 13 Virtues

## 📖 简介 Introduction

这是一个基于 ISO 周数循环的每日晨间准则提醒工具，帮助你通过富兰克林的13条道德准则进行自我修习。

This is a daily morning reminder tool based on ISO week rotation, helping you practice Benjamin Franklin's 13 Virtues.

### 核心理念 Core Philosophy

富兰克林在20岁时为自己制定了"道德完善计划"，每次专注于一条准则，用一周时间刻意修习。一年完成四轮练习，13条准则循环往复。

本 skill 按照 ISO 周数自动计算当日准则：
- 第 1 周 → 节制 (Temperance)
- 第 2 周 → 缄默 (Silence)
- ...
- 第 13 周 → 谦逊 (Humility)
- 第 14 周 → 回到节制，开始新一轮循环

## 🚀 安装 Installation

### 方法一：Claude Code 安装（推荐）

```bash
# 克隆仓库
git clone https://github.com/yourusername/franklin-morning-virtues.git

# 进入目录
cd franklin-morning-virtues

# 安装 skill
claude skills install ./franklin-virtues.skill
```

### 方法二：OpenClaw 安装

#### 选项 A：直接导入 System Prompt

1. 打开 OpenClaw 设置
2. 找到 **System Prompt** 或 **Custom Instructions**
3. 复制 [`openclaw/skill.md`](openclaw/skill.md) 的内容粘贴进去
4. 保存后，说"生成今日富兰克林准则"即可触发

#### 选项 B：使用 OpenClaw 的 Skill 系统

```bash
# 克隆到 OpenClaw skills 目录
git clone https://github.com/yourusername/franklin-morning-virtues.git ~/.openclaw/skills/franklin-virtues
```

然后在 OpenClaw 界面中启用该 skill。

### 方法三：手动使用

直接复制 `openclaw/skill.md` 中的内容到对话框，然后询问今日准则即可。

## 📝 使用方法 Usage

### 触发语句 Trigger Phrases

安装后，以下任意语句均可触发：

- "生成今日富兰克林晨间准则"
- "富兰克林晨间提醒"
- "今天富兰克林哪一条"
- "富兰克林十三条"
- "morning virtue"
- "富兰克林晨课"

### 设置定时提醒 Set Daily Reminder

#### Claude Code 定时任务

```bash
claude cron create "0 6 * * *" "生成今日富兰克林晨间准则提醒" --durable
```

每天早上 6 点自动生成当日准则。

#### OpenClaw 定时任务

在 OpenClaw 配置中添加：
```yaml
schedule: "0 6 * * *"
prompt: "生成今日富兰克林晨间准则提醒"
```

## 📂 项目结构 Project Structure

```
franklin-morning-virtues/
├── README.md                    # 项目说明
├── LICENSE                      # MIT 许可证
├── .gitignore                   # Git 忽略文件
├── franklin-virtues.skill       # Claude Code skill 包
├── claude-code/
│   ├── SKILL.md                 # Claude Code skill 定义
│   └── scripts/
│       └── virtue_selector.py   # ISO 周数计算脚本
└── openclaw/
    ├── skill.md                 # OpenClaw skill 提示词
    └── virtue_calculator.md     # 手动计算参考
```

## 🎯 输出格式 Output Format

每次触发会生成三段式结构：

```
🌅 富兰克林晨间准则 | 第{X}周

━━━━━━━━━━━━━━━━━━━━
一、本周准则
━━━━━━━━━━━━━━━━━━━━
{中文名} | {英文名}

"{英文原文}"

简要阐释：...

━━━━━━━━━━━━━━━━━━━━
二、名将通鉴
━━━━━━━━━━━━━━━━━━━━
古今中外名人事例...

━━━━━━━━━━━━━━━━━━━━
三、今日行动
━━━━━━━━━━━━━━━━━━━━
职业经理人专属行动建议...
```

## 📅 13条准则一览 13 Virtues Overview

| 周数 | 中文 | 英文 | 核心要义 |
|------|------|------|----------|
| 1 | 节制 | Temperance | 饮食有度，头脑清醒 |
| 2 | 缄默 | Silence | 言必有益，避免碎语 |
| 3 | 秩序 | Order | 各归其位，各按其时 |
| 4 | 决心 | Resolution | 当作必作，做则做成 |
| 5 | 节俭 | Frugality | 杜绝浪费，不花闲钱 |
| 6 | 勤奋 | Industry | 珍惜时光，忙有益事 |
| 7 | 真诚 | Sincerity | 不欺不诈，实事求是 |
| 8 | 正义 | Justice | 不损人利己，尽职守责 |
| 9 | 中庸 | Moderation | 避免极端，忍让化怨 |
| 10 | 清洁 | Cleanliness | 身体、衣着、居所整洁 |
| 11 | 宁静 | Tranquility | 不为琐事搅乱方寸 |
| 12 | 节欲 | Chastity | 珍视精力，远离沉溺 |
| 13 | 谦逊 | Humility | 效法耶稣和苏格拉底 |

## 🤝 贡献 Contributing

欢迎提交 Issue 或 Pull Request！

### 如何贡献

1. Fork 本仓库
2. 创建你的特性分支 (`git checkout -b feature/AmazingFeature`)
3. 提交更改 (`git commit -m 'Add some AmazingFeature'`)
4. 推送到分支 (`git push origin feature/AmazingFeature`)
5. 打开 Pull Request

## 📜 许可证 License

本项目采用 [MIT License](LICENSE) 开源。

## 🙏 致谢 Acknowledgments

- 本杰明·富兰克林 (Benjamin Franklin) - 13条道德准则的创立者
- Claude Code - 提供 skill 系统支持
- OpenClaw 社区 - 提供开源生态支持

---

> "我未曾见过一个早起、勤奋、谨慎、诚实的人抱怨命运不好。"
> —— 本杰明·富兰克林

Made with ❤️ for self-improvement.
