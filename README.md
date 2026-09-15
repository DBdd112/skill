# 🎯 技能商店 - Skill Store

[![Stars](https://img.shields.io/github/stars/anbeime/skill?style=social)](https://github.com/anbeime/skill/stargazers)
[![Forks](https://img.shields.io/github/forks/anbeime/skill?style=social)](https://github.com/anbeime/skill/network/members)
[![Last Commit](https://img.shields.io/github/last-commit/anbeime/skill)](https://github.com/anbeime/skill/commits/main)
[![License](https://img.shields.io/badge/license-CC--BY--4.0-blue)](https://creativecommons.org/licenses/by/4.0/)

收录最全、更新最快的 AI Agent 技能库，涵盖**文档处理、内容创作、编程开发、机器学习、自动化工作流**等多个领域的精选技能包。

## 📊 技能统计

| 分类 | 数量 | 说明 |
|------|------|------|
| 内容创作 | 12 | 网页采集→Markdown→配图→多平台发布 |
| 视频创作 | 10 | 视频生成、剪辑、分析 |
| 电商营销 | 7 | 跨境电商全链路 |
| 智能体协作 | 7 | 多智能体团队协作 |
| 设计可视化 | 8 | 前端、架构图、插画 |
| PPT演示 | 6 | PPT 生成与美化 |
| 数字人配音 | 5 | 数字人口播、TTS |
| 语音音频 | 3 | TTS/ASR |
| 文档分析 | 3 | 论文/股票/PDF |
| 系统工具 | 3 | 图标、简历、PM |
| 其他工具 | 4 | 浏览器、笔记 |
| 法律/媒体 | 2 | 法律合同、媒体处理 |
| **合计** | **70+** | |

## 📁 目录结构

```
skill/
├── skills/                    # 技能包（按分类组织）
│   ├── content-creation/      #   内容创作
│   ├── video-creation/        #   视频创作
│   ├── ecommerce/             #   电商营销
│   ├── agent-collaboration/   #   智能体协作
│   ├── design/                #   设计可视化
│   ├── ppt/                   #   PPT演示
│   ├── digital-human/         #   数字人配音
│   ├── audio/                 #   语音音频
│   ├── docs-analysis/         #   文档分析
│   ├── system/                #   系统工具
│   ├── tools/                 #   其他工具
│   ├── legal/                 #   法律
│   ├── media/                 #   媒体
│   └── _template/             #   技能模板
├── core/                      # Python 核心（爬虫/同步/数据管理）
├── api/                       # Flask API 服务
├── web/                       # 前端展示页面
├── projects/                  # AI 伴侣项目群
├── antinet-agentteams/        # Antinet 多智能体团队
├── docs/                      # 文档中心
├── data/                      # 数据文件
└── scripts/                   # 自动化脚本
```

## 🚀 快速开始

### 使用技能包

每个技能包包含 `SKILL.md`，直接放入 Agent 平台的技能目录：

| 平台 | 路径 |
|------|------|
| Claude Code | `~/.claude/skills/` 或项目 `.claude/skills/` |
| OpenClaw | `~/.openclaw/skills/` |
| OpenAI | `~/.openai/skills/` |

### 运行 Python 后端

```bash
cd core
pip install -r requirements.txt
python main.py crawl        # 爬取最新技能
python main.py list         # 列出已存储技能
```

### 启动 API

```bash
cd api
pip install flask
python server.py            # http://localhost:5000
```

## 📖 更多文档

- [架构说明](ARCHITECTURE.md)
- [开发指南](DEVELOPMENT.md)
- [部署指南](DEPLOYMENT.md)
