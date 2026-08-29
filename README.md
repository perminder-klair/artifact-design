# Artifact Design

A portable Agent Skill for designing polished, subject-specific websites, reports, dashboards, demos, documents, and interactive tools.

The core design guidance is agent-neutral. Runtime-specific behavior is isolated in references for Claude Artifacts and web publishing.

## Install

Install it with the open skills CLI:

```sh
npx skills add perminder-klair/artifact-design --skill artifact-design
```

Install globally for a specific agent:

```sh
npx skills add perminder-klair/artifact-design --skill artifact-design -g -a codex
```

Use it without installing:

```sh
npx skills use perminder-klair/artifact-design --skill artifact-design
```

The CLI supports Claude Code, Codex, Cursor, Gemini, OpenCode, GitHub Copilot, Windsurf, and other Agent Skills-compatible clients.

## Structure

```text
artifact-design/
├── SKILL.md
└── references/
    ├── claude-artifacts.md
    └── publishing.md
```

- `SKILL.md` contains the portable design workflow.
- `references/publishing.md` selects and verifies here.now or Vercel deployment.
- `references/claude-artifacts.md` contains only Claude Artifact runtime constraints.

## Publishing on skills.sh

skills.sh indexes skills from public Git repositories; there is no separate skill bundle to upload.

1. Run `npx skills add perminder-klair/artifact-design --skill artifact-design` to confirm discovery and installation.
2. Open `https://skills.sh/perminder-klair/artifact-design/artifact-design` after the directory indexes the repository.

The root-level `SKILL.md` is intentionally valid as a standalone skill repository. Keep `name: artifact-design` stable so updates resolve to the same installed skill.

## Publishing generated artifacts

The skill defaults to here.now for immediate static sharing and uses Vercel for framework builds or durable production workflows. It verifies the live deployment and reports whether the result is temporary, preview, or production.
