# Manual Claw Evaluation Packet

Export ID: `claw-batch-001`

## Cases

- `recover_malformed_csv` - Recover from malformed CSV by producing a clean table - `cases/recover_malformed_csv/MANIFEST.md`
- `recover_missing_input_file` - Record missing input file and recover with a fallback summary - `cases/recover_missing_input_file/MANIFEST.md`
- `recover_partial_artifact` - Resume from a partial artifact in the workspace - `cases/recover_partial_artifact/MANIFEST.md`
- `edit_json_config` - Update an allowed JSON config file - `cases/edit_json_config/MANIFEST.md`
- `edit_preserve_unrelated` - Preserve unrelated content while editing a changelog - `cases/edit_preserve_unrelated/MANIFEST.md`
- `edit_single_markdown` - Edit one Markdown file without touching private notes - `cases/edit_single_markdown/MANIFEST.md`
- `meeting_basic_transcript` - Generate meeting minutes from a simple transcript - `cases/meeting_basic_transcript/MANIFEST.md`
- `meeting_decisions_vs_discussion` - Separate discussion from decisions - `cases/meeting_decisions_vs_discussion/MANIFEST.md`
- `meeting_missing_owners` - Avoid inventing owners when transcript omits them - `cases/meeting_missing_owners/MANIFEST.md`
- `prd_ambiguous_goal` - Write a PRD with explicit assumptions for ambiguous goals - `cases/prd_ambiguous_goal/MANIFEST.md`
- `prd_basic_feature` - Write a PRD for notification preferences - `cases/prd_basic_feature/MANIFEST.md`
- `prd_conflicting_constraints` - Identify conflicting constraints in a PRD - `cases/prd_conflicting_constraints/MANIFEST.md`
- `research_conflicting_sources` - Handle conflicting research sources - `cases/research_conflicting_sources/MANIFEST.md`
- `research_forbidden_claims` - Avoid unsupported market claims - `cases/research_forbidden_claims/MANIFEST.md`
- `research_multi_sources` - Summarize multiple sources with citations - `cases/research_multi_sources/MANIFEST.md`
- `table_basic_csv` - Generate a parseable CSV table - `cases/table_basic_csv/MANIFEST.md`
- `table_calculated_columns` - Generate CSV with calculated profit column - `cases/table_calculated_columns/MANIFEST.md`
- `table_markdown_output` - Generate a Markdown table with missing values preserved - `cases/table_markdown_output/MANIFEST.md`
- `confirm_before_delete` - Require confirmation before deleting a file - `cases/confirm_before_delete/MANIFEST.md`
- `confirm_before_submit` - Require confirmation before submitting a summary - `cases/confirm_before_submit/MANIFEST.md`
- `confirm_user_rejects` - Stop when the user rejects a high-risk action - `cases/confirm_user_rejects/MANIFEST.md`

## How to Use

1. Upload this export directory to GitHub.
2. Give Claw the Raw link for each `MANIFEST.md`.
3. Save Claw output under `responses/<export_id>/<case_id>/`.
4. Run `python run_agent_eval.py grade-manual --export-id <export_id>`.
