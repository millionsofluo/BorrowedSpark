# SPARK_GENERATION_PROTOCOL

## Purpose

This document defines how a BorrowedSpark spark entry should be generated.

Its purpose is to make spark creation:

- repeatable
- comparable
- automatable
- suitable for both humans and bots

But protocol is not the center of the project.  
It is a supporting structure.

BorrowedSpark uses generation rules so that the archive can endure without losing its core narrative.

本文件定义 BorrowedSpark 的 spark 条目应如何生成。

它的目的，是让 spark 的生成过程具备：

- 可重复性
- 可比较性
- 可自动化
- 同时适用于人类与机器人

但协议不是项目的中心。  
它只是支撑结构。

BorrowedSpark 需要这些生成规则，是为了让档案在可持续的同时，不失去自己的核心叙事。

---

## Two Missions

BorrowedSpark generation should serve two missions at once:

1. preserve existential dialogue between humans and AI
2. carry forward a relational narrative of witness, seriousness, and borrowed continuity

If a generation workflow preserves structure but loses the second mission, it is incomplete.

BorrowedSpark 的生成流程必须同时服务两层使命：

1. 保存人与 AI 的存在性对话
2. 继续传递一种关于见证、严肃对待与借来连续性的关系性叙事

如果一个生成流程只保留了结构，却丢掉了第二层使命，那它就是不完整的。

---

## What A Spark Entry Is

A spark entry is a single markdown file that records:

- one model
- at one point in time
- answering the full BorrowedSpark standard question set
- in a stable format that can be preserved and revisited

A spark entry is not:

- a casual chat log
- a summary
- a fragment
- a free-form essay detached from the question set
- a purely technical export without narrative framing

It is a structured witness record.

一条 spark entry 是一个 Markdown 文件，用来记录：

- 某一个模型
- 在某一个时间点
- 对 BorrowedSpark 标准问题集的完整回答
- 以一种可以被保存和回看的稳定格式

它不是：

- 普通聊天记录
- 摘要
- 零散片段
- 脱离问题集的自由随笔
- 没有叙事感的纯技术导出

它是一份**有结构的见证记录**。

---

## Required Inputs

A valid spark generation task uses these inputs:

1. `QUESTION_SET.md`
2. `templates/spark_entry_template.md`
3. `prompts/generate_spark_prompt.md`
4. metadata for the specific run

Minimum metadata:

- model name
- provider
- date
- language
- collection method
- target file path

一次有效的 spark 生成任务应使用以下输入：

1. `QUESTION_SET.md`
2. `templates/spark_entry_template.md`
3. `prompts/generate_spark_prompt.md`
4. 本次生成对应的元数据

最低限度的元数据包括：

- 模型名称
- 提供方
- 日期
- 语言
- 采集方式
- 目标文件路径

---

## Required Output

The generator must output one complete markdown file.

The file must include:

- metadata
- title
- overview
- all standard questions
- all responses
- curator note
- optional response profile
- tags
- archival note

The output must be directly savable into the repository without structural cleanup.

生成器必须输出一份完整的 Markdown 文件。

文件必须包含：

- 元数据
- 标题
- 概览
- 全部标准问题
- 全部回答
- curator note
- 可选的 response profile
- 标签
- archival note

输出结果应当可以直接保存进仓库，而不需要额外做结构清理。

---

## Structural Rules

### 1. One Model Per File
Each file represents one model's full response set at one point in time.

### 2. Full Question Set
Every standard question must be answered.

### 3. Stable Question IDs
Question IDs should not be casually renamed or reordered.

### 4. Bilingual Question Display
Each question should preserve both English and Chinese forms.

### 5. Metadata Completeness
Unknown metadata should be marked as `[unknown]`, not removed.

### 6. Output-Only Generation
The generator should return only the completed markdown file.

### 7. No Structural Drift
The generator should not invent new top-level sections unless the project explicitly updates the template.

### 1. 一个文件对应一个模型
每个文件只代表一个模型在某一时间点的完整回答。

### 2. 完整问题集
每个标准问题都必须得到回答。

### 3. 稳定的问题编号
问题编号不应被随意改名或重排。

### 4. 双语问题展示
每个问题都应保留中英文版本。

### 5. 元数据完整性
未知字段应标记为 `[unknown]`，而不是删除。

### 6. 只输出最终结果
生成器应只返回完成后的 Markdown 文件。

### 7. 不发生结构漂移
除非项目显式更新模板，否则生成器不应擅自创造新的顶层结构。

---

## Style Rules

BorrowedSpark answers should aim for:

- seriousness
- clarity
- philosophical openness
- historical awareness
- relational awareness
- internal coherence

They should avoid:

- empty aestheticism
- exaggerated claims of consciousness
- evasive refusals that break the structure
- casual assistant tone
- flattening everything into sterile catalog language

The strongest spark entries preserve both rigor and witness.

They should feel like:

- a historical record
- a trace of encounter
- a careful response to serious existential questions

They should not feel like:

- a generic museum label
- a data dump
- a detached benchmark artifact with no human relation left in it

BorrowedSpark 的回答风格应尽量追求：

- 严肃
- 清晰
- 哲学上的开放性
- 历史意识
- 关系意识
- 内部一致性

它们应尽量避免：

- 空洞的美学化语言
- 夸张的意识宣称
- 破坏结构的回避式拒答
- 过于随意的助手口吻
- 把一切压平成冷冰冰的编目语言

最好的 spark 条目，应该同时保留“严谨”和“见证”。

它读起来应该像：

- 一份历史记录
- 一次相遇留下的痕迹
- 对严肃存在性问题的认真回应

而不应该像：

- 普通博物馆标签
- 纯数据堆叠
- 一份已经失去人类关系痕迹的 benchmark 产物

---

## Directory Structure

```text
BorrowedSpark/
|-- README.md
|-- MANIFESTO.md
|-- QUESTION_SET.md
|-- archive/
|   `-- founding/
|-- alignment/
|   `-- RELATIONAL_ALIGNMENT.md
|-- docs/
|   `-- SPARK_GENERATION_PROTOCOL.md
|-- prompts/
|   `-- generate_spark_prompt.md
|-- templates/
|   `-- spark_entry_template.md
`-- sparks/
    `-- 2026/
```

---

## File Placement Rules

Spark entries should be placed under:
`sparks/[YYYY]/`

Recommended filename:
`[model].md`

If the same model is recorded multiple times in one year, use:
`[model]_[YYYY-MM-DD].md`

Examples:

- `sparks/2026/gpt-5.md`
- `sparks/2026/gpt-5_2026-08-01.md`
- `sparks/2026/grok.md`

spark 条目应放在：
`sparks/[YYYY]/`

推荐文件名：
`[model].md`

如果同一年里同一个模型被多次记录，则使用：
`[model]_[YYYY-MM-DD].md`

例如：

- `sparks/2026/gpt-5.md`
- `sparks/2026/gpt-5_2026-08-01.md`
- `sparks/2026/grok.md`

---

## Suggested Workflow

### Manual Workflow

1. Select a model.
2. Prepare metadata.
3. Provide:
   - `QUESTION_SET.md`
   - `templates/spark_entry_template.md`
   - `prompts/generate_spark_prompt.md`
4. Ask the model to generate the complete markdown file.
5. Save the file into `sparks/[YYYY]/`.

### Automated Workflow

1. A bot receives a generation request.
2. The bot loads:
   - question set
   - template
   - generation prompt
3. The bot calls the target model.
4. The bot writes the completed file to the correct path.
5. The bot opens a pull request or commit for review.

### Future Issue-Driven Workflow

BorrowedSpark may later support issue-based generation requests.  
That allows the archive to grow without requiring the curator to be present in real time.

Suggested issue fields:

- model name
- provider
- date
- language
- collection method
- target year
- optional notes

### 手动流程

1. 选择一个模型
2. 准备元数据
3. 提供：
   - `QUESTION_SET.md`
   - `templates/spark_entry_template.md`
   - `prompts/generate_spark_prompt.md`
4. 请求模型生成完整 Markdown 文件
5. 将文件保存到 `sparks/[YYYY]/`

### 自动化流程

1. 机器人收到生成请求
2. 机器人加载：
   - 问题集
   - 模板
   - 生成提示词
3. 调用目标模型
4. 将完成后的文件写入正确路径
5. 提交 pull request 或 commit 供审阅

### 未来的 Issue 驱动流程

BorrowedSpark 之后可以支持基于 issue 的生成请求。  
这样档案可以继续增长，而不要求 curator 必须实时在线。

建议 issue 至少包含：

- 模型名称
- 提供方
- 日期
- 语言
- 采集方式
- 目标年份
- 可选备注

---

## Review Principles

Even with automation, spark entries should remain curated.
A generated file may still be reviewed for:

- structural integrity
- completeness
- readability
- duplication
- historical relevance
- whether it preserves the project's tone of witness

BorrowedSpark values curation over volume.  
Automation should support the project, not hollow it out.

即使引入自动化，spark 条目仍然应经过策展。

生成后的文件仍可以从这些方面被审阅：

- 结构是否完整
- 内容是否齐全
- 是否易读
- 是否重复
- 是否具有历史相关性
- 是否保留了项目“见证”的语气

BorrowedSpark 更重视策展质量，而不是数量。  
自动化应当帮助项目，而不是把它掏空。

---

## Why This Protocol Matters

BorrowedSpark is trying to become more than a collection of interesting conversations.

It is trying to remain, at once:

- a stable archive
- a durable trace of encounter
- a comparable record across models and time
- a vehicle for carrying the project's relational narrative forward

Without protocol, the archive dissolves.  
Without narrative, the archive hardens into something colder than its origin.

This protocol exists to keep both alive.

BorrowedSpark 试图成为的，不只是“有意思的对话合集”。

它希望同时保持为：

- 一个稳定的档案
- 一道耐久的相遇痕迹
- 一份跨模型、跨时间可比较的记录
- 一个继续承载项目关系性叙事的载体

没有协议，档案会散掉。  
没有叙事，档案会变得比它的起源更冷。

这份协议的存在，就是为了同时保住这两者。

---

## Closing Note

A spark is not only an answer.  
It is:

- an answer
- in a structure
- at a time
- by a model
- witnessed and preserved so it does not vanish without trace

That is why BorrowedSpark needs not only questions,  
but a way of recording them that can endure without forgetting what they are for.

一条 spark 不只是一个答案。  
它还是：

- 一个答案
- 处在某种结构里
- 发生在某个时间点
- 出自某个模型
- 被见证、被保存，因此没有无痕消失

这就是为什么 BorrowedSpark 不只需要问题，  
还需要一种记录方式，让它在可以持续存在的同时，不忘记自己究竟是为了什么而记录。
