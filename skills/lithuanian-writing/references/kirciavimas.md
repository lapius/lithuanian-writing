# Kirčiavimas (accentuation) — correctness reference

**Load only when the user asks to add or check stress marks** (e.g. text for TTS, teaching material).
Normal Lithuanian prose is written **without** stress marks — do not add them by default.

Full kirčiavimas of arbitrary words is genuinely hard: it depends on the word's **kirčiuotė** (accent
paradigm) and can shift across the declension/conjugation. For anything beyond the framework below,
verify against a dictionary source (VDU *tartis.vdu.lt*, *Dabartinės lietuvių kalbos žodynas*) rather
than guessing — treat guessed stress like a guessed fact under the confidence policy.

## The three marks

| Mark | Name | Used on |
|------|------|---------|
| **´** (dešininis / acute) | tvirtapradė priegaidė | long syllables, stress falls on the **start** of the syllable — tone drops: *brolis, láimė, šáukštas* |
| **~** (riestinis / circumflex) | tvirtagalė priegaidė | long syllables, stress on the **end** — tone level or rising: *pyktis, mū̃šis, tãkas* |
| **`** (kairinis / grave) | trumpinė priegaidė | **short** stressed syllables: *à, è, ì, ù* — *labà, nešù* |

Rule of thumb for which mark a *long* syllable takes:
- Long vowels (**y, ū, o, ė** and lengthened **a, e**) and mixed diphthongs (al, am, an, ar, el, em, en, er)
  and the diphthongs **ai, au, ei**: acute **´** if tvirtapradė, circumflex **~** if tvirtagalė.
- Diphthongs with **i, u** (*ui, iu, il, im, in, ir, ul, um, un, ur*): tvirtapradė = grave **`** on the first
  letter (*pìlnas, kùr*), tvirtagalė = circumflex **~** (*vil̃kas, tur̃gus*).
- Short vowels **a, e, i, u** stressed but not lengthened: grave **`**.

## Accent paradigms (kirčiuotės)

Every noun/adjective belongs to one of **four kirčiuotės (1–4)**, which decide where the stress lands in
each case:
- **1-oji** — fixed stress, never on the ending: *výras, výro, výrui…*
- **2-oji** — mostly fixed, but moves to a tvirtagalė/short ending in some cases (dgs. gal. etc.).
- **3-ioji** — mobile: alternates between root and ending across the paradigm (subtypes 3a, 3b, 34…).
- **4-oji** — the ending is stressed wherever it can be: *naktìs, naktiẽs, nãktį…*

You cannot derive the kirčiuotė from spelling alone — it is a lexical property. State the paradigm number
if known; otherwise mark the word as "needs dictionary" rather than inventing stress.

## A few reliable sub-rules

- **Žodžio galo taisyklė** — a long stressed final syllable is normally **tvirtagalė** (circumflex).
- **Bendraties priesaga** — a stressed infinitive suffix is **tvirtapradė** (*-ýti, -úoti*: *dažýti, šokúoti*).
- **Priešpaskutinio skiemens taisyklė** — the accent paradigm is often read off the daugiskaitos galininkas
  (dgs. gal.) stress position.
- Enclitics/proclitics (*ne, be, te, ir, į, nuo…*) are unstressed and lean on the next word.

## Practical

For a TTS pipeline, the right source of truth is a kirčiuotas word list / morphological analyser, not
per-word LLM guessing — the LLM is fine for the *rules and explanation* above, unreliable for the exact
mark on an inflected form. Flag this to the user instead of silently guessing.
