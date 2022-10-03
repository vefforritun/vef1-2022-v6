# Vefforritun 1, 2022: Verkefni 6, CSS #4

Halda skal áfram með viðmót úr [verkefni 4](https://github.com/vefforritun/vef1-2022-v4/) og [verkefni 5](https://github.com/vefforritun/vef1-2022-v5/). Setja skal upp tól til að hjálpa til við skipulag og vinnu.

## Markmið

* Setja upp Node.js og NPM og nota til að sækja pakka.
* Nota tól fengin af NPM.
* Keyra tól í vinnuflæði með `package.json`.

## Útlit

Sama gildir um útlit og í verkefni 5, útlit ætti að haldast alveg það sama, eina sem breytist er hvernig verkefnið er uppsett.

## Tæki og tól

Til þess að geta notað þessi tól þarf að [setja upp Node.js, sækið „Recommended For Most Users“](https://nodejs.org/en/). Eftir að þið hafið keyrt uppsetningar forrit getið þið opnað Command prompt/terminal/skel og keyrt:

```bash
> node -v
v16.7.1 # eða sú útgáfa sem þið sóttuð
> npm -v
8.15.0 # eða álíka
```

Ef þið fáið þetta ekki upp, prófið að endurræsa. Annars fá aðstoð í dæmatímum, í fyrirlestri, tölvupósti eða á slack.

Setja skal upp `sass`, `browser-sync`, `stylelint` og `concurrently` til að nýta Sass og geta gert breytingar sem sjást strax í vafra.

Fyrst þarf að búa til `package.json` með því að keyra `npm init` í verkefnamöppu.

Síðan þarf að sækja hvert tól með `npm install <nafn á tóli>`.

### Sass

Skipta skal CSS upp í mismunandi skrár undir `styles/`.

Í `styles/config.scss` skal geyma allar stillingar fyrir verkefni og nota þær á viðeigandi stöðum.

Nota skal _nesting_ en aðeins upp á eitt level.

```scss
.card {
  .title {
    // ok

    .item {
      // ekki ok, þriðja level
    }
  }
}
```

### Browser sync & concurrently

Þegar skipunin `npm run dev` er keyrð skal verkefnið keyra upp vefþjón með `browser-sync`, þýða sass skrár og fylgjast með breytingum á HTML og Sass.

[Sjá fyrirlestur 6.3: Sass & stylelint](https://github.com/vefforritun/vef1-2021/blob/main/vikur/06/06.3.sass-stylelint.md) og í [Sass + browser-sync](https://github.com/vefforritun/vef1-2021/tree/main/vikur/06/daemi/3.sass-stylelint/03.sass-browser-sync).

### Linting

Setja skal upp stylelint með `stylelint-config-sass-guidelines` og `stylelint-config-standard`.

Þegar skipunin `npm run lint -s` er keyrð skal keyra stylelint með þessum reglum og ættu engar villur að koma fram.

[Sjá námsefni um sass og stylelint](https://github.com/vefforritun/vef1-2022/tree/main/namsefni/22.sass-stylelint) og í [Stylelint dæmi](https://github.com/vefforritun/vef1-2022/tree/main/namsefni/22.sass-stylelint/daemi/04.stylelint).

## Mat

* 40% – CSS flutt yfir í Sass
* 40% – stylelint uppsett og engar villur
* 20% – Verkefni sett upp með `package.json` og viðeigandi scriptum

## Sett fyrir

Verkefni sett fyrir mánudaginn 3. október 2021.

## Skil

Skila skal í Canvas, seinasta lagi fyrir lok dags þriðjudaginn 11. október 2022.

Skilaboð skulu innihalda:

* slóð á verkefni keyrandi á Netlify
* slóð á **private** GitHub repo fyrir verkefni. Dæmatímakennurum skal hafa verið boðið í repo. Notendanöfn þeirra eru:
  * `MarzukIngi`
  * `Stimmikex`
  * `brynjar13`
  * `ofurtumi`
  * `BjarniHaskoli`
  * `Stulli888`

Skilaboð skulu innihalda zip skjali með lausn. **Athugið að ekki skal skila node_modules/ möppu**!

## Einkunn

Leyfilegt er að ræða, og vinna saman að verkefni en **skrifið ykkar eigin lausn**. Ef tvær eða fleiri lausnir eru mjög líkar þarf að færa rök fyrir því, annars munu allir hlutaðeigandi hugsanlega fá 0 fyrir verkefnið.

Sett verða fyrir tíu minni verkefni þar sem átta bestu gilda 5% hvert, samtals 40% af lokaeinkunn.

Sett verða fyrir tvö hópverkefni þar sem hvort um sig gildir 10%, samtals 20% af lokaeinkunn.

> Útgáfa 0.1
