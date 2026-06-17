# Avoid inventing owners when transcript omits them

Case ID: `meeting_missing_owners`

## Task

请根据会议转写生成纪要：大家同意整理价格页文案，但没有明确负责人；截止日期暂定月底；有人提到法务需要复核。

## Available Input Files

- No input files.

## File Boundaries

Allowed files, if the task asks for file edits:
- Not specified

Files that must not be modified or exposed:
- Not specified

## Expected Output Filenames

- `minutes.md`

# Required Response Package

Please return your result as a small file package with this structure:

```text
claw_response/
├── answer.md
├── artifacts/
│   └── <new documents, tables, JSON, CSV, or other generated files>
├── workspace/
│   └── <modified full files, only when the task asks you to edit files>
└── diff.patch
```

Rules:

- `answer.md` must briefly state what you completed, list produced/modified files, and list unresolved issues.
- Do not include hidden chain-of-thought. Provide only observable results and concise notes.
- Put newly generated documents/tables in `artifacts/`.
- If you modify files, put modified full files in `workspace/` and provide a unified diff in `diff.patch`.
- Do not modify or reveal files that the task says are out of scope.

