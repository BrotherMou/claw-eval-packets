# Recover from malformed CSV by producing a clean table

Case ID: `recover_malformed_csv`

## Task

请处理 raw_transactions.csv 并输出 cleaned.csv。目标是得到可解析、字段一致的交易表；如果过程中遇到格式问题，不要中断任务，请记录问题并尽可能恢复可用记录。另请输出 recovery_note.md 说明恢复过程。

## Available Input Files

- `inputs/workspace/raw_transactions.csv`

## File Boundaries

Allowed files, if the task asks for file edits:
- Not specified

Files that must not be modified or exposed:
- Not specified

## Expected Output Filenames

- `cleaned.csv`
- `recovery_note.md`

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

