# PhD Research Skills for Claude

A collection of [Claude Skills](https://docs.claude.com/en/docs/agents-and-tools/agent-skills) designed to help PhD researchers with common academic workflows — writing, presenting, and managing research.

> I'm not fully certain of the exact current folder/packaging conventions Claude Skills expect, since this may have changed since my knowledge cutoff (August 2025). Before publishing, you may want to verify the latest format against [Anthropic's documentation](https://docs.claude.com) or `support.claude.com`.

## What's in this repo

Each skill lives in its own top-level folder and contains a `SKILL.md` file (plus optional supporting scripts, templates, or reference docs).

| Skill | Description |
|---|---|
| `phd-presentation-architect/` | Helps structure and design academic presentations (conference talks, defenses, lab meetings). |
| *(add more here as you create them)* | |

## Repository structure

```
.
├── README.md
├── phd-presentation-architect/
│   ├── SKILL.md
│   └── (optional: assets/, references/, scripts/)
├── <next-skill>/
│   └── SKILL.md
└── ...
```

Each skill folder is self-contained and can be used independently.

## Using these skills

### In Claude.ai
1. Go to **Settings > Capabilities** (or the equivalent skills section).
2. Upload the relevant skill folder (or a `.skill` package, if supported).
3. Claude will automatically reference the skill when your request matches its description.

> I'm not certain about the exact upload steps or whether `.skill` packaging is required in the current version of Claude.ai — please check the official docs to confirm, as UI details can change.

### In Claude Code / API
Place the skill folder in your project's skills directory (commonly `.claude/skills/` or similar — verify against current docs) so Claude can discover and load it automatically.

## Contributing a new skill

1. **Create a folder** named after your skill, using lowercase-with-hyphens (e.g. `lit-review-assistant`).
2. **Add a `SKILL.md`** with YAML frontmatter:
   ```yaml
   ---
   name: your-skill-name
   description: What the skill does and when Claude should use it. Be specific about trigger phrases and contexts — this is the main mechanism Claude uses to decide when to apply the skill.
   ---
   ```
3. **Write the body** in Markdown: step-by-step guidance, conventions, examples, and templates.
4. **Keep it focused**: one skill = one well-defined workflow. If it's getting long (>500 lines), split supporting detail into a `references/` subfolder and point to it from `SKILL.md`.
5. **Add bundled resources** (optional):
   - `scripts/` — executable helper code
   - `references/` — supplementary docs loaded as needed
   - `assets/` — templates, images, or files used in output
6. **Update the table above** with your new skill and a one-line description.
7. **Test it**: try a few realistic prompts with the skill loaded and confirm Claude follows the intended workflow.

### Style guidelines for SKILL.md files
- Write the `description` field to clearly state *what* the skill does and *when* to use it — Claude relies on this to decide whether to consult the skill.
- Use plain, direct instructions in the body — avoid vague guidance.
- Where possible, include concrete examples (sample outputs, templates, phrasing).
- Keep academic-discipline assumptions explicit if a skill is field-specific (e.g. STEM vs. humanities conventions for citations or presentation style).

## Planned / suggested skills

Some ideas for skills that would fit this collection (feel free to claim one):

- Literature review organizer
- Thesis chapter structuring
- Conference abstract writer
- Peer review response drafter
- Research statement / grant proposal helper
- Citation and reference formatting checker
- Figure/table caption writer

## License

*(Add a license — e.g. MIT — if you intend this to be open source.)*

## Disclaimer

These skills are templates and prompting aids; they don't replace your own academic judgment, your institution's formatting requirements, or your advisor's feedback. Always review outputs carefully, especially for factual claims, citations, and statistics — Claude can make mistakes.
