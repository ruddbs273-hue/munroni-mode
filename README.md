# munroni-mode

[한국어](README.ko.md)

A working-style skill for [Claude Code](https://claude.com/claude-code). With it on, Claude puts the answer first, finishes the job without check-ins, asks only before steps that are hard to undo, checks its own work, and keeps screens and writing plain.

## Before and after

**Reporting a finished change**

> **Without:** I've updated the button color. Would you like me to update the hover state as well? I can also run the tests if you'd like.
>
> **With:** Done. The same button appeared in 3 places, and all 3 are updated. Type check and lint pass. In the browser, look at the Save button on /settings. Not committed.

**A fork in the road**

> **Without:** There are two ways to store this: a new column or a JSON field. Which would you prefer?
>
> **With:** Added a new column (migration V12, safe to run twice) and finished the screen. A JSON field would also work. Switching later takes one migration.

**A vague complaint: "this page looks empty"**

> **Without:** Sure! I've redesigned the page with a hero banner, feature cards and a gradient background.
>
> **With:** I found similar real products and put three mockups with different directions in one file, now open in your browser. I recommend B. No code changed yet.

## Who it's for

- For you if you want to hand off a job, get it back finished and checked, and be asked only about commits, pushes, deploys, deletions and outgoing mail.
- Not for you if you want to approve each step before Claude moves on.

## What it covers

| Section | Key rules |
|---|---|
| Replies | Answer in the first line, in plain words. Decisions come as numbered options with one recommendation. |
| Autonomy | No mid-task check-ins. Ask only before steps that are hard to undo. Do only what was asked. |
| Delegation | Run big jobs as parallel subagents. Assume other sessions share the repo and never revert their changes. |
| Verification | Tests, type check and lint. Open what was made. Never make up results. |
| Working method | A specific remark gets only that fix. A vague complaint gets three mockups first. Fix the same pattern across the app. |
| Code | One shared component for repeated UI. Never regenerate a file the user edited. Fake values only in tests and examples. |
| Notes | Write down decisions and leftovers so the next session can continue. |

Two reference files are read only when needed:

- `references/ui-defaults.md`, before building screens: no decoration, table alignment, what red means, dialog rules, input helpers, phone layouts
- `references/writing.md`, before writing documents: no AI tells, plain words for outside readers, one-page summaries, a template for handoff prompts

## Editions

| Skill | Rules written in |
|---|---|
| `munroni-mode` | English (default) |
| `munroni-mode-ko` | Korean |

The rules are the same in both. Either edition replies in the language you write in.

## Install

As a plugin:

```
/plugin marketplace add ruddbs273-hue/munroni-mode
/plugin install munroni@munroni
```

Then type `/munroni:munroni-mode` (or `/munroni:munroni-mode-ko`).

Or copy `skills/munroni-mode` (or `skills/munroni-mode-ko`) into `~/.claude/skills/` and type `/munroni-mode`.

## Notes

- The skill turns on only when you type its command (`disable-model-invocation: true`). Claude never loads it on its own.
- These are one person's preferences. Fork it, change the rules, and rename it to make it yours.

## License

[MIT](LICENSE)
