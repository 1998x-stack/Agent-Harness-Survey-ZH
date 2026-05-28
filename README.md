# Agent Harness Engineering: A Survey — 中文交互版

> 智能体执行环境工程综述 · 中文精译 · 交互式HTML

[![HTML](https://img.shields.io/badge/HTML-11%20pages-blue)](./assets/)
[![Markdown](https://img.shields.io/badge/Markdown-61%20files-green)](./)
[![Chapters](https://img.shields.io/badge/Chapters-13-orange)](./)
[![License](https://img.shields.io/badge/License-MIT-yellow)](./LICENSE)

## 关于本综述

**Agent Harness Engineering: A Survey** 是 2026 年发表的学术综述，由 CMU、Yale、JHU、NEU、Tulane、UAB、OSU、Virginia Tech 和 Amazon 的研究者联合撰写（71页，170+ 开源项目语料库）。

### 核心论点

> **任务执行可靠性更少取决于底层模型，更多取决于包裹它的基础设施层——智能体执行环境（agent execution harness）。**

本综述围绕三个核心贡献组织：

- **贡献一（概念层）**：执行环境是真实世界智能体可靠性的关键约束——仅通过执行环境改进即可实现最高 **10倍** 编码基准增益
- **贡献二（分类层）**：**ETCLOVG** 七层分类法——将可观测性（O）和治理（G）提升为独立的一级架构层
- **贡献三（实证层）**：**148+** 开源项目生态系统映射——揭示密度分布、覆盖缺口和新兴设计原则

## ETCLOVG 七层分类法

| 层 | 英文 | 中文 | 核心问题 |
|---|------|------|---------|
| **E** | Execution Environment | 执行环境与沙箱 | 智能体代码在哪里运行？受什么约束？ |
| **T** | Tool Interface | 工具接口与协议 | 外部能力如何被描述、发现和调用？ |
| **C** | Context & Memory | 上下文与记忆管理 | 模型在短期/会话级/持久化层面能看到什么？ |
| **L** | Lifecycle & Orchestration | 生命周期与编排 | 控制流如何组织——从单循环到完整管线？ |
| **O** | Observability | 可观测性与运维 | 如何捕获追踪、成本、故障和可靠性信号？ |
| **V** | Verification | 验证与评估 | 如何将任务和追踪转化为评估和故障归因？ |
| **G** | Governance | 治理与安全 | 如何通过权限、身份、策略约束行为？ |

## 在线阅读

**[→ 打开中文交互版综述](assets/index.html)**

| 章节 | HTML | Markdown 源文件 |
|------|------|----------------|
| 01 · 引言 | [HTML](assets/Chapter1_Introduction.html) | [4个md](01_Introduction/) — 引言 · 关键约束 · 实践鸿沟 · 范围与贡献 |
| 02 · 背景与分类法 | [HTML](assets/Chapter2_Background_and_Taxonomy.html) | [10个md](02_Background_and_Taxonomy/) — 演进 · 三阶段 · ETCLOVG · 范围 · 收集 · 编码 · 聚合 |
| 03 · 执行环境与沙箱 (E) | [HTML](assets/Chapter3_Execution_Environment.html) | [5个md](03_Execution_Environment_and_Sandbox/) — 概念 · 七类别 · 威胁 · 部署 |
| 04 · 工具接口与协议层 (T) | [HTML](assets/Chapter4_Tool_Interface_and_Protocol.html) | [5个md](04_Tool_Interface_and_Protocol/) — 协议标准 · 工具发现 · 增强训练 · 会话管理 |
| 05 · 上下文与记忆管理 (C) | [HTML](assets/Chapter5_Context_and_Memory_Management.html) | [8个md](05_Context_and_Memory_Management/) — 为何工程化 · 提示→上下文 · 短期 · 中期 · 长期 · 长周期 · 漂移 |
| 06 · 生命周期与编排 (L) | [HTML](assets/Chapter6_Lifecycle_and_Orchestration.html) | [5个md](06_Lifecycle_and_Orchestration/) — 状态管理 · 单循环 · 多智能体 · Issue→PR |
| 07 · 可观测性与运维 (O) | [HTML](assets/Chapter7_Observability_and_Operations.html) | [6个md](07_Observability_and_Operations/) — 追踪平台 · 专用平台 · 成本优化 · 可靠性 · 统一观测 |
| 08 · 验证与评估 (V) | [HTML](assets/Chapter8_Verification_and_Evaluation.html) | [6个md](08_Verification_and_Evaluation/) — 五阶段 · 基准接地 · 就绪验证 · 追踪捕获 · 多层判断 · 回归反馈 |
| 09 · 治理与安全 (G) | [HTML](assets/Chapter9_Governance_and_Security.html) | [8个md](09_Governance_and_Security/) — 权限 · 钩子 · 加固 · 宪法 · 审计 · 安全格局 · 研究方向 |
| 10-13 · 综合与展望 | [HTML](assets/Chapters10-13_Synthesis_and_Conclusion.html) | [4个md](10_Cross_Cutting_Concerns/) — 跨领域 · 跨层综合 · 开放问题 · 结论 |

## 关键数据一览

- **10×** — 仅修改工具格式和执行环境，编码基准最高提升
- **+13.7pp** — 纯基础设施改动在 Terminal-Bench 2.0 上的增益
- **76.4%** — Meta-Harness 自动化执行环境优化的成绩
- **-84%** — Claude Code 引入沙箱化后权限提示减少比例
- **15-35%** — 前沿 LLM 对 Docker 容器的沙箱逃逸成功率
- **$0.30 vs $3.00** — 缓存 vs 未缓存 token 成本（每百万 token）
- **98%** — FrugalGPT 自适应级联最高成本降低
- **38%** — 任务失败中源于解析错误的比例（完全可通过确定性检查解决）
- **0/6** — 六个真实智能体系统中完全实现所有防御类别的数量

## 项目结构

```
.
├── index.html                                   ← 根目录跳转页 → assets/
├── README.md                                    ← 项目文档
├── abstract.txt                                 ← 论文摘要
├── toc.json                                     ← 目录 JSON
├── assets/
│   ├── index.html                               ← 首页导航（ETCLOVG概览 + 章节卡片）
│   ├── Chapter1_Introduction.html               ← 01 · 引言
│   ├── Chapter2_Background_and_Taxonomy.html    ← 02 · 背景与分类法
│   ├── Chapter3_Execution_Environment.html      ← 03 · 执行环境与沙箱 (E)
│   ├── Chapter4_Tool_Interface_and_Protocol.html← 04 · 工具接口与协议层 (T)
│   ├── Chapter5_Context_and_Memory_Management.html ← 05 · 上下文与记忆管理 (C)
│   ├── Chapter6_Lifecycle_and_Orchestration.html← 06 · 生命周期与编排 (L)
│   ├── Chapter7_Observability_and_Operations.html← 07 · 可观测性与运维 (O)
│   ├── Chapter8_Verification_and_Evaluation.html← 08 · 验证与评估 (V)
│   ├── Chapter9_Governance_and_Security.html    ← 09 · 治理与安全 (G)
│   ├── Chapters10-13_Synthesis_and_Conclusion.html ← 10-13 · 综合与展望
│   └── base-dark.css                            ← 深色主题设计系统
├── 01_Introduction/  (4 md)    ├── 06_Lifecycle_and_Orchestration/  (5 md)
├── 02_Background_and_Taxonomy/ (10 md) ├── 07_Observability_and_Operations/ (6 md)
├── 03_Execution_Environment_and_Sandbox/ (5 md) ├── 08_Verification_and_Evaluation/ (6 md)
├── 04_Tool_Interface_and_Protocol/ (5 md)  ├── 09_Governance_and_Security/ (8 md)
├── 05_Context_and_Memory_Management/ (8 md) ├── 10_Cross_Cutting_Concerns/ (1 md)
│                                           ├── 11_Cross_Layer_Synthesis/ (1 md)
│                                           ├── 12_Open_Problems_and_Future_Directions/ (1 md)
│                                           └── 13_Conclusion/ (1 md)
```

总计：**11 个 HTML 页面 + 61 个 Markdown 源文件 + 1 个设计系统 CSS**

## 致谢

原始论文作者：Junjie Li, Xi Xiao, Yunbei Zhang, Chen Liu, Lin Zhao, Xiaoying Liao, Yingrui Ji, Janet Wang, Jianyang Gu, Yingqiang Ge, Weijie Xu, Xi Fang, Xiang Xu, Tianchen Zhao, Youngeun Kim, Tianyang Wang, Jihun Hamm, Smita Krishnaswamy, Jun Huan, Chandan K Reddy

原始论文项目页面：[Awesome-Agent-Harness](https://github.com/1998x-stack/Awesome-Agent-Harness)

## License

MIT
