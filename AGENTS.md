# Repository Development Instructions

## Mandatory first step

Before ANY development work in this repository — including planning implementation, editing code, adding features, fixing bugs, changing dependencies, refactoring, or changing architecture — read `PROJECT-DEVELOPMENT-SKILL.md` completely.

Then inspect the current repository and relevant code before making decisions or writing code.

`PROJECT-DEVELOPMENT-SKILL.md` is the primary development source of truth for this project. Do not rely on model/chat memory as a substitute for reading it and inspecting the repository.

## Mandatory final step

After every successful development change:

1. Test and verify the change.
2. Check the resulting repository state.
3. Update `PROJECT-DEVELOPMENT-SKILL.md` so its requirements, actual architecture, repository structure, components, decisions, completed work, problems, and single Main Next Step match reality.

Do not mark unverified work as completed.

## Greenfield constraint

This repository is a new project. Do not import, recreate, infer, or reuse architecture, workflows, agent structures, database structures, integrations, naming, SCOUT / ORBIT / PULSE, AFFLUX, or assumptions from older projects unless the user explicitly requests that specific reuse.

## Agent direction

Hermes Agent is the primary agent for this project. Start with Hermes through CLI and inspect existing Hermes capabilities before creating additional agent infrastructure.
