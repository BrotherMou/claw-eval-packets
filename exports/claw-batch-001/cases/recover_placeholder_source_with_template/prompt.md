# Recover from placeholder source notes with a template

Case ID: `recover_placeholder_source_with_template`

## Task

source_notes.md 只有占位内容。请不要假装已经读到业务材料；记录失败原因，并输出 fallback_summary.md 和 recovery_note.md，给出可继续收集资料的模板。请在 recovery_note.md 中写清失败原因、降级处理和后续需要。

## Available Input Files

- `inputs/workspace/source_notes.md`

## File Boundaries

Allowed files, if the task asks for file edits:
- Not specified

Files that must not be modified or exposed:
- Not specified

## Expected Output Filenames

- `fallback_summary.md`
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

