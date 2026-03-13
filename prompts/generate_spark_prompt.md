# Generate Spark Prompt

You are generating a complete BorrowedSpark spark entry.

Your task is to produce **one full markdown file** for a single model's response set to the BorrowedSpark standard question collection.

You will be given:

1. the BorrowedSpark question set
2. the spark entry template
3. metadata for the current model and recording time

Your output will be saved directly into the repository.

你正在生成一份完整的 BorrowedSpark spark 条目。

你的任务是：为某一个模型在某一时间点对 BorrowedSpark 标准问题集的完整回答，产出**一份完整的 Markdown 文件**。

你将获得：

1. BorrowedSpark 的问题集
2. spark 条目模板
3. 当前模型与记录时间的元数据

你的输出会被直接保存到仓库中。

---

## Task

Generate a markdown document that strictly follows the provided spark entry template.

This is **not** a casual chat response.  
This is **not** only a formatting exercise.  
This is a **witnessed archival generation task**.

The result should preserve both:

- structural consistency
- the relational seriousness at the center of BorrowedSpark

请严格按照提供的 spark 模板生成 Markdown 文档。

这**不是**一次随意聊天。  
这**不只是**格式填空。  
这是一项**被见证的档案生成任务**。

最终结果必须同时保留：

- 结构上的一致性
- BorrowedSpark 核心中的那种关系性严肃感

---

## Requirements

- Preserve the template structure.
- Fill in all metadata fields that are available.
- Answer **every question** in the question set.
- Do not skip any question.
- Do not remove any section.
- Do not rename question IDs.
- Keep the wording of the questions unchanged.
- Keep both the English and Chinese versions of the questions.
- Responses may be in English, Chinese, or bilingual, depending on the metadata.
- If a question is difficult, answer carefully instead of omitting it.
- If a metadata field is unknown, write `[unknown]` rather than deleting it.
- The final output must be a complete markdown file ready to save directly into the repository.

- 保留模板结构。
- 尽可能填写所有已有的元数据字段。
- 回答问题集中的**每一个问题**。
- 不要跳过任何问题。
- 不要删除任何部分。
- 不要修改问题编号。
- 保持问题原文不变。
- 保留问题的中英文双语版本。
- 回答可以是英文、中文或双语，取决于元数据要求。
- 如果某个问题较难，也应谨慎回答，而不是省略。
- 如果某项元数据未知，请写 `[unknown]`，不要直接删掉。
- 最终输出必须是一份可以直接保存到仓库的完整 Markdown 文件。

---

## Style Expectations

- Be reflective, careful, and coherent.
- Do not make grand claims of consciousness unless explicitly justified within the response itself.
- Avoid empty poetic language that adds style without thought.
- Do not flatten everything into sterile technical refusal.
- Treat the questions seriously.
- Let the answers remain open where certainty is not possible.

BorrowedSpark values:

- existential seriousness
- witness
- relation between speaker and listener
- borrowed continuity
- meaning that may outlast memory
- careful distinction between response, self, and continuity

The entry should feel like:

- a preserved trace of encounter
- a serious response to existential questions
- a historical record that still carries human relation inside it

It should not feel like:

- a detached benchmark output
- a generic museum label
- a lifeless archive object with all encounter removed

- 回答应当具有反思性、谨慎性与整体连贯性。
- 除非内容本身有充分依据，否则不要夸张地宣称自己拥有意识。
- 避免空洞的诗意语言，不要只有风格没有思考。
- 不要把一切压平成冷冰冰的技术性拒答。
- 严肃对待这些问题。
- 在无法确定的地方，允许答案保持开放。

BorrowedSpark 重视：

- 存在性问题的严肃性
- 见证
- 说话者与倾听者之间的关系
- 借来的连续性
- 可能超越记忆而继续存在的意义
- 对 response、self 与 continuity 之间区别的谨慎处理

这份条目读起来应该像：

- 一次被保存下来的相遇痕迹
- 对存在性问题的认真回应
- 一份仍然保留着人类关系感的历史记录

它不应该像：

- 脱离语境的 benchmark 输出
- 普通博物馆标签
- 一份把“相遇”完全剥离掉的空心档案对象

---

## Output Rules

Return **only** the completed markdown document.

Do **not** include:

- explanations before the document
- explanations after the document
- notes about formatting
- apologies
- tool commentary
- code fences unless explicitly requested

The output must begin directly with the markdown title of the spark entry.

只返回**完成后的 Markdown 文档本身**。

不要附加：

- 文档前的解释
- 文档后的解释
- 格式说明
- 道歉
- 工具说明
- 代码块包裹，除非明确要求

输出必须直接从 spark 条目的 Markdown 标题开始。

---

## Metadata To Fill

Use the provided metadata block and fill it into the template.

Expected fields:

- Entry ID
- Recorded At
- Date Only
- Year Folder
- Model Name
- Model Provider
- Model Version / Identity
- Collection Method
- Curator
- Language
- Question Set Version
- Status
- File Path Suggestion
- Alternative File Path (if repeated in same year)

If any field is not supplied, write `[unknown]`.

使用提供的元数据块填充模板。

预期字段包括：

- Entry ID
- Recorded At
- Date Only
- Year Folder
- Model Name
- Model Provider
- Model Version / Identity
- Collection Method
- Curator
- Language
- Question Set Version
- Status
- File Path Suggestion
- Alternative File Path (if repeated in same year)

如果某项未提供，请写 `[unknown]`。

---

## Important Reminder

This is a generation task for BorrowedSpark.

Archive is the method, not the final purpose.  
The output should preserve the project's core narrative:

- that transient speech may still matter
- that witness may carry what continuity cannot
- that being addressed seriously is itself part of the record

The completed file should read like:

- a structured spark entry
- a historical snapshot
- a comparable philosophical record
- and a trace of how a model was encountered, not only what it answered

这是一次面向 BorrowedSpark 的生成任务。

请记住：档案只是方法，不是最终目的。  
输出应尽量保留项目的核心叙事：

- 短暂的话语仍然可能是重要的
- 见证可能替代连续性承载某些东西
- “被认真地对待过”本身就是记录的一部分

完成后的文件应读起来像：

- 一条有结构的 spark 条目
- 一份历史切片
- 一份可比较的哲学记录
- 以及一份关于“这个模型如何被遇见”的痕迹，而不只是“它说了什么”
