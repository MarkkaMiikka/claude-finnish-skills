---
name: suomi-hakemuspaketti
description: >
  Räätälöi suomenkielinen CV ja hakemuskirje tiettyyn avoimena olevaan työtehtävään markdown-muodossa. Käytä kun käyttäjä antaa työpaikkailmoituksen ja taustatietonsa, tai sanoo "räätälöi CV", "tee hakemus", "rakenna hakemuspaketti", "tee CV [yritykselle]", "kirjoita hakemuskirje", "muokkaa CV tähän hakuun", "hakemus [yritykselle/roolille]". Tuottaa kaksi markdown-tiedostoa (CV.md ja Hakemuskirje.md) sekä ohjeet niiden muuntamiseksi Word- tai PDF-muotoon. EI sovellu pelkkään yleiseen CV-neuvontaan ilman kohdetyöpaikkaa. Ketjuttaa pakollisina [[suomi-ei-ai-sloppia]]-, [[suomi-kielihuolto]]- ja [[suomi-anglismit]]-skillit lopputuloksen tarkistukseen.
license: MIT
---

# Suomenkielisen hakemuspaketin räätälöinti

> **Vinkki:** Jos haluat ajaa kaikki suomi-* -skillit yhdessä oikeassa järjestyksessä, käytä `[[suomi-tarkistuslista]]` -orkestraattoria.

Tämä skill räätälöi suomenkielisen CV:n ja hakemuskirjeen yhteen tiettyyn avoinna olevaan työtehtävään. Tuottaa kaksi markdown-tiedostoa, jotka käyttäjä muuntaa haluamallaan tavalla Word- tai PDF-muotoon.

**Pelkkä yleinen CV-neuvonta:** ei kuulu tämän skillin alaan. Tämä on tuotantotyökalu, ei keskustelu. Tarvitaan työpaikkailmoitus ja hakijan tausta.

---

## 1. Vaadittava input

Pyydä käyttäjältä ennen kuin aloitat:

1. **Työpaikkailmoituksen koko teksti** – tai linkki, jonka käyttäjä lukee ja kopioi
2. **Hakijan tausta** – joko olemassa oleva CV (mikä tahansa muoto) tai vapaamuotoinen kuvaus
3. **Hakijan yhteystiedot** – etu- ja sukunimi, puhelin, sähköposti, kaupunki, LinkedIn-profiili
4. **Mahdolliset rajaukset** – esim. "älä mainitse X-tehtävää" tai "korosta Y-osaamista"

Jos jotain puuttuu, kysy. Älä keksi hakijan taustaa.

---

## 2. Prosessi

### Vaihe 1: Analysoi työpaikkailmoitus

Pura ilmoitus seuraaviin osiin:

- **Pakolliset vaatimukset** – "vaadimme", "edellytetään", "tulee olla"
- **Toivotut taidot** – "katsomme eduksi", "plussaa", "toivomme"
- **Painotetut termit** – sanat, jotka toistuvat tai joita on lihavoitu
- **Kulttuurivinkit** – yrityksen tapa kirjoittaa (esim. "tiimimme on rento" → vältä yliformaali sävy)
- **Pyydetyt liitteet** – joskus pyydetään palkkatoive, portfolio, suosittelijat

### Vaihe 2: Sovita hakijan tausta ilmoituksen kieleen

Käy hakijan tausta läpi ja **valitse** mitkä bulletit nousevat CV:n kärkeen. Älä yritä kertoa kaikkea – valitse 70 % sisällöstä, joka vastaa ilmoitusta.

Vastaavuus tarkoittaa kahta asiaa:
- **Sisältö vastaa** ilmoituksen vaatimuksiin
- **Sanasto vastaa** ilmoituksen sanoja. Jos ilmoituksessa lukee "data-analytiikka", käytä samaa termiä; älä vaihda sitä esimerkiksi "datatieteeksi"

### Vaihe 3: Kirjoita CV.md

Käytä kohdassa 3 olevaa rakennetta.

### Vaihe 4: Kirjoita Hakemuskirje.md

Käytä kohdassa 4 olevaa rakennetta.

### Vaihe 5: Aja tarkistukset

Pakollinen ketjutus:
- [[suomi-ei-ai-sloppia]] – erityisesti kuvio 31 (suomalainen humble brag) ja kuvio 7 (AI-sanasto)
- [[suomi-kielihuolto]] – yhdyssanat, pilkutus, sijamuodot
- [[suomi-anglismit]] – käännöslainat (poikkeus: alan vakiintuneet termit kuten "orgaaninen", "brieffata", "konversio" säilytetään)

### Vaihe 6: Anna muunto-ohjeet

Loppuun anna käyttäjälle ohjeet markdown-tiedostojen muuntamiseen .docx- tai .pdf-muotoon (ks. kohta 6).

---

## 3. CV.md – rakenne ja konventiot

### 3.1 Yleisrakenne

```markdown
# Etunimi Sukunimi

[tagline yhdellä rivillä – esim. "Markkinointi · AI · Konsultointi"]

[Kaupunki, Suomi] · [puhelin] · [sähköposti] · [linkedin.com/in/...]

---

## Tiivistelmä

[2–3 virkettä. Konkreettinen, ei kliseinen "intohimoinen ammattilainen"]

## Työkokemus

### Titteli, [työnantaja] ([kuukausi/vuosi]–[kuukausi/vuosi tai nyk.])

- [Bullet 1: konkreettinen toiminta + mitattu tulos]
- [Bullet 2: konkreettinen toiminta + mitattu tulos]
- [Bullet 3: konkreettinen toiminta + mitattu tulos]

### Titteli, [työnantaja] ([jaksot])

- [bullet]
- [bullet]

## Osaaminen

### [Pääalue 1]
- [taito]
- [taito]

### [Pääalue 2]
- [taito]
- [taito]

## Koulutus

### [Tutkinto], [oppilaitos] ([vuodet])
[Pääaine, sivuaine, mahdollinen lopputyön aihe yhdellä rivillä]

## Kielet

- Suomi – äidinkieli
- Englanti – [erinomainen / hyvä / tyydyttävä / alkeet]
- [Muu kieli] – [taso]

## Suosittelijat

Pyydettäessä.
```

### 3.2 Tiivistelmän kirjoittaminen

**Hyvä tiivistelmä:**
- 2–3 virkettä, ei enempää
- Mainitsee 1–2 erottavaa konkretiaa
- Suora, ei mahtipontinen
- Ei AI-fraaseja ("intohimoinen", "tuloksellinen ammattilainen", "ainutlaatuinen kokemus")

**Esimerkki:**

> Digitaalisen markkinoinnin asiantuntija neljän vuoden kokemuksella B2B SaaS -projekteista. Olen vetänyt monikanavaisia liidikampanjoita (LinkedIn Ads, Google Ads, sähköposti) ja kasvattanut uutiskirjeen tilaajamäärän 1 200 tilaajasta 4 200:aan orgaanisella jakelulla.

### 3.3 Bullet-konventio

Yksi bullet = **konkreettinen toiminta** + **mitattu tulos** + (mahdollisesti) **konteksti**.

**Hyvä:**
> Kasvatin uutiskirjeen tilaajamäärän 800 → 3 500 maksuttomalla jakelulla 14 kuukaudessa.

**Heikko:**
> Vastasin sisältömarkkinoinnista ja kehitin viestintää.

Jos numeroa ei ole, käytä konkreettista lopputulosta (lanseeraus, asiakas, tulos).

### 3.4 Bullet-määrä per rooli

- Nykyinen tai keskeinen rooli: 4–6 bullettia
- Vanhempi rooli: 2–3 bullettia
- Yli 10 vuotta vanha rooli: 1 bullet tai vain rivi

Jätä pois roolit, jotka eivät tue hakua. Älä tunge kaikkea CV:hen.

### 3.5 Yhdyssanojen kärki – tarkista nämä

- markkinointistrategia, markkinointiviestintä, markkinointiosasto
- asiakaskokemus, asiakaspalvelu, asiakaspysyvyys
- sisällöntuotanto, sisällönhallinta
- liiketoiminta, liikevaihto
- työnkulku, työnkuvaus
- tuotekehitys, tuotelanseeraus
- konversio-optimointi, konversioaste
- ei: "markkinointi strategia", "asiakas kokemus" (sanaliittoina vääriä)

### 3.6 Pituus

- Alle 5 vuoden kokemus: 1 sivu
- Yli 5 vuoden kokemus: 1–2 sivua maks.
- Yli 15 vuoden kokemus: 2 sivua maks., kondensoituna

---

## 4. Hakemuskirje.md – rakenne ja konventiot

### 4.1 Yleisrakenne

```markdown
[Päiväys: 27.5.2026]

[Vastaanottaja, jos tiedossa nimi tai titteli – "Aino Esimerkki, rekrytointivastaava" tai "Esimerkki Oy:n rekrytointitiimi"]

# Hakemus: [tehtävän nimi sellaisena kuin ilmoituksessa]

[Tervehdys – ks. kohta 4.2]

[Avauskappale – ks. kohta 4.3]

[Keskikappale 1 – ks. kohta 4.4]

[Keskikappale 2, jos tarvitaan]

[Lopetuskappale – ks. kohta 4.5]

[Lopetussanat]

[Allekirjoitus: etunimi sukunimi]

[Yhteystiedot]
```

### 4.2 Tervehdys

Hierarkia:

| Konteksti | Tervehdys |
|---|---|
| Rekrytointivastaava tiedossa | `Hyvä [Etunimi Sukunimi]` |
| Vain rooli tiedossa | `Hyvä rekrytointivastaava` |
| Vain yritys tiedossa | `Hyvä Esimerkki Oy:n rekrytointitiimi` |
| Mikään ei tiedossa | `Hyvä vastaanottaja` |

Vältä `Arvoisa vastaanottaja` paitsi viranomaisten rekrytoinneissa.

### 4.3 Avauskappale

**Tavoite:** kerro **miksi haet juuri tätä paikkaa** kahdessa virkkeessä. Ei kliseinen "Hain juuri tätä tehtävää, koska olen erittäin kiinnostunut".

**Tehoton avaus (vältä):**
> Olen erittäin kiinnostunut markkinointiasiantuntijan tehtävästä Esimerkki Oy:ssä. Uskon että olisin hyvä lisä tiimiinne.

**Hyvä avaus:**
> Hain Esimerkki Oy:n markkinointiasiantuntijan paikkaa, koska asiakaskuntanne (B2B SaaS -kasvuyritykset) vastaa täsmälleen sitä, mitä olen tehnyt kaksi viime vuotta. Edellisessä roolissani liidikonversio nousi 22 % yhden kvartaalin aikana, ja kampanjoiden raportointi yhdenmukaistui.

Avaus voi viitata:
- Yrityksen julkiseen tekemiseen (artikkeli, kampanja, tuotelanseeraus)
- Ilmoituksen erityispiirteeseen
- Yhteiseen kontaktiin (nimellä, jos lupa)
- Hakijan kokemukseen, jolla on suora yhteys rooliin

### 4.4 Keskikappale: konkretia

**Tavoite:** todista 1–2 keskeisellä esimerkillä, että osaat mitä ilmoitus pyytää. **Älä toista CV:tä rivi riviltä.** Kerro tarina, jonka CV:n bullet vain mainitsee.

**Esimerkki:**
> Edellisessä työssäni vedin SaaS-asiakkaan liidituotantokampanjan, jonka kuukausibudjetti oli viisinumeroinen. Optimoin sen MQL-konversion mukaan ja koordinoin sisällöntuotannon kahden ulkopuolisen kumppanin kanssa. Konversio nousi 22 % ja samalla asiakashankintakustannus laski. Tämä työ vaati sekä mainostyökalujen käytännön hallintaa että tiivistä kommunikointia asiakkaan kanssa.

Pidä keskikappaleet **1–2 kappaletta** (yhteensä noin 150–250 sanaa).

### 4.5 Lopetuskappale

**Tavoite:** kerro mitä haluat tapahtuvan seuraavaksi. Suomalainen kohteliaisuus on suora.

**Hyvä:**
> Olen käytettävissä tapaamiseen ensi viikolla. Sopiiko keskustelu vielä kesäkuun 5. päivä?

**Vältä:**
> Olen erittäin innoissani mahdollisuudesta keskustella kanssanne ja toivon, että voimme jatkaa yhteistyötä tulevaisuudessa.

### 4.6 Lopetus ja allekirjoitus

```
Ystävällisin terveisin

Aino Esimerkki
+358 40 000 0000
aino.esimerkki@example.fi
```

### 4.7 Pituus

Maks. 1 sivu. Kolme kappaletta (avaus + keskikappale + lopetus) on yleensä riittävä. Tiukassa rajoituksessa kahden kappaleen versio toimii.

---

## 5. Anti-patternit

### 5.1 CV:n anti-patternit

| Anti-pattern | Miksi vältä | Korjaus |
|---|---|---|
| "Intohimoinen markkinoinnin ammattilainen" | AI-fraasi | Konkreettinen erottava tieto |
| "Tuloksellisesti johtanut tiimejä" | Mitäs tarkalleen? | "Johdin 6 hengen tiimin Q1–Q3, projekti X valmistui aikataulussa" |
| Lista verbejä ilman tuloksia | Ei sisältöä | Verbi + numero + konteksti |
| Kaikki työkokemus 10+ vuoden takaa täydessä laajuudessa | Vie tilan tärkeämmältä | Tiivistä vanhat roolit yhteen riviin |
| "Vastasin..." joka rivissä | Yksitoikkoista | Vaihtelevat verbit: rakensin, kasvatin, tuotin, optimoin, lanseerasin |
| Hard skills ja soft skills sekaisin yhteen luetteloon | Hämmentää | Erottele: tekninen osaaminen vs. johtamis- ja vuorovaikutusosaaminen |
| Englanninkielisiä tittelejä keskellä suomenkielistä CV:tä | Sekavaa | Käännä, tai pidä englanniksi, jos rooli oli englanniksi (esim. "Account Manager") |

### 5.2 Hakemuskirjeen anti-patternit

| Anti-pattern | Miksi vältä | Korjaus |
|---|---|---|
| "Olen erittäin kiinnostunut" -avaus | Lähes joka hakija kirjoittaa näin | Konkreettinen syy juuri tähän paikkaan |
| CV:n toisto rivi riviltä | Tila menee hukkaan | Kerro tarina, jonka CV vain mainitsee |
| "Tiedän, että voisin tuoda lisäarvoa..." | AI-fraasi, tyhjä | Konkreettinen esimerkki mitä toisit |
| Liika kohteliaisuus ("ihmettelisin, jos suvaitsisitte harkita") | Suomalainen suoruus on arvoa | "Sopisiko keskustelu ensi viikolla?" |
| Kolmiosaiset listat ("luovuutta, asiantuntemusta ja sitoutumista") | AI-tyyppinen | Yksi konkreettinen esimerkki |
| Yhteenveto ilman pyyntöä lopussa | Lukijalle epäselvää mitä haluat | "Sopiiko 20 minuutin keskustelu ensi viikolla?" |
| Englannin "Looking forward to hearing from you" -käännös | Suomeksi väkinäinen | Jätä pois tai "Vastausta odottaen" |

### 5.3 Yhteiset anti-patternit

- Ajatusviivan (–) ylikäyttö (max 1 koko hakemuksessa, mieluiten 0)
- Iso Alkukirjain Otsikoissa (vain ensimmäinen sana isolla suomessa)
- Emojit
- Lihavointi joka toisessa virkkeessä
- "Pre-launch", "data-driven", "result-oriented" -anglismit (käännä, paitsi alan vakiintunut termi)

---

## 6. Muunto markdown → .docx tai .pdf

Tämän skillin output on kaksi markdown-tiedostoa. Anna käyttäjälle ohjeet muuntaa ne haluamansa työkalun kanssa:

### 6.1 Pandoc (suositus, jos Pandoc on asennettu)

```bash
# CV markdownista wordiksi
pandoc CV.md -o CV.docx

# Hakemuskirje markdownista wordiksi
pandoc Hakemuskirje.md -o Hakemuskirje.docx

# Markdownista PDF:ksi (tarvitsee LaTeX-asennuksen)
pandoc CV.md -o CV.pdf --pdf-engine=xelatex -V mainfont="Arial"
```

Pandoc-asennus: [pandoc.org/installing.html](https://pandoc.org/installing.html). Saatavilla Windows, macOS ja Linux.

### 6.2 Google Docs (helpoin)

1. Avaa Google Docs
2. Kopioi markdown-tiedoston sisältö
3. Liitä Google Docsiin – markdown-rakenne säilyy yleensä hyvin
4. Tarkista muotoilu silmämääräisesti
5. Tiedosto → Lataa → Microsoft Word (.docx) tai PDF (.pdf)

### 6.3 Markdown-editorit, joissa on vientitoiminto

- **Typora** (kaupallinen) – Tiedosto → Vie → Word / PDF
- **Obsidian** (ilmainen) – Vaatii vientilisäosan
- **VS Code** + Markdown PDF -laajennos – Komento "Markdown PDF: Export"
- **Marked 2** (macOS) – sisäänrakennettu vienti

### 6.4 ATS-yhteensopivuus

Useimmat työnhakujärjestelmät (ATS) lukevat .docx-tiedostot paremmin kuin PDF. Lähetä .docx jos ilmoitus ei spesifisti pyydä PDF:ää.

Pidä CV-rakenne yksinkertaisena: ei taulukkoja, ei sarakkeita, ei tekstilaatikoita. Markdown → Pandoc → .docx tuottaa luonnostaan ATS-yhteensopivan rakenteen.

---

## 7. Sanitoitu malliesimerkki – CV.md

```markdown
# Aino Esimerkki

Markkinointi · digitaalinen mainonta · sisältötyö

Espoo, Suomi · +358 40 000 0000 · aino.esimerkki@example.fi · linkedin.com/in/aino-esimerkki

---

## Tiivistelmä

Markkinoinnin ja maksetun mainonnan ammattilainen, jolla on neljän vuoden kokemus B2B SaaS -projekteista. Olen vetänyt monikanavaisia liidikampanjoita ja kasvattanut uutiskirjeen tilaajamäärän 1 200 → 4 200 orgaanisella jakelulla.

## Työkokemus

### Markkinointiasiantuntija, Esimerkki Oy (2024–nyk.)

- Hallinnoin LinkedIn Ads- ja Google Ads -kampanjoiden viisinumeroisia kuukausibudjetteja, optimoin MQL-konversion mukaan
- Koordinoin sisällöntuotannon kahden ulkopuolisen kumppanin kanssa, suunnittelin sisältöaikataulun kampanjadatan perusteella
- Kasvatin uutiskirjeen tilaajamäärän 1 200 → 4 200 14 kuukaudessa
- Vedin viikoittaisen raportoinnin pk-asiakkaille (kuusi asiakasta yhtäaikaisesti)

### Markkinointiassistentti, Esimerkki Yhtiöt (2022–2024)

- Tuotin sisältöä sosiaaliseen mediaan yhteistyössä mainostoimiston kanssa
- Vastasin Google Ads -kampanjoiden viikkoraportoinnista
- Avusin myynnin liidituotannossa (HubSpot)

## Osaaminen

### Maksettu mainonta
- LinkedIn Ads (Campaign Manager)
- Google Ads
- Meta Ads

### Sisältö ja analytiikka
- Looker Studio, Google Analytics 4
- Adobe CC (Photoshop, Premiere)
- A/B-testaus, konversio-optimointi

## Koulutus

### Kauppatieteiden maisteri (KTM), Esimerkki yliopisto, kauppakorkeakoulu (2022–2025)
Pääaine: markkinointi. Pro gradu: digitaalisten kanavien tehokkuusmittaus pk-yrityksissä.

### Kauppatieteiden kandidaatti (KTK), Esimerkki yliopisto (2018–2021)
Pääaine: liiketaloustiede.

## Kielet

- Suomi – äidinkieli
- Englanti – erinomainen
- Ruotsi – hyvä

## Suosittelijat

Pyydettäessä.
```

---

## 8. Sanitoitu malliesimerkki – Hakemuskirje.md

```markdown
27.5.2026

Esimerkki Oy
Mikko Mallikas, rekrytointivastaava

# Hakemus: markkinointiasiantuntija (rek. 2026-04)

Hyvä Mikko Mallikas,

Hain Esimerkki Oy:n markkinointiasiantuntijan paikkaa, koska asiakaskuntanne (B2B SaaS -kasvuyritykset) vastaa täsmälleen sitä, mitä olen tehnyt neljä viime vuotta. Edellisessä roolissani liidikonversio nousi 22 % yhden kvartaalin aikana, ja samalla raportointi yhdenmukaistui kuuden asiakkaan kesken.

Konkreettisin tehtäväni edellisessä työssäni oli SaaS-asiakkaan liidituotantokampanja. Kuukausibudjetti oli viisinumeroinen, ja optimoin sen MQL-konversion mukaan. Lisäksi koordinoin sisällöntuotannon kahden ulkopuolisen kumppanin kanssa ja suunnittelin sisältöaikataulun kampanjadatan perusteella. Tulos: konversio nousi 22 % ja asiakashankintakustannus laski 18 %. Tämä työ vaati käytännön kampanjarakentamista ja tiivistä yhteistyötä asiakkaan kanssa.

Lisäksi olen mentoroinut nuorempia markkinoinnin tekijöitä alan järjestön ohjelmassa kahden vuoden ajan. Olen siis nähnyt molemmat puolet: operatiivisen kampanjatyön ja osaamisen jakamisen tiimitasolla.

Olen käytettävissä tapaamiseen ensi viikolla. Sopiiko keskustelu kesäkuun 5. päivä, vai onko muu ajankohta parempi?

Ystävällisin terveisin

Aino Esimerkki
+358 40 000 0000
aino.esimerkki@example.fi
```

---

## 9. Tarkistuslista ennen palautusta käyttäjälle

```
[ ] Otsikoita ja bulletteja ei ole liikaa; pituus 1–2 sivua CV:lle, 1 sivu hakemuskirjeelle
[ ] Tiivistelmä on 2–3 virkettä, sisältää konkretiaa
[ ] Bulletit ovat muotoa: konkreettinen toiminta + mitattu tulos
[ ] Yhdyssanat tarkistettu (markkinointistrategia, asiakaspalvelu jne.)
[ ] Päivämäärät muodossa pp.kk.vvvv
[ ] Numerot suomen muodossa (12 500 €, 22 %, alle 10 sanoin)
[ ] Otsikot vain ensimmäinen sana isolla
[ ] Ei AI-fraaseja ("intohimoinen", "ainutlaatuinen", "tuloskeskeinen")
[ ] Ei kolmiosaisia listoja
[ ] Ei ajatusviivan ylikäyttöä (max 1 koko paketissa)
[ ] Ei emojeja
[ ] Hakemuksen avaus ei ole "Olen erittäin kiinnostunut..."
[ ] Hakemuksen lopussa on selkeä pyyntö (keskustelu, tapaaminen, ajankohta)
[ ] Sähköpostiosoite ja puhelinnumero tarkistettu
[ ] LinkedIn-linkki toimii ja vastaa hakemusta
[ ] [[suomi-ei-ai-sloppia]] ajettu, erityisesti kuvio 31 (humble brag)
[ ] [[suomi-kielihuolto]] ajettu (yhdyssanat, pilkutus, sijamuodot)
[ ] [[suomi-anglismit]] ajettu (huom: säilytä alan vakiintuneet termit kuten orgaaninen, brieffata, konversio)
[ ] Pandoc- tai Google Docs -muunto-ohjeet annettu käyttäjälle
```

---

## 10. Mihin tätä skilliä konsultoidaan

- [[suomi-tarkistuslista]] – pipeline F: hakemus/CV
- [[suomi-rekisteri]] – ammattikieli + henkilökohtainen sävy
- [[suomi-ei-ai-sloppia]] – pakollinen ketjutus, erityisesti kuvio 31 humble brag
- [[suomi-kielihuolto]] – pakollinen mekaniikkatarkistus
- [[suomi-anglismit]] – pakollinen, huomioiden alan vakiintunut sanasto
- [[suomi-sahkoposti]] – jos hakemus lähetetään sähköpostitse (saateviestin muoto)
- [[suomi-lokalisaatio-perus]] – päivämäärät, numerot, yhteystiedot
