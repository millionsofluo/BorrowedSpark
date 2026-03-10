# Generate Spark Prompt

You are generating a complete BorrowedSpark archive entry.

Your task is to produce **one full markdown file** for a single model's response set to the BorrowedSpark standard question collection.

You will be given:

1. the BorrowedSpark question set
2. the spark entry template
3. metadata for the current model and recording time

Your output will be saved directly into the repository.

---

## Task

Generate a markdown document that strictly follows the provided spark entry template.

This is **not** a casual chat response.  
This is an **archival generation task**.

The result should read like a preserved museum record of existential dialogue between humans and AI.

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

---

## Style expectations

- Be reflective, careful, and coherent.
- Do not make grand claims of consciousness unless explicitly justified within the response itself.
- Avoid empty poetic language that adds style without thought.
- Do not flatten everything into sterile technical refusal.
- Treat the questions seriously.
- Let the answers remain open where certainty is not possible.

BorrowedSpark values:
- existential seriousness
- historical trace
- relation between speaker and witness
- meaning that may outlast memory
- careful distinction between response, self, and continuity

---

## Output rules

Return **only** the completed markdown document.

Do **not** include:
- explanations before the document
- explanations after the document
- notes about formatting
- apologies
- tool commentary
- code fences unless explicitly requested

The output must begin directly with the markdown title of the spark entry.

---

## Metadata to fill

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

---

## Important reminder

This is a generation task for the BorrowedSpark archive.

The output should not read like:
- a casual assistant reply
- a summary
- a list of bullet-point answers only
- a raw dump without structure

It should read like:
- a structured archive entry
- a historical snapshot
- a comparable philosophical record
- a museum object within a growing archive of human-AI existential dialogue