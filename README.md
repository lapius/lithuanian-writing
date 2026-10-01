# lithuanian-writing

Dirbtinio intelekto agentams skirtas įgūdis lietuviškam tekstui rašyti ir taisyti: rašyba, kableliai ir
kita skyryba, didžiosios raidės, skaičių ir datų rašymas, svetimvardžiai, kalkės ir dažnos klaidos,
o paprašius – ir kirčiavimas.

Taisyklės sutrauktos iš oficialių Valstybinės lietuvių kalbos komisijos (VLKK) normų. Šalia sutrauktų
taisyklių pateikiamas ir visas oficialus tekstas, todėl agentas keblų atvejį gali pasitikrinti, o ne
spėlioti.

## Sandara

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

## Diegimas

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

## Principai

- **Rodyklė, ne visas sąvadas.** `SKILL.md` – tik turinys. Agentas vienam tekstui įkelia vieną ar du
  failus, o ne visas ~1 500 eilučių.
- **Pasirenkamas ženklas nėra klaida.** Pagal 2019 m. skyrybos taisykles daug kablelių yra pasirenkami, ir
  bet kuris leidžiamas variantas laikomas taisyklingu. Kablelių faile kiekvienas atvejis pažymėtas:
  ✔ privaloma, ◐ pasirenkama, ✘ neskiriama. Taip taisant nesugadinamas jau taisyklingas tekstas.
- **Nurodoma taisyklė.** Prie kiekvienos pataisos nurodoma taisyklė ar oficialaus sąrašo punktas, kad
  žmogus galėtų ją patikrinti.

## Licencija

Įgūdžio tekstas (`SKILL.md`, `references/`) platinamas pagal MIT licenciją. Aplanke `sources/` – oficialūs
norminiai VLKK tekstai, kurie pagal Lietuvos Respublikos autorių teisių ir gretutinių teisių įstatymo
5 straipsnį nėra autorių teisių objektas. Jie pateikti nekeisti, nurodant šaltinio adresą.
