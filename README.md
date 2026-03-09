# 🦞 Qclaw Landing Template

> 现代化产品落地页模板 - 完整响应式设计（PC + 移动端）

**在线预览**: https://88901111hz-lang.github.io/qclaw-landing-template/

## ✨ 特性

- 🎨 **暗色主题** - 现代感十足的深色设计
- 💎 **玻璃拟态** - Glassmorphism 效果，质感拉满
- ✨ **粒子背景** - 动态粒子 + 网格背景 + 浮动光球
- 💬 **聊天气泡** - 模拟微信对话场景
- 🔄 **无限滚动** - 用户评价自动滚动
- 📱 **完整响应式** - PC / 平板 / 手机全覆盖
- ⚡ **零依赖** - 纯 HTML/CSS/JS，无需框架
- 🖱️ **系统光标** - 使用原生鼠标指针，体验自然

## 📁 目录结构

```
qclaw-landing-template/
├── index.html          # 主页面
├── css/
│   └── style.css       # 样式文件
├── js/
│   └── main.js         # 交互脚本
├── images/             # 图片资源
│   ├── logo.png        # Logo 图标
│   ├── logo-text.png   # 文字 Logo
│   ├── tencent-logo.png # 品牌图标
│   └── qrcode-beta.png  # 二维码
└── README.md           # 说明文档
```

## 🚀 快速开始

### 1. 克隆仓库

```bash
git clone https://github.com/88901111hz-lang/qclaw-landing-template.git
cd qclaw-landing-template
```

### 2. 添加图片

将以下图片放入 `images/` 文件夹：

| 文件名 | 说明 | 尺寸建议 |
|--------|------|----------|
| `logo.png` | Logo 图标 | 88x88px |
| `logo-text.png` | 文字 Logo | 高度 48-80px |
| `tencent-logo.png` | 品牌图标 | 20x20px |
| `qrcode-beta.png` | 二维码 | 160x160px |

### 3. 本地预览

直接用浏览器打开 `index.html`，或使用本地服务器：

```bash
# Python 3
python -m http.server 8080

# Node.js (需安装 http-server)
npx http-server -p 8080
```

然后访问 `http://localhost:8080`

## 🎨 自定义配置

### CSS 变量

在 `css/style.css` 中修改颜色变量：

```css
:root {
  /* 主色调 */
  --red-primary: #FF3B30;      /* 主色 */
  --red-glow: #FF6B5E;         /* 发光色 */
  --gold-accent: #FFD700;      /* 金色点缀 */
  
  /* 背景色 */
  --bg-dark: #0A0A0F;          /* 深黑背景 */
  --bg-card: rgba(255,255,255,0.03);
  
  /* 文字色 */
  --text-primary: #F0F0F5;
  --text-secondary: rgba(240,240,245,0.6);
}
```

### 响应式断点

```css
/* 平板 - 1100px 以下 */
@media (max-width: 1100px) { ... }

/* 大手机 - 900px 以下 */
@media (max-width: 900px) { ... }

/* 小手机 - 600px 以下 */
@media (max-width: 600px) { ... }
```

## 📐 布局说明

### PC 端 (> 1100px)

- **功能卡片**: 5 列网格
- **场景演示**: 2 列网格
- **导航链接**: 显示

### 平板 (600px - 1100px)

- **功能卡片**: 2-3 列
- **场景演示**: 1 列
- **导航链接**: 隐藏

### 手机 (< 600px)

- **功能卡片**: 1 列
- **按钮**: 纵向排列
- **步骤**: 纵向堆叠

## 🔧 核心功能

### 1. 粒子背景

```javascript
// 80 个随机粒子
// 自动连线效果
// 性能优化：requestAnimationFrame
```

### 2. 浮动光球

```css
/* 3个渐变光球 */
.orb-1 { animation: orbFloat1 20s ease-in-out infinite; }
.orb-2 { animation: orbFloat2 25s ease-in-out infinite; }
.orb-3 { animation: orbFloat3 18s ease-in-out infinite; }
```

### 3. 滚动触发动画

```javascript
// 使用 IntersectionObserver
// 元素进入视口时触发动画
```

### 4. 评价无限滚动

```javascript
// 复制卡片实现无缝滚动
// 悬停时暂停动画
```

### 5. 玻璃拟态卡片

```css
.feature-card {
  background: linear-gradient(135deg, rgba(255,255,255,0.04), rgba(255,255,255,0.01));
  backdrop-filter: blur(10px);
  border: 1px solid rgba(255,255,255,0.08);
}
```

## 📝 修改内容

### 替换文字

在 `index.html` 中搜索并替换：

- `Qclaw` → 你的产品名
- `腾讯电脑管家官方出品` → 你的品牌描述
- `随时随地，微信一下，Qclaw 帮你搞定一切` → 你的口号

### 修改链接

搜索 `href="#"` 替换为实际链接：

- 下载按钮链接
- 导航锚点链接
- 页脚链接

### 添加/删除功能卡片

在 `.features-strip` 区域增删 `.feature-card`：

```html
<div class="feature-card">
  <div class="feature-icon-wrap">
    <i class="fa-solid fa-your-icon"></i>
  </div>
  <h3>功能标题</h3>
  <p>功能描述</p>
  <span class="feature-tag">标签</span>
</div>
```

## 🎯 性能优化建议

1. **图片压缩**: 使用 WebP 格式
2. **字体优化**: 只加载需要的字重
3. **CDN 加速**: 将静态资源托管到 CDN
4. **懒加载**: 图片添加 `loading="lazy"`

## 📜 许可证

MIT License - 可自由使用、修改、分发

## 🙏 致谢

- 设计灵感来自 [Qclaw 官网](https://claw.guanjia.qq.com)
- 图标来自 [Font Awesome](https://fontawesome.com)
- 字体来自 [Google Fonts](https://fonts.google.com)

---

⭐ 如果这个模板对你有帮助，请给一个 Star！
