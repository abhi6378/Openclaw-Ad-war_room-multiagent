# OpenClaw Ad War Room Multi-Agent

This repository showcases my work building and debugging an OpenClaw-based multi-agent ad review workflow.

The project is designed around a staged pipeline where one ad moves through specialized review roles:

- Creative review
- Strategy review
- Compliance review

## What I worked on

- Designed the orchestrator flow in [AGENTS.md](./AGENTS.md)
- Structured skill-based agent roles under [`skills/`](./skills)
- Improved pipeline safety for sequential execution and exact-stage handoff
- Tuned timeout/session behavior for long-running local model workflows
- Debugged issues around duplicate runs, stale session reuse, and subagent completion handling
- Integrated the workflow with OpenClaw UI and Telegram usage patterns

## Repository goal

This repo is meant to show the workflow design and agent architecture, not a full live OpenClaw home directory dump.

It intentionally excludes:

- secrets and tokens
- live runtime/session files
- local logs
- machine-specific OpenClaw state

## Main files

- [AGENTS.md](./AGENTS.md): orchestration rules for the ad review pipeline
- [`skills/`](./skills): specialized agent skill definitions
- [TOOLS.md](./TOOLS.md): tool-related workspace guidance
- [SOUL.md](./SOUL.md), [IDENTITY.md](./IDENTITY.md), [USER.md](./USER.md): agent behavior and workspace context

## Notes

This is a portfolio and workflow repo built around OpenClaw. Sensitive runtime config such as live `openclaw.json`, logs, session transcripts, and tokens are intentionally not committed.

If you want to run a version of this setup yourself, create your own local OpenClaw instance and add your own sanitized config separately.
