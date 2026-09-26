# Public API list guide

Read `.github/CONTRIBUTING.md` before editing `README.md`. Keep the five-column API/Description/Auth/HTTPS/CORS format, accepted value vocabulary, concise descriptions, alphabetical placement, and duplicate rules. Preserve the contribution limits (five entries, three sections) and cleanup/bulk-label exceptions; ordinary contributions are append-only under the existing policy.

`.github/scripts/validate_pr.py` validates a diff; it accepts `DIFF_FILE`, otherwise derives a Git base using `GITHUB_BASE_REF` (default master). Set the intended existing base/diff explicitly before running it and inspect `validation_result.json`; a wrong base is not a valid PR check. The workflows use Python 3.12. `build_api.py` transforms the README into generated API/Pages output using `README_PATH` and `OUTPUT_DIR`. There is no application package/test/typecheck command.

For prose edits, check changed rows, links, section order, and whitespace. Inspect helper effects before execution: `sort_entries.py --fix` rewrites the list, and link-check workflows make broad network calls and may create issues. Don't run those as a routine instruction check or treat a reachable homepage as proof every API contract works. Generated output should follow the checked-in workflow, not manual edits.

## Completing work

Carry the authorized change through the relevant checks and repair failures it causes. Make routine, reversible implementation choices using existing patterns; ask only when missing information, a material product decision, or an authorization boundary prevents the next step. Existing authorization remains valid within its scope. If blocked, name the exact action and missing prerequisite, retain concise evidence, and continue independent work.

Choose verification proportional to the change. For instructions or prose, inspect changed paths, links, and local instruction precedence and run `git diff --check -- <changed-paths>`; don't install dependencies or run the application solely for a prose edit. For behavior changes, exercise the affected behavior and applicable checks below, then broaden only for failures or unresolved risk. Report files changed, checks actually run and their results, commands only inspected, and remaining limitations. A build or source inspection alone does not prove runtime behavior. Continue through already-authorized follow-through; stop at explicit review checkpoints or boundaries requiring new authorization.
