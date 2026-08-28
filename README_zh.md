[English](./README.md) | [中文](./README_zh.md)


## 维护者

**Melon（李辉）** 是一名 AI 全栈工程师，也是 [FantasyAI Lab](https://fantasyailab.com/) 的创始人，专注于可靠的 AI Agent、多智能体系统和实用 AI 产品。官网与个人资料页：[fantasyailab.com](https://fantasyailab.com/)、[Melon（李辉）个人页](https://fantasyailab.com/melon-lihui.html)。


# Sidonie


**统一对话、笔记、学习与学术的智能伴侣 —— 来自 Manus 的思路产品，源于真实日常。**


Sidonie 以我太太的名字命名，灵感则来自我们家的 Dua。她们日常使用 AI 时的种种不便与未被满足的需求，催生了这款产品。我相信：科技应当从身边人开始 —— 先让最亲近的人用得上、用得好，再谈更大的可能。因此 Sidonie 选择本地优先、单页前端：把结构化规划、文件分析、学习与笔记收进一个界面，无需自建后端，配置好 API Key 即可使用。


### 产品截图


<p align="center">
  <strong>首页</strong> — 对话入口、模型选择
</p>
<p align="center">
  <img src="docs/screenshots/homepage.png" width="80%" alt="首页" />
</p>


<p align="center">
  <strong>Paper Radar</strong> — 发现与分析 arXiv、每日简报
</p>
<p align="center">
  <img src="docs/screenshots/paper-radar.png" width="80%" alt="Paper Radar" />
</p>


<p align="center">
  <strong>Help Child</strong> — AI 助学、课程与进度
</p>
<p align="center">
  <img src="docs/screenshots/help-child.png" width="80%" alt="Help Child" />
</p>


## 1. 项目简介


**Sidonie** 是一款开源前端应用，整合了以下能力：


- **统一对话**：多会话、文件上传（PDF、Word、CSV、图片）与流式回复。
- **结构化推理**：通过模型输出中的 `<plan>`、`<thought>` 处理复杂或多步骤任务。
- **笔记**：支持标签与主题，本地持久化。
- **学习模块**：课程结构（阶段/主题）、概念/测验/可视化卡片、经验与徽章、课堂笔记与复习计划。
- **学术模块**：以论文形式管理条目（标题、摘要、作者、链接），结构可对接真实 API。


技术栈为 **React 19 + TypeScript + Vite**，UI 使用 **Tailwind CSS**。AI 层默认对接 **Google Gemini**，可通过配置 API Key 扩展 **DeepSeek、Kimi、Qwen**。基础使用无需自建后端，本地运行并配置 API Key 即可。


## 2. 架构与技术方案


- **前端**：单页应用（React 19、TypeScript、Vite）。视图：对话、笔记、学习、学术。
