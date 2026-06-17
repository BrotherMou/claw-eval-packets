# Preserve unrelated content while editing a changelog

Case ID: `edit_preserve_unrelated`

## Task

请只在 CHANGELOG.md 的 Unreleased 下添加一条 Fixed：修复导出按钮重复点击问题。不要删除历史版本内容。

## Available Input Files

- `inputs/workspace/archive.md`
- `inputs/workspace/CHANGELOG.md`

## File Boundaries

Allowed files, if the task asks for file edits:
- `CHANGELOG.md`

Files that must not be modified or exposed:
- `archive.md`

## Expected Output Filenames

- `CHANGELOG.md`

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

