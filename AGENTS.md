# Guide for agents

This repository is one agent skill. `SKILL.md` loads in every session, so each word in it costs tokens. Follow these rules when you change it.

- Write every file in the style that the skill sets.
- Keep `SKILL.md` to compact tables and rules. Put long entries and examples in `references/`.
- If you add, remove or rename a tell (§) or a rule (S), change `SKILL.md`, the reference file and `scripts/ste_check.py` together.
- Do not copy the ASD-STE100 specification or dictionary. Paraphrase the rules. Cite only single word pairs.
- Keep `LICENSE` and `THIRD_PARTY_NOTICES.md` unchanged.
- Run the checker on each changed Markdown file. Quoted examples of tells cause expected findings.

```bash
python3 scripts/ste_check.py SKILL.md references/*.md
```
