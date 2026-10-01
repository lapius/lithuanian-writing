# lithuanian-writing

**[Lietuviškai](#lietuviškai) · [English](#english)**

Note for English readers: `SKILL.md` (agent instructions) is in English; the rule files in `references/`
are in Lithuanian, because the rules and their terms are Lithuanian and match the official VLKK texts in
`sources/` word for word.

## Lietuviškai

Dirbtinio intelekto agentams skirtas įgūdis lietuviškam tekstui rašyti ir taisyti: rašyba, kableliai ir
kita skyryba, didžiosios raidės, skaičių ir datų rašymas, svetimvardžiai, kalkės ir dažnos klaidos,
o paprašius – ir kirčiavimas.

Taisyklės sutrauktos iš oficialių Valstybinės lietuvių kalbos komisijos (VLKK) normų. Šalia sutrauktų
taisyklių pateikiamas ir visas oficialus tekstas, todėl agentas keblų atvejį gali pasitikrinti, o ne
spėlioti.

### Sandara

```
skills/lithuanian-writing/
├── SKILL.md                  # pradžios taškas: rodyklė, dažniausios klaidos, apimtis
├── references/               # sutrauktos taisyklės, viena tema – vienas failas; įkeliama tik tai, ko reikia
│   ├── rasyba-balsiai-priebalsiai.md   # i / y, u / ū, nosinės, priebalsiai
│   ├── kartu-atskirai.md               # sudurtiniai žodžiai, kartu ar atskirai, ne-
│   ├── didziosios-raides.md            # didžiosios raidės, tikriniai vardai
│   ├── skyrybos-zenklai.md             # brūkšniai, kabutės, skliaustai, skaičiai, datos, pinigai
│   ├── skyryba-kableliai.md            # kableliai: šalutiniai sakiniai, aplinkybės, įterpiniai, tiesioginė kalba
│   ├── svetimvardziai-santrumpos.md    # svetimvardžiai, santrumpos
│   ├── daznos-klaidos.md               # kalkės, netinkami linksniai ir prielinksniai
│   ├── humanizavimas-lt.md             # verstinis ar DI tekstas → natūrali lietuvių kalba
│   └── kirciavimas.md                  # kirčiavimas (tik paprašius)
└── sources/                  # visi oficialūs VLKK tekstai paieškai
    ├── skyrybos-taisykles-2019.md      # 2019 m. skyrybos taisyklės su visais pavyzdžiais
    └── klaidu-sarasas/                 # didžiųjų kalbos klaidų sąrašas, 9 sritys
```

Iš kur paimta medžiaga, taip pat žodynai ir įrankiai – [SOURCES.md](SOURCES.md).

### Diegimas

**Claude Code**: nukopijuok arba susiek (symlink) įgūdžio aplanką su savo įgūdžių katalogu.

```sh
git clone https://github.com/lapius/lithuanian-writing.git
ln -s "$PWD/lithuanian-writing/skills/lithuanian-writing" ~/.claude/skills/lithuanian-writing
```

Įgūdis įsijungia savaime, kai rašai ar taisai lietuvišką tekstą. Galima jį iškviesti ir komanda
`/lithuanian-writing`.

**Kiti agentai** (Cursor, Codex, opencode, paprastas sisteminis raginimas): nurodyk agentui
`skills/lithuanian-writing/SKILL.md` ir leisk jam skaityti failus, į kuriuos ten nukreipiama. Tai paprasti
Markdown failai, nepritaikyti kuriam nors vienam agentui.

### Principai

- **Rodyklė, ne visas sąvadas.** `SKILL.md` – tik turinys. Agentas vienam tekstui įkelia vieną ar du
  failus, o ne visas ~1 500 eilučių.
- **Pasirenkamas ženklas nėra klaida.** Pagal 2019 m. skyrybos taisykles daug kablelių yra pasirenkami, ir
  bet kuris leidžiamas variantas laikomas taisyklingu. Kablelių faile kiekvienas atvejis pažymėtas:
  ✔ privaloma, ◐ pasirenkama, ✘ neskiriama. Taip taisant nesugadinamas jau taisyklingas tekstas.
- **Nurodoma taisyklė.** Prie kiekvienos pataisos nurodoma taisyklė ar oficialaus sąrašo punktas, kad
  žmogus galėtų ją patikrinti.

### Licencija

Įgūdžio tekstas (`SKILL.md`, `references/`) platinamas pagal MIT licenciją. Aplanke `sources/` – oficialūs
norminiai VLKK tekstai, kurie pagal Lietuvos Respublikos autorių teisių ir gretutinių teisių įstatymo
5 straipsnį nėra autorių teisių objektas. Jie pateikti nekeisti, nurodant šaltinio adresą.

---

## English

An AI-agent skill for writing and proofreading Lithuanian: spelling, commas and punctuation,
capitalisation, number/date formatting, foreign names, calques and common errors, and stress marks on request.

The rules are condensed from official VLKK (State Commission of the Lithuanian Language) norms. Each
condensed reference has the full official text next to it, so the agent can look up an edge case
instead of guessing.

### Structure

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

See [SOURCES.md](SOURCES.md) (in Lithuanian) for where everything comes from, plus dictionaries and tools.

### Install

**Claude Code**: copy or symlink the skill folder into your skills directory.

```sh
git clone https://github.com/lapius/lithuanian-writing.git
ln -s "$PWD/lithuanian-writing/skills/lithuanian-writing" ~/.claude/skills/lithuanian-writing
```

It loads automatically when you write or proofread Lithuanian, or you can invoke it with `/lithuanian-writing`.

**Other agents** (Cursor, Codex, opencode, a plain system prompt): point the agent at
`skills/lithuanian-writing/SKILL.md` and let it read the references it routes to. The files are plain
Markdown and contain nothing agent-specific.

### Design notes

- **Router, not a dump.** `SKILL.md` is an index. The agent loads one or two references per text, not all
  ~1 500 lines.
- **Optional is not wrong.** The 2019 punctuation rules make many commas optional, and any permitted
  variant is correct. The comma reference marks each case ✔ mandatory / ◐ optional / ✘ none, so a
  proofread does not "fix" correct text.
- **Cite the rule.** Corrections name the rule or official list item, so a human can check them.

### License

The skill text (`SKILL.md`, `references/`) is MIT. The `sources/` folder holds official VLKK normative
texts, which are not subject to copyright under Lithuanian law (Autorių teisių ir gretutinių teisių
įstatymas, art. 5). They are reproduced unchanged, with their source URLs.
