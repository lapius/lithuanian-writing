# Humanizavimas lietuviškai: kad tekstas neskambėtų kaip vertimas ar DI tekstas

Naudok kartu su įgūdžiu **humanizer**: jis šalina bendruosius, nuo kalbos nepriklausančius DI teksto
požymius, o šis failas prideda lietuviškąjį sluoksnį. Čia surašyti požymiai teksto, kuris išverstas iš
anglų kalbos arba sugeneruotas modelio, „galvojančio“ angliškai. Prasmę išlaikyk, keisk skambesį.

## Sandaros požymiai

- **Angliška žodžių tvarka.** Lietuvių kalbos žodžių tvarka laisva, bet verstas tekstas laikosi
  angliškos tvarkos (veiksnys, tarinys, papildinys) ir svarbiausią žodį deda ne į galą. Lietuviškai
  svarbiausia dažnai eina **sakinio gale**. Perstatyk.
- **Įvardžių perteklius.** Anglų kalbai reikia *he, she, it, they*, o lietuvių nereikia: veiksnį rodo
  veiksmažodžio galūnė. „Jis paėmė savo knygą ir jis atsisėdo“ → „Paėmė knygą ir atsisėdo“. Mesk
  perteklinius *jis, ji, aš*.
- **Perteklinis „savo“.** Verčiant *his, her, their* „savo“ prikaišiojama ten, kur viskas ir taip aišku.
- **Daiktavardžių virtinės.** „duomenų apdorojimo optimizavimo sprendimas“ → veiksmažodinė forma.
  Angliškos daiktavardžių grandinės lietuviškai skamba biurokratiškai.
- **Neveikiamosios ir beasmenės formos.** „yra rekomenduojama“, „buvo nuspręsta“ → „rekomenduojame“,
  „nusprendėme“. Veikiamosios formos gyvesnės ir lietuviškesnės.
- **Jungiamųjų žodžių vertiniai.** „papildomai“, „be to, kas svarbu“, „kalbant apie“ dažnai yra
  tiesioginiai *additionally, that said, when it comes to* vertimai. Rinkis natūralius: „dar“, „tačiau“,
  „dėl“.

## Žodyno požymiai

- **DI ir verstiniai žodžiai:** *pasinerti* (dive in), *atrakinti (galimybes)* (unlock), *sklandus*
  (seamless), *galingas* (powerful), *patobulinti patirtį*, *ekosistema*, *kelionė* (journey, perkeltine
  reikšme), *įgalinti* (enable). Vartok tik tada, kai jų tikrai reikia, o ne kaip kimšalą.
- **Pažodžiui išversti posakiai (kalkės):** žr. `daznos-klaidos.md` (*įtakoti, pilnai, sekantis,
  apjungti*…). Verstas tekstas jų pilnas.
- **Angliški skoliniai vietoj lietuviškų žodžių:** *feedback* → **atsiliepimas, grįžtamasis ryšys**;
  *deadline* → **terminas**; *goalas* → **tikslas**. Techniniuose tekstuose kai kurie terminai lieka,
  tad spręsk pagal skaitytojus, bet nerašyk anglizmo ten, kur įprastas lietuviškas žodis.

## Formos požymiai

- **Kabutės.** „…“ (apatinės ir viršutinės), ne "…" ir ne “…”. → `skyrybos-zenklai.md`
- **Brūkšniai.** Lietuviškas brūkšnys yra „–“ su tarpais, angliškas ilgasis brūkšnys „—“ lietuviškai
  nevartojamas. Bet dar svarbiau **brūkšnių kiekis**: brūkšnys beveik kiekviename sakinyje yra vienas
  ryškiausių DI teksto požymių. Daugelis brūkšnių pagal 2019 m. taisykles yra pasirenkami, todėl juos
  keisk:
  - praleistas *yra*: „Jis – geras žmogus“ → „Jis geras žmogus“ arba „Jis yra geras žmogus“;
  - paaiškinimas, įterpinys: brūkšniai → kableliai (kablelis taisyklėse ir taip pagrindinis variantas);
  - priežastis, išvada, sąlyga be jungtuko: brūkšnys → dvitaškis, taškas arba jungtukas
    („Atsipūs arkliai – važiuosime“ → „Kai atsipūs arkliai, važiuosime“);
  - sąrašas prieš apibendrinamąjį žodį: „Draugus, kaimynus – visus pakvietė“ → „Pakvietė visus:
    draugus, kaimynus“.

  Brūkšnys lieka dialoge (`– Ką veiki? – paklausė jis.`) ir intervaluose be tarpų (*2–6*,
  *Vilnius–Kaunas*): tai privaloma. → `skyryba-kableliai.md`
- **Didžiosios raidės pavadinimuose ir mėnesiuose.** Verstas tekstas rašo „Sausis“, „Pirmadienis“,
  „Anglų Kalba“, „Rinkodaros Skyrius“, o lietuviškai visa tai rašoma mažąja raide.
  → `didziosios-raides.md`
- **Skaičiai ir datos:** kablelis dešimtainėse trupmenose (3,5), tarpas tūkstančiuose (10 000),
  „2022 m. sausio 5 d.“.

## Kaip dirbti

1. Paleisk **humanizer** bendriesiems požymiams pašalinti.
2. Perskaityk garsiai: ar skamba kaip lietuvio parašyta, ar kaip vertimas? Vertimą išduoda ritmas ir
   žodžių tvarka, ne vien atskiri žodžiai.
3. Pirma taisyk žodžių tvarką ir konstrukcijas, tada žodyną, tada formą.
4. Patikrink brūkšnius: kiekvienam paklausk, ar jį galima pakeisti kableliu, dvitaškiu, tašku ar *yra*.
5. Nepridėk faktų. Jei sakinys skamba tuščiai ir angliškai, perrašyk mintį lietuviškai, o ne lopyk
   žodį po žodžio.
