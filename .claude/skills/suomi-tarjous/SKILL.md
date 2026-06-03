---
name: suomi-tarjous
description: >
  Suomalainen kaupallinen tarjous — rakenne, pakolliset elementit, ALV-erottelu, maksuehdot ja voimassaolo. Käytä kun rakennat tarjousta yritysasiakkaalle, freelance-tarjousta tai konsultointitarjousta, tai kun käyttäjä sanoo "tee tarjous", "muotoile tarjouspohja", "kirjoita kaupallinen tarjous", "tuotantotarjous", "freelance-tarjous", "konsultointitarjous", "B2B-tarjous", "ALV-erottelu" tai "maksuehdot". EI tee oikeudellista neuvontaa — viittaa Asianajajaliittoon kun käyttäjä pyytää sopimusehtojen sisältöä. Konsultoi [[suomi-lokalisaatio-perus]] -skilliä hinnoittelun muotoiluun ja [[suomi-sinuttelu-teitittely]] -skilliä asiakaspuhuttelumuotoon.
license: MIT
---

# Suomalaisen kaupallisen tarjouksen rakenne

> **Vinkki:** Jos haluat ajaa kaikki suomi-* -skillit yhdessä oikeassa järjestyksessä, käytä `[[suomi-tarkistuslista]]` -orkestraattoria.

Tämä skill antaa rungon suomalaiselle kaupalliselle tarjoukselle. Kattaa B2B-tarjouksen, konsultointitarjouksen ja freelance-tarjouksen.

**Ei tee oikeudellista neuvontaa.** Jos asiakas pyytää sopimusehtojen sisältöä tai vastuukysymyksiä, ohjaa Asianajajaliiton resursseihin (asianajajaliitto.fi).

---

## 1. Pakolliset elementit

Suomalainen kaupallinen tarjous sisältää aina nämä osat. Jos osa puuttuu, tarjous on epätäydellinen ja voi aiheuttaa sekaannuksia tai juridisia ongelmia.

1. **Tarjouksen otsikko ja numero** — yksilöllinen viite, johon palataan sopimusvaiheessa
2. **Päiväys**
3. **Tarjoaja** — yritystiedot mukaan lukien Y-tunnus ja ALV-rekisteröinti
4. **Asiakas** — vastaanottava yritys ja yhteyshenkilö
5. **Tarjottava työ tai tuote** — mitä kuuluu ja mitä EI kuulu
6. **Hinnoittelu** — rivi riviltä, ALV erikseen
7. **Maksuehdot** — maksuaika ja viivästyskorko
8. **Tarjouksen voimassaolo** — esim. "30 päivää tarjouspäivästä"
9. **Sopimusehdot tai viittaus alan vakiosopimuksiin** (IT2022, JIT 2015, KSE 2013 jne. — tarkista aina uusin voimassa oleva versio)
10. **Yhteyshenkilö ja allekirjoitus**

---

## 2. Yleisrakenne

```markdown
[Tarjoaja Oy]
[Osoite]
Y-tunnus: [Y-tunnus]
ALV-rekisteri

[Päiväys]

TARJOUS [numero/viite]

Vastaanottaja:
[Asiakkaan yritys]
[Yhteyshenkilö, titteli]

## 1. Tarjottava työ

[Mitä työ sisältää. 2–5 kappaletta.]

## 2. Mitä ei kuulu tarjoukseen

[Eksplisiittinen lista siitä, mitä ei kuulu. Tämä on kriittinen osa, joka usein puuttuu AI-tuotetuista tarjouksista.]

## 3. Hinnoittelu

[Hinnoittelutaulukko, ALV eriteltynä]

## 4. Maksuehdot

[Maksuaika, viivästyskorko, laskutusrytmi]

## 5. Aikataulu

[Aloitus, virstanpylväät, valmistuminen]

## 6. Tarjouksen voimassaolo

Tämä tarjous on voimassa [pp.kk.vvvv asti] / [N päivää tarjouspäivästä].

## 7. Sopimusehdot

[Viittaus vakiosopimukseen tai liite]

## 8. Yhteyshenkilö

[Nimi, titteli, puhelin, sähköposti]

Allekirjoitus:

___________________________
[Nimi, titteli]
[Tarjoaja Oy]
```

---

## 3. Hinnoittelun ALV-erottelu

### 3.1 B2C-hinnoittelu (kuluttaja-asiakas)

Hinta sisältää ALV:n. Kuluttajansuojalain mukaan B2C-hinnoissa ALV:n tulee olla mukana.

```
Verkkokurssi: 99 € (sis. ALV 25,5 %)
```

### 3.2 B2B-hinnoittelu (yritysasiakas)

Hinta ilmoitetaan ilman ALV:tä, ja ALV eritellään erikseen.

```
Konsultointityö:      100,00 €/h (ALV 0 %)
40 tunnin sopimus:  4 000,00 €
ALV 25,5 %:         1 020,00 €
Yhteensä:           5 020,00 €
```

### 3.3 Sekoitettu hinnoittelu (kiinteähinta + tuntihinta)

```
Projektityö:
- Esiselvitys (kiinteähinta)      2 500,00 €
- Toteutus (kiinteähinta)         8 000,00 €
- Lisätyöt (tuntihinta)             95,00 €/h

Kaikki hinnat ALV 0 %. Arvonlisävero 25,5 % lisätään laskutuksessa.
```

### 3.4 Yleinen ALV-taso

Suomessa yleinen ALV on **25,5 %** (1.9.2024 alkaen). Aiempi 24 % pätee aiempiin sopimuksiin. Tarkista voimassa oleva taso ennen tarjouksen lähettämistä.

Erityistasot (tarkista aina ajantasainen kanta Verohallinnosta):
- Elintarvikkeet ja rehu: 14 %
- Alennettuun 13,5 %:n kantaan kuuluvat 1.1.2026 alkaen muun muassa kirjat, lääkkeet, henkilökuljetukset sekä liikunta- ja kulttuuripalvelut

Useimmissa konsultointi- ja markkinointiprojekteissa pätee yleinen 25,5 %.

---

## 4. Maksuehdot

### 4.1 Maksuaika

| Sopimus | Maksuaika |
|---|---|
| B2B oletus | 14 päivää netto |
| B2B isompi projekti | 21–30 päivää netto |
| Kuluttaja | Heti (verkkokauppa), 14 päivää lasku |
| Julkinen sektori | Useimmiten 21–30 päivää |

"Netto" tarkoittaa, että maksun on oltava perillä kyseiseen päivään mennessä. **Tarjouksessa maksuaika on neuvoteltavissa**, joten ehdota — älä määrää.

### 4.2 Viivästyskorko

Suomessa korkolaki (633/1982) määrittää viivästyskoron. Jos sopimusta ei ole, viivästyskorko on **Euroopan keskuspankin viitekorko + 8 prosenttiyksikköä**. Sopimuksessa voidaan sopia muusta.

Standardimuotoilu tarjouksessa:
```
Maksuehto: 14 päivää netto.
Viivästyskorko: korkolain mukainen.
```

### 4.3 Laskutusrytmi pitkissä projekteissa

Pidemmissä projekteissa laskuta vaihein, ei loppuun:
- Kuukausilasku
- Virstanpylväskohtaiset laskut (esim. 30 % aloitus, 40 % puolivälissä, 30 % toimitus)
- Tuntilaskutus kahdesti kuussa

---

## 5. Tarjouksen voimassaolo

### 5.1 Vakiomuotoilut

```
Tämä tarjous on voimassa 30 päivää tarjouspäivästä.
```

```
Tarjouksen voimassaolo: 27.6.2026 saakka.
```

### 5.2 Suositellut pituudet

| Tarjouksen tyyppi | Voimassaolo |
|---|---|
| Standardi B2B | 30 päivää |
| Suuri projekti | 60 päivää |
| Julkinen tarjouskilpailu | ilmoituksen mukainen |
| Pikatarjous | 7–14 päivää |

### 5.3 Miksi voimassaolo on tärkeä

Ilman voimassaoloaikaa tarjous voidaan tulkita avoimeksi, mikä rajoittaa hinnoittelumuutoksia. Pidä tarjous voimassa kohtuullisen aikaa mutta ei loputtomiin.

---

## 6. Työn rajaus: mitä kuuluu, mitä ei kuulu

Tämä on tärkein osa tarjouksesta. AI-tuotetut tarjoukset jättävät tämän usein liian löysäksi.

### 6.1 Mitä kuuluu

```markdown
## 1. Tarjottava työ

Tarjouksemme kattaa seuraavan kokonaisuuden:

- Markkinointikampanjan strategian suunnittelu
- Kampanjamateriaalien (1 maksullinen video, 5 staattista kuvaa) tuottaminen
- Meta Ads -kampanjan käynnistys ja optimointi 4 viikon ajan
- Viikoittainen raportointi sähköpostitse
```

### 6.2 Mitä ei kuulu (tärkeä!)

```markdown
## 2. Tarjouksen ulkopuolelle jäävät asiat

Seuraavat eivät kuulu tarjoukseen ja laskutetaan erikseen tai sovitaan myöhemmin:

- Mediaostot (asiakas maksaa suoraan Metalle)
- Kuvauspaikan vuokrat ja matkakulut
- Kolmannen osapuolen ohjelmistolisenssit
- Maksumuutokset kampanjan käynnistyksen jälkeen (kiinteät kustannukset)
- Muutostyöt yli sovitun 2 muutoskierroksen
```

### 6.3 Tyypilliset puuttuvat erottelut

Tarkista, että tarjous kertoo selkeästi:
- Sisältyykö projektin hallintatyö (project management) hintaan?
- Sisältyykö ensimmäinen palaveri vai onko se erillinen?
- Kuinka monta muutoskierrosta on mukana?
- Kuka maksaa kolmannen osapuolen kulut (ohjelmistot, mediaostot, matkakulut)?
- Onko viestintä rajoitettu tiettyihin aikoihin tai kanaviin?

---

## 7. Sopimusehdot ja vakiosopimukset

### 7.1 Yleiset suomalaiset vakiosopimukset

| Vakiosopimus | Käyttöala |
|---|---|
| IT2022 | IT-palvelusopimukset |
| JIT 2015 | Julkisen sektorin IT-hankinnat — vanha ehto, tarkista uusin versio ennen käyttöä |
| KSE 2013 | Konsulttitoiminnan yleiset sopimusehdot (suunnittelu ja konsultointi) |
| YSE 1998 | Rakennustyö |
| RYHT 2000 | Rakennusurakan yleiset hankintaehdot |

Tarjouksessa voi viitata sovellettavaan vakiosopimukseen:
> Sovellettavat ehdot: KSE 2013 (konsulttitoiminnan yleiset sopimusehdot).

**Tarkista aina sopimusehtojen uusin voimassa oleva versio ennen tarjouksen lähettämistä** — vakiosopimusten nimet ja vuosiluvut päivittyvät.

### 7.2 Jos ei viittaa vakiosopimukseen

Lisää tarjoukseen liite tai erillinen kohta keskeisistä ehdoista:
- Toimitusehto
- Vastuun rajoitus
- Vahinkojen vastuu
- Salassapito
- Tekijänoikeudet
- Riitojen ratkaisu

**Tämä on oikeudellinen asia, ei sisältöä tämän skillin alaan.** Hae apua Asianajajaliitosta tai yritysjuristista.

---

## 8. Anti-patternit

### 8.1 Englannin-tyylinen myyvä kieli

AI-tuotettu tarjous voi käyttää myyntipuheita, jotka suomalaisessa kontekstissa kuulostavat vieraalta.

❌ Vältä:
- "Empower your business to..."
- "Unlock the potential of..."
- "Vallankumouksellinen ratkaisu, joka mullistaa..."
- "Hopealuoti teidän markkinointiongelmiinne"

✅ Käytä:
- Konkreettinen kuvaus mitä työ sisältää
- Numerot ja päivämäärät
- Asiakkaan kielen sanasto

### 8.2 ALV puuttuu tai sekaisin

Tämä on yleisin virhe AI-tuotetuissa tarjouksissa. Joko ALV puuttuu kokonaan ("100 € konsultoinnista"), tai eri rivit ovat eri ALV-tilassa ilman selitystä.

Tarkista:
- Kaikki rivit ALV 0 % tai kaikki ALV 25,5 %
- Yhteishinta selvästi esillä
- Mikä on B2C-hinta (ALV mukana) vs B2B-hinta (ALV erikseen)

### 8.3 Voimassaolo puuttuu

Ilman voimassaoloa tarjous voi velvoittaa loputtomiin. Aina merkitse päättymispäivä.

### 8.4 Löysä rajaus

❌ "Toteutamme markkinointikampanjan tarpeidenne mukaisesti."
✅ "Toteutamme 4 viikon Meta Ads -kampanjan, sisältäen 1 maksullisen videon ja 5 staattista kuvaa. Kuukausibudjetti ja kohderyhmämääritys ovat erillinen sopimusasia."

### 8.5 Hinnoittelumalli ilman selitystä

❌ "Hinnoittelumalli: 2 500 €/kk + lisätyöt"
✅ "Kiinteähinta 2 500 € kuukaudessa kattaa 30 tuntia työtä. Yli menevä työ laskutetaan 95 €/h."

### 8.6 Ajatusviivan ylikäyttö

Tarjouksen kieli on neutraali ja informaatiopainotteinen. Ajatusviivan käyttö on harkittu, ei joka virkkeessä.

### 8.7 Kolmiosaiset listat tyhjästä

❌ "Tarjoamme luovuutta, asiantuntemusta ja sitoutumista."
✅ "Olemme tehneet vastaavan kampanjan kuudelle pk-asiakkaalle 2024–2025."

---

## 9. Sanitoitu malliesimerkki — B2B-konsultointitarjous

```markdown
Esimerkki Konsultointi Oy
Esimerkkikatu 12, 00100 Helsinki
Y-tunnus: 1234567-8
ALV-rekisteri

27.5.2026

TARJOUS 2026-117

Vastaanottaja:
Esimerkki Asiakas Oy
Mikko Mallikas, markkinointijohtaja

## 1. Tarjottava työ

Toteutamme markkinointiautomaation pilottiprojektin, joka koostuu seuraavista osista:

- Esiselvitys: nykyisen markkinointijärjestelmän auditointi (5 työpäivää)
- Suunnitelma: roadmap 12 kuukauden automaatiokehitykselle (3 työpäivää)
- Toteutus: HubSpot-perustan rakennus ja yhden kampanjan automatisointi (10 työpäivää)
- Tuki: 2 kuukauden tuki käyttöönoton jälkeen (yhteensä 8 tuntia)

## 2. Tarjouksen ulkopuolelle jäävät asiat

Seuraavat eivät kuulu tarjoukseen:

- HubSpot-lisenssimaksut (asiakas maksaa Hubille suoraan)
- Mediaostot, kampanjabudjetit
- Sisällöntuotanto (kopiotekstit, kuvat, videot)
- Yli sovitun 18 työpäivän menevä työ — laskutetaan erikseen 850 €/päivä

## 3. Hinnoittelu

| Vaihe | Työpäiviä | Hinta (ALV 0 %) |
|---|---|---|
| Esiselvitys | 5 | 4 250,00 € |
| Suunnitelma | 3 | 2 550,00 € |
| Toteutus | 10 | 8 500,00 € |
| Tuki (8 h) | — | 800,00 € |
| **Yhteensä** | **18 + tuki** | **16 100,00 €** |

ALV 25,5 % lisätään laskutuksessa: 4 105,50 €
Kokonaishinta: **20 205,50 €** (sis. ALV)

## 4. Maksuehdot

- Maksuaika: 14 päivää netto
- Viivästyskorko: korkolain mukainen
- Laskutusrytmi: 50 % aloituksen yhteydessä, 50 % toimituksen jälkeen

## 5. Aikataulu

- Aloitus: viikko 26/2026
- Esiselvitys valmis: viikko 27/2026
- Suunnitelma valmis: viikko 28/2026
- Toteutus valmis: viikko 32/2026
- Tukivaihe päättyy: viikko 41/2026

## 6. Tarjouksen voimassaolo

Tarjous on voimassa 30 päivää tarjouspäivästä, eli 26.6.2026 saakka.

## 7. Sopimusehdot

Sovellettavat ehdot: KSE 2013 (konsulttitoiminnan yleiset sopimusehdot).

## 8. Yhteyshenkilö

Aino Esimerkki
Konsultointijohtaja, Esimerkki Konsultointi Oy
+358 40 000 0000
aino.esimerkki@example.fi

Allekirjoitus:

___________________________
Aino Esimerkki
Konsultointijohtaja
```

---

## 10. Tarkistuslista ennen lähetystä

```
[ ] Tarjouksen otsikko ja viitenumero ovat selkeät
[ ] Päiväys on tarjouksessa
[ ] Tarjoaja: yrityksen nimi, Y-tunnus, ALV-status
[ ] Asiakas: yritys ja yhteyshenkilö
[ ] "Mitä kuuluu" ja "mitä ei kuulu" on eroteltu
[ ] Hinnoittelu on rivi riviltä, ei vain yhteissumma
[ ] ALV on eritelty (B2B) tai sisällytetty (B2C)
[ ] Maksuaika ja viivästyskorko mainittu
[ ] Voimassaolo on selvä päivämäärä tai päivien lukumäärä
[ ] Aikataulu on konkreettinen, ei "noin kuukauden"
[ ] Sopimusehdot tai viittaus vakiosopimukseen
[ ] Yhteyshenkilön nimi, titteli ja yhteystiedot
[ ] Allekirjoitusrivi
[ ] [[suomi-lokalisaatio-perus]] mukainen muotoilu (12 500 €, 25,5 %, 27.5.2026)
[ ] [[suomi-kielihuolto]] tarkistus tehty (yhdyssanat, pilkutus)
[ ] [[suomi-ei-ai-sloppia]] tarkistus tehty (ei myyntipuhetta)
[ ] [[suomi-sinuttelu-teitittely]] johdonmukainen
```

---

## 11. Mihin tätä skilliä konsultoidaan

- [[suomi-tarkistuslista]] — pipeline I: tarjous
- [[suomi-lokalisaatio-perus]] — hinnoittelu, päivämäärät, ALV
- [[suomi-sinuttelu-teitittely]] — asiakaspuhuttelumuoto
- [[suomi-rekisteri]] — ammattikielen rekisteri
- [[suomi-ei-ai-sloppia]] — myyntipuheen karsinta
- [[suomi-kielihuolto]] — mekaniikka
- [[suomi-sahkoposti]] — tarjouksen saateviestin muotoilu, kun tarjous lähetetään liitteenä
