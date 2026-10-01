---
name: lithuanian-writing
description: |
  Taisyklinga ir natūrali lietuvių kalba: rašymas, vertimas į lietuvių kalbą ir teksto taisymas –
  rašyba, skyryba (kableliai), didžiosios raidės, skaičių, datų ir kabučių rašymas, svetimvardžiai,
  dažnos klaidos ir kalkės, kirčiavimas (tik paprašius).
  Write correct, natural Lithuanian and check Lithuanian prose for errors. Use whenever writing,
  editing, translating into, or proofreading Lithuanian text — orthography (rašyba), comma placement
  and sentence punctuation (skyryba), capitalisation, number/date/quote formatting, foreign names,
  common mistakes and calques (įtakoti, apjungti, English word order), and accentuation (kirčiavimas)
  rules on request. Acts as a router: load only the reference file(s) relevant to the current text, not
  all of them; full official VLKK texts are in sources/ for grep lookup. Pair with the humanizer skill to
  also remove AI-writing tells.
license: MIT
metadata:
  version: "1.2.0"
  sources: "Lietuvių kalbos rašyba (VLKK, 2022); Lietuvių kalbos skyrybos taisyklės (VLKK 2019, N-8 (178)); VLKK didžiųjų kalbos klaidų sąrašas; VDU tartis.vdu.lt"
---

# Lietuvių kalba: taisyklingai ir natūraliai

Rašyk taip, kad tekstą be pataisų priimtų kruopštus lietuvių kalbos redaktorius. Šis įgūdis yra
**rodyklė**: taisyklės surašytos `references/` aplanke, o įkeliamas tik tas failas, kurio reikia
konkrečiam tekstui. Visų failų iš karto neįkelk.

## Kaip naudoti

1. **Rašant ar verčiant į lietuvių kalbą.** Parašyk juodraštį, tada patikrink pagal toliau pateiktus
   punktus. Jei tekstas verstas iš anglų kalbos, svarbiausi failai – `references/daznos-klaidos.md` ir
   `references/humanizavimas-lt.md`: būtent ten išryškėja vertimo kalkės ir angliška žodžių tvarka.
2. **Taisant lietuvišką tekstą.** Nustatyk, kas tekste yra (tikriniai vardai, skaičiai ir datos,
   kabutės, sudurtiniai žodžiai, sudėtiniai sakiniai), ir įkelk tik atitinkamus failus.
3. **Taisydamas nurodyk taisyklę.** Pasakyk, kuri taisyklė taikoma (pvz., „nosinė, nes kilmininko
   galūnė“), kad pataisą būtų galima patikrinti, o ne priimti aklai.
4. **Kirčiavimas – tik paprašius.** Taisykles žinok (`references/kirciavimas.md`), bet įprasto teksto
   **nekirčiuok**, nebent naudotojas to prašo (pvz., kalbos sintezei ar mokymui).

## Kurį failą įkelti

| Jei tekste yra…                                                   | Įkelk |
|-------------------------------------------------------------------|-------|
| Rašyba žodžio viduje: i / y, u / ū, e / ia, nosinės ą ę į ų, priebalsiai (supanašėjimas, j, minkštumas) | `references/rasyba-balsiai-priebalsiai.md` |
| Sudurtiniai žodžiai, rašymas kartu ar atskirai, neiginys *ne-*, dalelytės | `references/kartu-atskirai.md` |
| Didžiosios ir mažosios raidės, asmenvardžiai, vietovardžiai, organizacijų pavadinimai | `references/didziosios-raides.md` |
| Brūkšnys, brūkšnelis, kabutės „…“, skliaustai, skaičiai, datos, laikas, pinigai | `references/skyrybos-zenklai.md` |
| Kableliai ir sakinio skyryba: šalutiniai sakiniai, dalyvinės aplinkybės, įterpiniai, kreipiniai, vienarūšės dalys, tiesioginė kalba | `references/skyryba-kableliai.md` |
| Svetimvardžiai, santrumpos, akronimai                             | `references/svetimvardziai-santrumpos.md` |
| Dažnos klaidos, kalkės, svetimybės, netinkami linksniai ir prielinksniai | `references/daznos-klaidos.md` |
| Verstinis ar dirbtinio intelekto tekstas, kurį reikia padaryti natūralų | `references/humanizavimas-lt.md` |
| Kirčiavimas (tik paprašius)                                       | `references/kirciavimas.md` |

## Šešios dažniausios verstinio ir DI teksto klaidos

Pirmiausia tikrink šias – jos sudaro didžiąją dalį tikrų klaidų (išsamiau – failuose):

1. **Tiesios kabutės ir netinkami brūkšniai.** Lietuviškai rašoma „…“, ne "…", ir brūkšnys – su
   tarpais, ne angliškas ilgasis brūkšnys be tarpų. → `skyrybos-zenklai.md`
2. **Angliškos didžiosios raidės.** Mėnesiai, savaitės dienos, tautybės, kalbos, dauguma pavadinimų ir
   pareigybių žodžių rašomi mažąja raide: *sausio, pirmadienį, lietuvis, anglų kalba*. → `didziosios-raides.md`
3. **Kalkės.** *įtakoti* → *veikti, lemti, daryti įtaką*; *apjungti* → *sujungti* (*apjungti* tik
   reikšme „aprėpti“); *pilnai* → *visiškai*; *sekantis* → *kitas, tolesnis*. → `daznos-klaidos.md`
4. **Skaičiai ir datos.** Dešimtainis kablelis (3,5, ne 3.5), tūkstančiai skiriami tarpu (1 000),
   *2022 m. sausio 5 d.*, *14.30 val.* → `skyrybos-zenklai.md`
5. **Angliška žodžių tvarka ir daiktavardžių grandinės.** Kanceliarinis neveikiamasis būdas ir
   daiktavardžių virtinės; rinkis veikiamąsias veiksmažodžių formas. → `humanizavimas-lt.md`
6. **Kableliai.** Šalutinis sakinys neuždarytas antruoju kableliu (*Vyras, kuris sėdėjo, pradėjo ploti*);
   angliškas kablelis prieš vienintelį *ir* ar *ar*; kablelis kiekio palyginime (*daugiau nei 10*).
   Priešinga klaida – „taisomi“ pasirenkami kableliai (dalyvinės aplinkybės, modaliniai žodžiai).
   → `skyryba-kableliai.md`

## Apimtis

Įgūdis apima **rašybą**, **skyrybą** (kablelius ir kitus sakinio skyrybos ženklus), grafinius ženklus,
didžiąsias raides, dažnas leksikos ir gramatikos klaidas bei pagrindines **kirčiavimo** taisykles.

**Pasirenkamas skyrybos ženklas nėra klaida.** 2019 m. taisyklėse daug kablelių pažymėti kaip
pasirenkami – `(,)` – ir nurodyta, kad bet kuris leidžiamas variantas yra taisyklingas. Taisydamas
taisyk tik privalomus atvejus, o pasirenkamus daugių daugiausia siūlyk kaip stiliaus pastabą.
Faile `references/skyryba-kableliai.md` kiekvienas atvejis pažymėtas ✔ / ◐ / ✘.

## Visi oficialūs tekstai (`sources/`)

`references/` failuose taisyklės sutrauktos. Jei atvejo ten neišsprendi, ieškok visame oficialiame
tekste, o ne spėliok:

| Failas | Kas tai |
|--------|---------|
| `sources/skyrybos-taisykles-2019.md` | VLKK skyrybos taisyklės, visas tekstas su visais pavyzdžiais. Punktai prasideda numeriu: `grep -n -A3 "^11\.9\." …` |
| `sources/klaidu-sarasas/*.md` | VLKK didžiųjų kalbos klaidų sąrašas, 9 failai pagal sritis (žodynas, žodžių daryba, linksniai, prielinksniai, formos, sintaksė, žodžių tvarka, tartis). Forma: klaida → taisymas (`=`). `grep -i "žodis" sources/klaidu-sarasas/*.md` |

Rašybos norma – *Lietuvių kalbos rašyba* (VLKK, 2022); skyrybos – 2019 m. VLKK nutarimas ir A. Drukteinio
komentarai (2020). Šios knygos į rinkinį neįtrauktos dėl autorių teisių, nuorodos į jas – saugyklos
faile `SOURCES.md`. Dėl atskiro žodžio rašybos ar reikšmės patikimiausi šaltiniai – VLKK konsultacijų
bankas ir *Dabartinės lietuvių kalbos žodynas* (ekalba.lt).
