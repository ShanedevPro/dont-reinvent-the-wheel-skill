# Anti-Wheel Skill

Anti-Wheel Skill is a small agent skill that asks an AI coding agent to check mature existing solutions before writing custom software.

The goal is simple: avoid reinventing the wheel when an open-source project, commercial product, official API, internal tool, or ecosystem-standard library already solves the problem well enough.

Suggested repository name:

```text
anti-wheel-skill
```

## What Is Included

- `skills/reuse-before-build/SKILL.md`: official English skill content for agents that support `SKILL.md`.
- `README.zh-CN.md`: Chinese overview for Chinese-speaking developers.
- `docs/skill-reference.zh-CN.md`: Chinese reference explaining the principle, workflow, and expected output.
- `docs/publish-to-github.zh-CN.md`: short Chinese guide for publishing this package to a private GitHub repository.

## When To Use

Use this skill before starting new software work that may duplicate an existing solution, including features, tools, libraries, integrations, services, UI components, workflows, or automation.

## Core Rule

Prefer the simplest sufficient mature solution. Build custom code only when reuse, adaptation, or buying is not a good fit.

## Install

This is a personal skill (drop-in `SKILL.md`), not a Claude Code plugin. If you want plugin-style installation (e.g. `/plugin install`), additional packaging is needed.

Copy `skills/reuse-before-build` into the skills directory used by your AI coding agent.

Examples:

```sh
# Codex-style layout
mkdir -p "${CODEX_HOME:-$HOME/.codex}/skills"
cp -R skills/reuse-before-build "${CODEX_HOME:-$HOME/.codex}/skills/reuse-before-build"

# Claude Code-style layout
mkdir -p "$HOME/.claude/skills"
cp -R skills/reuse-before-build "$HOME/.claude/skills/reuse-before-build"
```

If your agent uses a different skills directory, keep the same folder structure and copy the `reuse-before-build` folder there.
