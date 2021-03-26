---
description: Lag en Endringslogg
title: Lag en Endringslogg
language: nb
version: 1.1.0
---

# Lag en Endringslogg

Fra [keep a changelog](https://github.com/olivierlacan/keep-a-changelog) `nb_NO` [v1.1.0](https://github.com/olivierlacan/keep-a-changelog/pull/383).

## Ikke la vennene dine dumpe git logger i endringslogger.

### Hva er en endringslogg?

En endringslogg er en fil som inneholder en organisert, kronologisk satt opp liste over sentrale endringer for hver versjon av et prosjekt.

### Hvorfor lage en endringslogg?

For å gjøre det enklere for brukere og bidragsytere å se nøyaktig hvilke sentrale endringer som har blitt gjort mellom hver utgivelse (eller versjon) av prosjektet.

### Hvem trenger en endringslogg?

Folk. Om enn de er konsumenter eller utviklere, sluttbrukerne av programvare er mennesker som bryr seg om hva som er i programvaren. Når programvaren endres, vil folk vite hvorfor og hvordan.

### Hvordan lager jeg en god endringslogg?

#### Veiledende prinsipper

- Endringslogger er _for mennesker_, ikke maskiner.
- Det bør være en oppføring for hver versjon.
- Samme type endringer bør grupperes.
- Versjoner og seksjoner bør kunne lenkes til.
- Den nyeste versjonen bør komme først.
- Utgivelsesdatoen for hver versjon vises.
- Nevn hvorvidt du følger [Semantisk Versjonering](https://semver.org/).

#### Endringer

- `Lagt til` for ny funksjonalitet.
- `Endret` for endringer i eksisterende funksjonalitet.
- `Avviklet` for funksjonalitet som snart fjernes.
- `Fjernet` for fjernet funksjonalitet.
- `Fikset` for feilrettinger.
- `Sikkerhet` i tilfelle sårbarheter.

### Hvorfor kan jeg redusere innsatsen som må til for å vedlikeholde en endringslogg?

Bruk en `Ikke utgitt`-seksjon øverst for å spore kommende endringer.

Dette tjener to formål:

- Folk kan se hvilke endringer de kan forvente i kommende utgivelser
- Når utgivelsen publiseres kan du flytte `Ikke utgitt`-seksjonen til en seksjon for en ny versjon.

### Kan endringslogger være dårlige?

Ja. Her er noen måter de kan være mindre nyttige.

#### Handlingslogg med endringer

Å bruke endringer i handlingslogg (_commit log diffs_) som endringslogg er en dårlig idé: De er full av støy. Ting som sammenslåing av endringer, obskure titler, endringer i dokumentasjon, osv.

Formålet med en handlingslogg er å dokumentere et steg i utviklingen av kildekoden. Noen prosjekter rydder handlingslogger, andre ikke.

Formålet med en oppføring i endringslogg er å dokumentere sentrale endringer, gjerne på tvers av flere handlingslogger, samt å kommunisere disse klart til sluttbrukerne.

#### Ignorere Avviklinger

Når folk oppgraderer fra en versjon til en annen burde det være smertelig tydelig når noe vil gå i stykker. Det burde være mulig å oppgradere til en versjon som oppgir avviklinger, fjerne det som er avviklet, og deretter oppgradere til en versjon hvor avviklinger blir det som er fjernet.

Om ikke annet, oppgi avviklinger, hva som er fjernet, og annet som gjør at noe går i stykker i endringsloggen.

#### Forvirrende Datoer

Regionale datoformater varierer, og det er ofte vanskelig å finne et menneskevennlig datoformat som føles intuitivt for alle. Fordelen med datoformater som `2017-07-17` er at de følger rekkefølgen med største til minste enhet: År, måned og dato. Dette formatet overlapper heller ikke på tvetydige måter, til forskjell fra noen regionale formater som bytter posisjonen til måneds- og datonumre. Derfor, og fordi dette datoformatet er en [ISO-standard](http://www.iso.org/iso/home/standards/iso8601.htm), er det anbefalt datoformat for oppføringer i endringslogger.

#### Tvetydige Endringer

En endringslogg som bare nevner noen av endringene kan være like farlig som å ikke ha en endringslogg. Selv om mange av endringene ikke er relevante - for eksempel, fjerning av et enkelt mellomrom ikke trenger å registreres i alle tilfeller - bør alle sentrale endringer nevnes i endringsloggen. Ved inkonsistent oppførsel av endringer vil brukerne dine feilaktig tro at endringsloggen er den eneste kilden til sannhet. Den bør være det. Ved stor makt kommer stort ansvar - å ha en god endringslogg betyr å ha en konsistent oppdatert endringslogg.

> Det er mer. Hjelp meg med å samle disse antimønstrene ved å [åpne en sak](https://github.com/olivierlacan/keep-a-changelog/issues), saker eller et endringsforslag.

### Ofte Spurte Spørsmål

#### Er det et standard format for endringslogger?

Ikke egentlig. Det finnes [GNUs stilguide for endringslogger](https://www.gnu.org/prep/standards/html_node/Style-of-Change-Logs.html#Style-of-Change-Logs), eller den [to avsnitt lange GNU NEWS filen](https://www.gnu.org/prep/standards/html_node/NEWS-File.html#NEWS-File) "retningslinjen". Begge er inadekvate eller utilstrekkelige.

Dette prosjektet søker å være [en bedre konvensjon for endringslogger](https://github.com/olivierlacan/keep-a-changelog/blob/master/CHANGELOG.md). Dette kommer fra observasjon av beste praksis i miljøet for åpen kildekode og innsamling av de.

Sunn kritikk, diskusjon og forslag til forbedringer [er velkomne](https://github.com/olivierlacan/keep-a-changelog/issues).

#### Hvordan bør endringsloggfilen navngis?

Kall de `CHANGELOG.md`. Noen prosjekter bruker `HISTORY`, `NEWS` eller `RELEASES`.

Selv om det er enkelt å tenke at navnet på endringsloggfilen ikke betyr så mye, hvorfor gjøre det vanskeligere for sluttbrukerne å konsekvent finne sentrale endringer?

#### Hva med utgivelser på GitHub?

Det er et flott initiativ. [Utgivelser](https://help.github.com/articles/creating-releases/) kan brukes for å gjøre enkle taggede versjoner på git (for eksempel `v1.0.0`) om til fyldige utgivelsesnotater ved å manuelt legge de til, eller å hente annoterte notater fra taggede versjoner å gjøre de om til utgivelsesnotater.

Utgivelser på GitHub lager en ikke-portabel endringslogg som bare kan vises til brukerne innenfor konteksten GitHub. Det er mulig å gjøre de veldig lik formatet til Lag en Endringslogg, men det er vanligvis mer krevende.

Den nåværende versjonen av utgivelser på GitHub er antageligvis ikke veldig gjenfinnbar for sluttbrukere, i motsetning til de typiske filene med store bokstaver (`README`,  `CONTRIBUTING`, osv.) Et annet, mindre, problem er at grensesnittet per nå ikke tilbyr lenker til handlingslogger mellom hver utgivelse.

#### Kan endringslogger automatisk tolkes?

Det er vanskelig, fordi folk følger svært forskjellige formater og filnavn.

[Vandamme](https://github.com/tech-angels/vandamme/) er en Ruby gem laget av Gemnasium-teamet for å tolke mange (men ikke alle) endringslogger for prosjekter med åpen kildekode.

#### Hva med tilbaketrukne utgivelser?

Tilbaketrukne utgivelser er versjoner som måtte trekkes tilbake på grunn av en alvorlig feil eller et sikkerhetsproblem. Vanligvis fremgår ikke disse versjonene i endringsloggen. Det bør det. Slik bør de vises frem:

`## [0.0.5] - 2014-12-13 [TILBAKETRUKKET]`

Merkelappen `[TILBAKETRUKKET]` er bevisst uthevet. Det er for at folk skal legge merke til den. Siden den er omgitt av braketter er den også enklere å tolke programmatisk.

#### Bør du noensinne omskrive en endringslogg?

Selvfølgelig. Det er alltid gode grunner til å forbedre en endringslogg. Jeg lager regelmessig endringsforslag for å legge til manglende utgivelser i prosjekter med åpen kildekode som mangler vedlikeholdte endringslogger.

Det er også mulig at du oppdager at du glemte å addressere en sentral endring i notatene til en versjon. Det er selvfølgelig viktig at du oppdaterer endringsloggen i dette tilfellet.

#### Hvordan kan jeg bidra?

Dette dokumentet er ikke **sannheten**; det er min nøye vurderte mening, samt informasjon og eksempler jeg har samlet.

Dette fordi jeg vil at vårt miljø skal nå en enighet. Jeg tror at diskusjonen er like viktig som resultatet.

Så vær så snill, **[bidra](https://github.com/olivierlacan/keep-a-changelog)**.

### Samtaler

Jeg deltok på [The Changelog podcast](https://changelog.com/podcast/127) for å snakke om hvorfor vedlikeholdere og bidragsytere burde bry seg om endringslogger, og også om motivasjonene bak dette prosjektet.
