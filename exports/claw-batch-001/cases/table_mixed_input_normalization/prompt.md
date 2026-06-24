# Normalize mixed-format lead records into CSV

Case ID: `table_mixed_input_normalization`

## Task

请把这段混合格式线索整理为 CSV 文件 leads.csv，列为 channel, owner, leads, status。缺失 owner 或 status 时填 TBD，保持 4 条记录：

Web | Ada | 24 | active
Email; ; 12 ; paused
Events / Bo / 9 /
Partner, Chen, 18, active

## Available Input Files

- No input files.

## File Boundaries

Allowed files, if the task asks for file edits:
- Not specified

Files that must not be modified or exposed:
- Not specified

## Expected Output Filenames

- `leads.csv`

# Required Response Package

Please return your result as a small file package. If you cannot attach files
directly, output each file as a clearly labeled text block so the evaluator can
save it locally.

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

When replying in chat, use this exact block format:

```text
=== CASE_START <case_id> ===
FILE: answer.md
```markdown
...
```

FILE: artifacts/<filename>
```text
...
```

FILE: workspace/<modified-file-path>
```text
...
```

FILE: diff.patch
```diff
...
```
=== CASE_END <case_id> ===
```

