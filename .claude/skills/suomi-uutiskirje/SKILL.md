---
name: suomi-uutiskirje
description: >
  Suomenkielinen sähköpostiuutiskirje — otsikkorivi, preheader, avaus, sisältöblokit, CTA-konventiot, allekirjoitus ja peruutuslinkki. Käytä kun rakennat asiakasuutiskirjettä, sisältöuutiskirjettä, yrityksen sisäistä uutiskirjettä tai sähköpostimarkkinointia, tai kun käyttäjä sanoo "tee uutiskirje", "kirjoita newsletter", "email-kampanja", "uutiskirjeen otsikko", "asiakaskirje" tai "kuukausikirje". Ei käsittele yksittäistä sähköpostia — käytä siihen [[suomi-sahkoposti]]. Konsultoi [[suomi-lokalisaatio-perus]] -skilliä päivämääriin ja [[suomi-sinuttelu-teitittely]] -skilliä lukijan puhuttelumuotoon.
license: MIT
---

# Suomenkielisen uutiskirjeen rakenne

> **Vinkki:** Jos haluat ajaa kaikki suomi-* -skillit yhdessä oikeassa järjestyksessä, käytä `[[suomi-tarkistuslista]]` -orkestraattoria.

Tämä skill antaa rungon suomenkieliselle sähköpostiuutiskirjeelle. Eroaa yksittäisestä sähköpostista ([[suomi-sahkoposti]]) siten, että uutiskirje on **markkinointiviesti useammalle vastaanottajalle**, jossa avaus- ja klikkausprosentti sekä peruutuslainsäädäntö ovat keskeisiä.

---

## 1. Otsikkorivi (subject line)

Otsikkorivi on tärkein osa avauksen kannalta. Suomalainen B2B-konventio eroaa amerikkalaisesta uutiskirjekulttuurista:
- Pituus: 35–50 merkkiä
- Ei tyypillisesti emojeja B2B:ssä (poikkeus: D2C-kuluttajauutiskirje)
- Ei isoja kirjaimia ("ÄLÄ MISSAA!")
- Ei monta huutomerkkiä
- Kuvaileva, ei klikkitavoitteinen mysteeri

### 1.1 Toimivia kaavoja

| Kaava | Esimerkki |
|---|---|
| Lupaus + täsmennys | `Q2-raportti: pk-yritysten markkinointitrendit` |
| Numero + aihe | `5 oppia kesän asiakaskampanjasta` |
| Kysymys + lyhyt | `Miksi konversio laskee mobiilissa?` |
| Tapahtuma + päivämäärä | `Webinaari 12.6.: AI-työnkulut sisällöntuotannossa` |
| Henkilökohtainen | `Aino, uusi opas on valmis` |

### 1.2 Vältä

- `Älä missaa! Viimeinen mahdollisuus!`
- `Mikä on uutta?` (käännöslaina "What's new?")
- `Ainutlaatuinen tarjous vain sinulle`
- Tyhjä otsikko ilman koukkua: `Uutiskirje toukokuu`

### 1.3 A/B-testaus

Lähetä saman uutiskirjeen kahdella eri otsikolla 10–20 %:n otokselle. Pidempi otsikko (45 merkkiä) vastaan lyhyempi (28 merkkiä) on tyypillinen vertailu. Voittaja menee koko listalle.

---

## 2. Preheader

Preheader on sähköpostiohjelmissa näkyvä esikatselurivi otsikon vieressä. 80–130 merkkiä, ja sen pitää **täydentää otsikkoa, ei toistaa sitä**.

**Hyvä yhdistelmä:**
- Otsikko: `Q2-raportti: pk-yritysten markkinointitrendit`
- Preheader: `Mitä 240 yrityksen vastaukset kertovat budjeteista, kanavista ja AI:n roolista.`

**Heikko yhdistelmä (toisto):**
- Otsikko: `Q2-raportti: pk-yritysten markkinointitrendit`
- Preheader: `Tutustu Q2-raporttiin ja pk-yritysten markkinointitrendeihin.`

### 2.1 Vältä

- Tyhjä preheader (näkyy raakana HTML:nä monessa sähköpostiohjelmassa)
- "View this email in your browser" suoraan käännettynä
- "Hi {firstname}" -personoinnin näkyminen preheaderissa

---

## 3. Tervehdys ja avaus

### 3.1 Tervehdyskonventiot

Sinuttelu on oletus kaikessa modernissa suomenkielisessä uutiskirjeessä. Vrt. [[suomi-sinuttelu-teitittely]].

| Konteksti | Tervehdys |
|---|---|
| Henkilökohtainen ja personoitu | `Hei [etunimi],` |
| Geneerinen lista | `Hei,` |
| Kollegan kanssa | `Moi,` tai `Hei,` |
| Yritysasiakasuutiskirje | `Hei [etunimi],` |
| Brändin oma sisältö | Voi alkaa myös ilman tervehdystä, suoraan asiaan |

### 3.2 Avauskappale

Suomalainen uutiskirjelukija **haluaa heti pointin**. Tämä eroaa amerikkalaisesta uutiskirjekulttuurista (Morning Brew, The Hustle), jossa pitkä kuulumisten kysely on yleinen.

**Suomalaisen lukijan kannalta hyvä avaus:**
> Hei Aino,
>
> Q2-raporttimme on valmis. Tärkein löytö: 240 yrityksen vastaukset osoittavat, että pk-yritysten markkinointibudjetti laski keskimäärin 12 % vuoden alusta — ja AI-työkalut korvaavat aiempaa sisäistä tuotantoa.
>
> [Lue koko raportti]

**Vältä kuulumisten kyselyä:**
> Hei Aino,
>
> Toivottavasti olet voinut hyvin ja kevät on hymyillyt sinulle. Meillä on ollut kiireinen ja innostava kvartaali. Ennen kuin sukellamme aiheeseen, halusin kertoa...

### 3.3 P.S. käytön sääntö

Englannin uutiskirjekulttuurissa P.S. on lähes pakollinen lopussa. Suomeksi se on harkittu, ei mekaaninen. Käytä P.S.-osaa, kun:
- Sinulla on aidosti yksi lisätieto, joka ei mahdu runkoon
- Haluat alleviivata yhden CTA:n
- Et joka uutiskirjeessä

Älä laita P.S.-osaa joka kerta — silloin se menettää tehonsa.

---

## 4. Sisältöblokit

### 4.1 Yleinen rakenne

Uutiskirje koostuu 2–4 sisältöblokista. Liian monta vie lukijan keskittymisen.

Tyypilliset blokkityypit:
- **Pääjuttu** (1 blokki): tärkein uutinen tai sisältö
- **Sivujuttu** (1–2 blokkia): toinen, kolmas olennainen aihe
- **Tapahtumat tai linkit** (1 blokki): listana
- **Toimitukselliset suositukset** (1 blokki, valinnainen)

### 4.2 Yksittäisen blokin rakenne

```
[Blokin otsikko — lyhyt ja kuvaileva]

[1–3 lyhyttä kappaletta. Mobiilissa kappale on 3–4 riviä.]

[CTA-painike tai -linkki]
```

### 4.3 Sisällön pituus mobiilissa

Suomalaiset lukevat uutiskirjeitä pääosin mobiilissa. Suunnittele:
- Kappaleen pituus: 3–4 riviä mobiilissa (n. 200–300 merkkiä)
- Lauseen pituus: 15–20 sanaa keskimäärin
- Otsikot lyhyitä, ei pitkiä kysymyslauseita

---

## 5. CTA-konventiot

### 5.1 Suomalaiset vakio-CTA:t

| Englanti | Suomeksi |
|---|---|
| Read more | Lue lisää |
| Learn more | Tutustu / Tutustu lisää |
| Sign up | Ilmoittaudu / Rekisteröidy |
| Download | Lataa |
| Watch the video | Katso video |
| Read the article | Lue artikkeli |
| Get the report | Lataa raportti |
| Book a meeting | Varaa aika |
| Start free trial | Aloita maksuton kokeilu |
| Subscribe | Tilaa |

### 5.2 Vältä

- `Klikkaa tästä` — ruudunlukijoiden ja saavutettavuuden kannalta huono (linkin teksti pitää kertoa, mihin se vie)
- `KLIKKAA HETI!` — yliampuva
- `Don't miss out` -käännös (`Älä missaa`) — anglismi
- CTA jolla on yli 5 sanaa

### 5.3 CTA-painikkeen muotoilu

- Yhden CTA:n per blokki (lukijan keskittyminen)
- Kontrastiväri (saavutettavuus — riittävä tekstin ja taustan kontrasti, WCAG 2.1 AA -taso)
- Linkin teksti kuvaileva (`Lataa Q2-raportti`, ei `Klikkaa tästä`)

---

## 6. Allekirjoitus

Uutiskirje allekirjoitetaan **henkilönä**, ei yrityksenä, jos mahdollista. Henkilökohtainen allekirjoitus nostaa avausprosenttia.

```
Terveisin

Aino Esimerkki
Päätoimittaja, Esimerkki Oy

P.S. Q2-raportti löytyy myös LinkedInistä, jos haluat jakaa sen tiimillesi.
```

---

## 7. Alatunniste (footer) ja peruutuslinkki

### 7.1 Pakolliset elementit

Tietosuoja-asetuksen (GDPR) ja sähköisen viestinnän palveluista annetun lain (917/2014) mukaan suoramarkkinointiviesteissä **on oltava**:

1. **Peruutuslinkki** ("Peruuta tilaus" / "Lopeta uutiskirjeen tilaus")
2. **Lähettäjän tunnistetiedot** (yritys, osoite)
3. **Miksi vastaanottaja saa viestin** (esim. "Saat tämän viestin, koska olet asiakkaamme")

### 7.2 Vakiomuoto

```
Esimerkki Oy
Esimerkkikatu 12, 00100 Helsinki
Y-tunnus: 1234567-8

Saat tämän viestin, koska olet tilannut Esimerkki Oy:n uutiskirjeen.

[Peruuta tilaus] · [Muokkaa tilausta] · [Avaa selaimessa]
```

### 7.3 Vältä

- `Click here to unsubscribe` — suomeksi peruutuslinkki
- Pieni harmaa peruutuslinkki, jota ei näe (saavutettavuus, juridinen riski)
- Pelkkä `Unsubscribe` ilman selitettä

---

## 8. Erityyppisten uutiskirjeiden ominaisuudet

### 8.1 Kuukausiuutiskirje

- 3–5 sisältöblokkia
- Yritysuutiset + toimialatiedotteet + tapahtumat
- Lähetys: kuukauden 1.–5. päivä on standardiajankohta

### 8.2 Sisältöuutiskirje (sisältömarkkinointi)

- 1–2 pääjuttua
- Linkit blogiin tai resurssipankkiin
- Henkilökohtaisempi sävy
- Lähetys: viikoittain tai kahden viikon välein

### 8.3 Tuoteuutiset (release notes -uutiskirje)

- Listapohjainen ("Mitä uutta")
- Tekninen mutta selkeä
- Linkki täysiin julkaisutiedotteisiin
- Lähetys: kun uutta julkaisua

### 8.4 Sisäinen henkilöstöuutiskirje

- Rento sävy, sinuttelu
- Henkilöesittelyt, yrityskuulumiset
- Lyhyt
- Lähetys: viikoittain tai kahden viikon välein

---

## 9. Anti-patternit

### 9.1 Käännöslainat otsikoissa

❌ `Mitä on uutta?` (What's new?)
❌ `Tunne hetki!` (Feel the moment!)
❌ `Inspiraatiota viikon` (Weekly inspiration)
✅ `Toukokuun katsaus`, `Tuoreet artikkelit`, `Q2-raportti valmis`

### 9.2 Kuulumisten kysely -alku

❌ `Toivottavasti voit hyvin ja kevät on alkanut mukavasti. Olemme olleet kovin kiireisiä ja innoissamme...`
✅ `Q2-raporttimme on valmis. Tärkein löytö: budjetit laskivat 12 %.`

### 9.3 "Tervetuloa uuteen uutiskirjeeseen!" -aloitus

Kaikki AI-uutiskirjeet alkavat tällä. Aloita sisällöllä, ei kuulutuksilla.

❌ `Tervetuloa uuteen uutiskirjeeseen! Tässä kuussa meillä on...`
✅ `Q2-raportin tärkein löytö: 240 yrityksen budjetti laski 12 % vuoden alusta.`

### 9.4 Liika lihavointi ja kursivointi

AI lihavoi avainsanat mekaanisesti. Lue uutiskirje ääneen — kohta, jonka korostat puheessa, on lihavoitavissa, muut eivät.

### 9.5 Liika emoji B2B-kontekstissa

Suomalainen B2B-uutiskirje sisältää 0–1 emojia koko viestissä. Amerikkalainen voi sisältää 5–10. Sopeudu Suomeen.

### 9.6 P.S. joka kerta

Jos P.S. on uutiskirjeen joka julkaisussa, se on tavanomainen, ei erityinen.

### 9.7 Liian monta CTA:ta

Yhdessä blokissa yksi CTA. Uutiskirjeessä yhteensä 2–4 CTA:ta. Liika valinta = ei klikkausta.

### 9.8 Kolmiosaiset luettelot AI-tyyliin

❌ `Saat oivalluksia, työkaluja ja inspiraatiota.`
✅ `Saat Q2-raportin ja webinaarin tallenteen.`

---

## 10. Sanitoitu malliesimerkki — sisältöuutiskirje

```markdown
[Otsikkorivi]: Q2-raportti: pk-yritysten markkinointitrendit
[Preheader]: Mitä 240 yrityksen vastaukset kertovat budjeteista, kanavista ja AI:n roolista.

---

Hei Aino,

Q2-raporttimme on valmis. Tärkein löytö: 240 pk-yrityksen vastaukset osoittavat, että markkinointibudjetit laskivat keskimäärin 12 % vuoden alusta. Samalla AI-työkalut korvaavat aiempaa sisäistä tuotantoa.

[Lataa Q2-raportti]

---

## Tämän kuun tärkein artikkeli

**Mihin kanavaan pk-yritys laittaa rahansa, kun budjetti tiukentuu?**

Q2-raportin yllättävin yksittäinen luku: 67 % vastaajista vähensi maksetun mainonnan budjettia, mutta vain 18 % vähensi sisältötuotantoa. Tämä viittaa siihen, että pitkän aikavälin sisältö nähdään turvallisempana panostuksena tiukassa taloustilanteessa.

[Lue koko analyysi]

---

## Tulossa kesäkuussa

**Webinaari 12.6. klo 14.00 — AI-työnkulut sisällöntuotannossa**

Mikko Mallikas kertoo, miten Esimerkki Oy automatisoi 80 % sisällöntuotannon rutiinityöstä Clauden työkaluilla. Mukana käytännön esimerkit ja avoin Q&A.

[Ilmoittaudu webinaariin]

---

Terveisin

Aino Esimerkki
Päätoimittaja, Esimerkki Oy

P.S. Q2-raportti löytyy myös LinkedInistä, jos haluat jakaa sen tiimillesi.

---

Esimerkki Oy
Esimerkkikatu 12, 00100 Helsinki
Y-tunnus: 1234567-8

Saat tämän viestin, koska olet tilannut Esimerkki Oy:n uutiskirjeen.

[Peruuta tilaus] · [Muokkaa tilausta] · [Avaa selaimessa]
```

---

## 11. Tarkistuslista ennen lähetystä

```
[ ] Otsikkorivi 35–50 merkkiä, kuvaileva, ei klikkitavoitteinen
[ ] Preheader 80–130 merkkiä, täydentää otsikkoa, ei toista
[ ] Tervehdys: "Hei [etunimi]" tai vastaava (sinuttelu)
[ ] Avauskappale: pointti heti, ei kuulumisten kyselyä
[ ] Sisältöblokit: 2–4, yhdessä yksi CTA
[ ] CTA-tekstit kuvailevia ("Lataa raportti", ei "Klikkaa tästä")
[ ] Allekirjoitus henkilönä, ei pelkkänä yrityksenä
[ ] Alatunniste: yritys, osoite, Y-tunnus
[ ] Peruutuslinkki näkyvä ja toimiva (laki)
[ ] Selitelause "Saat tämän viestin, koska..."
[ ] [[suomi-lokalisaatio-perus]] mukainen muotoilu (12.6.2026, 12 %)
[ ] [[suomi-ei-ai-sloppia]] tarkistus tehty (ei kuulumisten kyselyä, ei kolmiosalistoja)
[ ] [[suomi-kielihuolto]] tarkistus tehty (yhdyssanat, pilkutus)
[ ] [[suomi-anglismit]] tarkistus tehty (ei "Mitä on uutta?", "Älä missaa" jne.)
[ ] Testi mobiililaitteella ennen lähetystä
[ ] Linkit testattu (UTM-parametrit tarvittaessa)
```

---

## 12. Mihin tätä skilliä konsultoidaan

- [[suomi-tarkistuslista]] — pipeline J: uutiskirje
- [[suomi-lokalisaatio-perus]] — päivämäärät, kellonajat, numerot
- [[suomi-sinuttelu-teitittely]] — lukijan puhuttelumuoto
- [[suomi-rekisteri]] — rekisterin valinta (asiakaskieli tai ammattikieli)
- [[suomi-ei-ai-sloppia]] — kuulumisten kyselyjen ja kolmiosalistojen karsinta
- [[suomi-anglismit]] — käännöslainat otsikoissa ja CTA:ssa
- [[suomi-kielihuolto]] — mekaniikka
- [[suomi-sahkoposti]] — yksittäisen sähköpostin konventiot (ei uutiskirje)
