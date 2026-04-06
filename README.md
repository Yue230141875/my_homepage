# 个人主页 - Personal Homepage

一个简洁、美观、响应式的个人主页模板，专为计算机/AI专业学生设计。

## 功能特性

- 左侧固定侧边栏 + 右侧内容区域布局
- 5个导航标签：基本信息、关于我、项目经历、技能栈、联系方式
- 平滑的标签切换动画
- 完善的移动端适配（手机、平板、桌面三端响应）
- 汉堡菜单式侧边栏（移动端）
- 纯前端实现，无需后端

## 技术栈

- HTML5
- CSS3（自定义CSS + Tailwind CSS CDN）
- 原生JavaScript
- Google Fonts（Noto Sans SC + Roboto）

## 文件结构

```
Personal_Homepage/
├── index.html      # 主页面HTML结构
├── style.css       # 自定义样式文件
├── main.js         # 交互逻辑脚本
└── README.md       # 项目说明文档
```

## 快速开始

### 本地预览

1. 克隆或下载本项目
2. 直接用浏览器打开 `index.html`

或使用本地服务器：

```bash
# Python 3
python -m http.server 8000

# Node.js
npx serve .
```

访问 `http://localhost:8000` 查看效果。

## 修改内容指南

### 1. 基本信息

编辑 `index.html` 中 `section#basic` 部分：

```html
<span class="info-value">[Your Name]</span>  <!-- 姓名 -->
<span class="info-value">[你的学校名称]</span>  <!-- 学校 -->
<span class="badge badge-secondary">[考研备考中/求职中]</span>  <!-- 身份 -->
<span class="info-value italic">"[你的座右铭]"</span>  <!-- 座右铭 -->
```

### 2. 关于我

编辑 `section#about` 部分，修改：
- 教育经历（学校、入学年份、GPA）
- 学习方向（AI方向如深度学习、计算机视觉等）
- 求职/考研目标
- 个人特点和兴趣爱好

### 3. 项目经历

在 `section#projects` 中，每个项目卡片包含：

```html
<h3 class="card-title">[项目名称 - 项目类型]</h3>
<a href="#" class="link">GitHub ↗</a>  <!-- GitHub链接 -->
<span class="tag tag-success">[技术栈]</span>  <!-- 技术标签 -->
<p class="card-text">[项目简介]</p>  <!-- 项目描述 -->
```

### 4. 技能栈

在 `section#skills` 中，按类别添加技能标签：

```html
<span class="tag tag-primary">Python</span>      <!-- 主色标签 -->
<span class="tag tag-warning">C/C++</span>       <!-- 警告色标签 -->
<span class="tag tag-success">Git</span>         <!-- 成功色标签 -->
<span class="tag tag-neutral">[其他]</span>       <!-- 中性色标签 -->
```

可用标签颜色：`tag-primary`、`tag-success`、`tag-warning`、`tag-danger`、`tag-orange`、`tag-purple`、`tag-cyan`、`tag-neutral`

### 5. 联系方式

在 `section#contact` 中更新联系方式：

```html
<a href="mailto:your.email@example.com" class="link">your.email@example.com</a>
<a href="https://github.com/your-username" class="link">github.com/your-username</a>
```

### 6. 自定义样式

修改 `style.css` 中的CSS变量来自定义主题色：

```css
:root {
    --primary: #2563eb;        /* 主色（蓝色） */
    --primary-dark: #1d4ed8;   /* 主色深色 */
    --secondary: #10b981;      /* 辅助色（绿色） */
    --bg-page: #f8fafc;        /* 页面背景色 */
    /* ... */
}
```

## 部署到GitHub Pages

### 方法一：使用 GitHub 网页界面

1. 在GitHub创建新仓库 `your-username.github.io`
2. 点击 `Add file` → `Upload files`
3. 上传 `index.html`、`style.css`、`main.js` 三个文件
4. 等待几分钟后访问 `https://your-username.github.io`

### 方法二：使用 Git 命令行

```bash
# 1. 初始化Git仓库
git init

# 2. 添加文件
git add index.html style.css main.js README.md

# 3. 提交
git commit -m "Initial commit"

# 4. 添加远程仓库（替换为你的仓库地址）
git remote add origin https://github.com/your-username/your-repo.git

# 5. 推送到GitHub
git push -u origin main

# 6. 在GitHub仓库 Settings → Pages → Source 选择 main branch
```

### 方法三：部署到子路径

如果想部署到 `https://your-username.github.io/profile/`：

1. 将仓库名改为 `profile`
2. 在 `index.html` 的 `<head>` 中添加：
```html
<base href="/profile/">
```
3. 在GitHub Settings → Pages → Source 选择 main branch

## 浏览器兼容性

- Chrome (最新版)
- Firefox (最新版)
- Safari (最新版)
- Edge (最新版)

## 许可证

MIT License - 可自由使用、修改和分发。

## 致谢

- [Tailwind CSS](https://tailwindcss.com/) - CSS框架
- [Google Fonts](https://fonts.google.com/) - 思源黑体 + Roboto字体
- [Unsplash](https://unsplash.com/) - 免费图片资源（可选）