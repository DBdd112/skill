# 开发指南

## 快速开始

### 1. 克隆仓库

```bash
git clone https://github.com/anbeime/skill.git
cd skill
```

### 2. 安装依赖（Python 后端）

```bash
cd core
pip install -r requirements.txt
```

### 3. 运行爬虫

```bash
cd core
python main.py crawl          # 爬取最新技能
python main.py list           # 列出已存储技能
python main.py sync           # 同步到本地
```

### 4. 启动 API 服务

```bash
cd api
pip install flask
python server.py             # http://localhost:5000
```

### 5. 查看前端

直接用浏览器打开 `web/index.html`，或推送到 Vercel 自动部署。

## 添加新技能

1. 复制 `skills/_template/` 为新目录
2. 编辑 `SKILL.md`（名称、描述、触发条件、执行步骤）
3. 在 `skills/` 对应的分类目录下创建（或新建分类）
4. 可选：添加 `scripts/`、`assets/`、`references/`
5. 提交并推送到 GitHub

## 技能包结构

```
skills/某分类/技能名/
├── SKILL.md          # 必须：技能定义（Anthropic 格式）
├── scripts/          # 可选：可执行脚本
├── assets/           # 可选：模板/素材
├── references/       # 可选：参考文档
└── agents/           # 可选：多智能体配置
```

## CI/CD 流程

| 触发条件 | 动作 |
|---------|------|
| 推送到 main | 自动同步技能数据 → 更新 web/ → 部署 Vercel |
| 手动调度 | 每日爬取最新 awesome-agent-skills |

## 分类标准

| 分类 | 说明 | 示例 |
|------|------|------|
| content-creation | 网页采集→Markdown→配图→发布 | content-creation-publisher |
| video-creation | 视频生成、剪辑、分析 | video-creation-suite |
| ecommerce | 电商全链路 | ecommerce-full-pipeline |
| agent-collaboration | 多智能体协作 | agent-team |
| design | 前端、架构图、插画 | frontend-design |
| ppt | PPT 生成与美化 | NanoBanana-PPT-Skills |
| digital-human | 数字人、配音 | infinitetalk |
| audio | TTS/ASR | tts-voice-synthesis |
| docs-analysis | 论文/股票/PDF 分析 | paper-analysis-assistant |
| system | 系统级工具 | icon-generator |
| tools | 浏览器、笔记 | chrome-automation |
| legal | 法律相关 | legal-assistant-skills-main |
| media | 媒体处理 | media-processor |
