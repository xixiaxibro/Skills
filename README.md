# journal-workflow

A Codex skill for turning raw daily reflections into structured journal entries and an easy-to-read mood narrative.

## What this skill does

- Captures free-form reflections without losing the original meaning
- Structures entries into a consistent daily format
- Preserves context (`what happened`) before emotion (`how I felt`)
- Extracts reusable lessons and 1-3 concrete next actions
- Supports an offline visualization workflow for journal review

## Repository structure

```text
journal-workflow/
├── SKILL.md
├── agents/
│   └── openai.yaml
├── assets/
│   └── journal-template.md
└── references/
    └── best-practices.md
```

## How to use

1. Put this skill folder in your Codex skills directory (or keep it in your local skills repo).
2. Trigger it with requests like:
   - "帮我整理今天的感悟并存成日记"
   - "Summarize today’s reflection and keep emotional context"
   - "把刚才的日记优化成可执行的下一步"
3. Follow the structure in `assets/journal-template.md`.
4. Apply quality checks from `references/best-practices.md`.

## Output standard

Each entry should include:

- 今日关键词
- 今天发生了什么
- 我的感受
- 我学到的
- 接下来想做的 1-3 件小事
- 给未来自己的话

## Notes

- `SKILL.md` is the source of behavior and triggering instructions.
- `agents/openai.yaml` contains UI metadata for skill surfaces.
- Keep Markdown as the source of truth; treat visualization as a rendering layer.
