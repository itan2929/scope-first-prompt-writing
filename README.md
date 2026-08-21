# Scope-First Prompt Writing

Codex Skill for writing implementation prompts with a clear feature boundary.

It combines concise technical-writing practices with two focused rules: separate release context from the current Beta, and rewrite ordinary negative scope statements as positive, testable boundaries.

## Contents

- `SKILL.md`: skill instructions
- `references/negative-to-positive.md`: wording transformations and review guide
- `agents/openai.yaml`: Codex UI metadata

## Validate

```bash
python3 /Users/katada/.codex/skills/.system/skill-creator/scripts/quick_validate.py .
```
