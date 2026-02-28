---
name: journal-workflow
description: Capture, structure, and present personal journal reflections as reusable Markdown entries plus an offline visual mood board. Use when the user asks to record daily insights, organize raw thoughts, preserve emotional context, generate next actions, or refresh/open local journal visualization files.
---

# Journal Workflow

Use this workflow to turn free-form reflections into clear daily entries and visible emotional trends.

## Execute Workflow

1. Capture raw reflection first.
Collect the user's original text without forcing structure in the first pass.

2. Structure the entry with the template.
Use [assets/journal-template.md](assets/journal-template.md) sections and fill only non-empty items.

3. Preserve emotional context.
Write `今天发生了什么` before `我的感受`. Ensure readers can answer "why this emotion happened" from the entry itself.

4. Distill insights and actions.
Extract 1-3 concrete next actions with observable outcomes. Avoid vague goals.

5. Keep source of truth in Markdown.
Store each day as `journals/YYYY-MM-DD.md`. Treat visualization as a render layer, not the primary storage.

6. Refresh offline visualization.
Run:
```powershell
./journals/update-manifest.ps1
./journals/open-journals.cmd
```

## Apply Output Standard

Require these sections in every entry:
- `今日关键词`
- `今天发生了什么`
- `我的感受`
- `我学到的`
- `接下来想做的 1-3 件小事`
- `给未来自己的话`

Prioritize narrative completeness over short summaries. If the user says the result feels empty, expand the event narrative first.

## Use References

- Read [references/best-practices.md](references/best-practices.md) for quality checks and rewrite rules.
