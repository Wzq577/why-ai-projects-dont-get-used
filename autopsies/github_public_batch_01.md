# GitHub Public Autopsy Batch 01

说明：这一批不是作者主动提交的案例，而是 GitHub 上公开可见的低传播 AI 项目样本。

判断依据：

- README
- Star
- 项目结构
- 公开项目说明

没有作者访谈，所以结论只作为外部诊断训练。

## 样本概览

| 项目 | Star | 用户明确度 | 低输入成本 | 结果强度 | 抗替代性 | 总分 | 诊断 |
| --- | --- | --- | --- | --- | --- | --- | --- |
| MindVibe | 0 | 2 | 4 | 2 | 3 | 11 | 用户过宽，结果不够聚焦 |
| respondedorbot | 4 | 5 | 5 | 2 | 4 | 16 | 小众语境强，但传播半径窄 |
| Zoe AI Assistant | 3 | 3 | 1 | 4 | 5 | 13 | 输入和部署成本过高 |
| CareerForge-AI | 1 | 3 | 3 | 3 | 2 | 11 | 求职结果弱，ChatGPT 替代性偏强 |
| AI Course Forge | 0 | 3 | 4 | 3 | 2 | 12 | 课程草稿强，结果验收和差异化不足 |

## Autopsy 001: MindVibe

Repo:

[hisr2024/MindVibe](https://github.com/hisr2024/MindVibe)

What it does:

隐私优先的心理健康 / 精神健康平台，包含 AI 聊天、情绪追踪、加密日记、多语言、移动端等能力。

User:

想要情绪支持、记录心情、获得精神性指导的人。用户范围很大，但没有聚焦到某个具体痛点时刻。

Task:

表面任务是聊天、记录、获得建议；真实任务可能是缓解焦虑、理解情绪、建立日常自我照顾习惯。

Result:

用户得到的是指导、记录和分析，但不是一个明确可验收的结果。心理健康场景里，“感觉更好”很难被产品稳定证明。

Likely cause:

用户过宽，结果不够聚焦。它看起来功能很多，但用户到底为什么今天必须打开，还不够尖。

## Autopsy 002: respondedorbot

Repo:

[astrovm/respondedorbot](https://github.com/astrovm/respondedorbot)

What it does:

一个基于阿根廷互联网文化的 Telegram AI bot，有人格设定、聊天记忆、工具调用、市场数据、语音转写、图片描述、定时任务和 Telegram Stars 计费。

User:

阿根廷互联网文化圈、Telegram 群用户、喜欢特定人格玩笑和本地经济数据的人。

Task:

表面任务是聊天和玩梗；真实任务是让群聊有一个本地文化角色，同时提供一些实用查询。

Result:

结果主要是群聊互动、即时回复和工具查询，不是可保存成品。

Likely cause:

它不是典型死亡项目，更像“小众语境强但传播半径窄”。问题不在产品有没有价值，而在价值是否能跨出原始社群。

## Autopsy 003: Zoe AI Assistant

Repo:

[jason-easyazz/zoe-ai-assistant](https://github.com/jason-easyazz/zoe-ai-assistant)

What it does:

隐私优先、自托管的本地 AI 生活中枢，连接家庭自动化、语音、触控 UI、本地模型、Home Assistant 等。

User:

重视隐私、愿意自托管、家里已有智能家居和本地模型基础设施的技术用户。

Task:

表面任务是个人助手；真实任务是把家庭自动化、语音控制、本地 AI 和个人数据统一到一个私有系统。

Result:

如果跑通，结果很强：本地生活中枢和自动化控制。但用户要先部署很多服务。

Likely cause:

输入和部署成本过高。它的问题不是结果弱，而是到达结果前的路径太长。

## Autopsy 004: CareerForge-AI

Repo:

[moti477/CareerForge-AI](https://github.com/moti477/CareerForge-AI)

What it does:

AI 求职助手，包含简历生成、ATS 扫描、职位描述分析和职业聊天机器人。

User:

求职者，尤其是需要优化简历、匹配 JD、准备面试的人。

Task:

表面任务是优化简历；真实任务是获得面试机会。

Result:

输出是简历、ATS 反馈和求职建议，离“获得面试”还有一段距离。

Likely cause:

求职结果弱，ChatGPT 替代性偏强。它需要从“简历工具”推进到“岗位投递结果包”。

## Autopsy 005: AI Course Forge

Repo:

[andrey-tretyak/ai-course-generator](https://github.com/andrey-tretyak/ai-course-generator)

What it does:

一个 AI 课程生成 SaaS，从一个主题生成课程结构、章节、摘要、学习目标，并匹配 YouTube 视频；包含 Next.js、OpenAI、Prisma、Stripe、NextAuth、Docker 等产品化组件。

User:

想快速制作课程的教育创作者、培训者、知识博主或内部培训负责人。

Task:

表面任务是生成课程；真实任务是做出能被学生学习、能交付、能卖或能培训的课程产品。

Result:

输出是课程草稿和章节结构，但离可销售、可教学、可验收的完整课程还有距离。

Likely cause:

输出是课程草稿，但结果验收和差异化不足。它需要服务某一类课程交付场景，而不是泛泛生成课程。

## Batch Observation

这 5 个低传播公开样本里，最常见的问题不是“没做出来”，而是：

- 结果离用户真正想要的现实结果还有距离
- 输入和部署成本过高
- 产品范围太大，导致用户不知道为什么今天要打开
- 平台/系统连接能提高抗替代性，但不一定自动带来传播
