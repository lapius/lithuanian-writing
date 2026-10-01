---
name: lithuanian-writing
description: |
  Taisyklinga ir natūrali lietuvių kalba: rašymas, vertimas į lietuvių kalbą ir teksto taisymas:
  rašyba, skyryba (kableliai), didžiosios raidės, skaičių, datų ir kabučių rašymas, svetimvardžiai,
  dažnos klaidos ir pažodžiui išversti posakiai (kalkės), kirčiavimas (tik paprašius).
  Write correct, natural Lithuanian and check Lithuanian prose for errors. Use whenever writing,
  editing, translating into, or proofreading Lithuanian text: orthography (rašyba), comma placement
  and sentence punctuation (skyryba), capitalisation, number/date/quote formatting, foreign names,
  common mistakes and calques (įtakoti, apjungti, English word order), and accentuation (kirčiavimas)
  rules on request. Acts as a router: load only the reference file(s) relevant to the current text, not
  all of them; full official VLKK texts are in sources/ for grep lookup. Pair with the humanizer skill to
  also remove AI-writing tells.
license: MIT
metadata:
  version: "1.4.1"
  sources: "Lietuvių kalbos rašyba (VLKK, 2022); Lietuvių kalbos skyrybos taisyklės (VLKK 2019, N-8 (178)); VLKK didžiųjų kalbos klaidų sąrašas; VDU tartis.vdu.lt"
---

# Lithuanian writing: correctness + natural style

Write Lithuanian that a careful native editor would pass. This skill is an **index**: the rules live in
`references/`, and you load only the file the current text needs; do not pull them all into context.

## How to use

1. **Writing/translating into Lithuanian.** Draft normally, then run the relevant checks below. If the
   text was translated from English, `references/daznos-klaidos.md` and `references/humanizavimas-lt.md`
   matter most, because that is where translation calques and English word order show up.
2. **Proofreading Lithuanian.** Identify what kinds of tokens the text contains (proper names? numbers
   and dates? quotes? compound words?) and load only the matching reference(s).
3. **Grep the VLKK error list before any Lithuanian text goes out.** Every draft and every revision, not
   only the first pass. For each preposition phrase, pronoun phrase and suspicious verb, run
   `grep -i "<word>" sources/klaidu-sarasas/*.md`. The `references/` files are condensed and miss entries:
   „pas save“ (1.3.15) and „pas mane“ (4.6.1) are only in `sources/`. Proofreading from memory does not
   count as checking.
4. **Cite the rule when correcting.** Say which rule applies (e.g. „nosinė, nes kilmininko galūnė“) so the
   correction is checkable, not a guess. Cite only rules you actually opened this session.
5. **Kirčiavimas is a correctness rule, not a default.** Know the rules (`references/kirciavimas.md`) but
   do **not** add stress marks to normal text unless the user asks (e.g. for TTS input or teaching).

## Which reference to load

| If the text involves…                                             | Load |
|-------------------------------------------------------------------|------|
| Spelling inside words: i/y, u/ū, e/ia, nosinės ą ę į ų, consonants (assimilation, j, softness) | `references/rasyba-balsiai-priebalsiai.md` |
| Compound words, together-or-apart, the negative *ne-*, particles  | `references/kartu-atskirai.md` |
| Capital vs. lowercase, proper names, org/place/personal names     | `references/didziosios-raides.md` |
| Dashes, hyphen, quotes „…“, brackets, numbers, dates, time, money | `references/skyrybos-zenklai.md` |
| Commas and sentence punctuation: clauses, participles, asides, address, lists, direct speech | `references/skyryba-kableliai.md` |
| Foreign names, abbreviations, acronyms                            | `references/svetimvardziai-santrumpos.md` |
| Common mistakes, calques, anglicisms, wrong cases/prepositions    | `references/daznos-klaidos.md` |
| Making translated/AI Lithuanian sound native                      | `references/humanizavimas-lt.md` |
| Stress marks / accentuation, only on request                      | `references/kirciavimas.md` |

## The six things AI/translated Lithuanian gets wrong most

Check these first. They cover the bulk of real errors (details in the references):

1. **Straight quotes and wrong dashes.** Lithuanian uses „…“ (not "…"), and – (brūkšnys) with spaces,
   not the English em-dash. → `skyrybos-zenklai.md`
2. **English capitalisation.** Lithuanian lowercases months, weekdays, nationalities/languages, and most
   words inside titles and job names. *sausio, pirmadienį, lietuvis, anglų kalba.* → `didziosios-raides.md`
3. **Calques.** *įtakoti* → *veikti / lemti / daryti įtaką*; *apjungti* → *sujungti / apjungti(=aprėpti)*;
   *pilnai* → *visiškai*; *sekantis* → *kitas / tolesnis*. → `daznos-klaidos.md`
4. **Number/date format.** Decimal comma (3,5 not 3.5), space thousands (1 000), *2022 m. sausio 5 d.*,
   14.30 val. → `skyrybos-zenklai.md`
5. **English word order and over-nominalisation.** Bureaucratic passive and noun stacks; prefer active
   verbs. → `humanizavimas-lt.md`
6. **Commas.** Subordinate clause not closed by a second comma (*Vyras, kuris sėdėjo, pradėjo ploti*);
   English Oxford comma before a single *ir/ar*; comma inside quantity comparisons (*daugiau nei 10*).
   Opposite error: "fixing" optional commas (participle phrases, modal words). → `skyryba-kableliai.md`

## Scope

This skill covers **rašyba** (orthography), **skyryba** (commas and sentence punctuation), graphic signs,
capitalisation, common lexical/grammar errors, and basic **kirčiavimas**.

**Optional punctuation is not an error.** The 2019 rules mark many commas as optional, written `(,)`, and state
that any permitted variant is correct. When proofreading, correct only mandatory cases; offer optional
ones as style suggestions at most. `references/skyryba-kableliai.md` marks each case ✔/◐/✘.

## Full official texts (`sources/`)

The `references/` files are condensed. When a case is not settled there, grep the full official text
instead of guessing:

| File | What it is |
|------|------------|
| `sources/skyrybos-taisykles-2019.md` | VLKK punctuation rules, full text with all examples. Rules start with their number: `grep -n -A3 "^11\.9\." …` |
| `sources/klaidu-sarasas/*.md` | VLKK list of major language errors, 9 files by category (vocabulary, word formation, cases, prepositions, forms, syntax, word order, pronunciation). Format: error → correction (`=`). `grep -i "<word>" sources/klaidu-sarasas/*.md` |

Source of truth for orthography is *Lietuvių kalbos rašyba* (VLKK, 2022); for punctuation, the 2019 VLKK
resolution plus A. Drukteinis's commentary (2020). Those books are not bundled (copyright); links are in
the repo's `SOURCES.md`. For a single word's spelling/meaning, the VLKK consultation bank and the DLKŽ
dictionary (ekalba.lt) are the authorities.
