# 📚 在线考试系统 (Online Exam System)

一个为小学到高中学生设计的**完整在线考试平台**，支持题库管理、按时间组织考试、自动评分等功能。

## ✨ 核心功能

- 📖 **题库管理** - 按学段/学科/年份组织考试资料
- 📝 **在线考试** - 支持选择题、填空题、简答题等多种题型
- ⏱️ **考试管理** - 按时间发布和管理考试
- 📊 **自动评分** - 支持客观题自动评分，主观题辅助评分
- 📈 **成绩统计** - 学生成绩查看、错题分析
- 👥 **多角色** - 学生、教师、管理员权限管理

## 🗂️ 项目结构

```
exam-system/
├── frontend/              # 前端应用 (Vue 3)
│   ├── src/
│   │   ├── components/
│   │   ├── views/
│   │   ├── stores/        # 状态管理
│   │   └── App.vue
│   └── package.json
│
├── backend/               # 后端API (Node.js/Express)
│   ├── src/
│   │   ├── routes/        # API路由
│   │   ├── controllers/   # 业务逻辑
│   │   ├── models/        # 数据模型
│   │   └── middleware/    # 中间件
│   ├── database/
│   │   └── init.sql       # 数据库初始化
│   └── package.json
│
├── question-bank/         # 题库资料
│   ├── 小学/
│   │   ├── 一年级/
│   │   │   ├── 语文/
│   │   │   └── 数学/
│   │   └── ...
│   ├── 初中/
│   └── 高中/
│
└── docs/                  # 文档
    ├── API-DOCS.md
    ├── DATABASE-SCHEMA.md
    └── INSTALL.md
```

## 🚀 快速开始

### 前置要求
- Node.js >= 14
- MySQL >= 5.7 或 SQLite
- npm 或 yarn

### 安装步骤

1. **克隆仓库**
```bash
git clone https://github.com/123456lichao/exam-system.git
cd exam-system
```

2. **后端设置**
```bash
cd backend
npm install
cp .env.example .env
npm run dev
```

3. **前端设置**
```bash
cd ../frontend
npm install
npm run dev
```

4. **访问应用**
- 前端：http://localhost:5173
- 后端API：http://localhost:3000

## 📚 题库组织规范

### 文件结构
```
question-bank/
└── 高中/
    └── 高一/
        ├── 语文/
        │   ├── 2024年期末考试.json
        │   └── 2024年期中考试.json
        └── 数学/
            └── 2024年高考模拟.json
```

### 题目JSON格式
```json
{
  "exam_id": "exam_001",
  "exam_name": "2024年高考数学模拟",
  "subject": "数学",
  "grade": "高三",
  "exam_date": "2024-06-01",
  "time_limit": 120,
  "total_score": 150,
  "questions": [
    {
      "id": "q001",
      "type": "single_choice",
      "question": "1+1=?",
      "options": ["1", "2", "3", "4"],
      "correct_answer": "2",
      "score": 5
    }
  ]
}
```

## 🔐 用户角色

| 角色 | 权限 |
|------|------|
| **学生** | 参加考试、查看成绩、分析错题 |
| **教师** | 创建考试、出题、批改、查看统计 |
| **管理员** | 用户管理、题库管理、系统配置 |

## 🛠️ 技术栈

### 前端
- Vue 3 + TypeScript
- Vite
- Pinia (状态管理)
- Tailwind CSS

### 后端
- Node.js + Express
- JWT 认证
- MySQL / SQLite
- Joi (数据验证)

## 📖 文档

- [API文档](./docs/API-DOCS.md)
- [数据库设计](./docs/DATABASE-SCHEMA.md)
- [安装指南](./docs/INSTALL.md)
- [贡献指南](./CONTRIBUTING.md)

## 📝 使用流程

### 学生流程
1. 注册/登录
2. 浏览可用考试列表
3. 参加考试
4. 查看成绩和错题分析

### 教师流程
1. 登录系统
2. 创建考试（选择或上传题目）
3. 设置考试时间和参加学生
4. 批改主观题
5. 查看成绩统计

## 🤝 贡献

欢迎提交 Issue 和 Pull Request！

## 📄 许可证

MIT License

---

**开始使用！** 📖 查看 [安装指南](./docs/INSTALL.md) 获取详细步骤。
