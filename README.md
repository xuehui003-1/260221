# 增值税测试题 - 部署到 Vercel 指南

## 📋 项目简介
这是一个增值税计算与缴纳的互动测试网页，包含选择题、判断题、简答题、计算题和会计分录题。

---

## ⚠️ Vercel 部署常见问题解决

### 问题：构建完成后未找到名为"public"的输出目录

**解决方法：** 项目已配置好 `public` 目录和 `vercel.json`，直接使用即可！

---

## 🚀 部署到 Vercel 的方法

### 方法一：通过 GitHub 仓库部署（推荐）

#### 步骤 1：准备项目文件
确保您的目录包含以下文件：
```
20260221/
├── public/
│   └── index.html          # 主网页文件
├── vercel.json              # Vercel 配置文件
├── package.json             # 项目配置
├── .gitignore              # Git 忽略配置
└── README.md               # 本说明文件
```

#### 步骤 2：创建 GitHub 仓库
1. 访问 https://github.com 并登录
2. 点击 "New repository" 创建新仓库
3. 仓库名称可以是：`vat-exam` 或其他您喜欢的名称
4. 选择 "Public" 或 "Private"
5. 点击 "Create repository"

#### 步骤 3：上传文件到 GitHub
1. 在仓库页面点击 "uploading an existing file"
2. 将以下文件和文件夹全部拖拽上传：
   - `public/` 文件夹（包含里面的 index.html）
   - `vercel.json`
   - `package.json`
   - `README.md`
   - `.gitignore`
3. 填写提交信息，点击 "Commit changes"

#### 步骤 4：连接到 Vercel
1. 访问 https://vercel.com 并使用 GitHub 账号登录
2. 点击 "Add New" → "Project"
3. 选择刚才创建的 GitHub 仓库
4. 点击 "Import"
5. **重要**：在配置页面确认以下设置（通常保持默认即可）：
   - Framework Preset: `Other`
   - Root Directory: `./`
   - Output Directory: 留空或自动识别
   - Install Command: 留空
   - Build Command: 留空
6. 点击 "Deploy"
7. 等待部署完成（通常需要1-2分钟）

#### 步骤 5：访问您的网站
部署完成后，Vercel 会提供一个类似 `https://your-project-name.vercel.app` 的链接，您就可以访问了！

---

### 方法二：使用 Vercel CLI（需要 Node.js）

如果您已经安装了 Node.js 和 npm，可以使用以下命令：

#### 1. 安装 Vercel CLI
```bash
npm install -g vercel
```

#### 2. 登录 Vercel
```bash
vercel login
```

#### 3. 部署项目
在项目目录下运行：
```bash
vercel
```

按照提示完成部署即可。

---

## 📂 文件说明

- **public/index.html** - 增值税测试题的主网页，包含完整的互动功能
- **vercel.json** - Vercel 部署配置文件（解决输出目录问题）
- **package.json** - 项目配置文件
- **.gitignore** - Git 忽略文件配置
- **README.md** - 本部署指南
- **index.html** - 根目录下的备份文件
- **增值税测试题.html** - 原始文件名的备份

## ✨ 网页功能

- ⏰ 120分钟倒计时
- 📝 五种题型：单选、判断、简答、计算、会计分录
- ✅ 客观题自动评分
- 📖 每道题都有详细答案解析
- 📱 响应式设计，支持手机和电脑

## 🎯 本地预览

在部署之前，您可以先在本地预览：
1. 双击 `public/index.html` 文件
2. 或在浏览器中打开该文件

## 📞 帮助

如果在部署过程中遇到问题，请访问：
- Vercel 文档：https://vercel.com/docs
- GitHub 帮助：https://docs.github.com

---

## 📌 已解决的问题

✅ **已配置**：项目包含 `public` 目录和 `vercel.json`，不会再出现"未找到 public 输出目录"的错误！
