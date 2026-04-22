<div align="center">

# WePlus - 校园智能助手平台

**基于 RAG 技术的全栈校园智能助手 · 前后端同仓 · 单容器部署**

[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![Python](https://img.shields.io/badge/python-3.11%2B-blue)](https://www.python.org/)
[![FastAPI](https://img.shields.io/badge/FastAPI-0.104-green)](https://fastapi.tiangolo.com/)
[![React](https://img.shields.io/badge/React-19-61DAFB)](https://react.dev/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.7-3178C6)](https://www.typescriptlang.org/)
[![PostgreSQL](https://img.shields.io/badge/PostgreSQL-14%2B-4169E1)](https://www.postgresql.org/)
[![Docker](https://img.shields.io/badge/Docker-ready-2496ED)](https://www.docker.com/)
[![Railway](https://img.shields.io/badge/Railway-deploy-7C3AED)](https://railway.app/)
[![Star](https://img.shields.io/badge/Star-✨-yellow)](https://github.com/your-username/weplus)

---

[📘 中文文档](#中文) | [📗 English Docs](#english)

</div>

---

# 中文

<p align="center">
  <a href="#项目简介">项目简介</a> •
  <a href="#在线体验">在线体验</a> •
  <a href="#最新动态">最新动态</a> •
  <a href="#核心功能">核心功能</a> •
  <a href="#系统架构">系统架构</a> •
  <a href="#快速开始">快速开始</a> •
  <a href="#部署指南">部署指南</a> •
  <a href="#项目结构">项目结构</a> •
  <a href="#文档">文档</a> •
  <a href="#api-文档">API 文档</a> •
  <a href="#路线图">路线图</a> •
  <a href="#贡献指南">贡献指南</a>
</p>

---

## 项目简介

WePlus 是一个基于 **RAG（检索增强生成）** 技术的校园智能助手平台，集成 DeepSeek 大语言模型和 pgvector 向量搜索引擎，为校园用户提供智能问答、文档管理、学习资源共享等服务。

> 🎯 **设计目标**：打造一个功能完整、可直接部署的全栈 Web 应用，展示现代 Web 开发的最佳实践。

### 适用场景

| 场景 | 说明 |
|------|------|
| 🎓 **校园智能问答** | 基于校园知识库的 AI 助手，回答学生各类问题 |
| 📄 **文档智能处理** | 上传 PDF/Word/Excel，自动解析、向量化、语义检索 |
| 📚 **学习资源共享** | 资源上传、分类、评分、评论、在线预览 |
| 🔧 **后台管理** | 用户管理、系统监控、日志审计、备份恢复 |

---

## 在线体验

<!--
  TODO: 部署后替换为实际链接
  示例:
  - 前端: https://weplus-demo.railway.app
  - API: https://weplus-demo.railway.app/api/healthz
-->

| 服务 | 地址 |
|------|------|
| 🌐 前端页面 | 部署后可用 |
| 📡 API 健康检查 | 部署后可用 |
| 📖 API 文档 (Swagger) | 部署后可用 |

> 💡 你也可以参考 [快速开始](#快速开始) 在本地启动项目进行体验。

### 界面预览

> 项目运行后，以下为主要页面：

| 页面 | 说明 |
|------|------|
| 🤖 RAG 智能聊天 | 上传文档后与 AI 进行基于知识库的对话 |
| 📚 学习资源 | 浏览、上传、搜索学习资源 |
| 👤 用户中心 | 注册、登录、个人信息管理 |
| 🛠️ 后台管理 | 系统仪表板、用户管理、日志审计 |

---

## 最新动态

### 🚀 近期更新

| 日期 | 更新内容 |
|------|----------|
| 2026-Q1 | 数据库从 SQLite 迁移至 PostgreSQL + pgvector |
| 2026-Q1 | 向量存储从 ChromaDB + FAISS 迁移至 pgvector |
| 2026-Q1 | 重构 Docker 部署为单容器架构（Nginx + Supervisord + Uvicorn） |
| 2026-Q1 | 集成 Railway 云部署支持 |
| 2026-Q1 | 全面重构项目文档，合并为结构化文档体系 |
| 2026-Q1 | 新增 Sentry 错误追踪与 Prometheus 监控 |
| 2025-Q4 | 完成 RAG 引擎核心功能开发 |
| 2025-Q4 | 完成前后端分离架构改造 |

### ⭐ 保持关注

如果你觉得这个项目有帮助，欢迎 Star 收藏，获取最新更新通知！

---

## 核心功能

### 🤖 RAG 智能聊天

检索增强生成引擎，让 AI 回答基于你的文档，告别幻觉。

- **文档即知识库**：上传 PDF、Word、Excel、PPT，自动构建知识库
- **语义搜索**：基于 pgvector 的向量相似度搜索，精准找到相关内容
- **流式响应**：Server-Sent Events 实时输出，打字机效果体验
- **多轮对话**：上下文记忆，连续问答

### 📚 学习资源管理

一站式学习资源平台，支持上传、分享、评价。

- **多格式支持**：文档、图片、视频等多种资源格式
- **分类标签**：灵活的标签和分类系统
- **社区互动**：评分、评论、收藏
- **在线预览**：无需下载即可查看文档内容

### 👥 用户系统

完整的用户生命周期管理，安全可靠。

- **JWT 认证**：Token 鉴权，自动续期
- **邮箱验证**：注册验证码，防止机器注册
- **权限分级**：普通用户 / 管理员两级权限
- **安全防护**：bcrypt 密码哈希、速率限制、IP 白名单

### 🛠️ 后台管理

功能完备的管理控制台，轻松运维。

- **系统仪表板**：实时数据概览和统计图表
- **用户管理**：用户 CRUD、状态管理、权限分配
- **文档管理**：上传记录、存储统计、索引管理
- **向量数据库**：索引重建、清理优化
- **系统日志**：操作审计、日志查询、导出
- **备份恢复**：一键备份、数据恢复

### 🔧 测试与监控

生产级可观测性，问题早发现早处理。

- **健康检查**：`/api/healthz` 端点，组件连通性检测
- **API 测试**：完整的 API 端点测试套件
- **性能监控**：Prometheus 指标收集
- **错误追踪**：Sentry 集成
- **结构化日志**：JSON 格式，便于日志分析

---

## 系统架构

### 架构总览

```
┌─────────────────────────────────────────────────────────┐
│                    用户层 (User)                         │
│         Web 浏览器  ·  移动端  ·  API 客户端             │
└──────────────────────┬──────────────────────────────────┘
                       │ HTTPS
┌──────────────────────▼──────────────────────────────────┐
│                  接入层 (Gateway)                        │
│    Nginx (反向代理 + 静态文件 + SSL 终止)                 │
│    CORS · 速率限制 · 请求 ID 注入                       │
└──────────────────────┬──────────────────────────────────┘
                       │
┌──────────────────────▼──────────────────────────────────┐
│                   应用层 (Application)                   │
│  ┌─────────────┐  ┌──────────────┐  ┌────────────────┐ │
│  │ 认证系统     │  │ RAG 引擎     │  │ 资源管理系统   │ │
│  │ JWT · bcrypt │  │ 检索·生成    │  │ CRUD · 搜索    │ │
│  ├─────────────┤  ├──────────────┤  ├────────────────┤ │
│  │ 后台管理     │  │ 文档处理     │  │ 监控系统       │ │
│  │ 仪表板·审计  │  │ 解析·分块    │  │ 指标·日志      │ │
│  └─────────────┘  └──────────────┘  └────────────────┘ │
│                   FastAPI + Uvicorn                      │
└──────────────────────┬──────────────────────────────────┘
                       │
┌──────────────────────▼──────────────────────────────────┐
│                    数据层 (Data)                         │
│  ┌──────────────┐  ┌──────────────┐  ┌────────────────┐ │
│  │ PostgreSQL   │  │ pgvector     │  │ 文件存储       │ │
│  │ 关系数据      │  │ 向量数据      │  │ 上传文件       │ │
│  └──────────────┘  └──────────────┘  └────────────────┘ │
└─────────────────────────────────────────────────────────┘
```

### 技术栈

| 层级 | 技术 | 用途 |
|------|------|------|
| **后端框架** | FastAPI + Uvicorn | 高性能异步 Web 框架 |
| **ORM** | SQLAlchemy 2.0 | 数据库 ORM |
| **数据库** | PostgreSQL 14+ + pgvector | 关系数据 + 向量存储 |
| **AI 模型** | DeepSeek API + 豆包 Embedding | 大语言模型 + 向量嵌入 |
| **文档处理** | PyPDF2 · python-docx · openpyxl · python-pptx | 多格式文档解析 |
| **认证** | JWT · bcrypt · HTTPBearer | 用户认证与安全 |
| **前端** | React 19 + TypeScript + Vite 7 | 现代化前端框架 |
| **路由** | React Router DOM 7 | 前端路由管理 |
| **UI 动画** | Framer Motion + Lucide React | 动画与图标 |
| **部署** | Docker + Nginx + Supervisord | 单容器部署 |
| **监控** | Sentry + Prometheus | 错误追踪 + 指标收集 |

### 数据流：RAG 问答流程

```
用户提问
    │
    ▼
┌──────────────┐
│  查询理解      │  ← 意图识别、关键词提取
└──────┬───────┘
       │
       ▼
┌──────────────┐
│  向量检索      │  ← 文本 → 向量 → pgvector 相似度搜索
└──────┬───────┘
       │
       ▼
┌──────────────┐
│  上下文融合    │  ← 检索结果 + 原始问题 = Prompt
└──────┬───────┘
       │
       ▼
┌──────────────┐
│  LLM 生成     │  ← DeepSeek API → 流式输出
└──────┬───────┘
       │
       ▼
   返回结果（SSE 流式）
```

---

## 快速开始

### 环境要求

- Python 3.11+
- Node.js 18+
- PostgreSQL 14+（含 pgvector 扩展）
- Docker 20.10+（可选，用于容器化部署）

### 1. 克隆项目

```bash
git clone <repository-url>
cd weplus-12.0
```

### 2. 后端设置

```bash
cd backend

# 创建并激活虚拟环境
python -m venv venv
# Windows
venv\Scripts\activate
# Linux/macOS
# source venv/bin/activate

# 安装依赖
pip install -r requirements.txt

# 配置环境变量
cp .env.example .env
# ⚠️ 编辑 .env 文件，填入你的数据库连接和 API 密钥

# 初始化数据库
python init_db.py

# 启动开发服务器（热重载）
uvicorn main:app --reload --host 0.0.0.0 --port 8000
```

### 3. 前端设置

```bash
cd frontend2

# 安装依赖
npm install

# 启动开发服务器
npm run dev
```

### 4. 访问应用

| 服务 | 地址 |
|------|------|
| 前端页面 | http://localhost:5173 |
| 后端 API | http://localhost:8000 |
| API 文档 (Swagger) | http://localhost:8000/docs |
| API 文档 (ReDoc) | http://localhost:8000/redoc |

---

## 部署指南

### 🐳 Docker 部署（推荐）

```bash
# 使用 Docker Compose（推荐用于生产）
docker-compose -f deploy/docker-compose.yml up -d

# 或构建单容器镜像
docker build -t weplus:latest .
docker run -p 80:80 \
  -e DATABASE_URL=postgresql://user:pass@host/db \
  -e SECRET_KEY=your-secret-key \
  weplus:latest
```

### ☁️ Railway 部署

一键部署到 Railway，自动构建和发布。

**必需环境变量：**

| 变量 | 说明 |
|------|------|
| `DATABASE_URL` | PostgreSQL 连接字符串 |
| `SECRET_KEY` | JWT 签名密钥 |
| `ALLOWED_ORIGINS` | CORS 允许的源 |
| `OPENAI_API_KEY` | OpenAI / DeepSeek API 密钥 |

> 📖 完整部署方案见 [部署指南](docs/部署指南.md)

---

## 项目结构

```
weplus-12.0/
├── backend/                        # FastAPI 后端服务
│   ├── app/                       # 应用核心代码
│   │   ├── api/                  # API 路由层
│   │   │   ├── user_api.py          # 用户管理
│   │   │   ├── rag_routes.py        # RAG 聊天
│   │   │   ├── study_resources_api.py  # 学习资源
│   │   │   ├── document_routes.py   # 文档处理
│   │   │   ├── admin_*.py          # 后台管理
│   │   │   └── vector_database_api.py  # 向量数据库
│   │   ├── core/                 # 核心配置
│   │   ├── dependencies/         # 安全依赖
│   │   ├── middlewares/          # 中间件
│   │   ├── models/               # 数据模型
│   │   └── services/             # 业务服务层
│   ├── database/                 # 数据库配置与迁移
│   ├── scripts/                  # 运维脚本
│   ├── docs/                     # 后端文档
│   ├── requirements.txt          # Python 依赖
│   └── main.py                   # 应用入口
├── frontend2/                      # React 前端
│   ├── src/
│   │   ├── components/           # React 组件
│   │   │   ├── admin/           # 管理后台组件
│   │   │   ├── common/          # 通用组件
│   │   │   ├── RAGChat.tsx       # 智能聊天
│   │   │   ├── StudyResources.tsx # 学习资源
│   │   │   └── ...              # 其他组件
│   │   ├── contexts/            # React Context
│   │   ├── services/            # API 客户端
│   │   ├── types/               # TypeScript 类型
│   │   └── utils/               # 工具函数
│   ├── public/                   # 静态资源
│   ├── package.json              # 前端依赖
│   └── vite.config.ts            # Vite 配置
├── deploy/                        # 部署配置
│   ├── nginx.conf                # Nginx 配置
│   ├── docker-compose.yml        # Docker Compose
│   └── checks/                   # 部署检查脚本
├── docs/                          # 项目文档
│   ├── 项目架构设计文档.md
│   ├── 部署指南.md
│   ├── 数据库迁移与配置指南.md
│   ├── 开发过程记录_完整版.md
│   ├── 后台管理系统开发记录.md
│   └── 系统测试与问题分析报告.md
├── scripts/                       # 自动化脚本
├── Dockerfile                     # 单容器 Dockerfile
├── railway.json                   # Railway 配置
└── README.md                      # 本文件
```

---

## 文档

除了本 README，项目还提供了以下详细文档，存放在 `docs/` 目录下：

| 文档 | 说明 |
|------|------|
| [📐 项目架构设计文档](docs/项目架构设计文档.md) | 系统架构、设计决策、安全设计、性能优化 |
| [🚀 部署指南](docs/部署指南.md) | 本地开发、Docker 部署、Railway 部署、运维指南 |
| [🗄️ 数据库迁移与配置指南](docs/数据库迁移与配置指南.md) | SQLite→PostgreSQL、ChromaDB→pgvector、RDS 配置 |
| [📝 开发过程记录_完整版](docs/开发过程记录_完整版.md) | 完整开发历程、技术亮点、Changelog |
| [📊 后台管理系统开发记录](docs/后台管理系统开发记录.md) | 管理后台功能开发、技术实现 |
| [🧪 系统测试与问题分析报告](docs/系统测试与问题分析报告.md) | 测试报告、问题分析、架构评估 |

---

## API 文档

### 认证

| 方法 | 端点 | 说明 |
|------|------|------|
| POST | `/api/auth/register` | 用户注册（邮箱验证码） |
| POST | `/api/auth/login` | 用户登录（返回 JWT Token） |
| POST | `/api/auth/send-verification-code` | 发送邮箱验证码 |

### RAG 聊天

| 方法 | 端点 | 说明 |
|------|------|------|
| POST | `/api/rag/chat` | 发送聊天消息（SSE 流式） |
| POST | `/api/rag/documents/upload` | 上传文档 |
| GET | `/api/rag/documents` | 获取文档列表 |
| DELETE | `/api/rag/documents/{id}` | 删除文档 |
| GET | `/api/rag/health` | 系统健康检查 |

### 学习资源

| 方法 | 端点 | 说明 |
|------|------|------|
| GET | `/api/study-resources` | 资源列表（支持筛选） |
| POST | `/api/study-resources/upload` | 上传资源 |
| GET | `/api/study-resources/{id}/download` | 下载资源 |
| POST | `/api/study-resources/{id}/rate` | 评分 |
| POST | `/api/study-resources/{id}/comment` | 评论 |

### 后台管理

| 方法 | 端点 | 说明 |
|------|------|------|
| GET | `/api/admin/dashboard` | 系统仪表板 |
| GET | `/api/admin/users` | 用户列表 |
| GET | `/api/admin/logs` | 系统日志 |
| POST | `/api/admin/backup` | 创建备份 |

> 📋 完整 API 接口清单见 [WePlus_API接口清单.md](WePlus_API接口清单.md)

---

## 路线图

### 🎯 已完成

- [x] 用户注册 / 登录 / JWT 认证
- [x] RAG 引擎：文档上传、向量检索、LLM 生成
- [x] 学习资源 CRUD + 搜索 + 评分评论
- [x] 后台管理系统：仪表板、用户管理、日志
- [x] PostgreSQL + pgvector 数据库迁移
- [x] Docker 单容器部署 + Railway 云部署
- [x] Sentry 错误追踪 + Prometheus 监控

### 🗺️ 规划中

- [ ] 移动端适配（响应式优化）
- [ ] OAuth 第三方登录（微信、GitHub）
- [ ] WebSocket 实时通知
- [ ] 多语言国际化（i18n）
- [ ] 知识库可视化图谱
- [ ] 批量文档导入与自动分类
- [ ] CI/CD 自动化流水线
- [ ] 单元测试覆盖率提升至 80%+

---

## 贡献指南

### 开发流程

1. **Fork** 本仓库
2. 创建功能分支：`git checkout -b feature/amazing-feature`
3. 提交更改：`git commit -m "feat: add amazing feature"`
4. 推送分支：`git push origin feature/amazing-feature`
5. 创建 **Pull Request**

### 提交规范

| 类型 | 说明 |
|------|------|
| `feat:` | 新功能 |
| `fix:` | 修复 Bug |
| `docs:` | 文档更新 |
| `style:` | 代码格式调整 |
| `refactor:` | 代码重构 |
| `test:` | 测试相关 |
| `chore:` | 构建/工具 |

### 数据库迁移

```bash
# 创建迁移
alembic revision --autogenerate -m "description"

# 应用迁移
alembic upgrade head

# 回滚
alembic downgrade -1
```

---

### 社区

| 渠道 | 说明 |
|------|------|
| 🐛 [Issues](https://github.com/your-username/weplus/issues) | 报告 Bug 或提出功能建议 |
| 💬 [Discussions](https://github.com/your-username/weplus/discussions) | 参与技术讨论 |
| 🔀 [Pull Requests](https://github.com/your-username/weplus/pulls) | 提交代码贡献 |

---

## 许可证

[MIT](LICENSE) © WePlus Contributors

---

<p align="center">
  <b>WePlus - 让校园更智能</b><br>
  <sub>Built with ❤️ for the campus community</sub>
  <br><br>
  <a href="#中文">⬆ 返回顶部</a>
</p>

---

# English

<p align="center">
  <a href="#introduction">Introduction</a> •
  <a href="#live-demo">Live Demo</a> •
  <a href="#whats-new">What's New</a> •
  <a href="#key-features">Key Features</a> •
  <a href="#architecture">Architecture</a> •
  <a href="#quick-start">Quick Start</a> •
  <a href="#deployment">Deployment</a> •
  <a href="#project-structure">Project Structure</a> •
  <a href="#documentation">Documentation</a> •
  <a href="#api-reference">API Reference</a> •
  <a href="#roadmap">Roadmap</a> •
  <a href="#contributing">Contributing</a>
</p>

---

## Introduction

**WePlus** is a full-stack campus smart assistant platform powered by **RAG (Retrieval-Augmented Generation)** technology. It integrates LLM capabilities with pgvector vector search to provide intelligent Q&A, document management, and learning resource sharing for campus users.

> 🎯 **Design Goal**: Build a production-ready full-stack web application showcasing modern web development best practices.

### Use Cases

| Scenario | Description |
|----------|-------------|
| 🎓 **Campus Q&A** | AI assistant powered by campus knowledge base |
| 📄 **Document Intelligence** | Upload PDF/Word/Excel for auto-parsing and semantic search |
| 📚 **Resource Sharing** | Upload, categorize, rate, and preview learning resources |
| 🔧 **Admin Console** | User management, system monitoring, audit logs, backup |

---

## Live Demo

<!--
  TODO: Replace with actual URLs after deployment.
  Example:
  - Frontend: https://weplus-demo.railway.app
  - API: https://weplus-demo.railway.app/api/healthz
-->

| Service | URL |
|---------|------|
| 🌐 Frontend | Available after deployment |
| 📡 API Health | Available after deployment |
| 📖 Swagger Docs | Available after deployment |

> 💡 You can also run the project locally by following the [Quick Start](#quick-start) guide.

### Screenshots

> The following pages are available when the project is running:

| Page | Description |
|------|-------------|
| 🤖 RAG Chat | Chat with AI based on uploaded documents |
| 📚 Study Resources | Browse, upload, and search learning materials |
| 👤 User Center | Register, login, and manage profile |
| 🛠️ Admin Panel | Dashboard, user management, audit logs |

---

## What's New

### 🚀 Recent Updates

| Date | Update |
|------|--------|
| 2026-Q1 | Migrated database from SQLite to PostgreSQL + pgvector |
| 2026-Q1 | Migrated vector store from ChromaDB + FAISS to pgvector |
| 2026-Q1 | Refactored Docker deployment to single-container (Nginx + Supervisord + Uvicorn) |
| 2026-Q1 | Added Railway cloud deployment support |
| 2026-Q1 | Restructured project documentation into organized docs |
| 2026-Q1 | Integrated Sentry error tracking and Prometheus monitoring |
| 2025-Q4 | Completed RAG engine core functionality |
| 2025-Q4 | Completed front-end/back-end separation architecture |

### ⭐ Stay Tuned

If you find this project helpful, feel free to Star it to receive notifications on future updates!

---

## Key Features

### 🤖 RAG-Powered Chat

- **Documents as Knowledge Base**: Upload PDF, Word, Excel, PPT to build your knowledge base
- **Semantic Search**: pgvector-based vector similarity search for accurate retrieval
- **Streaming Response**: Server-Sent Events for real-time typewriter effect
- **Multi-turn Dialogue**: Context-aware conversation with memory

### 📚 Learning Resource Management

- **Multi-format Support**: Documents, images, videos
- **Tag & Category**: Flexible classification system
- **Community Features**: Rating, comments, favorites
- **Online Preview**: View documents without downloading

### 👥 User System

- **JWT Authentication**: Token-based auth with auto-refresh
- **Email Verification**: Prevent bot registrations
- **Role-based Access**: User / Admin two-tier permissions
- **Security**: bcrypt hashing, rate limiting, IP whitelist

### 🛠️ Admin Dashboard

- **System Overview**: Real-time statistics and charts
- **User Management**: CRUD, status management, permissions
- **Document Management**: Upload records, storage stats
- **Vector Database**: Index rebuild, cleanup optimization
- **Audit Logs**: Operation audit, log query and export
- **Backup & Restore**: One-click backup and recovery

### 🔧 Testing & Monitoring

- **Health Check**: `/api/healthz` endpoint for component status
- **API Testing**: Comprehensive endpoint test suite
- **Performance**: Prometheus metrics collection
- **Error Tracking**: Sentry integration
- **Structured Logging**: JSON format for log analysis

---

## Architecture

### Overview

```
┌─────────────────────────────────────────────────────────┐
│                    User Layer                            │
│         Web Browser · Mobile · API Clients              │
└──────────────────────┬──────────────────────────────────┘
                       │ HTTPS
┌──────────────────────▼──────────────────────────────────┐
│                   Gateway Layer                          │
│    Nginx (Reverse Proxy · Static Files · SSL)            │
│    CORS · Rate Limiting · Request ID                     │
└──────────────────────┬──────────────────────────────────┘
                       │
┌──────────────────────▼──────────────────────────────────┐
│                Application Layer                         │
│  ┌─────────────┐  ┌──────────────┐  ┌────────────────┐ │
│  │ Auth        │  │ RAG Engine   │  │ Resource Mgmt  │ │
│  │ JWT·bcrypt  │  │ Retrieve·Gen │  │ CRUD·Search    │ │
│  ├─────────────┤  ├──────────────┤  ├────────────────┤ │
│  │ Admin       │  │ Doc Processor│  │ Monitoring     │ │
│  │ Dashboard   │  │ Parse·Chunk  │  │ Metrics·Logs   │ │
│  └─────────────┘  └──────────────┘  └────────────────┘ │
│                   FastAPI + Uvicorn                      │
└──────────────────────┬──────────────────────────────────┘
                       │
┌──────────────────────▼──────────────────────────────────┐
│                    Data Layer                            │
│  ┌──────────────┐  ┌──────────────┐  ┌────────────────┐ │
│  │ PostgreSQL   │  │ pgvector     │  │ File Storage   │ │
│  │ Relational   │  │ Vector Data  │  │ Uploads        │ │
│  └──────────────┘  └──────────────┘  └────────────────┘ │
└─────────────────────────────────────────────────────────┘
```

### Tech Stack

| Layer | Technology | Purpose |
|-------|-----------|---------|
| **Backend** | FastAPI + Uvicorn | High-performance async web framework |
| **ORM** | SQLAlchemy 2.0 | Database ORM |
| **Database** | PostgreSQL 14+ + pgvector | Relational + Vector storage |
| **AI** | DeepSeek API + Doubao Embedding | LLM + Embeddings |
| **Documents** | PyPDF2 · python-docx · openpyxl · python-pptx | Multi-format parsing |
| **Auth** | JWT · bcrypt · HTTPBearer | Authentication & security |
| **Frontend** | React 19 + TypeScript + Vite 7 | Modern frontend |
| **Routing** | React Router DOM 7 | Client-side routing |
| **UI** | Framer Motion + Lucide React | Animations & icons |
| **Deploy** | Docker + Nginx + Supervisord | Single-container deploy |
| **Monitoring** | Sentry + Prometheus | Error tracking + metrics |

### RAG Query Flow

```
User Question
    │
    ▼
┌──────────────┐
│ Query        │ ← Intent recognition, keyword extraction
│ Understanding│
└──────┬───────┘
       │
       ▼
┌──────────────┐
│ Vector       │ ← Text → Embedding → pgvector similarity search
│ Retrieval    │
└──────┬───────┘
       │
       ▼
┌──────────────┐
│ Context      │ ← Retrieved chunks + Question = Prompt
│ Fusion       │
└──────┬───────┘
       │
       ▼
┌──────────────┐
│ LLM          │ ← DeepSeek API → Streaming output
│ Generation   │
└──────┬───────┘
       │
       ▼
   Response (SSE Stream)
```

---

## Quick Start

### Prerequisites

- Python 3.11+
- Node.js 18+
- PostgreSQL 14+ (with pgvector extension)
- Docker 20.10+ (optional)

### 1. Clone

```bash
git clone <repository-url>
cd weplus-12.0
```

### 2. Backend Setup

```bash
cd backend

# Create virtual environment
python -m venv venv
# Windows
venv\Scripts\activate
# Linux/macOS
# source venv/bin/activate

# Install dependencies
pip install -r requirements.txt

# Configure environment
cp .env.example .env
# ⚠️ Edit .env with your database URL and API keys

# Initialize database
python init_db.py

# Start dev server
uvicorn main:app --reload --host 0.0.0.0 --port 8000
```

### 3. Frontend Setup

```bash
cd frontend2

npm install

npm run dev
```

### 4. Access

| Service | URL |
|---------|-----|
| Frontend | http://localhost:5173 |
| Backend API | http://localhost:8000 |
| API Docs (Swagger) | http://localhost:8000/docs |
| API Docs (ReDoc) | http://localhost:8000/redoc |

---

## Deployment

### 🐳 Docker (Recommended)

```bash
# Docker Compose for production
docker-compose -f deploy/docker-compose.yml up -d

# Or build single-container image
docker build -t weplus:latest .
docker run -p 80:80 \
  -e DATABASE_URL=postgresql://user:pass@host/db \
  -e SECRET_KEY=your-secret-key \
  weplus:latest
```

### ☁️ Railway

One-click deploy to Railway with auto-build.

**Required Environment Variables:**

| Variable | Description |
|----------|-------------|
| `DATABASE_URL` | PostgreSQL connection string |
| `SECRET_KEY` | JWT signing key |
| `ALLOWED_ORIGINS` | CORS allowed origins |
| `OPENAI_API_KEY` | OpenAI / DeepSeek API key |

> 📖 See [Deployment Guide](docs/部署指南.md) for details.

---

## Project Structure

```
weplus-12.0/
├── backend/                        # FastAPI backend
│   ├── app/                       # Application core
│   │   ├── api/                  # API routes
│   │   ├── core/                 # Configuration
│   │   ├── dependencies/         # Security deps
│   │   ├── middlewares/          # Middleware
│   │   ├── models/               # Data models
│   │   └── services/             # Business logic
│   ├── database/                 # DB config & migrations
│   ├── scripts/                  # Utility scripts
│   ├── requirements.txt          # Python deps
│   └── main.py                   # Entry point
├── frontend2/                      # React frontend
│   ├── src/
│   │   ├── components/           # React components
│   │   ├── contexts/             # React Context
│   │   ├── services/             # API clients
│   │   ├── types/                # TypeScript types
│   │   └── utils/                # Utilities
│   ├── public/                   # Static assets
│   └── package.json              # Frontend deps
├── deploy/                        # Deployment configs
├── docs/                          # Documentation
├── Dockerfile                     # Docker build
├── railway.json                   # Railway config
└── README.md                      # This file
```

---

## Documentation

In addition to this README, the project provides detailed documentation in the `docs/` directory:

| Document | Description |
|----------|-------------|
| [📐 Architecture Design](docs/项目架构设计文档.md) | System architecture, design decisions, security |
| [🚀 Deployment Guide](docs/部署指南.md) | Local dev, Docker, Railway, operations |
| [🗄️ Database Migration Guide](docs/数据库迁移与配置指南.md) | SQLite→PostgreSQL, ChromaDB→pgvector, RDS |
| [📝 Development Log](docs/开发过程记录_完整版.md) | Complete development history, changelog |
| [📊 Admin System Dev Log](docs/后台管理系统开发记录.md) | Admin panel features and implementation |
| [🧪 Testing & Analysis Report](docs/系统测试与问题分析报告.md) | Test reports, issue analysis, architecture review |

---

## API Reference

### Authentication

| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/api/auth/register` | Register with email verification |
| POST | `/api/auth/login` | Login, returns JWT |
| POST | `/api/auth/send-verification-code` | Send email code |

### RAG Chat

| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/api/rag/chat` | Chat message (SSE stream) |
| POST | `/api/rag/documents/upload` | Upload document |
| GET | `/api/rag/documents` | List documents |
| DELETE | `/api/rag/documents/{id}` | Delete document |
| GET | `/api/rag/health` | Health check |

### Study Resources

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/api/study-resources` | List resources |
| POST | `/api/study-resources/upload` | Upload resource |
| GET | `/api/study-resources/{id}/download` | Download |
| POST | `/api/study-resources/{id}/rate` | Rate resource |
| POST | `/api/study-resources/{id}/comment` | Add comment |

### Admin

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/api/admin/dashboard` | Dashboard stats |
| GET | `/api/admin/users` | User list |
| GET | `/api/admin/logs` | System logs |
| POST | `/api/admin/backup` | Create backup |

> 📋 See [WePlus_API接口清单.md](WePlus_API接口清单.md) for the complete API reference.

---

## Roadmap

### 🎯 Completed

- [x] User registration / login / JWT authentication
- [x] RAG engine: document upload, vector retrieval, LLM generation
- [x] Study resources CRUD + search + rating & comments
- [x] Admin dashboard: overview, user management, logs
- [x] PostgreSQL + pgvector database migration
- [x] Docker single-container + Railway cloud deployment
- [x] Sentry error tracking + Prometheus monitoring

### 🗺️ Planned

- [ ] Mobile responsive optimization
- [ ] OAuth third-party login (WeChat, GitHub)
- [ ] WebSocket real-time notifications
- [ ] Internationalization (i18n)
- [ ] Knowledge base visualization graph
- [ ] Batch document import & auto-classification
- [ ] CI/CD automated pipeline
- [ ] Unit test coverage > 80%

---

## Contributing

### Workflow

1. **Fork** the repository
2. Create feature branch: `git checkout -b feature/amazing-feature`
3. Commit: `git commit -m "feat: add amazing feature"`
4. Push: `git push origin feature/amazing-feature`
5. Open a **Pull Request**

### Commit Convention

| Type | Description |
|------|-------------|
| `feat:` | New feature |
| `fix:` | Bug fix |
| `docs:` | Documentation |
| `style:` | Code style |
| `refactor:` | Refactoring |
| `test:` | Testing |
| `chore:` | Build/tooling |

---

### Community

| Channel | Description |
|---------|-------------|
| 🐛 [Issues](https://github.com/your-username/weplus/issues) | Report bugs or suggest features |
| 💬 [Discussions](https://github.com/your-username/weplus/discussions) | Join technical discussions |
| 🔀 [Pull Requests](https://github.com/your-username/weplus/pulls) | Submit code contributions |

---

## License

[MIT](LICENSE) © WePlus Contributors

---

<p align="center">
  <b>WePlus - Making Campus Smarter</b><br>
  <sub>Built with ❤️ for the campus community</sub>
  <br><br>
  <a href="#english">⬆ Back to Top</a>
</p>
