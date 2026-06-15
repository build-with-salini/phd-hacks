# translate-bm-academic

A Claude Code skill that translates English academic documents into formal, high-quality Bahasa Malaysia following Dewan Bahasa dan Pustaka (DBP) standards.

## What It Does

- Translates research papers, journal articles, theses, and other scholarly documents from English into academic Bahasa Malaysia
- Preserves conceptual meaning, academic argumentation, and rhetorical nuance — not a word-for-word translation
- Uses only DBP-approved terminology
- Outputs a full translation + a comprehensive glossary table of key terms

## Output Format

**Bahagian 1 — Terjemahan**
The complete translated document in academic Bahasa Malaysia, with all headings, paragraphs, and citations intact.

**Bahagian 2 — Jadual Glosari**
A table mapping every key English academic/technical term to its precise Bahasa Malaysia equivalent.

## Installation

Copy `SKILL.md` into your Claude Code skills directory:

```bash
mkdir -p ~/.claude/skills/translate-bm-academic
cp SKILL.md ~/.claude/skills/translate-bm-academic/SKILL.md
```

## Usage

In any Claude Code session:

1. Paste your English academic text into the chat (or share a file path)
2. Type `/translate-bm-academic`

## Guidelines Applied

| Guideline | Description |
|---|---|
| Academic Tone | Formal scholarly BM suitable for high-impact journals |
| Conceptual Fidelity | Meaning, metaphors, and arguments preserved — not literal translation |
| DBP Terminology | Standardized terms approved by Dewan Bahasa dan Pustaka |
| Structural Fidelity | Headings, lists, citations, and paragraph structure preserved |
| Consistency | Key term translations are uniform throughout the document |

## Author

Salini A/P Anbalagan — PhD Researcher, Universiti Kebangsaan Malaysia (UKM)
