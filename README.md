# Usina Editorial

Shared editorial skill for Usina de Justicia. GitHub is intended to be the source of truth; each supported agent can consume the same skill directory without duplicating its editorial rules.

## What it does

Transforms raw material (text, PDFs, links, interviews, images, datasets, or mixed sources) into a publication-ready WordPress package for Usina de Justicia. It reads supporting material, enriches only with verifiable information, keeps a victim-centered editorial stance, adapts structure to the content type, and surfaces an editorial alert only when human review is genuinely needed.

The skill does not publish to WordPress and does not modify the website repository.

## Repository layout

- `SKILL.md`: core workflow and non-negotiable editorial rules.
- `references/site-contract.md`: current WordPress/frontend boundary and categories.
- `references/content-types.md`: adaptive article patterns.
- `references/research-and-sourcing.md`: research, verification, source hierarchy, privacy, and media-framing rules.
- `references/output-contract.md`: default copy-ready WordPress deliverable.
- `references/examples.md`: behavioral examples, not rigid templates.
- `agents/openai.yaml`: OpenAI skill metadata.

## Claude Code

Clone this repository directly into a Claude Code skill directory:

```bash
git clone https://github.com/UsinaDeJusticia/usina-editorial.git ~/.claude/skills/usina-editorial
```

For a project-only installation, clone it at `.claude/skills/usina-editorial` inside that project.

## OpenCode

OpenCode can discover Claude-compatible skill directories. The same clone under `~/.claude/skills/usina-editorial` can therefore be shared by Claude Code and OpenCode. Alternatively, clone it under `~/.config/opencode/skills/usina-editorial`.

## Hermes

Clone the repository to a stable local directory and add its parent skill directory to `skills.external_dirs` in the Hermes configuration. If the shared checkout must remain authoritative, keep it read-only to Hermes and update it through Git.

## Codex

Codex can install a skill from a GitHub repository/path with its skill installer. Point the installer at this repository once it is published.

## ChatGPT

Package the skill directory as `skill.zip` with the OpenAI skill tooling and install that archive in ChatGPT. The GitHub repository remains the editable source of truth; regenerate the archive when the skill changes.

## Maintenance rule

Do not copy the editorial instructions into separate Claude/OpenCode/Hermes variants. Update this repository first, then refresh each local installation from Git. Platform-specific installation notes belong in this README, not in `SKILL.md`.
