---
name: suomi-tarkistuslista
description: Orkestroi muut suomi-* -skillit oikeassa järjestyksessä suomenkielisen tekstin täyttä laadunvarmistusta varten. Käytä AINA kun käyttäjä sanoo "aja täysi suomi-tarkistus", "tarkista koko teksti", "tee final-pass suomeksi", "suomi-check", "humanisoi ja tarkista", "viimeistele suomenkielinen teksti", tai antaa tekstin, joka pitää käydä läpi useilla laaduntarkistuksilla. Tunnistaa tekstin kontekstin (markkinointi, hakemus, blogi, some, YMYL, selkokieli, sähköposti, tarjous, tiedote, uutiskirje) ja ajaa oikeat skillit oikeassa järjestyksessä – yleiset tyylipassit ensin, mekaniikka viimeiseksi. Konsolidoi löydökset yhdeksi raportiksi. Ei tee mekaniikkatyötä itse; delegoi alaskilleille [[suomi-anglismit]], [[suomi-ei-ai-sloppia]], [[suomi-kielihuolto]], [[suomi-rekisteri]], [[suomi-some-tyyli]], [[suomi-ymyl]], [[suomi-selkokieli]], [[suomi-sahkoposti]], [[suomi-tarjous]], [[suomi-tiedote]], [[suomi-uutiskirje]], [[suomi-hakemuspaketti]] ja konsultoiviin meta-skilleihin [[suomi-sinuttelu-teitittely]] ja [[suomi-lokalisaatio-perus]].
license: MIT
---

# Suomi-tarkistuslista – orkestraattori

## Mitä tämä skill tekee

Tämä on **meta-skill**. Se ei itse korjaa tekstiä, vaan valitsee oikeat alaskillit ja ajaa ne oikeassa järjestyksessä. Lopputulos: yksi konsolidoitu laatutarkistus, jossa kaikki suomi-* -skillit on hyödynnetty tarkoituksenmukaisesti.

**Käyttäjälle näkyvä etu:** sinun ei tarvitse muistaa "ensin anglismit, sitten ai-sloppia, sitten kielihuolto, sitten ehkä rekisteri tai some-tyyli". Sano vain "aja suomi-tarkistus", niin orkestraattori hoitaa loput.

## Skillien rooli pipelinessä

Suomi-* -skillit ovat kolmessa kategoriassa:

**Yleiset puhdistus-skillit (ajetaan lähes aina pipelinen lopussa):**

- `suomi-rekisteri` – määrittää kohderekisterin (vaikuttaa kaikkiin myöhempiin valintoihin)
- `suomi-ei-ai-sloppia` – yleinen AI-kuvioiden puhdistus
- `suomi-anglismit` – käännöslainojen puhdistus (kapeampi kuin ei-ai-sloppia)
- `suomi-kielihuolto` – mekaniikka (yhdyssanat, pilkutus, sijamuodot, rektiot, erisnimien taivutus)

**Kontekstuaaliset pää-skillit (konteksti-spesifinen vaihe pipelinen alussa, ennen puhdistusvaihetta):**

- `suomi-some-tyyli` – some-postaus (LinkedIn / Instagram / TikTok / Facebook)
- `suomi-ymyl` – terveys, talous, lakiasiat, turvallisuus, ravitsemus, eläinten hoito, viranomaisasiat
- `suomi-selkokieli` – selkokieliversio monimutkaisesta tekstistä
- `suomi-sahkoposti` – yksittäinen sähköposti (asiakasviesti, B2B, sisäinen, kylmäkontaktiviesti)
- `suomi-tarjous` – kaupallinen tarjous yritysasiakkaalle
- `suomi-tiedote` – lehdistötiedote tai sisäinen tiedote
- `suomi-uutiskirje` – sähköpostiuutiskirje
- `suomi-hakemuspaketti` – räätälöity CV + hakemuskirje tiettyyn työpaikkaan

**Meta-skillit (konsultoivat referenssit, eivät pipeline-vaihe itsessään):**

- `suomi-sinuttelu-teitittely` – puhuttelumuodon päätösmatriisi, käytetään esim. sähköpostista, tarjouksesta, YMYL-tekstistä
- `suomi-lokalisaatio-perus` – päivämäärät, kellonajat, numerot, valuutta, osoitteet – käytetään minkä tahansa pipelinen sisällä, jossa on numeerista tai aikatietoa

## VAIHE 0 – kontekstin tunnistus (PAKOLLINEN)

Ennen yhtäkään skilliä, tunnista tekstin konteksti. Kysy käyttäjältä jos ei selvää.

### Tekstityyppi-kysymykset

```
1. Mikä tekstityyppi tämä on?
   [ ] Markkinointikopio (verkkosivu, brosyyri, mainos)
   [ ] Sähköposti / asiakasviestintä (yksittäinen viesti)
   [ ] Uutiskirje (sähköpostikampanja useammalle vastaanottajalle)
   [ ] Some-postaus (LinkedIn / Instagram / TikTok / Facebook)
   [ ] Blogi tai artikkeli
   [ ] Hakemus tai CV
   [ ] Tarjous (kaupallinen, konsultointi, freelance)
   [ ] Sopimusteksti / käyttöehdot
   [ ] Lehdistötiedote tai sisäinen tiedote
   [ ] Käyttöohje tai opas
   [ ] Tieto-/uutisartikkeli
   [ ] Selkokielinen versio jostain
   [ ] Muu – määritä

2. Sisältääkö teksti YMYL-aiheita (terveys, talous, oikeudet, turvallisuus, ravitsemus, eläimet, viranomaisasia)?
   [ ] Kyllä – minkä alueen
   [ ] Ei

3. Mikä on kohderekisteri?
   [ ] Virallinen
   [ ] Ammattikieli
   [ ] Yleiskieli / asiakaskieli
   [ ] Puhekielinen / rento
   [ ] Selkokieli (jos kohta 1 oli selkokieli)
   [ ] Vaihtelevasti eri osioissa
```

### Automaattinen tunnistus jos käyttäjä ei kerro

Jos kysymyksiin ei saa vastauksia, päättele tekstistä:

| Vihje | Päätelmä |
|---|---|
| "Käyttöehdot", "tietosuojaseloste", lakiviittauksia | Sopimusteksti, virallinen rekisteri |
| Otsikko hashtagien kanssa, lyhyt | Some-postaus |
| "Hei [nimi]" + tervehdys + lopussa "Ystävällisin terveisin" | Sähköposti |
| Otsikkorivi + preheader + peruutuslinkki | Uutiskirje |
| "Tiedote" + "julkaisuvapaa" + sitaatti | Lehdistötiedote |
| Sisäinen tiedote tiimille tai henkilöstölle | Sisäinen tiedote (käytä `suomi-tiedote`) |
| "Tarjous" + hinnoittelu + ALV + voimassaolo | Tarjous |
| "Hakemus" + työpaikkailmoituksen viittaus + CV | Hakemus/CV |
| Lääketieteellinen terminologia, annosohjeet, oireet | YMYL – terveys |
| Sijoitus-, korko-, tuotto-, eläke-puhe | YMYL – talous |
| Pykäliä, lakiviittauksia, oikeudellisia neuvoja | YMYL – laki |
| "Yksi ajatus per virke", lyhyet virkkeet, selittäviä apusanoja | Selkokielinen – saattaa olla jo tehty tai tarpeen |
| Mainosadjektiivit, CTA, hyödyt | Markkinointi |
| Pitkät kappaleet, otsikkohierarkia, FAQ | Blogi tai artikkeli |

## VAIHE 1 – Pipelinen valinta kontekstin mukaan

### Pipeline A – Yleinen teksti (markkinointi, blogi, verkkosivut, sisäinen viestintä)

```
1. [[suomi-rekisteri]]      – lukitse kohderekisteri
2. [[suomi-ei-ai-sloppia]]  – yleinen AI-kuvioiden puhdistus
3. [[suomi-anglismit]]      – käännöslainojen puhdistus
4. [[suomi-kielihuolto]]    – mekaniikka
```

Huom: yksittäiseen sähköpostiin käytä Pipeline G:tä, uutiskirjeeseen Pipeline J:tä.

### Pipeline B – Some-postaus

```
1. [[suomi-some-tyyli]]     – kanavakohtainen rakenne, pituus, rekisteri
2. [[suomi-ei-ai-sloppia]]  – yleinen AI-kuvioiden puhdistus
3. [[suomi-anglismit]]      – käännöslainojen puhdistus
4. [[suomi-kielihuolto]]    – mekaniikka
```

Huom: `suomi-rekisteri` jää väliin, koska `suomi-some-tyyli` sisältää kanavakohtaiset rekisteri-säännöt.

### Pipeline C – YMYL-teksti (terveys, talous, oikeudet, turvallisuus jne.)

```
1. [[suomi-ymyl]]           – journalistinen näkökulma, lähteet, lähdelinkit
2. [[suomi-rekisteri]]      – varmistaa, että rekisteri sopii aiheen vakavuuteen
3. [[suomi-ei-ai-sloppia]]  – yleinen AI-kuvioiden puhdistus
4. [[suomi-anglismit]]      – käännöslainojen puhdistus
5. [[suomi-kielihuolto]]    – mekaniikka
```

### Pipeline D – Selkokielistäminen

```
1. [[suomi-selkokieli]]     – rakenteellinen muunnos (lyhyet virkkeet, tuttu sanasto)
2. [[suomi-anglismit]]      – käännöslainat pois (selkokielessä erityisen tärkeää)
3. [[suomi-kielihuolto]]    – mekaniikka
```

Huom: `suomi-ei-ai-sloppia` jää pääosin väliin, koska selkokieli vaatii erilaiset säännöt (yksinkertaisuus ennen tyyliä). Jos selkokielinen teksti on AI-tuotettu, voit tarkistaa erikseen mahtipontisuuden ja anglismit.

### Pipeline E – Virallinen / sopimusteksti / käyttöehdot

```
1. [[suomi-rekisteri]]      – virallinen rekisteri lukittava
2. [[suomi-kielihuolto]]    – mekaniikka erityisen tärkeä virallisessa tekstissä
3. [[suomi-anglismit]]      – käännöslainoja erityisesti vältettävä
```

Huom: `suomi-ei-ai-sloppia` jää yleensä väliin – virallinen rekisteri sallii tiettyjä rakenteita, jotka muissa konteksteissa olisi AI-slop (esim. passiivi-vahvuus virkamiestekstissä).

### Pipeline F – Hakemus tai CV

```
1. [[suomi-hakemuspaketti]] – räätälöinti työpaikkailmoituksen mukaan, CV.md + Hakemuskirje.md
2. [[suomi-rekisteri]]      – ammattikieli + henkilökohtainen sävy
3. [[suomi-ei-ai-sloppia]]  – yleinen AI-kuvioiden puhdistus, erityisesti kuvio 31 (humble brag)
4. [[suomi-anglismit]]      – käännöslainat (huom: säilytä alan vakiintuneet termit kuten "orgaaninen", "brieffata", "konversio")
5. [[suomi-kielihuolto]]    – mekaniikka
```

### Pipeline G – Sähköposti

```
1. [[suomi-sinuttelu-teitittely]] – konsultoiva, valitse puhuttelumuoto
2. [[suomi-sahkoposti]]     – tervehdys, runko, lopetus, allekirjoitus
3. [[suomi-ei-ai-sloppia]]  – yleinen AI-kuvioiden puhdistus, erityisesti chatbot-aloitukset
4. [[suomi-anglismit]]      – käännöslainojen puhdistus ("toivottavasti voit hyvin" jne.)
5. [[suomi-kielihuolto]]    – mekaniikka
```

Huom: `suomi-rekisteri` jää yleensä väliin – sähköposti-skill sisältää tervehdys- ja lopetus-hierarkian, joka kalibroi rekisterin.

### Pipeline H – Tiedote

```
1. [[suomi-tiedote]]        – rakenne, käänteinen pyramidi, sitaatit, lisätietolohko
2. [[suomi-ei-ai-sloppia]]  – yleinen AI-kuvioiden puhdistus, erityisesti AI-sitaatit ja mahtailuretoriikka
3. [[suomi-anglismit]]      – käännöslainojen puhdistus
4. [[suomi-kielihuolto]]    – mekaniikka
```

Huom: konsultoi `suomi-lokalisaatio-perus` -skilliä päivämäärien ja numeroiden muotoiluun.

### Pipeline I – Tarjous

```
1. [[suomi-rekisteri]]      – ammattikieli, neutraali sävy
2. [[suomi-tarjous]]        – rakenne, ALV-erottelu, maksuehdot, voimassaolo
3. [[suomi-ei-ai-sloppia]]  – yleinen AI-kuvioiden puhdistus, erityisesti myyntipuheen karsinta
4. [[suomi-anglismit]]      – käännöslainojen puhdistus
5. [[suomi-kielihuolto]]    – mekaniikka
```

Huom: konsultoi `suomi-lokalisaatio-perus` -skilliä hinnoittelun, ALV:n ja päivämäärien muotoiluun. Konsultoi `suomi-sinuttelu-teitittely` -skilliä asiakaspuhuttelumuotoon.

### Pipeline J – Uutiskirje

```
1. [[suomi-rekisteri]]      – asiakaskieli tai ammattikieli kohderyhmän mukaan
2. [[suomi-uutiskirje]]     – otsikkorivi, preheader, sisältöblokit, CTA, peruutuslinkki
3. [[suomi-ei-ai-sloppia]]  – yleinen AI-kuvioiden puhdistus, erityisesti kuulumisten kyselyt ja kolmiosalistat
4. [[suomi-anglismit]]      – käännöslainojen puhdistus ("Mikä on uutta?" jne.)
5. [[suomi-kielihuolto]]    – mekaniikka
```

Huom: konsultoi `suomi-lokalisaatio-perus` -skilliä päivämäärien muotoiluun. Konsultoi `suomi-sinuttelu-teitittely` -skilliä lukijan puhuttelumuotoon.

## VAIHE 2 – Skillikohtainen suoritus

Jokaisen pipelineen kuuluvan skillin kohdalla:

### Suoritussykli

```
Vaihe N – Käynnistä [skill-nimi]
   ↓
1. Lue skillin SKILL.md (jos et muista sääntöjä)
2. Käy teksti läpi skillin sääntöjen mukaan
3. Listaa löydökset (per löydös: tiedosto/kohta, ongelma, korjausehdotus)
4. Älä tee vielä korjauksia, vaan kerää löydökset
   ↓
Vaihe N+1 – Käynnistä seuraava skill
```

### Tärkeä periaate: kerää löydökset, älä korjaa peräkkäin

Älä korjaa tekstiä jokaisen skillin jälkeen erikseen. Tämä luo turhaa työtä (myöhempi skill voi muuttaa myös aiemman skillin korjauksen kohteen). Sen sijaan:

1. Aja jokainen skill puhtaalla alkuperäisellä tekstillä
2. Kerää löydökset listana
3. Konsolidoi yhdeksi korjauskokonaisuudeksi
4. Vasta sitten kirjoita lopullinen versio, joka noudattaa kaikkia löydöksiä

Poikkeus: jos teksti vaatii rakenteellisen muunnoksen (esim. selkokielistäminen, some-kanavakohtaistus, YMYL-näkökulma), tee se ENSIN ja sitten aja mekaaniset tarkistukset puhdistetulle versiolle.

## VAIHE 3 – Löydösten konsolidointi

Kun kaikki pipelinen skillit on ajettu, konsolidoi löydökset:

### Konsolidointi-rakenne

```markdown
# Suomi-tarkistus – yhteenveto

## Kontekstin tunnistus
- Tekstityyppi: [esim. markkinointikopio, verkkosivun pääsivu]
- Kohderekisteri: [esim. ammattikieli]
- YMYL: [kyllä/ei, alue]
- Ajettu pipeline: [A / B / C / D / E / F / G / H / I / J]

## Löydökset per skill

### Rekisteri ([[suomi-rekisteri]])
- [Löydös 1]
- [Löydös 2]

### AI-kuvioiden puhdistus ([[suomi-ei-ai-sloppia]])
- Kuvio X: [konkreettinen virke + korjausehdotus]
- Kuvio Y: [konkreettinen virke + korjausehdotus]

### Anglismit ([[suomi-anglismit]])
- [Löydös 1]

### Mekaniikka ([[suomi-kielihuolto]])
- Yhdyssanavirheet: [lista]
- Pilkutus: [lista]
- Sijamuodot/rektiot: [lista]
- Erisnimien taivutus: [lista]

## Lopullinen versio

[Kirjoita korjattu versio koko tekstistä, joka noudattaa kaikkia löydöksiä]

## Itse-audit

"Mikä tästä on edelleen AI-makuista?" – käy lyhyesti läpi.

[Vastaa kysymykseen, korjaa jäljelle jääneet kuviot, esitä lopullinen versio]
```

## VAIHE 4 – Iterointi

Jos itse-auditissa löytyi vielä AI-kuvio-merkkejä:

1. Käy ne läpi
2. Korjaa
3. Esitä uudelleen-tarkistettu lopullinen versio

Korkeintaan kaksi iteraatiokierrosta. Jos kolmannella kierroksella on vielä AI-merkkejä, kerro käyttäjälle, ettei lopullinen versio ole täysin puhdas, mutta on niin lähellä kuin järkevillä rajauksilla pääsee.

## YLEISIÄ PERIAATTEITA

### Älä ohita skilliä ilman syytä

Jokaisella skillillä on roolinsa pipelinessä. Ohittamisen pitää olla harkittu päätös (esim. selkokielessä `suomi-ei-ai-sloppia` ei ole pääpriorisoitu).

### Älä aja samaa skilliä kahdesti

Jos skillin löydökset on jo käsitelty, älä aja sitä uudelleen.

### Tunnista konteksti ennen valintaa

Pipelinejen valinnan pohja on konteksti. Älä aja Pipeline A:ta jokaiselle tekstille – some-postaus ansaitsee Pipeline B:n, YMYL Pipeline C:n.

### Ei käyttäjän tehtäväksi muistaa skillinimiä

Käyttäjä sanoo "aja suomi-tarkistus" ja saa yhden raportin. Skillinimiä ei tarvitse muistaa – orkestraattori valitsee ne kontekstista.

### Älä piilota löydöksiä

Lopulliseen raporttiin tulee kaikki löydökset jokaiselta skilliltä – myös pienet. Käyttäjä päättää itse miten paljon korjaa.

### Sisältösarjan toistotarkistus

Nämä skillit tarkistavat yhden tekstin kerrallaan, joten ne eivät rakenteellisesti näe toistuvaa kaavaa sarjan sisällä – samaa lopetuskappaletta, johdantokoukkua tai perustelufraasia kierrätettynä monessa artikkelissa. Kun tuotat tai editoit sisältösarjaa (esimerkiksi pSEO-sivut, blogisarja tai useampi laskeutumissivu), aja lisäksi sarjatason vertailu: lue kaikki osat yhdessä ja merkitse lähes sanatarkasti toistuvat kappaleet. Yksittäisen tekstin slop-tarkistus ei tätä havaitse.

## YHTEENVETO – orkestraattori-tarkistuslista

```
[ ] Vaihe 0: konteksti tunnistettu (tekstityyppi + YMYL + rekisteri)
[ ] Vaihe 1: oikea pipeline (A–J) valittu
[ ] Vaihe 2: jokainen skill pipelinessä ajettu, löydökset kerätty
[ ] Vaihe 3: löydökset konsolidoitu yhdeksi raportiksi
[ ] Vaihe 4: lopullinen korjattu versio kirjoitettu
[ ] Vaihe 4: itse-audit "mikä jäi AI-makuiseksi?" tehty
[ ] Iteraatio jos tarpeen – max 2 lisäkierrosta
```

## TULOS

Käyttäjälle palautetaan **yksi konsolidoitu yhteenveto**, joka sisältää:

1. Tunnistettu konteksti
2. Käytetty pipeline
3. Löydökset per skill
4. Lopullinen korjattu versio
5. Itse-audit

Käyttäjän ei tarvitse erikseen muistaa eikä ajaa skillejä, koska orkestraattori on tehnyt sen hänen puolestaan.
