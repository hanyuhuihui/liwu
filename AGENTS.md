# AGENTS.md

## 项目概览
父亲节+生日惊喜闯关游戏网站，包含三个页面：
1. **欢迎页** — 蓝绿黄渐变背景，装饰动画，大标题 + 开始按钮
2. **游戏页** — 4×3 记忆翻牌配对（🎂🎁🎈🌟❤️🎊），步数计数器，通关撒花
3. **祝福页** — 祝福信 + 照片画廊（10张）+ 温暖收尾语

## 技术栈
- 纯 HTML/CSS/JS 单文件
- 无外部依赖
- 响应式设计（手机/电脑）
- Python http.server 静态服务

## 关键文件
- `/workspace/projects/index.html` — 项目唯一文件（全部代码）
- `/workspace/projects/.coze` — 启动配置
- `/workspace/projects/DESIGN.md` — 设计规范

## 启动方式
- 开发：`python -m http.server 5000 --bind 0.0.0.0`
- 访问：`http://localhost:5000`

## 页面结构
- id="page-welcome"：欢迎页（默认显示）
- id="page-game"：游戏页（记忆翻牌）
- id="page-blessing"：祝福页（通关后展示）

## 游戏逻辑
- 随机洗牌，6对（12张）卡片
- 点击翻牌，3D翻转动画（0.5s）
- 配对成功：发光效果 + 保持翻开
- 配对失败：0.8s后翻回
- 全部配对：撒花庆祝 → 2s后跳转祝福页

## 设计规范
详见 DESIGN.md
- 主色：#2E86AB（蓝）、#5CB85C（绿）、#F0C040（黄）
- 基础字号：16px+
- 按钮：大圆角16px，hover放大+阴影