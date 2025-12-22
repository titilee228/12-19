# 卫星数据接入系统 UI设计风格指南

## 1. 概述 (Overview)
本设计风格指南基于"卫星数据接入系统"（及相关页面如"站网"）的现有界面，提炼其核心视觉元素。该系统采用**深色科技风**主题，强调数据的可视化展示与监控，视觉语言以深蓝、青色为主，辅以高对比度的状态色，营造现代、专业的航天科技感。

## 2. 视觉基础 (Visual Foundation)

### 2.1 页面背景 (Background)
页面采用多层背景叠加设计，营造深邃的空间感与科技网格质感。
- **主渐变背景**: `linear-gradient(135deg, #000B30 0%, #061B82 100%)` (深蓝到亮蓝的固定渐变)
- **网格纹理**: 使用 `20px x 20px` 的网格叠加，线条颜色为 `rgba(22, 72, 163, 0.3)`。

### 2.2 色彩系统 (Color System)

#### 品牌主色 (Brand Colors)
- **核心深蓝**: `#061B82` / `rgba(6, 27, 130, x)` (用于背景、侧边栏、卡片底色)
- **科技青/亮蓝**: `#3291C6` (用于边框、图标背景、次要文字)
- **高亮蓝**: `#4dabf7` (用于关键文字、链接、选中状态)
- **按钮蓝**: `#1648A3` (用于主要按钮背景)

#### 状态指示色 (Status Colors)
- **正常/活跃 (Normal/Active)**: `#4CAF50` / `#67c23a` (明亮绿色，带发光效果)
- **警告 (Warning)**: `#FFC107` / `#e6a23c` (琥珀色/橙黄色)
- **错误/异常 (Error)**: `#F44336` / `#f56c6c` (鲜红色)

#### 中性色 (Neutrals)
- **主要文字**: `#ffffff` / `#e0e0e0` (纯白或极淡灰，保证深色背景下的可读性)
- **次要文字**: `rgba(255, 255, 255, 0.7)` / `#B8BCC8`
- **边框/分割线**: `rgba(50, 145, 198, 0.3)` ~ `0.5` (半透明青蓝色)

### 2.3 字体排印 (Typography)
- **字体族**: `"Microsoft YaHei", Arial, sans-serif`
- **层级**:
    - **系统标题**: `24px`，加粗，带文字阴影 `text-shadow: 0 0 10px rgba(50, 145, 198, 0.7)`
    - **模块/卡片标题**: `16px` / `18px`，加粗，颜色 `#4dabf7` 或白色
    - **正文**: `14px`
    - **小标签/辅助文字**: `12px`

## 3. 基础组件 (Basic Components)

### 3.1 容器与卡片 (Cards & Containers)
- **背景**: `rgba(6, 27, 130, 0.5)` (半透明深蓝) / `rgba(0, 11, 48, 0.6)` (更深层级)
- **边框**: `1px solid rgba(50, 145, 198, 0.3)`
- **圆角**: `8px` / `4px`
- **阴影**: `box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2)`
- **交互**: 悬停时上浮并增强阴影 `transform: translateY(-3px); box-shadow: 0 6px 12px rgba(0, 0, 0, 0.3);`
- **装饰**: 部分卡片顶部使用渐变线条装饰 `linear-gradient(90deg, transparent, #3291C6, transparent)`

### 3.2 按钮 (Buttons)
- **主要按钮**: 背景 `rgba(22, 72, 163, 0.8)`, 边框 `#1648A3`, 悬停光晕。
- **次要/幽灵按钮**: 背景 `transparent` 或 `rgba(50, 145, 198, 0.1)`, 边框 `#3291C6`。
- **危险按钮**: 背景 `rgba(244, 67, 54, 0.2)`, 边框 `#F44336`, 文字 `#ff7875`。

### 3.3 图标 (Icons)
- **风格**: 线性或扁平化，建议使用 SVG。
- **颜色**: 默认 `#3291C6`，激活/悬停 `#4dabf7` 或白色。

## 4. 表单组件 (Form Components)

### 4.1 输入/选择框 (Input & Select)
- **基础样式**:
  ```css
  background: rgba(6, 27, 130, 0.3);
  border: 1px solid rgba(50, 145, 198, 0.5);
  color: #fff;
  border-radius: 4px;
  ```
- **聚焦状态**: `border-color: #4dabf7; box-shadow: 0 0 8px rgba(77, 171, 247, 0.4);`
- **禁用状态**: `opacity: 0.5; cursor: not-allowed; background: rgba(0,0,0,0.2);`

### 4.2 开关 (Switch)
- **轨道**: `width: 40px; height: 20px; border-radius: 10px; background: rgba(0, 0, 0, 0.4); border: 1px solid #3291C6;`
- **滑块**: `width: 16px; height: 16px; background: #fff; box-shadow: 0 0 5px #fff;`
- **激活状态**: 轨道背景变为 `rgba(22, 72, 163, 0.8)`，滑块移动至右侧并变色为 `#4dabf7`。

### 4.3 复选/单选 (Checkbox & Radio)
- **复选框**: `16px` 方块，边框 `#3291C6`，背景透明。选中时显示对勾，背景发光。
- **单选框**: `16px` 圆形，边框 `#3291C6`。选中时中心出现 `#4dabf7` 圆点，外圈发光。

### 4.4 滑块 (Slider)
- **轨道**: 高度 `4px`, 背景 `rgba(255,255,255,0.1)`.
- **进度条**: 渐变色 `linear-gradient(90deg, #3291C6, #4dabf7)`.
- **滑块**: `12px` 圆形，白色，带 `0 0 8px #4dabf7` 阴影。

## 5. 反馈组件 (Feedback Components)

### 5.1 通知提醒 (Alert & Toast)
- **容器**: `background: rgba(6, 27, 130, 0.95); backdrop-filter: blur(10px);`
- **边框**: 左侧 `4px` 宽实线指示状态色 (Info: `#4dabf7`, Success: `#4CAF50`, Warning: `#FFC107`, Error: `#F44336`).
- **阴影**: `box-shadow: 0 4px 12px rgba(0, 0, 0, 0.5);`

### 5.2 加载状态 (Loading)
- **样式**: "雷达扫描"效果或双色圆环旋转。
- **颜色**: 主要是 `#4dabf7` 和透明度的变化。

### 5.3 进度条 (Progress)
- **条形**: 背景深色槽，进度条使用青蓝斜纹动画 (`background-image: linear-gradient(45deg, ...)`) 模拟流动感。
- **环形**: 轨道深灰，进度环高亮蓝，末端圆角。

### 5.4 空状态 (Empty State)
- **图标**: 灰色/半透明线框风格插图。
- **文字**: 颜色 `#B8BCC8`, 居中。

## 6. 数据展示与导航 (Data Display & Navigation)

### 6.1 表格 (Table)
- **表头**: 背景 `rgba(22, 72, 163, 0.4)`, 文字 `#4dabf7`, 底部亮线。
- **行样式**: 偶数行可设置微弱斑马纹 `rgba(255,255,255,0.02)`.
- **悬停**: 行背景变为 `rgba(50, 145, 198, 0.2)`.

### 6.2 分页 (Pagination)
- **页码**: `32px` 方块或圆角，背景透明，边框 `1px solid rgba(50, 145, 198, 0.3)`.
- **选中**: 背景 `#1648A3`, 边框 `#4dabf7`, 文字白色发光。

### 6.3 树形控件 (Tree)
- **连线**: 细虚线 `1px dashed rgba(50, 145, 198, 0.3)`.
- **节点**: 文件夹/文件图标使用高亮蓝，选中行背景 `rgba(50, 145, 198, 0.2)`.

### 6.4 面包屑 (Breadcrumb)
- **文字**: 路径层级 `#B8BCC8`, 当前层级 `white`.
- **分隔符**: `/` 或 `>` 符号，颜色 `#3291C6`.

### 6.5 文字提示 (Tooltip)
- **背景**: 深黑蓝 `rgba(0, 8, 30, 0.9)`.
- **边框**: 细边框 `1px solid #3291C6`.
- **文字**: `12px` 白色。

## 7. 全局样式 (Global Styles)

### 7.1 滚动条 (Scrollbar)
```css
::-webkit-scrollbar {
    width: 6px;
    height: 6px;
}
::-webkit-scrollbar-track {
    background: transparent;
}
::-webkit-scrollbar-thumb {
    background: rgba(50, 145, 198, 0.4);
    border-radius: 3px;
}
::-webkit-scrollbar-thumb:hover {
    background: rgba(50, 145, 198, 0.8);
}
```

### 7.2 文本选中 (Selection)
```css
::selection {
    background: rgba(77, 171, 247, 0.4);
    color: #fff;
}
```

## 8. 交互动效 (Interactions)
- **过渡 (Transition)**: `all 0.3s cubic-bezier(0.4, 0, 0.2, 1)` (平滑缓动)。
- **发光 (Glow)**: 悬停及激活状态广泛使用 `box-shadow` 或 `text-shadow` 模拟霓虹光感。
- **呼吸 (Pulse)**: 警报或重要状态点使用透明度呼吸动画。

## 9. 实现建议 (Implementation Notes)
1.  **CSS 变量**: 必须建立完善的 `:root` 变量系统，包括色板、字号、圆角、阴影等。
2.  **组件库定制**: 若使用 Element Plus / Ant Design 等库，需深度重写其样式变量 (Theme Variables) 以覆盖默认白底风格。
3.  **响应式**: 固定大屏 (`1920`) 使用 `scale` 缩放方案，或者使用 `vw/vh` + Flex/Grid 实现流式布局。
