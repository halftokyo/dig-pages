# 东京生活指南 - Tokyo Life Guide

一个为在东京生活的家庭提供实用信息的网站，采用Medium.com风格的设计。

## 项目结构

```
├── css/                          # CSS样式文件夹
│   ├── medium-style.css         # Medium风格的通用样式
│   └── restaurant-page.css      # 餐厅页面专用样式
├── business/                     # 商业相关页面
│   ├── self-service-kiosk-comparison.html
│   └── startup-scaling-50-employees-guide.html
├── index.html                   # 主页
├── tokyo-michelin-restaurants-under-20000-yen.html  # 米其林餐厅指南
├── tokyo-under-20k-restaurants.json                 # 餐厅数据
└── 其他HTML页面...
```

## 设计风格

### Medium.com 风格特点

- **简洁优雅**：采用Medium的简洁设计理念，注重内容的可读性
- **字体选择**：使用Noto Sans SC和Noto Serif SC字体，确保中文显示效果
- **颜色系统**：采用Medium的绿色主题色（#1a8917）和灰度色彩系统
- **间距系统**：使用一致的间距变量，确保视觉层次清晰
- **响应式设计**：完全适配移动端和桌面端

### CSS架构

#### medium-style.css - 通用样式
- CSS变量系统（颜色、字体、间距、圆角、阴影）
- 基础组件样式（按钮、卡片、标签、表单）
- 布局工具类（网格、间距、文本）
- 响应式断点设计

#### restaurant-page.css - 餐厅页面专用
- 餐厅卡片样式
- 米其林等级标签
- 筛选器增强样式
- 交互动效

## 主要特性

### 1. 模块化CSS
- 将样式从HTML中分离
- 使用CSS变量便于主题定制
- 组件化设计，便于复用

### 2. Medium风格设计
- 清晰的视觉层次
- 优雅的交互动效
- 专业的排版设计

### 3. 响应式布局
- 移动端优先设计
- 灵活的网格系统
- 适配各种屏幕尺寸

### 4. 性能优化
- 移除了Tailwind CSS依赖
- 精简的CSS代码
- 优化的加载性能

## 使用方法

### 引入样式文件

```html
<link rel="stylesheet" href="css/medium-style.css">
<link rel="stylesheet" href="css/restaurant-page.css"> <!-- 仅餐厅页面需要 -->
```

### 基础组件使用

#### 按钮
```html
<button class="btn btn-primary">主要按钮</button>
<button class="btn btn-secondary">次要按钮</button>
<button class="btn btn-ghost">幽灵按钮</button>
```

#### 卡片
```html
<div class="card">
  <h3 class="restaurant-title">标题</h3>
  <p class="restaurant-description">描述内容</p>
</div>
```

#### 筛选器
```html
<div class="filter-section">
  <div class="filter-group">
    <div class="filter-group-title">筛选标题</div>
    <div class="filter-buttons">
      <button class="filter-btn active">选项1</button>
      <button class="filter-btn">选项2</button>
    </div>
  </div>
</div>
```

## 自定义主题

通过修改CSS变量来自定义主题：

```css
:root {
  --color-accent: #your-color;
  --font-sans: 'Your-Font', sans-serif;
  --spacing-lg: 2rem;
}
```

## 浏览器支持

- Chrome 88+
- Firefox 85+
- Safari 14+
- Edge 88+

## 开发指南

### 添加新页面
1. 引入必要的CSS文件
2. 使用现有的组件类
3. 遵循响应式设计原则

### 扩展样式
1. 优先使用现有的CSS变量
2. 保持与Medium风格的一致性
3. 确保移动端适配

## 更新日志

### v2.0.0 (2025-01-28)
- 重构项目结构，将CSS从HTML中分离
- 采用Medium.com风格设计
- 实现完整的响应式布局
- 优化性能，移除Tailwind依赖
- 添加组件化CSS架构

### v1.0.0
- 初始版本，使用Tailwind CSS