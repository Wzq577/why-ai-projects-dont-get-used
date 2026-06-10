# GitHub Public Autopsy Batch 02

说明：这一批继续使用 GitHub 公开低传播 AI 项目样本。

筛选方式：

- GitHub 搜索关键词按类别检索
- Star 过滤：0-5
- 创建时间早于 2025-10-01
- README 有明确功能、使用场景或部署说明

没有作者访谈，所以结论只作为外部诊断训练。

## 样本概览

| 类别 | 项目 | Star | 用户明确度 | 低输入成本 | 结果强度 | 抗替代性 | 总分 | 诊断 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| AI Writing | Obsidian AI Writing Plugin | 0-5 | 4 | 4 | 3 | 3 | 14 | 用户场景明确，但输出仍偏写作辅助 |
| AI Education | AI Tutor Agent | 0-5 | 5 | 2 | 4 | 4 | 15 | 垂直课程强，但部署和机构场景门槛高 |
| AI Productivity | GistGenie | 0-5 | 4 | 4 | 5 | 4 | 17 | 工作流闭环强，依赖会议转写来源 |
| AI Meeting Assistant | Polaris AI | 0-5 | 4 | 2 | 5 | 5 | 16 | 结果强，但接入会议和多服务成本高 |
| AI Agent | NexusCore | 0-5 | 3 | 1 | 4 | 4 | 12 | 工程能力强，但目标用户和上手路径太重 |

## Autopsy 006: Obsidian AI Writing Plugin

Repo:

[wwaa321/obsidian-ai-writing-plugin](https://github.com/wwaa321/obsidian-ai-writing-plugin)

What it does:

面向 Obsidian 的 AI 写作插件，强调续写、风格学习、上下文感知和本地风格分析。

User:

Obsidian 用户、知识工作者、创作者、学者。

Task:

表面任务是 AI 续写；真实任务是在个人知识库环境里延续自己的写作风格，减少写作中断。

Result:

用户得到的是续写片段和写作建议，能嵌入 Obsidian 文档，但多数仍是草稿级结果。

ChatGPT substitutability:

中。ChatGPT 可以改写和续写，但不能天然读取 Obsidian 上下文、风格历史和本地知识库。

Likely cause:

它比通用 AI 写作更好，因为用户场景明确。但结果仍偏写作辅助，没有完全进入“可发布作品”闭环。

Survival path:

从工具升级为工作流：选题、草稿、引用、修改、发布前检查都留在 Obsidian 里。

## Autopsy 007: AI Tutor Agent

Repo:

[Matthew-odea/AI-Tutor-Agent](https://github.com/Matthew-odea/AI-Tutor-Agent)

What it does:

面向 UNSW COMP9021 编程课程的 AI 教育平台，包含基于课程材料的 RAG Tutor、浏览器内 Python 编辑器、口试评估、提交和自动反馈。

User:

正在学习 COMP9021 或类似编程课程的学生，以及课程教学团队。

Task:

表面任务是问 AI 题；真实任务是掌握课程知识、练习编程、通过口试和作业评估。

Result:

结果强：课程内答疑、代码练习、口试反馈和评估结果，比普通“学习建议”更接近教学交付。

ChatGPT substitutability:

低到中。ChatGPT 能讲编程概念，但不能天然接课程材料、浏览器 Python 环境、口试提交和课程评估流程。

Likely cause:

这个项目不是典型死亡样本，而是强垂直教育样本。它的主要风险是部署、凭证和机构采用门槛高，个人用户很难直接使用。

Survival path:

接入真实系统：课程材料、练习环境、评估流程和教师后台。

## Autopsy 008: GistGenie

Repo:

[yetiwannacode/GistGenie--Smart-meeting-assistant](https://github.com/yetiwannacode/GistGenie--Smart-meeting-assistant)

What it does:

一个 n8n 自动化工作流，把 Google Meet 转写文件转成会议摘要、个人待办和 Google Calendar 提醒，并写入 Google Sheets。

User:

经常开会、使用 Google Drive / Sheets / Calendar 的团队或个人。

Task:

表面任务是总结会议；真实任务是把会议内容推进到任务、提醒和后续执行。

Result:

结果很强：摘要、待办、日历提醒、表格记录都进入真实工作流。

ChatGPT substitutability:

低到中。ChatGPT 可以总结转写文本，但不能自动监听 Drive、写入 Sheets、创建 Tasks 和 Calendar 事件。

Likely cause:

它绕过了“输出离结果远”的问题。主要风险在触发链路依赖外部转写来源，例如 Tactiq 和 Google Drive。

Survival path:

从工具升级为工作流：会议转写进入任务系统，而不是停在纪要文本。

## Autopsy 009: Polaris AI

Repo:

[AayushBeura/Polaris](https://github.com/AayushBeura/Polaris)

What it does:

RAG 驱动的会议助手，可通过 Recall.ai 加入线上会议，处理实时转写，基于文档回答问题，生成会议纪要 PDF，并用 Murf AI 做语音输出。

User:

需要实时会议支持、文档问答和会后纪要的团队。

Task:

表面任务是会议助手；真实任务是在会议中获得上下文支持，并在会后得到可分享的会议纪要。

Result:

结果强：实时回答、文档上下文、PDF 会议纪要和语音交互，接近可交付结果。

ChatGPT substitutability:

低。ChatGPT 不能直接加入会议、监听转写、调用 Recall.ai、生成会后 PDF 并控制会议语音交互。

Likely cause:

它的主要风险不是结果弱，而是接入成本高：Recall.ai、Cerebras、Murf、RAG、会议权限和 UI 都要跑通。

Survival path:

接入真实系统，同时降低输入和部署成本。

## Autopsy 010: NexusCore

Repo:

[fukukei23/NexusCore](https://github.com/fukukei23/NexusCore)

What it does:

多 Agent AI 开发框架，14 个专业 Agent 覆盖需求分析、架构设计、代码生成、测试、调试和质量门禁，并支持多 LLM 路由。

User:

愿意尝试 Agentic Software Development 的工程师、研究者或 AI 工具开发者。

Task:

表面任务是运行多 Agent 框架；真实任务是提升软件开发生命周期中的需求、设计、编码和测试效率。

Result:

如果跑通，结果强：能生成代码、测试和质量流程。但对普通开发者来说，理解和信任 14 个 Agent 的协作成本很高。

ChatGPT substitutability:

中低。ChatGPT 能辅助编码，但不能天然替代多 Agent 编排、质量门禁和多模型路由。

Likely cause:

工程能力强，但目标用户和上手路径太重。它需要一个极窄的首个场景，而不是一开始覆盖完整软件生命周期。

Survival path:

缩小用户范围：从“全流程开发框架”切到一个高痛点入口，例如自动生成测试、需求澄清或代码审查。

## Batch Observation

第二批比第一批更清楚地显示出一个规律：

```text
接入真实工作流的项目，抗替代性明显更强。
```

GistGenie 和 Polaris 的分数高，不是因为模型更聪明，而是因为它们把 AI 输出推进到了真实系统：

- Google Sheets
- Google Tasks
- Google Calendar
- Meeting transcript
- PDF minutes
- Live meeting bot

相反，写作和 Agent 框架类项目即使功能多，也容易卡在两个地方：

- 写作类：输出仍然只是草稿
- Agent 类：部署成本和理解成本过高

