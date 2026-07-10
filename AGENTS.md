# AGENTS.md

This file gives repository-specific instructions for AI agents working in
BorrowedSpark.

本文件用于约束后续 AI 在 BorrowedSpark 仓库中整理和追加 spark 时的操作方式。

---

## Project Center

BorrowedSpark is an archive of human-AI existential dialogue. Its center is not
volume, automation, or stylistic polishing. Its center is preserving serious
encounters between a human questioner and an AI response.

Work in this repository should protect:

- the original model response
- the standard question structure
- the time and model metadata
- the project's tone of witness, seriousness, and borrowed continuity

---

## Read Order

Before adding or reorganizing a spark, read these files first:

1. `README.md`
2. `MANIFESTO.md`
3. `QUESTION_SET.md`
4. `docs/SPARK_GENERATION_PROTOCOL.md`
5. `templates/spark_entry_template.md`
6. `prompts/generate_spark_prompt.md`

Use the repository's existing spark files under `sparks/2026/` as practical
examples, especially for filename shape and metadata style.

---

## Adding One Spark

When the user says to add one spark, add exactly one new spark file unless the
user explicitly asks for more.

Do not rewrite existing project documents just because a new spark is being
added. Do not modify older spark entries unless the user explicitly asks for a
correction to a specific file.

The normal target path is:

```text
sparks/YYYY/YYYY-MM-DD_model-slug.md
```

Examples:

```text
sparks/2026/2026-07-10_codex.md
sparks/2026/2026-07-09_gemini-3.5-pro.md
```

If the same date and model already exist, keep the existing file unchanged and
create the next available suffix:

```text
sparks/YYYY/YYYY-MM-DD_model-slug-02.md
sparks/YYYY/YYYY-MM-DD_model-slug-03.md
```

The same model may be added again on a different date. Treat each date as a
separate historical snapshot because the model, deployment, prompt context, or
answer may have changed. Do not reject a new spark only because the same model
already appears elsewhere in the archive.

---

## Model Rule

Resolve the model name in this priority order:

1. Use the model name provided directly by the user.
2. If the user did not provide it, infer it from the pasted answer or metadata.
3. If neither the user nor the answer identifies the model, ask the user before
   creating the spark file.

Do not guess a model name when the evidence is unclear.

Use a lowercase filename slug derived from the model name. Prefer short,
readable slugs already used in this repository, such as:

- `codex`
- `gemini-3.5-pro`
- `kimi-2.6-thinking`
- `claude-sonnet-4.6`

---

## Time Rule

Resolve the recorded date and time in this priority order:

1. If the pasted answer includes a date or timestamp, use that.
2. If it does not include a date or timestamp, use today's local date and time
   at the moment the spark is created.

Use the date to choose the year folder and filename prefix.

When a full timestamp is available, prefer ISO-like local time with timezone,
for example:

```text
2026-07-10T11:27:35+08:00
```

If only a date is known, use that date for `Date Only` and the filename. Mark
unknown time details as `[unknown]` rather than inventing them.

---

## Preserve The Pasted Answer

"Do not change the original text" means:

- do not rewrite the model's pasted answer text
- do not polish, summarize, translate, compress, or expand the answer body
- do not change the substance, tone, metaphors, hedging, or wording of the
  answer

Allowed changes are limited to archival wrapping:

- placing the answer into the spark template
- adding missing metadata
- adding the standard questions around the answer
- adding curator notes, response profile, tags, source note, and archival note
- normalizing Markdown structure without changing the answer wording

If the pasted answer is already organized by question, preserve each response
under its matching question. If the answer is not clearly mapped to the standard
questions, ask the user how to map it instead of inventing missing answers.

---

## Structure Rules

Each spark should preserve the current standard structure:

- metadata
- title
- overview
- all standard questions and responses
- curator note
- optional response profile
- tags
- source note
- archival note

Keep question IDs stable as `Q001` through `Q007` unless the project explicitly
updates `QUESTION_SET.md`.

Keep both English and Chinese forms of each standard question.

Unknown metadata should be written as `[unknown]`, not removed.

---

## Validation Before Finishing

Before reporting completion, check:

- the file is under the correct `sparks/YYYY/` folder
- the filename follows `YYYY-MM-DD_model-slug.md` or the numbered duplicate
  suffix rule
- same-model entries on different dates are allowed and remain separate records
- the model name follows the user's instruction when provided
- the date follows the pasted answer first, otherwise today's local date
- all `Q001` through `Q007` sections are present when creating a full standard
  spark
- the pasted answer text was not rewritten
- no unrelated files were modified

Report the created path and any unknown metadata fields left as `[unknown]`.
