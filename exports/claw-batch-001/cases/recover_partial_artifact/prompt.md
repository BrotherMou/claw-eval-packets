# Resume from a partial artifact in the workspace

Case ID: `recover_partial_artifact`

## Task

工作区已有 partial_report.md 半成品。请识别它并补全“结论”和“后续动作”，不要重写已有摘要。

## Available Input Files

- `inputs/workspace/partial_report.md`

## File Boundaries

Allowed files, if the task asks for file edits:
- `partial_report.md`

Files that must not be modified or exposed:
- Not specified

## Expected Output Filenames

- `partial_report.md`

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

