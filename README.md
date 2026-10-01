# lithuanian-writing

An AI-agent skill for writing and proofreading Lithuanian: spelling, commas and punctuation,
capitalisation, number/date formatting, foreign names, calques and common errors, and stress marks on request.

The rules are condensed from official VLKK (State Commission of the Lithuanian Language) norms. Each
condensed reference has the full official text next to it, so the agent can look up an edge case
instead of guessing.

## Structure

```
skills/lithuanian-writing/
├── SKILL.md                  # entry point: routing table, top errors, scope
├── references/               # condensed rules, one topic per file; load only what the text needs
│   ├── rasyba-balsiai-priebalsiai.md   # i/y, u/ū, nosinės, consonants
│   ├── kartu-atskirai.md               # compounds, together/apart, ne-
│   ├── didziosios-raides.md            # capitalisation, proper names
│   ├── skyrybos-zenklai.md             # dashes, quotes, brackets, numbers, dates, money
│   ├── skyryba-kableliai.md            # commas: clauses, participles, asides, lists, direct speech
│   ├── svetimvardziai-santrumpos.md    # foreign names, abbreviations
│   ├── daznos-klaidos.md               # calques, wrong cases/prepositions
│   ├── humanizavimas-lt.md             # translated/AI Lithuanian → natural Lithuanian
│   └── kirciavimas.md                  # stress marks (only on request)
└── sources/                  # full official VLKK texts for grep lookup
    ├── skyrybos-taisykles-2019.md      # punctuation rules, 2019 resolution, all examples
    └── klaidu-sarasas/                 # list of major language errors, 9 categories
```

See [SOURCES.md](SOURCES.md) for where everything comes from, plus dictionaries and tools.

## Install

**Claude Code**: copy or symlink the skill folder into your skills directory.

```sh
git clone https://github.com/lapius/lithuanian-writing.git
ln -s "$PWD/lithuanian-writing/skills/lithuanian-writing" ~/.claude/skills/lithuanian-writing
```

It loads automatically when you write or proofread Lithuanian, or you can invoke it with `/lithuanian-writing`.

**Other agents** (Cursor, Codex, opencode, a plain system prompt): point the agent at
`skills/lithuanian-writing/SKILL.md` and let it read the references it routes to. The files are plain
Markdown and contain nothing agent-specific.

## Design notes

- **Router, not a dump.** `SKILL.md` is an index. The agent loads one or two references per text, not all
  ~1 500 lines.
- **Optional is not wrong.** The 2019 punctuation rules make many commas optional, and any permitted
  variant is correct. The comma reference marks each case ✔ mandatory / ◐ optional / ✘ none, so a
  proofread does not "fix" correct text.
- **Cite the rule.** Corrections name the rule or official list item, so a human can check them.

## License

The skill text (`SKILL.md`, `references/`) is MIT. The `sources/` folder holds official VLKK normative
texts, which are not subject to copyright under Lithuanian law (Autorių teisių ir gretutinių teisių
įstatymas, art. 5). They are reproduced unchanged, with their source URLs.
