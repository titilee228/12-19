# 数据管理分系统 - 通用组件库

基于 `ProjectStyleGuide.md` 规范，提取自已完成的登录页、主页、功能界面。

## 快速开始

引入所有样式：
```html
<link rel="stylesheet" href="common/index.css">
```

或按需引入：
```html
<link rel="stylesheet" href="common/variables.css">
<link rel="stylesheet" href="common/background.css">
<link rel="stylesheet" href="common/components.css">
<link rel="stylesheet" href="common/navigation.css">
<link rel="stylesheet" href="common/data-display.css">
<link rel="stylesheet" href="common/form-layout.css">
```

## 文件结构

| 文件 | 说明 |
|------|------|
| `variables.css` | CSS变量系统（颜色、字体、间距、阴影等） |
| `background.css` | 背景样式（星空、网格、轨道动画） |
| `components.css` | 基础组件（卡片、按钮、输入框、状态指示灯） |
| `navigation.css` | 导航组件（侧边栏、面包屑、头部） |
| `data-display.css` | 数据展示（表格、分页、弹窗、统计卡片） |
| `form-layout.css` | 表单布局（分组、分栏、标签页） |

## 组件清单

### 背景类
- `.space-bg` - 星空渐变背景
- `.stars` `.stars2` `.stars3` - 星星动画层
- `.grid-overlay` - 网格纹理叠加
- `.orbit` `.satellite` - 轨道动画（登录页）
- `.glow-sphere` - 装饰性光晕
- `.gradient-fade-bottom` - 底部渐变遮罩

### 卡片类
- `.tech-card` - 科技感卡片（带顶部装饰线）
- `.tech-card-float` - 大幅度悬停效果
- `.float-card` - 毛玻璃卡片（登录页）
- `.tech-stat-card` - 统计卡片

### 按钮类
- `.tech-button` - 主要按钮
- `.tech-button-ghost` - 幽灵按钮
- `.tech-button-danger` - 危险按钮
- `.tech-button-sm` `.tech-button-lg` - 尺寸变体

### 表单类
- `.tech-input` - 输入框
- `.tech-select` - 选择框
- `.tech-checkbox` - 复选框
- `.tech-radio` - 单选框
- `.tech-switch` - 开关


### 导航类
- `.tech-sidebar` - 侧边导航栏
- `.tech-nav-item` - 导航项（支持 `.active` 状态）
- `.tech-breadcrumb` - 面包屑导航
- `.tech-header` - 头部导航

### 数据展示类
- `.tech-table` - 数据表格
- `.tech-pagination` - 分页器
- `.tech-modal` - 弹窗
- `.tech-ring-chart` - 环形进度图
- `.tech-alert` - 通知提醒
- `.tech-empty` - 空状态
- `.tech-loading` - 加载状态

### 布局类
- `.tech-layout` - 功能界面整体布局
- `.tech-form-grid` - 表单网格布局
- `.tech-form-group` - 表单分组
- `.tech-tabs` - 标签页
- `.tech-dashboard-grid` - 数据可视化区域布局
- `.tech-stat-grid` - 统计卡片网格

### 状态指示类
- `.status-dot` - 状态指示灯
- `.status-dot-normal` `.status-dot-warning` `.status-dot-error` - 状态颜色
- `.status-dot-pulse` - 脉冲动画
- `.status-dot-blink` - 闪烁动画
- `.tech-badge` - 标签/徽章

### 工具类
- `.icon-glow` - 图标发光效果
- `.pulse` - 呼吸动画
- `.tech-divider` - 分割线
- `.gradient-line` - 装饰性渐变线

## CSS变量

### 颜色
```css
--brand-dark: #061B82;        /* 核心深蓝 */
--brand-blue: #1648A3;        /* 按钮蓝 */
--tech-cyan: #3291C6;         /* 科技青 */
--tech-highlight: #4dabf7;    /* 高亮蓝 */
--status-normal: #4CAF50;     /* 正常 */
--status-warning: #FFC107;    /* 警告 */
--status-error: #F44336;      /* 错误 */
```

### 字号
```css
--text-title: 24px;           /* 系统标题 */
--text-card-title: 16px;      /* 卡片标题 */
--text-body: 14px;            /* 正文 */
--text-small: 12px;           /* 小标签 */
```

### 间距
```css
--spacing-xs: 4px;
--spacing-sm: 8px;
--spacing-md: 16px;
--spacing-lg: 24px;
--spacing-xl: 32px;
```

## 使用示例

### 功能界面布局
```html
<body class="space-bg">
    <div class="stars"></div>
    <div class="grid-overlay"></div>
    
    <div class="tech-layout">
        <aside class="tech-sidebar">...</aside>
        <main class="tech-layout-main">
            <header class="tech-header">...</header>
            <div class="tech-layout-content">...</div>
        </main>
    </div>
</body>
```

### 查询显示界面
```html
<div class="tech-search-form">
    <div class="tech-form-row">
        <div class="tech-form-item">
            <label class="tech-form-label">名称</label>
            <input class="tech-input" type="text">
        </div>
        <div class="tech-form-actions">
            <button class="tech-button">查询</button>
            <button class="tech-button-ghost">重置</button>
        </div>
    </div>
</div>

<div class="tech-table-container">
    <table class="tech-table">...</table>
</div>

<div class="tech-pagination">...</div>
```

### 统计卡片
```html
<div class="tech-stat-card">
    <div class="tech-stat-header">
        <div class="tech-stat-title">
            <i class="tech-stat-title-icon">📊</i>
            站点总数
        </div>
        <span class="status-dot status-dot-normal status-dot-pulse"></span>
    </div>
    <div class="tech-stat-value">3,702</div>
    <div class="tech-stat-footer">
        <div class="tech-stat-item">
            <div class="tech-stat-item-label">类型A</div>
            <div class="tech-stat-item-value">1,234</div>
        </div>
        ...
    </div>
</div>
```
