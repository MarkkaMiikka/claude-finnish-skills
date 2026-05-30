---
name: suomi-kielihuolto
description: >
  Kielitoimiston ohjepankkiin perustuva suomen kielen oikeinkirjoitus, kielioppi ja välimerkkisäännöt. Käytä AINA kun kirjoitat tai tarkistat suomenkielistä tekstiä, mukaan lukien markkinointiviestintä, hakemukset, CV:t, verkkosivut, blogiartikkelit, käännökset, some-julkaisut, sähköpostit ja viralliset asiakirjat. Aktivoituu myös kun käyttäjä mainitsee yhdyssanat, pilkutus, alkukirjaimet, lyhenteet, päivämäärät, numerot, lainausmerkit, viivat, sijamuodot, oikoluku, kielihuolto, oikeinkirjoitus tai pyytää suomenkielisen tekstin tarkastusta. Tämä skill keskittyy mekaniikkaan ja sääntöihin. AI-slopin (mahtipontinen tyyli, käännöslainat, kliseet) tunnistamiseen käytä rinnalla [[suomi-ei-ai-sloppia]] -skilliä.
license: MIT
---

# Suomen kielen oikeinkirjoitus- ja kielioppiohjeistus

> **Vinkki:** Jos haluat ajaa kaikki suomi-* -skillit yhdessä oikeassa järjestyksessä, käytä `[[suomi-tarkistuslista]]` -orkestraattoria. Se valitsee oikeat skillit ja pipeline-järjestyksen tekstin kontekstin perusteella.

Tämä skill perustuu Kielitoimiston ohjepankkiin (Kotimaisten kielten keskus). Noudata näitä sääntöjä aina suomenkielistä tekstiä tuottaessasi tai tarkistaessasi.

Pohjana akunikkola/suomi-finnish-skill (MIT). Lähde: Kielitoimiston ohjepankki, Kielitoimiston sanakirja, Iso suomen kielioppi.

---

## 1. YHDYSSANAT — yleisin AI-virhe

Yhdyssanavirheet ovat suomen kielen yleisin kirjoitusvirhe ja erityisen tyypillisiä tekoälyn tuottamassa tekstissä.

### 1.1 Perusperiaate

- **Kiinteä merkityskokonaisuus → yhteen:** aamupala, äidinkieli, hengitysilma, asiakaspalvelu
- **Rinnakkaiset sanat ilman vakiintunutta merkitystä → erikseen:** talon katto, nuori kapinallinen, sen sijaan

### 1.2 Nominatiivialkuiset yhdyssanat — AINA yhteen

Kun ensimmäinen osa on perusmuodossa oleva substantiivi, kyseessä on AINA yhdyssana:

- aamupala (EI: aamu pala)
- verkkosivusto (EI: verkko sivusto)
- asiakaspalvelu (EI: asiakas palvelu)
- tietoturva (EI: tieto turva)
- rantakunto (EI: ranta kunto)
- tulikuuma (EI: tuli kuuma)

### 1.3 Genetiivialkuiset: vakiintuneisuus ratkaisee

- äidinkieli (vakiintunut käsite → yhdyssana)
- äidin kieli (konkreettinen omistus → sanaliitto)
- maahanmuutto (vakiintunut termi → yhdyssana)
- tähän maahan muutto (konkreettinen tilanne → sanaliitto)

### 1.4 Adjektiivialkuiset

Perusmuotoinen adjektiivi + substantiivi → yhdyssana, kun kokonaisuus on vakiintunut lajinnimi tai termi:
- harmaalokki, mustikka, pitkämekko, isoveli

Erikseen kun adjektiivi kuvaa vapaasti:
- harmaa lokki (yksittäinen lokki, joka sattuu olemaan harmaa)

### 1.5 Partisiippi- ja infinitiivi-ilmaukset → yleensä erikseen

- läsnä oleva (EI: läsnäoleva)
- edellä mainittu (EI: edellämainittu)
- voimassa oleva (EI: voimassaoleva)
- huomioon ottaen (EI: huomioonottaen)
- lukuun ottamatta (EI: lukuunottamatta)

POIKKEUS — kuvallinen tai vakiintunut merkitys → yhteen:
- silmäänpistävä (huomiota herättävä)
- poissaoleva (hajamielinen)
- asiantunteva (osaava)

### 1.6 Yhdysmerkki yhdyssanassa

Käytä yhdysmerkkiä kun:
- alkuosana on kirjain, numero tai lyhenne: A-rappu, F1-kilpailu, EU-maa, tosi-tv
- alkuosana on vierassana ja kokonaisuus muuten hankalalukuinen: pop-ohjelma, hip-hop-musiikki
- sanaliittomainen ilmaus on määritteenä: avaimet käteen -periaate

### 1.7 Tarkista nämä erityisen huolellisesti — AI tekee usein virheitä

AINA yhteen:
- verkkosivusto, verkkokauppa, verkkopalvelu
- asiakaspalvelu, asiakaskokemus, asiakassuhde
- tietoturva, tietokanta, tietojärjestelmä, tietosuoja
- peruskoulu, peruspalvelu, perustaso
- alkukirjain, alkuperä, alkuaika
- ympäristönsuojelu, ympäristövaikutus, ympäristöteko
- sosiaaliturva, sosiaalipalvelu
- terveyspalvelu, terveydenhuolto
- työelämä, työpaikka, työtehtävä, työnantaja, työntekijä
- markkinointiviestintä, markkinointistrategia, markkinointiosasto
- sisällöntuotanto, sisällönhallinta
- liiketoiminta, liikeidea
- kohderyhmä, kohderyhmänä
- some-näkyvyys, some-mainonta (yhdysmerkki, koska some on lyhenne)

---

## 2. PILKUTUS

### 2.1 Päälauseiden välissä

Kahden kokonaisen päälauseen väliin tulee pilkku:
- "Kesällä perhe kunnosti saunaa, ja talvella osa perheestä viimeisteli keittiön."

Jos rinnastuskonjunktiolla alkavalla lauseella on edeltävän kanssa yhteinen jäsen, ei pilkkua:
- "Perhe kunnosti saunaa ja viimeisteli keittiön." (yhteinen tekijä)

### 2.2 Pää- ja sivulauseen välissä — AINA pilkku

- "Ministeri totesi, että asia on loppuun käsitelty."
- "Jos ääniä ei kerry tarpeeksi, päätöstä ei voi tehdä."
- "Hän kysyi, tulenko ajoissa."

### 2.3 Pilkku ja konjunktiot

- **että, jos, kun, koska, vaikka, jotta** → edelle aina pilkku
- **mutta, vaan** → edelle aina pilkku
- **sillä** → edelle aina pilkku
- **ja, tai, sekä** → pilkku vain kun molemmat lauseet kokonaisia

### 2.4 Relatiivilauseet (joka, mikä) — pilkku molemmin puolin

- "Talo, joka oli rakennettu 1920, oli myynnissä."
- "Mies, jota etsittiin, löytyi lopulta."

### 2.5 Pilkku ja kuten

- "Monet marjat, kuten mustikat ja puolukat, kypsyvät elokuussa."

### 2.6 Luetteloissa — EI Oxford-pilkkua

- "Tarvitsemme jauhoja, sokeria, voita ja kananmunia." (ei pilkkua ennen "ja")

### 2.7 Desimaalipilkku

Suomessa desimaalierotin on pilkku, EI piste:
- 3,14 (EI: 3.14)
- 1 000,50 € (EI: 1,000.50 €)

---

## 3. ALKUKIRJAIMET

### 3.1 Iso alkukirjain

- Virkkeen alussa
- Erisnimissä: Suomi, Helsinki, Euroopan unioni, Kotimaisten kielten keskus
- Nimien kaikissa osissa (paitsi pikkusanoissa pitkissä nimissä): Suomen Pankki, Tampereen yliopisto

### 3.2 Pieni alkukirjain — AI tekee usein virheitä isoilla

- Kansallisuudet ja kielet: suomalainen, ruotsin kieli, englanti
- Viikonpäivät: maanantai, tiistai
- Kuukaudet: tammikuu, helmikuu
- Vuodenajat: kevät, kesä, syksy, talvi
- Uskontokunnat: luterilainen, katolinen, muslimi
- Tittelit ja arvonimet: presidentti, ministeri, tohtori, markkinointijohtaja
- Kasvi- ja eläinlajien yleisnimet: koivu, harmaalokki

### 3.3 Erityistapauksia

- Lakien nimet pienellä: perustuslaki, kuntalaki
- Juhlapyhät: vaihtelua — juhannus / joulu yleensä pienellä, mutta vakiintuneessa nimimäisessä käytössä isolla
- Taideteokset: vain ensimmäinen sana isolla: Seitsemän veljestä

---

## 4. LYHENTEET

### 4.1 Pisteelliset (loppulyhenne)

- esim. (esimerkiksi)
- mm. (muun muassa)
- jne. (ja niin edelleen)
- ns. (niin sanottu)
- ks. (katso)
- vrt. (vertaa)

### 4.2 Pisteettömät

- Sisälyhenteet, joissa sanan loppu mukana: nro, tri
- Isokirjainlyhenteet: EU, YK
- Organisaationimet, joita ei nykykäytössä kirjoiteta isokirjainlyhenteinä: Yle, Kela
- Mittayksiköt: kg, km, m, cm, l, dl, h, min, s

### 4.3 Lyhenteiden taivutus

- Isokirjainlyhenteisiin pääte kaksoispisteellä: EU:n, YK:ssa
- Yle ja Kela taipuvat suoraan: Ylen, Ylessä, Kelan, Kelassa
- Pieniin kirjainlyhenteisiin pääte suoraan: kg:n, km:llä
- Pisteellisiä lyhenteitä ei taivuteta

### 4.4 Välilyönnit

- Lukuun ja yksikköön väliin välilyönti: 5 kg, 100 km
- Prosenttimerkin edelle välilyönti: 15 %, 3,5 %
- Valuuttamerkin edelle välilyönti: 100 €, 50 $

---

## 5. LUVUT JA NUMEROT

### 5.1 Numerot vs. kirjaimet

- Pienet luvut (1–10) mielellään kirjaimin juoksevassa tekstissä: yksi, kaksi, kolme
- Suuret/tarkat luvut numeroin: 150, 2 500, 1 000 000
- Tilasto- ja tekniset luvut aina numeroin

### 5.2 Tuhaterottimet ja desimaalit

- Tuhaterotin on välilyönti (mieluiten sitova U+00A0), EI piste, EI pilkku: 1 000, 10 000, 1 000 000
- Desimaalierotin on pilkku: 3,14
- Nelinumeroiset luvut voi kirjoittaa ilman erotinta: 1000 tai 1 000

### 5.3 Päivämäärät

- Suositeltavat muodot: 11. maaliskuuta 2026 tai 11.3.2026
- Pisteet ilman välilyöntejä: 11.3.2026 (EI: 11. 3. 2026)
- Kellonajat pisteellä: klo 14.30 (EI: 14:30)

### 5.4 Järjestysluvut

- Tunnus piste: 1., 2., 3.
- Perusluvut taipuvat kaikissa osissa: kahdensadan, kolmestasadasta

---

## 6. VIIVAT — yhdysmerkki vs. ajatusviiva

### 6.1 Yhdysmerkki (-)

- Yhdyssanoissa: EU-maa, A-rappu
- Tavutuksessa: kir-joi-tus

### 6.2 Ajatusviiva (–)

- Väleissä: sivut 10–15, klo 8–16, vuosina 2020–2025
- Lauseen keskellä taukomerkkinä: "Asiaa pohdittiin – eikä vähiten siksi, että…"
- Luetelman alussa

**Ajatusviiva on pidempi kuin yhdysmerkki. AI sekoittaa nämä usein.**

---

## 7. LAUSERAKENNE JA KIELIOPPI

### 7.1 Kongruenssi

- "Lapset leikkivät pihalla." (monikko + monikko)
- "Osa lapsista leikkii pihalla." (yksikkö, koska "osa" on subjekti)

### 7.2 Sijamuodot — partitiivi, akkusatiivi, genetiivi

Sijamuodot ovat suomen kielen perustana ja AI-tekstissä toistuva virhealue. Tunne kolme yleisintä, joiden välillä AI tekee sekaannuksia.

#### 7.2.1 Partitiivi vs. akkusatiivi objektissa

**Partitiivi (mitä?):**
- Toiminta on kesken tai jatkuvaa: "Luen kirjaa." (en ole vielä lukenut loppuun)
- Negaatio: "En ostanut autoa."
- Epämääräinen tai osittainen objekti: "Tarvitsen apua."
- Numerollinen objekti monikossa: "Ostin kaksi kirjaa."
- Tunne- tai aistitilan kohde: "Rakastan musiikkia."

**Akkusatiivi (nominatiivi tai genetiivi):**
- Toiminta on loppuun saatettu: "Luin kirjan." (luettu kokonaan)
- Konkreettinen, määrätty objekti: "Ostin auton."
- Konkreettinen kerran tehty teko: "Avasin oven."

**AI-virhe-esimerkki:**

| Vältä (AI tekee tämän) | Käytä | Sääntö |
|---|---|---|
| "Käytämme strategian" (jos käyttö on jatkuvaa, ei kertaluonteista) | "Käytämme strategiaa" | Jatkuva tai keskeneräinen tekeminen = partitiivi |
| "Tarjoamme palvelu yrityksille" | "Tarjoamme palvelua yrityksille" | Yleinen tarjoaminen = partitiivi |
| "Ostimme uudet ratkaisut" (kun ei kerralla kaikkia) | "Ostimme uusia ratkaisuja" | Epämääräinen monikko = partitiivi |

#### 7.2.2 Genetiivi — possessiivi vs. ajan ja keston merkitsijä

Genetiivillä on suomessa monta käyttötarkoitusta. Yleisimmät AI-virheet:

| Vältä | Käytä | Sääntö |
|---|---|---|
| "Viikon ajan kuluessa" | "Viikon kuluessa" tai "viikossa" | Älä kasaa "ajan" ja "kuluessa" -ilmauksia päällekkäin |
| "Yrityksenmme palvelut" | "Yrityksemme palvelut" | Monikon 1. persoonan possessiivi on -mme, ei -nmme |
| "Asiakas käytössä on" | "Asiakkaan käytössä on" | Possessiivirakenne vaatii genetiivin omistajalle |

#### 7.2.3 Paikallissijat — sisä-, ulko-, tulosija

Suomen paikallissijat (kuusi sijaa):

| Tyyppi | Mistä? (eroaminen) | Missä? (olo) | Mihin? (suunta) |
|---|---|---|---|
| Sisä- (sisältä/sisällä/sisään) | -sta/-stä (elatiivi) | -ssa/-ssä (inessiivi) | -Vn (illatiivi: taloon, sänkyyn) |
| Ulko- (päältä/päällä/päälle) | -lta/-ltä (ablatiivi) | -lla/-llä (adessiivi) | -lle (allatiivi) |

Lisäksi olotila-sijat (eivät paikallissijoja, mutta usein samassa yhteydessä):
- **Essiivi** (-na/-nä) — olotila: "lapsena", "opettajana"
- **Translatiivi** (-ksi) — muutos: "lääkäriksi", "kauniiksi"

**AI-virhe-esimerkkejä:**

- "Sopimuksessa allekirjoittaminen tapahtuu seuraavasti" → "Sopimuksen allekirjoittaminen tapahtuu seuraavasti" (genetiivi koska "allekirjoittaminen" on substantiivin attribuutti)
- "Tähän projektiin kuuluu" → OK
- "Tämän projektin osalta" → OK
- "Tämän projektin kuuluu" → "Tähän projektiin kuuluu" (verbin "kuulua" rektio on illatiivi, ei genetiivi)

#### 7.2.4 Postpositioiden rektio — yleisin AI-virhe

Postpositiot vaativat tietyn sijan ennen niitä. AI sekoittaa nämä jatkuvasti:

| Postpositio | Vaadittu sija | Esimerkki |
|---|---|---|
| **suhteen** | genetiivi | "asian suhteen" (EI: asiaan suhteen) |
| **kanssa** | genetiivi | "asiakkaan kanssa" |
| **takia / vuoksi** | genetiivi | "asian takia" |
| **jälkeen** | genetiivi | "kokouksen jälkeen" |
| **välissä** | genetiivi | "kahden työvaiheen välissä" |
| **kuluessa** | genetiivi | "viikon kuluessa" |
| **lisäksi** | genetiivi | "tämän lisäksi" |
| **ohella** | genetiivi | "työn ohella" |
| **ympärillä** | genetiivi | "rakennuksen ympärillä" |

**Säännön poikkeukset:**
- **ennen** ottaa partitiivin: "ennen kokousta" (EI: ennen kokouksen)
- **päässä / etäisyydellä** ottaa genetiivin: "kymmenen kilometrin päässä"
- **mukaan** ottaa genetiivin pääkäytössä ("tutkimuksen mukaan", "asian mukaan"); allatiivilla se on liikeverbin täydennys ("tuli meille mukaan"), ei postpositio

### 7.3 Verbin rektio — verbi vaatii tietyn sijan

Eri verbeillä on tietyt sijavaatimukset niiden objektille tai täydennykselle. AI sekoittaa näitä toistuvasti. Kun käytät verbiä, tarkista, että objekti tai täydennys on oikeassa sijassa.

#### 7.3.1 Yleisimmät rektiot — opettele nämä

| Verbi | Vaadittu sija | Esimerkki |
|---|---|---|
| **odottaa** | partitiivi | "Odotan vastausta." (EI: vastauksen, EI: vastaukselle) |
| **uskoa** | illatiivi (-on) | "Uskon tähän projektiin." (EI: tämän projektin) |
| **luottaa** | illatiivi | "Luotan tiimiin." |
| **tarvita** | partitiivi | "Tarvitsen apua." |
| **rakastaa** | partitiivi | "Rakastan musiikkia." |
| **vihata** | partitiivi | "Vihaan odottamista." |
| **välittää** | elatiivi (-sta/-stä) | "En välitä tästä." |
| **pitää** | elatiivi | "Pidän tästä ratkaisusta." |
| **suostua** | illatiivi | "Suostun tähän ehtoon." |
| **kieltäytyä** | elatiivi | "Kieltäydyn tästä." |
| **kysyä** | elatiivi tai ablatiivi | "Kysyn asiakkaalta" (henkilöltä) tai "kysyn asiasta" (aiheesta) |
| **vastata** | illatiivi tai elatiivi | "Vastaan kysymykseen" (= mihin) tai "vastaan tästä projektista" (= mistä olen vastuussa) |
| **opettaa** | objektina henkilöä/ryhmää tai allatiivi + opetettava asia partitiivissa | "Opetan oppilaita" / "Opetan oppilaille matematiikkaa." |
| **muistaa** | kokonaisobjekti tai partitiivi merkityksen mukaan | "Muistan sen tapaamisen hyvin." / "Muistan tapaamista hämärästi." |
| **unohtaa** | kokonaisobjekti tai partitiivi merkityksen mukaan | "Unohdin avaimen." / "Unohdin nimen hetkeksi." |

#### 7.3.2 Erityisen huijaavia rektioita

| Tilanne | Oikein | Väärin |
|---|---|---|
| Pelätä jotakuta vs. jotakin | "Pelkään koiraa" (henkilöä myös: "pelkään häntä") | "Pelkään hänen" |
| Toivoa parasta | "Toivon parasta" (partitiivi) | "Toivon paras" |
| Etsiä jotakin (kesken vs. valmis) | "Etsin avainta" (etsintä kesken, partitiivi) tai "Etsin avaimen ja löysin sen" (valmis, akkusatiivi) | "Etsin avaimen" yksin, jos haku on yhä kesken |
| Käyttää aikaa | "Käytän aikaa tähän" | "Käytän ajan tähän" |
| Käyttää X:ää Y:hyn | "Käytän työkalua tähän" | "Käytän työkalun tähän" |
| Luottaa siihen, että | "Luotan siihen, että..." | "Luotan sitä, että..." |

#### 7.3.3 Rektioiden tarkistus AI-tekstissä

Kun tarkistat AI-tekstiä, listaa verbit ja tarkista per verbi:

1. Onko verbillä erityinen rektio (vaatii muun kuin akkusatiivin)?
2. Onko objekti tai täydennys oikeassa sijassa?
3. Jos epäselvä, tarkista Kielitoimiston sanakirjasta (kielitoimistonsanakirja.fi) — verbin kohdalla mainitaan rektio.

### 7.4 Erisnimien taivutus — kotimaiset ja vieraskieliset

Erisnimi on yleinen AI-virhealue, erityisesti vieraskielisten nimien taivutus suomeksi.

#### 7.4.1 Kotimaiset paikannimet

Kotimaiset paikannimet taipuvat normaalisti:

- Helsinki → Helsingissä, Helsingistä, Helsinkiin
- Tampere → Tampereella, Tampereelta, Tampereelle (ulkopaikallissijat!)
- Turku → Turussa, Turusta, Turkuun
- Espoo → Espoossa, Espoosta, Espooseen
- Lappi → Lapissa, Lapista, Lappiin

Huom: Joillakin paikkakunnilla on perinteisesti ulkopaikallissijat (-lla/-lta/-lle) sisäsijojen sijasta. Tampere on yksi tällainen, samoin Sodankylä, Rovaniemi, Inari ja monet muut. Tarkista epäselvissä tapauksissa Kielitoimiston ohjepankki.

#### 7.4.2 Vieraskielisten paikannimien taivutus — AI:n yleinen virhealue

Vieraskielisillä paikannimillä ja brändeillä on kaksi vaihtoehtoa:

**A. Suora taivutus** (suositeltava kun sana päättyy konsonanttiin tai vokaaliin, joka sopii suomen rakenteeseen):

- New York → New Yorkissa, New Yorkista, New Yorkiin
- Berlin → Berliinissä, Berliinistä, Berliiniin (vakiintunut suomalainen muoto)
- Pariisi → Pariisissa
- Lontoo → Lontoossa
- Tokio → Tokiossa
- Kalifornia → Kaliforniassa

**B. Kaksoispiste-erotin** (vain kun suora taivutus näyttäisi epäselvältä tai kyse on lyhenteestä):

- Lyhenteet: EU:n, YK:ssa, EKP:n
- Nimet, jotka päättyvät äännettäessä eri tavalla kuin kirjoitettaessa: Bordeaux'ssa (ääntyy "bordoo")
- Digipalvelujen nimet taipuvat sen sijaan suoraan, älä käytä niissä kaksoispistettä: LinkedInissä, Skypessä, Excelissä, TikTokissa, Slackissa

**Tärkeä sääntö:** valitse yksi tapa ja pidä se yhtenäisenä tekstin sisällä. AI:n yleisin virhe on **vaihdella** tekstin sisällä: "LinkedInissä" yhdessä virkkeessä, "LinkedIn:ssä" toisessa, "LinkedIn:issä" kolmannessa — käytä johdonmukaisesti suoraa muotoa "LinkedInissä".

#### 7.4.3 Brändien ja palveluiden taivutus

| Brändi | Suora muoto | Kaksoispiste-muoto | Suositus |
|---|---|---|---|
| Facebook | Facebookissa | Facebook:issa | Suora |
| Instagram | Instagramissa | Instagram:issa | Suora |
| Twitter | Twitterissä | Twitter:issä | Suora |
| YouTube | YouTubessa | YouTube:ssa | Suora |
| Google | Googlessa | Google:ssa | Suora |
| Microsoft Teams | Teamsissa | Teams:issa | Suora |
| Zoom | Zoomissa | Zoom:issa | Suora |
| Slack | Slackissa | Slack:issa | Molemmat OK, suora ehkä luonnollisempi |
| Telegram | Telegramissa | Telegram:issa | Suora |
| WhatsApp | WhatsAppissa | WhatsApp:issa | Suora |

**Periaate:** suora muoto on ensisijainen kun se kuulostaa luonnolliselta. Kaksoispistettä käytetään lähinnä lyhenteissä (EU:n, YK:ssa) ja kun taivutus ilman sitä olisi epäselvä lukuvaiheessa.

#### 7.4.4 Henkilönnimien taivutus

Kotimaiset:
- Matti → Matin, Matille, Matissa
- Anna → Annan, Annalle, Annassa

Vieraskielinen (vokaalipäätteinen, suora):
- John → Johnin, Johnille
- Sarah → Sarahin, Sarahille

Vieraskielinen (konsonanttipäätteinen, suora):
- Mark → Markin, Markille
- Sam → Samin, Samille

Vieraskielinen (epäselvä päätös, kaksoispiste auttaa):
- Cheng → Cheng:in (kun -in-pääte voisi sekoittua)
- Bach → Bach:in tai Bachin

#### 7.4.5 Yhteisten erisnimien taivutus

Joitain monisanaisia erisnimiä taivutetaan vain viimeisestä sanasta:

- Yhdysvallat → Yhdysvalloissa
- Iso-Britannia → Iso-Britanniassa
- Suomen Pankki → Suomen Pankissa
- Helsingin yliopisto → Helsingin yliopistossa

### 7.5 Omistusliitteet kirjakielessä

- "taloni" (minun taloni), "talosi" (sinun talosi)
- Puhekielinen "mun talo" ei kuulu yleiskieleen

### 7.6 Passiivin maltillinen käyttö

Suomen passiivi on yleistävä:
- "Suomessa puhutaan suomea ja ruotsia."

**Liiallinen passiivi on AI-tekstin tunnusmerkki.** Aktiivinen ilmaus on usein selkeämpi. Ks. lisää [[suomi-ei-ai-sloppia]].

---

## 8. LAINAUS- JA ERIKOISMERKIT

### 8.1 Lainausmerkit

- Ensisijaisesti suomenkielisessä viimeistellyssä tekstissä: ”lainaus” eli kaarevat kokolainausmerkit (U+201D), sama merkki alussa ja lopussa
- Toissijaisesti sisäkkäisenä: ’lainaus lainauksen sisällä’
- EI kulmikkaita »näin» (ruotsin malli)
- Digitaalisessa raakatekstissä suorat "lainausmerkit" ovat usein hyväksyttäviä
- Älä sekoita samassa tekstissä suoria, suomalaisia kaarevia ja englannin erimuotoisia alku- ja loppulainausmerkkejä

### 8.2 Heittomerkki sanan sisällä

- Hyvä'lainen (sanan sisäisen suomenkielisen heittomerkin tehtävä on usein katoamassa, mutta vakiintuneissa muodoissa säilyy)

---

## 9. OIKOLUKU — seitsemän vaihetta

Kun tarkistat suomenkielistä tekstiä, käy listan läpi järjestyksessä:

### Vaihe 1: Yhdyssanat
- Käy läpi kaikki substantiivi + substantiivi -yhdistelmät
- Tarkista nominatiivialkuiset (verkkosivusto, asiakaspalvelu, tietoturva)
- Tarkista partisiippi-ilmaukset (läsnä oleva, edellä mainittu)
- Tarkista yhdysmerkki vs. ajatusviiva

### Vaihe 2: Pilkutus
- Sivulauseet (että, jos, kun, koska, joka, mikä)
- Päälauseiden välinen pilkutus
- Ei Oxford-pilkkua
- Desimaalipilkut

### Vaihe 3: Alkukirjaimet
- Kansallisuudet, kielet, viikonpäivät, kuukaudet → pienellä
- Erisnimet → isolla
- Tittelit → pienellä (paitsi virallinen yhteys)

### Vaihe 4: Numerot ja lyhenteet
- Tuhaterotin välilyönti
- Desimaalierotin pilkku
- Lyhenteiden pisteet ja taivutus
- Mittayksiköiden välilyönti (5 kg, 15 %)

### Vaihe 5: Sijamuodot, rektiot ja erisnimien taivutus
- Partitiivi vs. akkusatiivi objekteissa (jatkuva vs. loppuun saatettu)
- Postpositioiden rektio ("asian suhteen", "kokouksen jälkeen", "viikon kuluessa")
- Verbin rektio (odottaa + partitiivi, uskoa + illatiivi, pitää + elatiivi)
- Vieraskielisten erisnimien taivutus — yksi tapa koko tekstin läpi (suora muoto TAI kaksoispiste-erotin, ei sekoita)
- Paikannimien sisä- vs. ulkopaikallissijat (Helsingissä vs. Tampereella)

### Vaihe 6: Tyyli ja sujuvuus
- Ks. [[suomi-ei-ai-sloppia]] — anglismit, mahtipontisuus, AI-fraasit, käännöslainat
- Liiallinen passiivi
- Virkkeiden pituus

### Vaihe 7: Yhteenveto
- Listaa löydetyt virheet
- Perustele korjaukset säännöin
- Tarjoa korjattu versio

---

## 10. LISÄTIEDOT

Tarkista epäselvissä tapauksissa:
- Kielitoimiston ohjepankki: https://kielitoimistonohjepankki.fi/
- Kielitoimiston sanakirja: https://www.kielitoimistonsanakirja.fi/
- Iso suomen kielioppi: https://kaino.kotus.fi/visk/etusivu.php
- Kielikello: https://kielikello.fi/
