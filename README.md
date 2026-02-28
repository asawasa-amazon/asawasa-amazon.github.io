# 亚马逊商店宣传网站

这是一个多页面响应式静态网站，用于宣传您的亚马逊商店。网站使用纯 HTML5、Tailwind CSS（CDN）和原生 JavaScript 构建，无需任何构建工具，可以直接在浏览器中打开预览。

## 📁 项目结构

```
amazon_website/
├── index.html          # 主页
├── products.html       # 产品列表页
├── about.html          # 关于我们页面
├── images/             # 图片文件夹
│   └── README.txt      # 图片说明文件
└── README.md           # 项目说明文档（本文件）
```

## 🚀 快速开始

### 本地预览

1. 直接在文件管理器中找到 `index.html` 文件
2. 双击文件，它会在您的默认浏览器中打开
3. 或者右键点击文件，选择"打开方式" → 选择浏览器

### 在线部署

#### 方法一：GitHub Pages（推荐）

1. **创建 GitHub 仓库**
   - 登录 GitHub
   - 点击右上角 "+" → "New repository"
   - 输入仓库名称
   - 选择 Public（GitHub Pages 免费版需要公开仓库）
   - 点击 "Create repository"

2. **上传文件到 GitHub**
   ```bash
   # 在项目目录下执行
   git init
   git add .
   git commit -m "Initial commit"
   git branch -M main
   git remote add origin https://github.com/asawasa-amazon/asawasa-amazon.github.io.git
   git push -u origin main
   ```

3. **启用 GitHub Pages**
   - 进入仓库页面
   - 点击 "Settings" → 左侧菜单找到 "Pages"
   - 在 "Source" 下拉菜单中选择 "main" 分支
   - 点击 "Save"
   - 等待几分钟，您的网站将在 `https://asawasa-amazon.github.io/asawasa-amazon/` 上线

#### 方法二：Netlify

1. 访问 [Netlify](https://www.netlify.com/)
2. 注册/登录账号
3. 点击 "Add new site" → "Deploy manually"
4. 将整个项目文件夹拖拽到上传区域
5. 网站会自动部署并提供一个免费域名

#### 方法三：Vercel

1. 访问 [Vercel](https://vercel.com/)
2. 注册/登录账号
3. 点击 "Add New Project"
4. 导入您的 GitHub 仓库或直接上传文件夹
5. 点击 "Deploy"

## ✏️ 如何修改内容

### 1. 修改亚马逊商店链接

在所有 HTML 文件中搜索 `YOUR_STORE_ID`，替换为您的实际亚马逊商店 ID。

**查找位置：**
- `index.html`: Hero Section 的 "立即购买" 按钮
- `products.html`: CTA Section 的 "前往亚马逊商店" 按钮
- `about.html`: 联系信息中的亚马逊商店链接和 CTA Section

**示例：**
```html
<!-- 替换前 -->
<a href="https://www.amazon.com/s?me=YOUR_STORE_ID" target="_blank">

<!-- 替换后（假设您的商店 ID 是 A1B2C3D4E5F6G7） -->
<a href="https://www.amazon.com/s?me=A1B2C3D4E5F6G7" target="_blank">
```

### 2. 修改产品链接

在所有 HTML 文件中搜索 `PRODUCT_ASIN_X`，替换为产品的实际 ASIN 码。

**查找位置：**
- `index.html`: Featured Products 部分的 3 个产品
- `products.html`: Product Grid 部分的 8 个产品

**示例：**
```html
<!-- 替换前 -->
<a href="https://www.amazon.com/dp/PRODUCT_ASIN_1" target="_blank">

<!-- 替换后（假设产品 ASIN 是 B08XYZ1234） -->
<a href="https://www.amazon.com/dp/B08XYZ1234" target="_blank">
```

### 3. 添加产品图片

1. 将产品图片放入 `images/` 文件夹
2. 在 HTML 文件中找到图片占位符
3. 替换为实际图片路径

**示例：**
```html
<!-- 替换前 -->
<div class="bg-gray-200 h-64 flex items-center justify-center">
    <span class="text-gray-400">产品图片 1</span>
</div>

<!-- 替换后 -->
<img src="images/product1.jpg" alt="产品名称 1" class="w-full h-64 object-cover">
```

### 4. 修改品牌 Logo

在三个 HTML 文件的 Header 部分，找到 Logo 区域：

```html
<!-- 当前是文字 Logo -->
<a href="index.html" class="text-2xl font-bold text-gray-800">
    <span class="text-blue-600">My</span>Store
</a>

<!-- 替换为图片 Logo -->
<a href="index.html">
    <img src="images/logo.png" alt="MyStore" class="h-10">
</a>
```

### 5. 修改 YouTube 视频

在 `products.html` 中找到视频嵌入部分：

```html
<!-- 替换前 -->
<iframe src="https://www.youtube.com/embed/YOUR_VIDEO_ID" ...>

<!-- 替换后（假设视频 ID 是 dQw4w9WgXcQ） -->
<iframe src="https://www.youtube.com/embed/dQw4w9WgXcQ" ...>
```

**如何获取 YouTube 视频 ID：**
- 视频链接：`https://www.youtube.com/watch?v=dQw4w9WgXcQ`
- 视频 ID 就是 `v=` 后面的部分：`dQw4w9WgXcQ`

### 6. 修改品牌故事和联系方式

在 `about.html` 中找到以下部分并修改：
- **品牌故事文本**：搜索 "我们的故事" 部分
- **联系邮箱**：搜索 `contact@yourstore.com`
- **社交媒体链接**：搜索社交媒体部分，替换 `#` 为实际链接

### 7. 修改网站标题和元信息

在每个 HTML 文件的 `<head>` 部分：

```html
<title>我的亚马逊商店 - 主页</title>
```

修改为您想要的标题。

## 🎨 自定义样式

### 修改主题颜色

网站使用蓝色和紫色作为主色调。要修改颜色，搜索以下 Tailwind CSS 类：

- `blue-600` → 主蓝色
- `purple-600` → 主紫色
- `blue-100` → 浅蓝色（用于文本）

**示例：** 如果想改为绿色主题，将 `blue-600` 替换为 `green-600`。

### 修改字体大小

Tailwind CSS 使用响应式字体大小：
- `text-4xl` → 手机端
- `md:text-6xl` → 平板端
- `lg:text-7xl` → 桌面端

可以根据需要调整这些数值。

## 📱 响应式设计

网站已经针对以下设备进行了优化：
- **手机**：320px - 640px
- **平板**：641px - 1024px（使用 `md:` 前缀）
- **桌面**：1025px+（使用 `lg:` 前缀）

所有布局都会自动适配不同屏幕尺寸。

## 🔍 常见问题

### Q: 为什么我的图片不显示？
A: 请确保：
1. 图片文件已放入 `images/` 文件夹
2. 图片路径正确（例如：`images/product1.jpg`）
3. 图片文件名大小写匹配（某些服务器区分大小写）

### Q: 如何添加更多产品？
A: 在 `products.html` 中复制一个产品卡片，修改内容即可。确保保持网格布局（`grid-cols-1 sm:grid-cols-2 lg:grid-cols-4`）。

### Q: 可以添加更多页面吗？
A: 当然可以！创建新的 HTML 文件，复制 Header 和 Footer 部分，然后添加您的内容。记得在导航菜单中添加链接。

### Q: 如何修改汉堡菜单图标？
A: 汉堡菜单使用 SVG 图标，位于每个页面的 Header 部分。可以替换为其他 SVG 图标或使用图片。

## 📝 技术栈

- **HTML5**: 页面结构
- **Tailwind CSS**: 样式框架（通过 CDN 引入）
- **原生 JavaScript**: 移动端菜单交互

## 📄 许可证

本项目为个人使用项目，可根据需要自由修改和使用。

## 🆘 需要帮助？

如果您在使用过程中遇到问题，可以：
1. 检查浏览器控制台是否有错误信息（按 F12 打开开发者工具）
2. 确保所有文件路径正确
3. 确保网络连接正常（Tailwind CSS 通过 CDN 加载）

---

**祝您的亚马逊商店生意兴隆！** 🎉
