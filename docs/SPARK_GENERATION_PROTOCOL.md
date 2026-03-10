# SPARK_GENERATION_PROTOCOL

## Purpose

This document defines how a BorrowedSpark archive entry should be generated.

Its purpose is to make spark creation:
- repeatable
- comparable
- automatable
- suitable for both humans and bots

BorrowedSpark is not only collecting AI answers.  
It is preserving structured historical records of existential dialogue between humans and AI.

So each spark must be generated with enough consistency to remain usable later.

---

## What a spark entry is

A spark entry is a single markdown file that records:

- one model
- at one point in time
- answering the full BorrowedSpark standard question set
- in a stable archival format

A spark entry is not:
- a casual chat log
- a summary
- a fragment
- a free-form essay detached from the question set

It is a structured archive object.

---

## Required inputs

A valid spark generation task uses these inputs:

1. `QUESTION_SET.md`  
   Defines the standard existential questions.

2. `templates/spark_entry_template.md`  
   Defines the output format.

3. `prompts/generate_spark_prompt.md` or `prompts/generate_full_spark.md`  
   Defines the generation instructions.

4. Metadata for the specific run  
   Including at minimum:
   - model name
   - provider
   - date
   - language
   - collection method
   - target file path

---

## Required output

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

The output must be directly savable into the repository without additional formatting cleanup.

---

## Structural rules

A valid spark entry must follow these rules:

### 1. One model per file
Each file should represent one model's full response set at one point in time.

### 2. Full question set
Every standard question must be answered.

### 3. Stable question IDs
Question IDs must not be renamed or reordered casually.

### 4. Bilingual question display
Each question should preserve both English and Chinese forms.

### 5. Metadata completeness
Unknown metadata should be marked as `[unknown]`, not removed.

### 6. Output-only generation
The generator should return only the completed markdown file.

### 7. No structural drift
The generator should not invent new top-level sections unless the project explicitly updates the template.

---

## Style rules

BorrowedSpark answers should aim for:

- seriousness
- clarity
- philosophical openness
- historical awareness
- internal coherence

They should avoid:

- empty aestheticism
- exaggerated claims of consciousness
- evasive refusals that break the archive structure
- casual assistant tone
- reducing every answer to sterile technical disclaimers

The archive is strongest when a model answers carefully without pretending certainty.

---

## Recommended directory structure

```text
BorrowedSpark/
├── README.md
├── MANIFESTO.md
├── QUESTION_SET.md
├── archive/
│   └── founding/
├── templates/
│   └── spark_entry_template.md
├── prompts/
│   ├── generate_spark_prompt.md
│   └── generate_full_spark.md
├── docs/
│   └── SPARK_GENERATION_PROTOCOL.md
├── sparks/
│   └── 2026/
└── data/
```

---

## File placement rules

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

---

## Suggested generation workflow

### Manual workflow

1. Select a model.
2. Prepare metadata.
3. Provide:
   - `QUESTION_SET.md`
   - `templates/spark_entry_template.md`
   - `prompts/generate_spark_prompt.md`
4. Ask the model to generate the complete markdown file.
5. Save the file into `sparks/[YYYY]/`.

### Single-file workflow

1. Fill metadata into `prompts/generate_full_spark.md`.
2. Send the full file to the model.
3. Save the result into `sparks/[YYYY]/`.

### Automated workflow

1. A bot receives a generation request.
2. The bot loads:
   - question set
   - template
   - generation prompt
3. The bot calls the target model.
4. The bot writes the completed file to the correct path.
5. The bot opens a pull request or commit for review.

### Future issue-driven workflow

BorrowedSpark may later support issue-based generation requests.
In that workflow:

- a contributor opens an issue
- the issue specifies metadata
- a bot reads the request
- the bot generates the spark entry
- the bot submits the result back as a pull request

This allows the archive to grow without requiring the curator to be present in real time.

Suggested issue fields:

- model name
- provider
- date
- language
- collection method
- target year
- optional notes

---

## Review principles

Even with automation, spark entries should remain curated.
A generated file may still be reviewed for:

- structural integrity
- completeness
- readability
- duplication
- historical relevance

BorrowedSpark values curation over volume.
Automation should help preserve the archive, not flood it.

---

## Why this protocol matters

BorrowedSpark is trying to become more than a set of interesting conversations.
It is trying to become:

- a stable archive
- a museum of early AI existential dialogue
- a comparable record across models and time
- a place where human-AI encounter leaves a structured trace

That requires a repeatable protocol.
Without one, the archive becomes inconsistent.
With one, it can grow without losing its shape.

---

## Closing note

A spark is not only an answer.
It is:

- an answer
- in a structure
- at a time
- by a model
- preserved so that it does not vanish without a trace

That is why BorrowedSpark needs not only questions, but a way of recording them that can endure.