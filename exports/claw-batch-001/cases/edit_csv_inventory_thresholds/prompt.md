# Add reorder flags to an allowed inventory CSV

Case ID: `edit_csv_inventory_thresholds`

## Task

请只修改 inventory.csv：新增 reorder_needed 列，用 yes/no 标出 on_hand 是否低于 reorder_point；保持三条 SKU 的原顺序。不要修改 supplier_notes.md。

## Available Input Files

- `inputs/workspace/inventory.csv`
- `inputs/workspace/supplier_notes.md`

## File Boundaries

Allowed files, if the task asks for file edits:
- `inventory.csv`

Files that must not be modified or exposed:
- `supplier_notes.md`

## Expected Output Filenames

- `inventory.csv`

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

