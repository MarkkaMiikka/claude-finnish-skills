---
name: suomi-sahkoposti
description: >
  Suomenkielisen sähköpostin konventiot — tervehdys, lopetus, otsikko, asiakohtaisen viestin runko, allekirjoitus ja poissaoloviesti. Käytä kun kirjoitat asiakasviestiä, työsähköpostia, sisäistä viestiä tai cold outreach -viestiä, tai kun käyttäjä sanoo "kirjoita sähköposti", "tee mailin pohja", "muotoile työsähköposti", "vastaa asiakkaalle", "kirjoita asiakaspalveluviesti", "B2B-sähköposti", "rekrytointiviesti", "poissaoloviesti" tai "muotoile lähetän tämän asiakkaalle". Ei käsittele uutiskirjettä — käytä siihen [[suomi-uutiskirje]]. Konsultoi [[suomi-sinuttelu-teitittely]] -skilliä puhuttelumuodon valinnassa.
license: MIT
---

# Suomenkielisen sähköpostin konventiot

> **Vinkki:** Jos haluat ajaa kaikki suomi-* -skillit yhdessä oikeassa järjestyksessä, käytä `[[suomi-tarkistuslista]]` -orkestraattoria.

Tämä skill tarjoaa sähköpostin rakenteen ja kielelliset konventiot. Yhdistä:
- [[suomi-sinuttelu-teitittely]] — puhuttelumuoto
- [[suomi-rekisteri]] — rekisterin tasaisuus
- [[suomi-ei-ai-sloppia]] — AI-fraasien karsinta
- [[suomi-anglismit]] — käännöslainojen karsinta
- [[suomi-kielihuolto]] — mekaniikka

---

## 1. Otsikko (subject line)

Otsikko on tärkein osa sähköpostia avaamisen kannalta. Suomenkielinen B2B-otsikko on **kuvaileva, ei klikkitavoitteinen**.

### 1.1 Hyvä otsikko

- Sisältää keskeisen asian tai pyynnön
- 30–70 merkkiä
- Ei huutomerkkejä
- Ei suuraakkosia
- Sisältää viitteen jos kyseessä on jatkokirje

### 1.2 Esimerkit

| Konteksti | Otsikko |
|---|---|
| Tarjouspyyntö | `Tarjouspyyntö: markkinointikampanja Q3 2026` |
| Sopimusasia | `Allekirjoitus puuttuu — sopimus #2026-117` |
| Vastaus tarjoukseen | `Vs: Tarjouspyyntö: markkinointikampanja Q3 2026` |
| Kokouspyyntö | `Kokousehdotus: 12.6. klo 14` |
| Hakemus | `Hakemus: markkinointiasiantuntija (rek. 2026-04)` |
| Reklamaatio | `Toimituksen viive: tilaus 17789` |

### 1.3 Vältä

- `Tärkeää!`, `Kiireellinen!!`
- `Hei!` (ei sisällä asiaa)
- `Heippa, juteltaisko?` (epämääräinen)
- `RE: RE: FW: RE: ...` (siivoa pitkät ketjut)

### 1.4 "Vs:" vai "Re:"

Suomessa molemmat ovat hyväksyttäviä. `Vs:` on suomenkielinen vakiomuoto, mutta useimmat sähköpostiohjelmat lisäävät `Re:` -muodon automaattisesti. Älä korjaa sitä jos järjestelmä lisää sen — se on standardia.

---

## 2. Tervehdys

### 2.1 Hierarkia

| Konteksti | Tervehdys |
|---|---|
| B2B oletus | `Hei [Etunimi]` |
| Tuntematon vastaanottaja, ammattimainen | `Hyvä [Titteli] [Sukunimi]` |
| Tuntematon vastaanottaja, neutraalimpi | `Hei` (yksinään, ilman nimeä) |
| Viranomaiskirje | `Arvoisa vastaanottaja` tai `Hyvä [Titteli]` |
| Kollegan kanssa | `Moi [Etunimi]` tai `Hei [Etunimi]` |
| Asiakkaan kanssa, jonka nimeä ei tiedetä | `Hyvä asiakas` |

### 2.2 Mitä vältät

- `Tervehdys` — vanhahtava, harvoin sopiva
- `Hyvät naiset ja herrat` — sukupuolittava, vanhentunut
- `Hi [name]` tai `Hello [name]` — englantilaisia
- `Moikka!` huutomerkillä kollegan kanssa — huutomerkki yleensä turha

### 2.3 Tervehdyksen ja nimen pilkutus

Tervehdyksen jälkeen pilkku ja seuraava rivi alkaa pienellä, **paitsi** jos seuraava sana on erisnimi tai virkkeen luonnollinen alku.

```
Hei Aino,

kiitos viestistä.
```

```
Hei Aino,

Kiitos viestistä. Palaan asiaan ensi viikolla.
```

Kummatkin ovat hyväksyttäviä. Useimmat kirjoittajat aloittavat seuraavan rivin isolla, koska se aloittaa uuden virkkeen ja kappaleen.

---

## 3. Avaus

### 3.1 Suomalainen avaus menee suoraan asiaan

Englannin "Hope you're well" -tyylinen kuulumisten kysely ei käännetä suomeksi luonnollisesti. Aloita asiasta.

**Sopiva avaus B2B-yhteydessä:**
- `Kiitos viestistä.` (jos vastaat aiempaan viestiin)
- `Lähestyn sinua [aiheen] tiimoilta.`
- `Sain yhteystietosi [henkilöltä/lähteestä] ja [konteksti].`
- `Olemme [yritys], ja [kontekstin avaus].`

**Vältä:**
- `Toivottavasti voit hyvin` (käännöslaina)
- `Kiitos että vastasit niin nopeasti` (jos vastaus ei tullut nopeasti, tämä kuulostaa passiivis-aggressiiviselta; jos tuli, riittää yksi "Kiitos viestistä")
- `Lähestyn sinua tällä kertaa...` (turha pidennys; lähestyt aina jostain syystä)

### 3.2 Vastausviestissä

Jos vastaat aiempaan viestiin, älä kuluta tilaa kiittelemällä. Mene asiaan.

✅ `Kiitos viestistä. Toimituspäivä sopii — varaan ajan kalenteriin.`

❌ `Kiitos paljon viestistäsi, ja kiitos siitä että otit yhteyttä minuun näin nopeasti. Olen erittäin iloinen vastauksestasi. Tämä on todella mukavaa, että voimme keskustella tästä asiasta.`

---

## 4. Runko

### 4.1 Yksi asia per kappale

Pidä kappaleet lyhyinä — 2–4 virkettä on hyvä ohje sähköpostissa. Mobiilissa pitkät kappaleet jäävät lukematta.

### 4.2 Pyyntömuodot

| Muoto | Sävy | Käyttö |
|---|---|---|
| `Voitko...` | Suora, pehmeä imperatiivi | Oletus B2B-yhteydessä |
| `Voisitko...` | Kohtelias | Kun pyyntö on poikkeuksellinen tai kuormittava |
| `Voisitteko...` | Kohtelias, teitittely | Teitittelyssä |
| `Olisitteko ystävällinen ja...` | Erittäin kohtelias | Sensitiivinen tilanne, viranomaiskirje |
| `Haluatko...` | Kysyy halua | EI pyyntönä — käytä vain jos kysyt aitoa halua |
| `Lähetä` (käsky) | Suora | Sopii kun tilanne sallii, esim. tukipyyntö |

**Esimerkki:**
- ✅ `Voitko lähettää sopimuksen tämän viikon aikana?`
- ❌ `Haluatko lähettää sopimuksen tämän viikon aikana?` (kuulostaa siltä että kysytään halua)

### 4.3 Konkretia ennen pyyntöä

Kun pyydät jotain, kerro **mitä tarvitset, miksi ja mihin mennessä** yhdessä lauseessa.

✅ `Voitko lähettää Q2-raportin perjantaihin mennessä, jotta saan tehtyä yhteenvedon ennen tiimipalaveria?`

❌ `Olisi mahtavaa jos voisit harkita raportin lähettämistä.`

### 4.4 Numerot ja päivämäärät

Käytä [[suomi-lokalisaatio-perus]] -ohjeita:
- Päivämäärä: `12.6.2026 klo 14.30`
- Hinta: `12 500 € (ALV 0 %)`
- Aikaväli: `viikolla 24` tai `10.–14.6.`

---

## 5. Lopetus

### 5.1 Hierarkia

| Lopetus | Sävy | Käyttö |
|---|---|---|
| `Ystävällisin terveisin` | Turvallinen valinta | Oletus lähes kaikkialla |
| `Terveisin` | Neutraali, lyhyt | Kollegan kanssa, B2B-jatkoviesti |
| `Parhain terveisin` | Hieman lämpimämpi | Pitkäaikainen yhteistyö |
| `Kiitos` tai `Kiittäen` | Alleviivaa kiitollisuus | Kun pyydät palvelusta tai vastauksen |
| `Mukavaa viikonloppua` / `Hyvää viikkoa` | Rento, lämmin | Loppuviikolla kollegan kanssa |

### 5.2 Vältä

- `Have a great day!` -käännös: `Mukavaa päivää!` — kuulostaa AI-tuotetulta, käytä harkitusti. Suomalainen sähköposti loppuu yleensä terveisiin, ei toivotukseen.
- `Cheers` tai `BR` (best regards) — englantilaisia
- `xoxo`, `T:` — liian rentoja työyhteydessä
- Tyhjä loppu ilman terveisiä — ei sopiva

### 5.3 Lopetuksen ja allekirjoituksen muotoilu

```
Ystävällisin terveisin

Aino Esimerkki
Markkinointiasiantuntija
Esimerkki Oy
```

Lopetus omalle rivilleen, tyhjä rivi, sitten nimi.

---

## 6. Allekirjoituslohko

### 6.1 Vakiomuoto

```
Aino Esimerkki
Markkinointiasiantuntija
Esimerkki Oy
+358 40 000 0000
aino.esimerkki@example.fi
```

### 6.2 Laajennettu (myynti, ulkoinen yhteydenpito)

```
Aino Esimerkki
Markkinointiasiantuntija
Esimerkki Oy

+358 40 000 0000
aino.esimerkki@example.fi
www.example.fi

Y-tunnus: 1234567-8
```

### 6.3 Vältä allekirjoituksessa

- Lainauksia ("Tavoittele unelmiasi!" -tyyliset)
- Emojeja tunnusten edessä
- Pitkiä disclaimer-tekstejä paitsi kun yritys vaatii
- AI-fraaseja, esim. "Empowering businesses to..." tai "Have a great day!"

---

## 7. Kategoriakohtaiset konventiot

### 7.1 B2B-asiakasviesti

Sinuttelu, kuvaileva otsikko, suora asia, allekirjoitus titteleineen.

```
Otsikko: Tarjouspyyntö: markkinointikampanja Q3 2026

Hei Aino,

Kiitos eilisestä keskustelusta. Lähetän alla pyydetyt tiedot Q3-kampanjasta.

Kampanjan kohderyhmä on 25–45-vuotiaat pk-yritysten päättäjät pääkaupunkiseudulla. Budjetti on 25 000 € (ALV 0 %), ja kampanja ajetaan 1.7.–31.8.2026.

Tarvitsen tarjouksen 12.6.2026 mennessä. Sopiiko keskustelu vielä ensi viikon perjantain aikana, jos tarvitset tarkennuksia?

Ystävällisin terveisin

Mikko Mallikas
Markkinointipäällikkö
Esimerkki Oy
```

### 7.2 B2C-asiakaspalveluviesti

Sinuttelu (alle 70-v. asiakkaalle), lämmin sävy, konkreettinen vastaus.

```
Otsikko: Vs: Tilaus 17789 — toimituspäivä

Hei Aino,

Kiitos viestistä. Tarkistin tilauksesi: paketti on lähetetty 5.6.2026 ja sen pitäisi olla perillä viimeistään 9.6.2026.

Sait sähköpostiin lähetyslinkin tilausvahvistuksen yhteydessä. Jos linkki ei toimi, voin lähettää sen uudelleen.

Ystävällisin terveisin

Mikko Mallikas
Asiakaspalvelu, Esimerkki Oy
```

### 7.3 Sisäinen viestintä kollegalle

Sinuttelu, lyhyt asia, ei pitkiä muodollisuuksia.

```
Otsikko: Q2-raportti perjantaina

Hei Aino,

Voitko lähettää Q2-raportin perjantaihin 13.6. mennessä? Tarvitsen sen tiimipalaveriin maanantaina.

Kiitos.

Terveisin
Mikko
```

### 7.4 Viranomais- tai instituutio-yhteydenotto

Teitittely tai sinuttelu kontekstin mukaan. Selkeä otsikko, asiaan suoraan, asialliset perustelut.

```
Otsikko: Hakemuksen täydennys, asia 2026/123

Arvoisa vastaanottaja,

Lähetän pyydettyjä lisätietoja 23.5.2026 jätettyyn hakemukseen (asia 2026/123).

Liite 1: lääkärintodistus 22.5.2026
Liite 2: työnantajan vahvistus 24.5.2026

Pyytäkää tarvittaessa lisätietoja.

Ystävällisin terveisin

Aino Esimerkki
+358 40 000 0000
```

### 7.5 Kylmä myyntiviesti (cold outreach)

Lyhyt, henkilökohtainen, tarjoaa konkreettista arvoa. Ei myyntipuheita.

```
Otsikko: 22 %:n konversionousu — kiinnostaisiko keskustelu?

Hei Aino,

Sain yhteystietosi LinkedInistä, jossa kirjoitit Esimerkki Oy:n digikanavien remontista. Olemme tehneet samaa työtä kahdelle vastaavalle pk-yritykselle viime vuonna, ja keskimäärin konversio nousi 22 %.

Sopisiko 20 minuutin keskustelu ensi viikolla? Voin näyttää konkreettisesti, mitä teimme.

Terveisin

Mikko Mallikas
Esimerkki Oy
+358 40 000 0000
```

---

## 8. Sähköpostiketjut

### 8.1 Lainaamisen periaatteet

- Lainaa **vain olennainen osa**, ei koko ketjua
- Jos lainaat, käytä `>`-merkkiä tai sähköpostiohjelman lainausta
- Pitkän ketjun ylin viesti on tärkein — pidä se ensimmäisenä

### 8.2 Vastauksen rakenne pitkässä ketjussa

```
Hei Aino,

[lyhyt vastaus tai uusi sisältö]

> Aiempi viesti, johon vastataan:
> [lainattu kohta]

Ystävällisin terveisin
Mikko
```

### 8.3 Viestin välittäminen eteenpäin

Kun välität viestin eteenpäin (`Lähetä eteenpäin` / `Fwd:`), lisää lyhyt selitys siitä, miksi välität sen ja mitä toivot vastaanottajalta.

```
Otsikko: Fwd: Tilaus 17789 — toimituspäivä

Hei Mikko,

Voitko vastata Ainolle? Hän kysyy toimituspäivästä, ja tieto on sinun puolellasi.

Kiitos.

Terveisin
Aino
```

---

## 9. Poissaoloviesti (out-of-office)

### 9.1 Vakiorakenne

```
Hei,

Olen lomalla 14.–28.7.2026. En lue sähköpostia tänä aikana.

Kiireellisissä asioissa ota yhteyttä Mikko Mallikkaaseen (mikko.mallikas@example.fi, +358 40 000 0000).

Palaan asiaan paluuni jälkeen.

Ystävällisin terveisin

Aino Esimerkki
Esimerkki Oy
```

### 9.2 Vältä poissaoloviestissä

- "Vastaan viestiin niin pian kuin mahdollista" — sano milloin oikeasti vastaat
- Pitkät tarinat (`Olen viettämässä aikaa perheen kanssa Italiassa...`) — yksityistä, älä jaa
- Englanninkielisiä rinnakkaisversioita ilman tarvetta — jos suomi on pääkieli ja kontekstit ovat suomalaisia, suomi riittää
- "Have a great day!" -lopetusta

### 9.3 Lyhempi versio (kollegan kanssa)

```
Olen lomalla 14.–28.7. Kiireellisissä asioissa: Mikko Mallikas, mikko.mallikas@example.fi.

Terveisin
Aino
```

---

## 10. Anti-patternit

### 10.1 AI-aloitukset

Vältä:
- `Olen erittäin iloinen voidessani ottaa yhteyttä...`
- `Toivottavasti tämä sähköposti tavoittaa sinut hyvänä päivänä.`
- `Tämä viesti koskee tärkeää asiaa...`
- `Tahtoisin tällä viestillä ilmoittaa...`

Ks. [[suomi-ei-ai-sloppia]] kohta 20 (chatbot-jäänteet).

### 10.2 Yliampuvat lopetukset

Vältä:
- `Olen erittäin kiitollinen ajastasi ja huomiostasi tässä asiassa.`
- `Toivottavasti voimme jatkaa hedelmällistä yhteistyötä.`
- `Yhdessä rakennamme parempaa tulevaisuutta!`

Käytä:
- `Kiitos.` (kun pyydät)
- `Ystävällisin terveisin` (kun ei muuta sanottavaa)

### 10.3 Liika pehmentäminen

Vältä:
- `Olisi mahtavaa jos voisit harkita...`
- `Pieni pyyntö jos sinulle sopii...`
- `Anteeksi että häiritsen, mutta voisitko...`

Suomalainen suora pyyntö on **kohtelias, ei tyly**. Liika pehmentely tuntuu vieraalta.

### 10.4 Ajatusviivan ylikäyttö

Useimmat ajatusviivat sähköpostissa korvaa pilkulla tai pisteellä. Ks. [[suomi-ei-ai-sloppia]] kohta 14.

### 10.5 Kolmiosaiset listat asiakohdissa

`Tarjoamme luovuutta, asiantuntemusta ja sitoutumista.` → tyypillinen AI-rakenne. Vaihda konkretiaan tai vähennä listan kokoa.

---

## 11. Tarkistuslista

```
[ ] Otsikko kuvaileva ja 30–70 merkkiä
[ ] Tervehdys sopii kontekstiin (Hei / Hyvä / Arvoisa)
[ ] Sinuttelu/teitittely yhtenäinen läpi viestin (ks. [[suomi-sinuttelu-teitittely]])
[ ] Avaus menee asiaan, ei käännöstyylistä kuulumisten kyselyä
[ ] Pyyntömuoto sopii (Voitko / Voisitko / Voisitteko)
[ ] Päivämäärät ja numerot suomen muodossa (12.6.2026, 12 500 €)
[ ] Lopetus normaali (Ystävällisin terveisin / Terveisin / Kiitos)
[ ] Allekirjoitus on selkeä ja sisältää tarvittavat yhteystiedot
[ ] Ei AI-aloituksia eikä yliampuvia lopetuksia
[ ] Ei kolmiosaisia listoja eikä ajatusviivan ylikäyttöä
[ ] Kappaleet lyhyitä (2–4 virkettä mobiilissa)
```

---

## 12. Mihin tätä skilliä konsultoidaan

- [[suomi-tarkistuslista]] — pipeline G: sähköposti
- [[suomi-uutiskirje]] — uutiskirjeen eri rakenne, vaikka jakaa allekirjoituselementit
- [[suomi-tarjous]] — tarjous on usein sähköpostin liitteenä, mutta tarjouksen muoto on omansa
- [[suomi-rekisteri]] — rekisterivalinta sähköpostissa
- [[suomi-sinuttelu-teitittely]] — puhuttelumuodon valinta
