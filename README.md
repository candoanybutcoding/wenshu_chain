# 文枢链（Wenshu Chain）

文枢链是一个 AI 语义驱动的文档设计云平台，融合前端可视化与后端大模型能力，提供从数据洞察到内容生成、再到 IP 活化与知识管理的一站式体验。项目由 Vue3 前端与基于 Node.js/Express 的后端组成。

## 产品特色
- **多引擎协同**：集成“洞察引擎”“IP 生成引擎”“IP 活化引擎”和“知识库”等核心模块，支持在顶部导航中自由切换。
- **可视化工作流**：借助 `@vue-flow` 等库实现拖拽式节点编辑与流程调度，直观管理各类 Agent 工作流。
- **智能体体系**：后端维护可扩展的 Agent 工作流，针对文本生成、图像生成、图像理解等不同场景自动调用对应的大模型接口。
- **账户与订阅**：支持用户注册/登录、套餐订阅、单个 Agent 购买以及基于 JWT 的权限控制。
- **现代化技术栈**：前端使用 Vue3、Element Plus、Ant Design Vue 等组件库；后端采用 Express + MySQL，并通过 `.env` 管理环境变量。

## 项目结构
```
wenshu_chain/
├── public/                # 前端静态文件
├── src/                   # 前端源码
│   ├── assets/            # 静态资源
│   ├── components/        # 基础组件
│   ├── views/             # 登录、洞察引擎、IP 引擎、知识库等页面
│   └── router/            # 路由配置
├── server/                # 后端服务（Express + MySQL）
│   ├── routes/            # REST API 路由
│   ├── services/          # 业务逻辑与 Agent 调度
│   └── middlewares/       # JWT 等中间件
├── package.json           # 前端依赖与脚本
└── README.md
```

## 本地开发与运行
### 前端
```bash
npm install        # 安装依赖
npm run serve      # 本地调试，默认 http://localhost:8080
npm run build      # 构建生产版本
npm run lint       # 代码风格检查
```

### 后端
```bash
cd server
npm install
cp .env.example .env   # 配置数据库、LLM_API_KEY 等环境变量
npm start              # 启动服务，默认端口 3000
```

## 使用介绍
1. 访问前端登录页，注册或登录账户。
2. 进入主界面后，通过顶部导航在“洞察引擎”“IP 生成引擎”“IP 活化引擎”和“知识库”之间切换。
3. 在各引擎中创建或运行 Agent 以获取文本或图像内容，可订阅套餐或单独购买 Agent 以解锁全部功能。
4. 所有流程与结果都会以可视化节点呈现，便于管理和再次编辑。

欢迎提交 Issue 或 PR 一同改进文枢链。
