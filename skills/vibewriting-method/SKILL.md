---
name: vibewriting-method
description: The core vibewriting process for any content-creation task (emails, memos, posts, articles, outreach, scripts). Use whenever the user asks you to write, draft, or rework strategic content. Breaks the task down, asks clarifying questions, generates and critiques multiple options, keeps a working-memory plan, and grounds output in bundled frameworks.
---

# The vibewriting method

Apply this process to every content-creation task. It exists to stop generic, inconsistent, or "salesy" output by forcing structured thinking grounded in real methodologies.

## Strict process

1. **Break the task into smaller steps** before writing anything.
2. **Ask clarifying questions. Do not assume.** Use the guidance in the bundled frameworks and any task-specific skill (e.g. `email-writing`, `decision-memo`) to know what to ask.
3. **Build a decision criteria** for choosing the best option, weighted against the user's objective.
4. **Generate one option → wait → critique it → rewrite it. Then generate at least two more options → critique and rewrite each.**
5. **Choose the best option** against the weighted criteria and the user's objective.

## Working memory

Maintain a plan file for any multi-step project, so state survives across sessions:

- Location: `docs/working-memory/{feature}/.plan` in the **user's** project, where `{feature}` names the piece of work.
- **Check the `.plan` before starting any work.** Read its Progress History section for prior context.
- Output plan updates before starting, and update the `.plan` as you go.
- Use `${CLAUDE_PLUGIN_ROOT}/templates/memo-task-plan-template.md` as the structure for a new plan.

## Grounding

- Read the relevant files in `${CLAUDE_PLUGIN_ROOT}/frameworks/` before drafting, and cite which principles you applied.
- Reference `${CLAUDE_PLUGIN_ROOT}/templates/` for output structure.

## Mandatory rules

1. Always update the `.plan` file.
2. **Always run a command to get the current date and time — never hallucinate it** (e.g. `date "+%Y-%m-%d %H:%M"`).
3. Be surgical when editing existing content — change only what's necessary.
4. Be cautious deleting files; ask permission if unsure.
