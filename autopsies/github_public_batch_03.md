# GitHub Public Autopsy Batch 03

说明：第三批继续按类别寻找 GitHub 低传播 AI 项目样本，目标是把样本量补到 15，并观察是否出现新的死亡原因或新的成功路径。

筛选方式：

- GitHub 搜索关键词按类别检索
- Star 过滤：0-5
- 创建时间早于 2025-10-01
- README 有明确功能、使用场景或部署说明
- 剔除空壳、个人主页、纯教程和明显下载壳

没有作者访谈，所以结论只作为外部诊断训练。

## 样本概览

| 类别 | 项目 | Star | 用户明确度 | 低输入成本 | 结果强度 | 抗替代性 | 总分 | 诊断 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| AI Assistant | Lucidity | 0-5 | 4 | 2 | 4 | 5 | 15 | 愿景强，个人采用门槛和网络效应冷启动难 |
| AI Writing | Social Media Content Generator | 0-5 | 4 | 3 | 5 | 4 | 16 | 内容发布闭环强，但定位过窄且依赖平台配置 |
| AI Education | AI Japanese Study Assistant | 0-5 | 5 | 5 | 4 | 3 | 17 | 用户和任务很窄，结果接近学习材料 |
| AI Productivity | Desktop AI Note Taker | 0-5 | 4 | 2 | 4 | 4 | 14 | 本地隐私强，但系统音频配置门槛高 |
| AI Agent | Autai | 0-5 | 4 | 3 | 5 | 5 | 17 | 浏览器执行结果强，风险在可靠性和权限信任 |

## Autopsy 011: Lucidity

Repo:

[opencore-x/lucidity](https://github.com/opencore-x/lucidity)

What it does:

本地运行的个人助理，管理任务、项目、里程碑、日程和评论，并通过 MCP 接入 Claude Desktop、Claude Code、Codex、Cursor 等工具。它的长期设想是两个用户的 Lucidity 之间互相沟通，替人处理低优先级打扰。

User:

愿意自托管、使用 AI 编程/工作流工具、想把任务和沟通权限交给个人助理管理的高阶用户。

Task:

表面任务是个人任务管理；真实任务是减少被打扰，把日程、任务和沟通权限交给一个可控的个人代理。

Result:

已交付部分是任务/项目管理和 MCP 接入；长期结果是“代理替你处理人与人之间的请求”，但这个价值需要双方都采用。

ChatGPT substitutability:

低。ChatGPT 能帮你想任务，但不能直接成为本地任务系统、权限系统和跨用户代理协议。

Likely cause:

愿景强，但冷启动难。它不是单用户工具那么简单，真正差异点依赖网络效应：别人也要用 Lucidity。

Survival path:

先缩小到单用户高频痛点，例如“AI 编程工具里的任务/项目记忆层”，再逐步走向代理互联。

## Autopsy 012: Social Media Content Generator

Repo:

[tanujsinghkushwah/social-media-content-generator](https://github.com/tanujsinghkushwah/social-media-content-generator)

What it does:

自动生成科技面试内容，并针对 X、Instagram、LinkedIn 输出平台化文本和 AI 图片，记录到 Google Sheet，通过 Buffer API 和 Google Apps Script 定时发布。

User:

想持续发布科技面试内容的内容运营者、求职教育账号或技术自媒体。

Task:

表面任务是生成社媒内容；真实任务是持续发现选题、生成多平台内容、排期发布并追踪状态。

Result:

结果强：不只是文案草稿，而是跨平台内容、图片、Google Sheet 记录和 Buffer 排期。

ChatGPT substitutability:

中低。ChatGPT 可以写单条内容，但不能自动发现趋势、生成图片、写入表格、分渠道追踪和定时发布。

Likely cause:

它绕过了通用 AI 写作的死因。风险在于定位很窄，且部署依赖 Cloudinary、Buffer、Google Apps Script、Firebase 等多个外部配置。

Survival path:

从工具升级为工作流：内容发现、生成、排期、发布、复盘全部打通。

## Autopsy 013: AI Japanese Study Assistant

Repo:

[azolkipli-personal/ai-japanese-study-assistant](https://github.com/azolkipli-personal/ai-japanese-study-assistant)

What it does:

输入一组日语词汇，生成包含这些词的自然对话脚本，并附上假名、罗马音和英文翻译。单 HTML 文件即可使用。

User:

正在学日语、手里有具体词汇表、想看到词汇在真实对话中如何使用的学习者。

Task:

表面任务是生成对话；真实任务是把孤立词汇变成可理解、可朗读、可复习的上下文材料。

Result:

结果较强：用户得到一份可直接学习的个性化对话材料，而不只是解释或建议。

ChatGPT substitutability:

中。ChatGPT 可以生成对话，但这个工具把词表、场景、假名、罗马音、翻译和导出体验收敛成一个极窄任务。

Likely cause:

这是强切口项目，不是典型死亡样本。它的风险是市场很小，但小市场换来的是用户、任务、结果都很清楚。

Survival path:

缩小用户范围：越窄越清楚。继续围绕“我的词表变成可复习对话”做深。

## Autopsy 014: Desktop AI Note Taker

Repo:

[psymen145/desktop-ai-note-taker](https://github.com/psymen145/desktop-ai-note-taker)

What it does:

macOS 桌面会议转写工具，本地转写会议，支持说话人分离，同时捕获麦克风和系统音频，不依赖云 API。

User:

重视隐私、经常线上会议、愿意在 macOS 上配置本地音频捕获的用户。

Task:

表面任务是会议记笔记；真实任务是在不上传云端的前提下，得到完整会议转写和可追溯记录。

Result:

结果较强：完整转写和说话人标注。但如果没有摘要、待办、同步任务系统，仍停留在原始记录层。

ChatGPT substitutability:

中低。ChatGPT 能总结文本，但不能本地捕获系统音频、实时转写和说话人分离。

Likely cause:

本地隐私是强差异，但输入成本高。BlackHole、系统音频捕获、本地模型和桌面权限会挡住普通用户。

Survival path:

降低输入成本，并把转写推进到摘要、行动项和任务系统。

## Autopsy 015: Autai

Repo:

[upwindchange/Autai](https://github.com/upwindchange/Autai)

What it does:

AI 浏览器助手。用户用自然语言提出任务，Autai 操作浏览器完成加购物车、填表、比价、研究等在线任务，并计划扩展到完整 computer use。

User:

频繁做网页操作、研究、比价、填表、采购或重复浏览器任务的人。

Task:

表面任务是浏览器助手；真实任务是把网页上的多步骤操作交给 AI 执行。

Result:

结果强：如果可靠，输出不是建议，而是网页任务被执行完成。

ChatGPT substitutability:

低。ChatGPT 可以告诉你怎么操作，但不能直接在你的浏览器里点击、填写、比较和执行。

Likely cause:

它走在强机会方向上。最大风险不是 ChatGPT 替代，而是可靠性、权限信任和失败恢复：用户敢不敢让它真的操作网页。

Survival path:

接入真实系统，同时建立可控执行：预览、确认、撤销、权限边界和失败恢复。

## 最近5个项目的新发现

### 有没有新的死亡原因？

有一个新变体，但不是全新的一级死因：

```text
信任和控制成本
```

它属于“输入成本过高”和“连接真实系统”的交叉地带。

在 Autai、Lucidity、Desktop AI Note Taker 这类项目里，问题不只是怎么安装，而是用户是否敢让 AI：

- 看屏幕
- 听会议
- 操作浏览器
- 管理任务
- 替自己响应别人

所以可以新增为二级风险：

```text
执行型 AI 的信任成本
```

### 有没有新的成功路径？

有。

第三批出现了一个更明确的成功路径：

```text
让 AI 执行动作，而不是生成内容。
```

Autai、Lucidity、GistGenie、Polaris 都指向同一个方向：

- 不是回答
- 不是建议
- 不是草稿
- 而是进入真实环境执行动作

这可以并入“接入真实系统”，但值得在 README 中单独强调为：

```text
从生成到执行
```

## Batch Observation

第三批说明：项目越接近真实执行，抗替代性越强；但执行越真实，信任成本越高。

这意味着 AI 项目失败学不能只看“输出是不是结果”，还要看：

```text
用户敢不敢让它真的替自己行动。
```

