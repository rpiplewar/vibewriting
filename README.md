# vibewriting — a Claude Code plugin

Framework-grounded content creation for Claude Code. Instead of generic, inconsistent, "salesy" output, vibewriting makes Claude **plan the task, generate multiple options, critique them, and ground every draft in your own methodologies** (Gap Selling, Munger's bias checklist, decision frameworks).

Originally a Cursor `.cursor/rules` setup, now packaged as an installable Claude Code plugin.

## Install

```
/plugin marketplace add rpiplewar/vibewriting
/plugin install vibewriting@vibewriting
```

Local development (before pushing):

```
/plugin marketplace add /absolute/path/to/vibewriting
/plugin install vibewriting@vibewriting
```

## What's inside

**Skills** (Claude invokes these automatically based on your task):

| Skill | Triggers on |
|-------|-------------|
| `vibewriting-method` | Any content-creation task — the core plan → options → critique → choose process |
| `email-writing` | Writing or replying to emails |
| `decision-memo` | Decision/strategy memos and recommendations |
| `social-content` | LinkedIn posts and blog articles |

**Bundled frameworks** (`frameworks/`) — the methodologies skills read before drafting:
- `gap_selling.md` — problem-centric communication
- `bias_checklist_munger.md` — cognitive biases to activate / guard against
- `effective-decision-making-framework.md`
- `virtual-videos-questionnaire.md`

**Templates** (`templates/`) — output structures for memos, LinkedIn posts, and blogs, plus `memo-task-plan-template.md` used for working-memory `.plan` files.

## How it works

Just ask Claude to write something (e.g. "draft a cold email to this prospect"). The matching skill fires, reads the relevant frameworks/templates from inside the plugin, and follows the vibewriting method. For multi-step projects it keeps a working-memory plan at `docs/working-memory/{feature}/.plan` in **your** project so state survives across sessions.

## Customize

Edit the files in `frameworks/` and `templates/` to encode your own methodology, then reinstall. Add new skills under `skills/<name>/SKILL.md` — the `description` field is what tells Claude when to use them.
