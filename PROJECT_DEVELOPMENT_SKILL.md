# PROJECT DEVELOPMENT SKILL

## Purpose
This file is the development rulebook and current-state record for this repository.
Read it before planning, coding, modifying, debugging, or reviewing the project.

## Project
- Repository: `fla02054-hub/shopee-affiliate-agent`
- Status: Greenfield / starting from zero
- Primary AI agent: Hermes Agent
- Initial interface: CLI

## Development Rules
1. Treat this as a completely new project.
2. Do not copy, reuse, mirror, or derive architecture, workflows, agent names, module names, or assumptions from any previous project unless the user explicitly requests it.
3. Start with the simplest working design that satisfies the current requirement.
4. Add systems, dependencies, abstractions, services, and automation only when they are actually needed.
5. Every added feature must have a clear purpose and should be testable.
6. Do not create speculative architecture for future features.
7. Before making changes, read this file and inspect the current repository/code first.
8. Avoid duplicate responsibilities and duplicate implementations.
9. Never hard-code secrets, tokens, passwords, cookies, or API keys.
10. Develop incrementally: make one clear step work before expanding the system.
11. Update this file after meaningful development changes so it reflects the real project, not a future design.

## What This File Should Record
Keep this document short. Record only:
- Current requirements
- Actual current structure
- Completed work
- Important decisions already made
- Current problems/blockers
- One clear next step

Do not turn this file into a large architecture document or speculative roadmap.

## Current Requirements
- Build a new Shopee Affiliate project from zero.
- Use Hermes Agent as the AI agent.
- Start by operating Hermes Agent through CLI.
- Establish the project incrementally before adding broader automation.

## Current Structure
- `PROJECT_DEVELOPMENT_SKILL.md` — development rules and current project state.

## Completed
- Confirmed the repository is empty and writable.
- Established this greenfield development skill.

## Decisions
- Hermes Agent is the primary AI agent.
- CLI is the first interface.
- No architecture or workflow from older projects will be introduced automatically.

## Current Problems / Blockers
- None identified yet.

## Next Step
Define and implement the smallest runnable CLI project foundation needed to invoke Hermes Agent, based only on the requirements of this new project.
