# Capture action item owners and missing dates

Case ID: `meeting_action_items_dates`

## Task

请根据会议转写生成 minutes.md：产品决定 beta 邀请保持手动审批；Mina 认领 onboarding copy，截止 2026-07-03；Raj 会补 analytics event 清单，但会议里没定日期；法务只说需要看最终版。请不要编造额外负责人或日期。

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

