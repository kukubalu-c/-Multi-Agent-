# 旅算家 · 多Agent智能旅游行程规划系统

> **5 分钟完成原本 8 小时的行程规划** — 输入预算和偏好，6 个 AI 智能体协作完成目的地推荐、交通比价、住宿匹配、行程安排，全程预算闭环。

---

## 预览

直接打开 `index.html` 即可体验，无需安装任何依赖。

| 引导页 | AI 规划首页 | 推荐结果页 | 活动详情页 |
|:------:|:-----------:|:----------:|:----------:|
| 品牌展示 → 进入 | 输入预算/偏好 | 预算条 + 交通/住宿 | 地图 + 时光轴 |

## 核心功能

### 🤖 6 Agent 智能协作
| Agent | 职责 |
|-------|------|
| **PreferenceAgent** | 分析用户偏好，补充兴趣标签 |
| **DestinationAgent** | 基于预算和地域推荐 3 个目的地 |
| **TransportAgent** | 搜索去程/返程交通（航班/高铁） |
| **HotelAgent** | 匹配合适的住宿选项 |
| **ActivityAgent** | 规划每日行程活动 |
| **BudgetAgent** | 核算总花费，超预算自动循环调整 |

### 📱 交互特性
- 目的地横向滚动选择，勾选标识已选
- 交通/住宿/活动三段切舱
- 多日行程时光轴
- Leaflet 交互地图（全屏展开）
- 预算进度条实时反馈
- 切换目的地时所有数据联动更新

### 🎨 设计风格
轻氧薄荷奶油风 — 薄荷绿主色、奶油白卡片、大圆角、柔和阴影

## 快速体验

```bash
git clone <repo-url>
cd demo
# 用浏览器直接打开
open index.html      # macOS
start index.html     # Windows
```

点击「开始 AI 智能规划」即可观看 6 Agent 按顺序执行的加载动画，或点击「跳过演示」直接查看完整数据。

> **注意**：这是一个前端演示 Demo，所有数据均为 Mock 数据，不涉及真实 API 调用。完整项目包含 Python FastAPI 后端 + 通义千问 LLM 集成。

## 技术栈

| 层 | 技术 |
|----|------|
| 前端 | 纯 HTML/CSS/JS，零框架 |
| 图标 | Feather Icons |
| 地图 | Leaflet + OpenStreetMap |
| 后端（完整版） | Python FastAPI |
| LLM（完整版） | 通义千问 DashScope |

## 项目结构

```
demo/
├── index.html          # 单页面应用，包含全部样式/逻辑/数据
├── README.md           # 本文件

完整版项目结构（不在本 demo 内）：
python/
├── agents/             # 6 个 Agent 实现
├── orchestrator/       # Pipeline 编排 + 预算循环
├── api/                # FastAPI 后端
├── models/             # Pydantic 数据模型
├── config/             # 配置
mobile/
├── mobile-travel.html  # 移动端 UI
├── api.js              # API 调用层
docs/pm/                # 产品文档
```

## License

MIT
