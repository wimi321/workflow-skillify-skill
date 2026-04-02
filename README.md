# Workflow Skillify

[![Repo](https://img.shields.io/badge/github-workflow-skillify-skill-181717?logo=github)](https://github.com/wimi321/workflow-skillify-skill)
[![License](https://img.shields.io/badge/license-MIT-green.svg)](./LICENSE)
[![Collection](https://img.shields.io/badge/collection-claude--code--skills--extract-blue)](https://github.com/wimi321/claude-code-skills-extract)

Use when a successful session or repeatable process should be captured as a reusable skill with steps, arguments, and invocation guidance.

English | [简体中文](./README.zh-CN.md)

## Why This Skill Exists

Workflow Skillify packages a reusable Claude Code workflow as a standalone public skill repository. It is designed for agent teams that want a well-documented, installable, and maintainable capability rather than an internal prompt fragment.

## Highlights

- Focused, reusable workflow with a clear trigger boundary
- Standalone skill root that works well in agent workspaces
- Agent metadata in `agents/openai.yaml`
- Public provenance back to the extracted Claude Code source
- Bilingual documentation for English and Chinese readers

## What It Is Good At

- Turn a session into a reusable skill
- Running the workflow described in `SKILL.md` with explicit boundaries
- Producing repeatable outputs for operators and agent runtimes

## Example Requests

- Turn this successful session into a reusable skill.
- Capture the process we just followed as a formal skill.

## Workflow

1. Summarize the session and extract user-visible goals, corrections, and constraints.
2. Identify inputs, outputs, artifacts, and success criteria.
3. Interview for missing details only where the workflow is ambiguous.
4. Write a clean `SKILL.md` with trigger conditions, steps, and optional arguments.
5. Save the skill in the appropriate repo-level or personal location.

## Inputs

- Session history
- User corrections
- Desired save scope

## Outputs

- Reusable SKILL.md
- Trigger and argument guidance

## Success Criteria

- The resulting skill captures the real workflow.
- User corrections are preserved as rules.
- The saved skill is specific and reusable.

## Non-Goals

- Over-interviewing simple workflows
- Saving a vague process with no triggers or success criteria

## Installation

### Use as a standalone skill

Clone this repository and place the repository root in a compatible skill directory.

### Use from a larger collection

This skill is also included in the parent collection:

- [claude-code-skills-extract](https://github.com/wimi321/claude-code-skills-extract)

## Repository Layout

- `SKILL.md`: canonical skill instructions
- `README.md`: English project overview
- `README.zh-CN.md`: Simplified Chinese project overview
- `agents/openai.yaml`: UI-facing metadata for agent runtimes
- `references/`: provenance and support notes
- `LICENSE`: repository license

## Provenance

Derived from `src/skills/bundled/skillify.ts`.

## Related Projects

- Parent collection: [claude-code-skills-extract](https://github.com/wimi321/claude-code-skills-extract)
- GitHub repository: [workflow-skillify-skill](https://github.com/wimi321/workflow-skillify-skill)
