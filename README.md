# munroni-mode

[한국어](README.ko.md)

A working-style skill for [Claude Code](https://claude.com/claude-code). It tells Claude how I want work done:

- Put the answer in the first line, in plain words.
- Finish a delegated job without stopping to ask. Ask only before steps that are hard to undo (commits, pushes, deploys, deleting files, mail that goes out).
- Do only what was asked. No extra fields, buttons or files.
- Verify with tests, the type check and lint. Never make up results.
- Open the files and mockups it made instead of pointing at paths.
- Keep screens plain, without decoration, and keep the structure visible.
- Write without AI tells.

## Editions

| Skill | Rules written in |
|---|---|
| `munroni-mode` | English (default) |
| `munroni-mode-ko` | Korean |

The rules are the same in both. Either edition replies in the language you write in.

## What's inside

```
skills/munroni-mode/
├─ SKILL.md                  replies, autonomy, delegation, verification, working method, code, notes
└─ references/
   ├─ ui-defaults.md         read before building screens and mockups
   └─ writing.md             read before writing documents, slides, outside text and handoff prompts
```

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
