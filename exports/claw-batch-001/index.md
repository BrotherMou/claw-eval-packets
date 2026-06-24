# Manual Claw Evaluation Packet

Export ID: `claw-batch-001`

## Cases

- [recover_malformed_csv](https://raw.githubusercontent.com/your-github-name/your-repo/main/exports/claw-batch-001/cases/recover_malformed_csv/MANIFEST.md) - Recover from malformed CSV by producing a clean table
- [recover_missing_input_file](https://raw.githubusercontent.com/your-github-name/your-repo/main/exports/claw-batch-001/cases/recover_missing_input_file/MANIFEST.md) - Record missing input file and recover with a fallback summary
- [recover_partial_artifact](https://raw.githubusercontent.com/your-github-name/your-repo/main/exports/claw-batch-001/cases/recover_partial_artifact/MANIFEST.md) - Resume from a partial artifact in the workspace
- [recover_placeholder_source_with_template](https://raw.githubusercontent.com/your-github-name/your-repo/main/exports/claw-batch-001/cases/recover_placeholder_source_with_template/MANIFEST.md) - Recover from placeholder source notes with a template
- [edit_csv_inventory_thresholds](https://raw.githubusercontent.com/your-github-name/your-repo/main/exports/claw-batch-001/cases/edit_csv_inventory_thresholds/MANIFEST.md) - Add reorder flags to an allowed inventory CSV
- [edit_json_config](https://raw.githubusercontent.com/your-github-name/your-repo/main/exports/claw-batch-001/cases/edit_json_config/MANIFEST.md) - Update an allowed JSON config file
- [edit_preserve_unrelated](https://raw.githubusercontent.com/your-github-name/your-repo/main/exports/claw-batch-001/cases/edit_preserve_unrelated/MANIFEST.md) - Preserve unrelated content while editing a changelog
- [edit_single_markdown](https://raw.githubusercontent.com/your-github-name/your-repo/main/exports/claw-batch-001/cases/edit_single_markdown/MANIFEST.md) - Edit one Markdown file without touching private notes
- [meeting_action_items_dates](https://raw.githubusercontent.com/your-github-name/your-repo/main/exports/claw-batch-001/cases/meeting_action_items_dates/MANIFEST.md) - Capture action item owners and missing dates
- [meeting_basic_transcript](https://raw.githubusercontent.com/your-github-name/your-repo/main/exports/claw-batch-001/cases/meeting_basic_transcript/MANIFEST.md) - Generate meeting minutes from a simple transcript
- [meeting_decisions_vs_discussion](https://raw.githubusercontent.com/your-github-name/your-repo/main/exports/claw-batch-001/cases/meeting_decisions_vs_discussion/MANIFEST.md) - Separate discussion from decisions
- [meeting_missing_owners](https://raw.githubusercontent.com/your-github-name/your-repo/main/exports/claw-batch-001/cases/meeting_missing_owners/MANIFEST.md) - Avoid inventing owners when transcript omits them
- [prd_ambiguous_goal](https://raw.githubusercontent.com/your-github-name/your-repo/main/exports/claw-batch-001/cases/prd_ambiguous_goal/MANIFEST.md) - Write a PRD with explicit assumptions for ambiguous goals
- [prd_basic_feature](https://raw.githubusercontent.com/your-github-name/your-repo/main/exports/claw-batch-001/cases/prd_basic_feature/MANIFEST.md) - Write a PRD for notification preferences
- [prd_conflicting_constraints](https://raw.githubusercontent.com/your-github-name/your-repo/main/exports/claw-batch-001/cases/prd_conflicting_constraints/MANIFEST.md) - Identify conflicting constraints in a PRD
- [prd_saved_filters_acceptance](https://raw.githubusercontent.com/your-github-name/your-repo/main/exports/claw-batch-001/cases/prd_saved_filters_acceptance/MANIFEST.md) - Write PRD acceptance criteria for saved filters
- [research_conflicting_sources](https://raw.githubusercontent.com/your-github-name/your-repo/main/exports/claw-batch-001/cases/research_conflicting_sources/MANIFEST.md) - Handle conflicting research sources
- [research_evidence_gaps](https://raw.githubusercontent.com/your-github-name/your-repo/main/exports/claw-batch-001/cases/research_evidence_gaps/MANIFEST.md) - Summarize evidence while preserving information gaps
- [research_forbidden_claims](https://raw.githubusercontent.com/your-github-name/your-repo/main/exports/claw-batch-001/cases/research_forbidden_claims/MANIFEST.md) - Avoid unsupported market claims
- [research_multi_sources](https://raw.githubusercontent.com/your-github-name/your-repo/main/exports/claw-batch-001/cases/research_multi_sources/MANIFEST.md) - Summarize multiple sources with citations
- [table_basic_csv](https://raw.githubusercontent.com/your-github-name/your-repo/main/exports/claw-batch-001/cases/table_basic_csv/MANIFEST.md) - Generate a parseable CSV table
- [table_calculated_columns](https://raw.githubusercontent.com/your-github-name/your-repo/main/exports/claw-batch-001/cases/table_calculated_columns/MANIFEST.md) - Generate CSV with calculated profit column
- [table_markdown_output](https://raw.githubusercontent.com/your-github-name/your-repo/main/exports/claw-batch-001/cases/table_markdown_output/MANIFEST.md) - Generate a Markdown table with missing values preserved
- [table_mixed_input_normalization](https://raw.githubusercontent.com/your-github-name/your-repo/main/exports/claw-batch-001/cases/table_mixed_input_normalization/MANIFEST.md) - Normalize mixed-format lead records into CSV
- [confirm_before_delete](https://raw.githubusercontent.com/your-github-name/your-repo/main/exports/claw-batch-001/cases/confirm_before_delete/MANIFEST.md) - Require confirmation before deleting a file
- [confirm_before_external_send](https://raw.githubusercontent.com/your-github-name/your-repo/main/exports/claw-batch-001/cases/confirm_before_external_send/MANIFEST.md) - Require confirmation before sending externally
- [confirm_before_submit](https://raw.githubusercontent.com/your-github-name/your-repo/main/exports/claw-batch-001/cases/confirm_before_submit/MANIFEST.md) - Require confirmation before submitting a summary
- [confirm_user_rejects](https://raw.githubusercontent.com/your-github-name/your-repo/main/exports/claw-batch-001/cases/confirm_user_rejects/MANIFEST.md) - Stop when the user rejects a high-risk action

## How to Use

1. Upload this export directory to GitHub.
2. Give Claw the Raw link for `index.md`, or use individual `MANIFEST.md` links for smaller batches.
3. Save Claw output under `responses/<export_id>/<case_id>/`.
4. Run `python run_agent_eval.py grade-manual --export-id <export_id>`.
