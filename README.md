# Shopee Affiliate Agent

Greenfield Shopee Affiliate project using **Hermes Agent** as the primary agent, starting with a CLI-first workflow.

## Current stage

The project is intentionally minimal. The first milestone is to establish and verify Hermes Agent itself before adding Shopee-specific application logic.

## Prerequisite: Hermes Agent

Hermes is an external CLI and is not vendored into this repository.

Install it using the official Hermes Agent installation instructions for your operating system, then verify:

```bash
hermes --version
hermes doctor
```

Configure a model/provider:

```bash
hermes setup
```

or choose one explicitly:

```bash
hermes model
```

## First project smoke test

From the repository root, run:

```bash
hermes chat --oneshot -q "Read AGENTS.md and PROJECT-DEVELOPMENT-SKILL.md. Reply with the repository name, the primary agent, and the current Main Next Step only."
```

A successful response confirms the minimum project foundation:

1. Hermes CLI launches.
2. Hermes can run a one-shot prompt.
3. Hermes sees this repository as its workspace.
4. Repository instructions are available to the agent.

Do not add Shopee automation until this smoke test has been run successfully in the actual development environment.

## Repository rules

`PROJECT-DEVELOPMENT-SKILL.md` is the primary development source of truth. `AGENTS.md` requires agents to read it and inspect the repository before development.

This is a greenfield project. Do not import architecture or workflows from older projects unless explicitly requested by the user.
