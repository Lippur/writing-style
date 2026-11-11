# writing-style

An agent skill that sets the writing style for all prose: Simplified Technical English (ASD-STE100) at 80%, with British spelling and an impersonal register. Pass 1 removes 26 AI writing tells. Pass 2 applies the sentence structure of STE.

`SKILL.md` is the skill. `references/` holds the detail that the skill loads on demand. `scripts/ste_check.py` is a linter for the measurable rules.

To install it for Claude Code, link the clone into the skills folder:

```bash
ln -s ~/Dev/writing-style ~/.claude/skills/writing-style
```

`LICENSE` and `THIRD_PARTY_NOTICES.md` hold the licence terms.
