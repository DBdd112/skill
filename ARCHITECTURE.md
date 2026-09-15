# 架构总览

## 项目定位

一站式 AI 技能生态系统：
- 收集、整理、分发 245+ 个 Claude/Anthropic 兼容技能
- 提供技能商店前端展示
- 支持 Python 后端自动化（爬取、同步、数据管理）
- 包含 Antinet 多智能体协作系统

## 目录结构

```
skill/
├── skills/                    # 技能包（核心资产）
│   ├── content-creation/      #   内容创作与发布（12个）
│   ├── video-creation/        #   视频创作（10个）
│   ├── ecommerce/             #   电商与营销（7个）
│   ├── agent-collaboration/   #   智能体协作（7个）
│   ├── design/                #   设计与可视化（8个）
│   ├── ppt/                   #   PPT与演示（6个）
│   ├── digital-human/         #   数字人与配音（5个）
│   ├── audio/                 #   语音与音频（3个）
│   ├── docs-analysis/         #   文档与分析（3个）
│   ├── system/                #   系统工具（3个）
│   ├── tools/                 #   浏览器/笔记等工具（4个）
│   ├── legal/                 #   法律（1个）
│   ├── media/                 #   媒体处理（1个）
│   └── _template/             #   技能创建模板
│
├── core/                      # Python 核心引擎
│   ├── main.py                #   入口（命令行）
│   ├── crawler.py             #   爬虫
│   ├── data_manager.py        #   数据管理（JSON 存储）
│   ├── api_client.py          #   API 客户端
│   ├── scheduler.py           #   定时任务
│   ├── config.py              #   配置
│   └── requirements.txt
│
├── api/                       # Flask 后端
│   └── server.py              #   技能 CRUD + 搜索接口
│
├── web/                       # 前端展示（静态页面）
│   ├── index.html             #   技能商店首页
│   ├── skills.html            #   技能列表
│   ├── projects.html          #   项目展示
│   └── styles.css
│
├── projects/                  # AI 伴侣项目群
│   ├── assistant/             #   助手核心
│   ├── companion-skill/       #   伴侣技能
│   └── xiaoyue-web/           #   小跃 Web 端
│
├── antinet-agentteams/        # Antinet 多智能体团队
│
├── docs/                      # 文档中心
├── data/                      # 数据文件
├── scripts/                   # 自动化脚本
├── .github/workflows/         # CI/CD
└── README.md
```

## 数据流

```
GitHub 上游仓库 (awesome-agent-skills)
        │
        ▼
  core/crawler.py 爬取
        │
        ▼
  core/data_manager.py 存储 (data/local_skills.json)
        │
        ├──▶ api/server.py → 前端 web/
        └──▶ scripts/sync_skills.py → GitHub 仓库 → CI/CD → 部署
```

## 技术栈

| 层 | 技术 |
|----|------|
| 后端 | Python 3.9+, Flask |
| 前端 | 原生 HTML/CSS/JS（无框架） |
| 数据 | JSON 文件 |
| CI/CD | GitHub Actions |
| 部署 | Vercel（前端）+ GitHub Pages |
