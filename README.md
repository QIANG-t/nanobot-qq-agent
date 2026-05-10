# nanobot-qq-agent
# 🤖 QQ AI Agent - 本地化智能助手

> 基于 Nanobot 框架、运行在 QQ 平台的个人 AI 助理，支持本地大模型（Ollama）、自定义技能、任务规划与长期记忆。

[![Python](https://img.shields.io/badge/Python-3.10+-blue.svg)](https://python.org)
[![Nanobot](https://img.shields.io/badge/Nanobot-0.1.5-green.svg)](https://github.com/HKUDS/nanobot)
[![Ollama](https://img.shields.io/badge/Ollama-0.5+-orange.svg)](https://ollama.com)

---

## ✨ 核心能力

- 🧠 **完全本地化**：通过 Ollama 部署 Qwen2.5:7b 模型，数据不出本地，零 API 费用，保护隐私。
- 🛠️ **自定义技能扩展**：新增能力只需编写一个 `SKILL.md` 文件，无需修改核心代码。
- 💬 **QQ 平台接入**：7×24 小时在线，支持私聊和群聊 @ 唤醒。
- 🔄 **ReAct 推理闭环**：Agent 自主完成“思考 → 行动 → 观察”的完整任务流程。
- 📊 **对话式运维**：通过自然语言即可查询系统状态（CPU、内存、磁盘）。
- 🧠 **长期记忆**：Dream 进程自动提炼对话关键信息，存入 `MEMORY.md`，跨会话生效。

---

## 🎯 功能示例

| 用户指令 | Agent 行为 |
|----------|-------------|
| `你好` | 普通对话 |
| `用 daily-news` | 自动搜索并返回当日科技/AI 新闻简报 |
| `用 system-monitor` | 返回本机 CPU、内存、磁盘使用情况 |

---

## 🛠️ 技术栈

| 组件 | 选型 | 说明 |
|------|------|------|
| Agent 框架 | Nanobot | 轻量（~4000行核心代码），易于理解与二次开发 |
| 大模型 | Ollama + Qwen2.5:7b | 本地推理，支持 Function Calling |
| IM 平台 | QQ 官方机器人 API | 稳定、免费、易申请 |
| 工具调用 | Windows 原生命令 (wmic) + DuckDuckGo 搜索 | 打通 LLM 与操作系统 / 互联网 |

---

## 🚀 快速开始

### 1. 环境准备
- Python 3.10+
- Ollama（[下载](https://ollama.com/)）
- QQ 机器人（[官方申请教程](https://q.qq.com/)）

### 2. 克隆项目
```bash
git clone https://github.com/QIANG-t/nanobot-qq-agent.git
