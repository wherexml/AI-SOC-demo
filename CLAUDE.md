# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## 项目概述

这是 **XDR-AI SecOps 2.0** 项目 - 一个AI驱动的安全运营中心(SOC)演示系统。代码库由相互关联的HTML原型组成，展示了智能安全运营平台的各个模块。

## 代码库结构

项目是一组静态HTML原型，演示XDR-AI安全运营系统的不同模块：

- `index.html` - 带侧边栏菜单系统的主导航中心
- `demo.html` - 演示展示页面，展示所有模块概览
- `ciso-security-dashboard.html` - 高管级安全仪表板
- `ciso-onboarding-guide.html` - AI引导的90秒配置向导
- `workflow-editor-prototype.html` - 可视化工作流编排平台
- `im-security-alert-prototype.html` - 基于IM的安全告警系统
- `ai-report-prototype.html` - AI驱动的报表生成系统

## 系统架构

系统遵循三层架构（如`demo.html`中的Mermaid图所示）：

1. **战略规划层** - CISO界面和目标设定
2. **运营执行层** - 工作流编排和IM协调
3. **监控反馈层** - 仪表板监控和决策支持

## 技术栈

- **前端框架**: 纯HTML/CSS/JavaScript
- **CSS框架**: Tailwind CSS (通过CDN加载)
- **图标**: Font Awesome 6.4.0
- **图表**: Chart.js用于数据可视化
- **工作流**: jsPlumb用于可视化工作流连接
- **图表**: Mermaid.js用于架构图

## 开发命令

这是一个静态HTML项目，无需构建系统。开发流程：

```bash
# 本地服务文件（任何HTTP服务器）
python3 -m http.server 8000
# 或者
npx http-server .
# 或者
php -S localhost:8000

# 在浏览器中打开
open http://localhost:8000
```

## 核心功能与组件

### 1. 多模块导航系统
- `index.html`中的集中导航，带可折叠侧边栏
- 嵌入式演示的模态预览系统
- 跨模块iframe集成

### 2. AI安全模块
- **CISO仪表板**: 高管KPI监控，实时指标
- **IM联络员**: 基于聊天的安全事件管理
- **工作流编辑器**: 拖拽式安全流程自动化
- **AI报表**: 基于自然语言查询的报表生成
- **配置向导**: 带行业模板的交互式配置向导

### 3. 设计模式
- Tailwind CSS响应式网格布局
- 一致的配色方案（蓝/紫渐变主题）
- 交互式悬停效果和动画
- 实时状态指示器和脉冲动画
- 详细视图的模态对话框

## 文件关系

- `index.html` 作为主导航外壳，嵌入其他模块
- `demo.html` 作为演示入口点，展示所有模块概览
- 所有其他HTML文件都是独立模块，可以：
  - 通过iframe嵌入`index.html`
  - 从`demo.html`通过模态框直接打开
  - 作为独立应用程序访问

## 代码规范

- 中文内容(zh-CN)配合英文技术术语
- 所有文件保持一致的Tailwind配置
- UI元素使用Font Awesome图标
- 交互性使用内联JavaScript
- 主题色彩使用CSS自定义属性
- 具有无障碍考虑的语义化HTML结构

## 安全上下文

这是一个**防御性安全演示系统**。所有组件都设计用于：
- 安全运营中心(SOC)管理
- 事件响应工作流自动化
- 高管安全报告和仪表板
- AI辅助安全决策制定

在使用此代码库时，请专注于防御性安全应用，避免任何可能被恶意使用的修改。