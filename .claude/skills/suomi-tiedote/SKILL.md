---
name: suomi-tiedote
description: >
  Suomenkielinen lehdistötiedote ja sisäisen organisaation tiedote — rakenne, otsikko, ingressi, sitaatit, lisätietolohko ja taustaosa. Käytä kun kirjoitat lehdistötiedotteen, asiakastiedotteen, muutostiedotteen tai sisäisen tiedotteen, tai kun käyttäjä sanoo "kirjoita lehdistötiedote", "tee tiedote", "PR-tiedote", "asiakasviestintä", "muutostiedote", "lanseeraustiedote", "henkilöstötiedote" tai "embargo". Konsultoi [[suomi-sinuttelu-teitittely]] -skilliä asiakaspuhuttelumuotoon ja [[suomi-lokalisaatio-perus]] -skilliä päivämääriin ja numeroihin.
license: MIT
---

# Suomenkielisen tiedotteen rakenne

> **Vinkki:** Jos haluat ajaa kaikki suomi-* -skillit yhdessä oikeassa järjestyksessä, käytä `[[suomi-tarkistuslista]]` -orkestraattoria.

Tämä skill kattaa kaksi suomalaista tiedote-tyyppiä:
- **Lehdistötiedote** — toimittajille ja medialle, julkaistaan organisaation kanavissa
- **Sisäinen tai asiakastiedote** — organisaation jäsenille tai asiakkaille

Molemmat noudattavat **käänteistä pyramidia**: tärkein ensin, taustat lopussa. Lehdistötiedote on muodollisempi ja sisältää yritysesittelyn; sisäinen tiedote on lyhyempi ja suorempi.

---

## 1. Lehdistötiedotteen rakenne

### 1.1 Yläosa

```
Tiedote
Julkaisuvapaa heti / Embargo: pp.kk.vvvv klo HH.MM

[Päiväys]
```

**Julkaisuvapaa-merkintä:** kerro toimittajille, milloin tieto saa julkaista. "Julkaisuvapaa heti" on vakiomuoto. Embargoa käytetään, kun tieto on annettu etukäteen mutta julkistettava tiettynä hetkenä.

### 1.2 Otsikko

Otsikko on **kuvaileva, ei klikkitavoitteinen**. AI-tuotetut tiedotteet käyttävät usein yliampuvia adjektiiveja, jotka eivät kuulu suomalaiseen tiedotekulttuuriin.

**Hyvä:**
- `Esimerkki Oy lanseeraa uuden palvelun pk-yrityksille`
- `Esimerkki Säätiö myöntää 1,2 miljoonan euron apurahat`
- `Esimerkki Oy:n liikevaihto kasvoi 18 % Q1:llä`

**Vältä:**
- `Vallankumouksellinen uutuus mullistaa pk-markkinat!`
- `Esimerkki Oy:llä on uskomattomia uutisia jaettavanaan`
- `Tämän vuoden kuumin lanseeraus on täällä`

### 1.3 Ingressi

Ingressi on **1–3 virkettä** otsikon jälkeen, joka vastaa peruskysymyksiin: kuka, mitä, missä, milloin, miksi. Tämä on tiedotteen tärkein osa — toimittaja tekee usein päätöksen sen perusteella, lukeeko loppua.

**Esimerkki:**
> Esimerkki Oy julkaisi tänään 27.5.2026 uuden Esimerkki-palvelun pk-yrityksille. Palvelu automatisoi laskutuksen ja kirjanpidon ja maksaa 49 € kuukaudessa. Kohderyhmänä ovat 1–10 hengen yritykset, joiden liikevaihto on alle miljoona euroa.

### 1.4 Leipäteksti

Leipäteksti rakennetaan käänteisen pyramidin mukaan:
1. Mitä tapahtui (otsikon ja ingressin laajennus)
2. Miksi tämä on olennaista (konteksti, tarve)
3. Miten se toimii (mekaniikka, käyttäjäkokemus)
4. Sitaatti tai kommentti
5. Taustat (vähemmän kriittinen tieto)

Toimittaja voi katkaista jutun mistä tahansa kohdasta, ja keskeisen tiedon pitää olla edellä.

### 1.5 Sitaatti

Sitaatti **tunnistettavalta henkilöltä virallisella tittelillä**. Pituus enintään 2 virkettä. Sitaatti voi olla suoraan ladattavissa tiedotteesta julkaisuun.

**Hyvä sitaatti:**
> "Pk-yritysten kirjanpito on edelleen liian aikaa vievää. Esimerkki-palvelu hoitaa nyt 80 % rutiinista automaattisesti", sanoo Esimerkki Oy:n toimitusjohtaja Aino Esimerkki.

**Vältä sitaatissa:**
- "Olemme erittäin innoissamme..."
- "Tämä on todella merkittävä askel..."
- Yli 3 virkettä
- Mahtailuretoriikkaa ("pohjimmiltaan", "todellisuudessa")
- Sitaatit jotka eivät kuulosta ihmisen puhumalta

### 1.6 Lisätietolohko

Lehdistötiedotteen lopussa on yhteyshenkilön nimi, titteli ja yhteystiedot. Toimittajat soittavat tästä numerosta.

```
Lisätietoja:

Aino Esimerkki
Toimitusjohtaja, Esimerkki Oy
+358 40 000 0000
aino.esimerkki@example.fi
```

### 1.7 Tausta-osa (yritysesittely / boilerplate)

Lehdistötiedotteen lopussa lyhyt yritysesittely, joka pysyy samana eri tiedotteissa. 2–4 virkettä.

```
Tietoa Esimerkki Oy:stä

Esimerkki Oy on vuonna 2017 perustettu suomalainen ohjelmistoyhtiö, joka kehittää automaation työkaluja pk-yrityksille. Yhtiössä on 24 työntekijää, ja sen pääkonttori sijaitsee Helsingissä. Esimerkki Oy:n omistavat sen perustajat ja henkilökunta.
```

---

## 2. Sisäisen tiedotteen rakenne

Sisäinen tiedote on **lyhyempi ja suorempi** kuin lehdistötiedote. Ei tarvita boilerplate-yritysesittelyä — vastaanottajat ovat jo organisaation jäseniä.

### 2.1 Yleisrakenne

```
[Otsikko]

[Päiväys]

Hei [tiimi / kaikki / kohderyhmä],

[Avauskappale: mitä tapahtuu ja milloin]

[Kappale 2: konkreettiset vaikutukset vastaanottajille]

[Kappale 3: mitä tehdään seuraavaksi, mitä vastaanottajalta odotetaan]

[Yhteyshenkilö, kenelle voi soittaa kysymysten kanssa]

Ystävällisin terveisin / Terveisin

[Lähettäjän nimi]
[Titteli]
```

### 2.2 Esimerkki — muutostiedote

```
Otsikko: Uusi sähköpostijärjestelmä käyttöön 1.7.2026

27.5.2026

Hei kaikki,

Esimerkki Oy:n sähköpostijärjestelmä vaihtuu Microsoft 365:een 1. heinäkuuta. Nykyiset sähköpostit ja kalenterimerkinnät siirretään automaattisesti.

Mitä tämä tarkoittaa sinulle:
- Käytät 30.6. asti vanhaa järjestelmää normaalisti
- 1.7. aamulla saat ohjeet uuden järjestelmän käyttöönotosta
- Vanhat osoitteet säilyvät, vain palvelu vaihtuu

IT-tiimi järjestää 15.6. ja 22.6. tunnin mittaiset koulutukset, joissa käydään läpi tärkeimmät muutokset. Ilmoittaudu Aino Esimerkille viikon 24 aikana.

Kysymykset: IT-tukeen tickets@example.fi tai +358 40 000 0000.

Terveisin

Mikko Mallikas
IT-päällikkö, Esimerkki Oy
```

---

## 3. Käänteinen pyramidi

Tämä on tiedotteen rakentamisen tärkein periaate.

```
═══════════════════════════════════════
TÄRKEIN: mitä tapahtui, ketä koskee   (otsikko + ingressi)
───────────────────────────────────────
LISÄTIETO: miten, miksi, konteksti      (leipätekstin alkupuoli)
───────────────────────────────────────
SITAATTI: ihmisen kommentti              (sitaatti)
───────────────────────────────────────
TAUSTA: vähemmän kriittinen tieto       (yritysesittely lehdistötiedotteessa)
═══════════════════════════════════════
```

Toimittaja, joka käyttää tiedotetta, voi leikata jutun mistä tahansa kohdasta — ja keskeisen tiedon pitää olla aina edellä.

---

## 4. Anti-patternit

### 4.1 Yliampuva otsikko

Suomalainen tiedotekulttuuri suosii **rauhallista, kuvailevaa** otsikkoa. Amerikkalainen tiedotekulttuuri suosii dramaattista otsikkoa. AI tuottaa usein amerikkalaisen otsikon suomenkielisessä tiedotteessa.

❌ "Vallankumouksellinen läpimurto mullistaa pk-yritysten arjen"
✅ "Esimerkki Oy lanseeraa kirjanpidon automaation"

### 4.2 Liian montaa adjektiivia samassa virkkeessä

❌ "Esimerkki Oy julkaisi ainutlaatuisen, mullistavan ja ennennäkemättömän palvelun, joka tarjoaa erinomaista käyttäjäkokemusta."

✅ "Esimerkki Oy julkaisi kirjanpidon automaatiopalvelun pk-yrityksille."

### 4.3 Passiivimuodon ylikäyttö

Tiedote on tekijä-tyyppinen viesti — joku tekee jotain. Passiivi piilottaa tekijän.

❌ "Tiedotetaan, että uusi palvelu otetaan käyttöön. Sopimukset uudistetaan ja asiakkaat informoidaan."

✅ "Esimerkki Oy ottaa käyttöön uuden palvelun. Yhtiö uudistaa sopimukset ja lähettää asiakkaille tiedotteen."

### 4.4 AI-sitaatti

AI-tuotettu sitaatti kuulostaa lähes aina samalta: "Olemme erittäin iloisia voidessamme ilmoittaa..." Tämä paljastaa tiedotteen AI-tuotetuksi heti.

❌ "Olemme erittäin iloisia voidessamme tarjota asiakkaillemme tämän ainutlaatuisen mahdollisuuden, joka muokkaa pk-yritysten arkea perinpohjaisesti", sanoo Esimerkki Oy:n toimitusjohtaja.

✅ "Pk-yritysten kirjanpito on edelleen liian aikaa vievää. Esimerkki-palvelu hoitaa nyt 80 % rutiinista automaattisesti", sanoo Esimerkki Oy:n toimitusjohtaja Aino Esimerkki.

### 4.5 Boilerplate ennen pääasiaa

Tiedote ei aloita yritysesittelyllä. Ensimmäinen virke kertoo, mitä tapahtui.

❌ "Esimerkki Oy on vuonna 2017 perustettu suomalainen ohjelmistoyhtiö, joka kehittää pk-yrityksille automaation työkaluja. Tänään yhtiö julkaisi..."

✅ "Esimerkki Oy julkaisi tänään 27.5.2026 uuden palvelun pk-yrityksille. [...] Tausta-osa: Esimerkki Oy on vuonna 2017 perustettu..."

### 4.6 Ajatusviivan ylikäyttö

Tiedotteen kieli on jäsenneltyä proosaa, ei ajatusviivapainotteista myyntiretoriikkaa.

❌ "Esimerkki Oy — alan pioneeri — lanseeraa uuden palvelun — pk-yrityksille — joka mullistaa kirjanpidon — automaation avulla."

✅ "Esimerkki Oy lanseerasi kirjanpidon automaatiopalvelun pk-yrityksille."

### 4.7 Kolmiosaiset listat

❌ "Palvelu tarjoaa nopeutta, helppoutta ja luotettavuutta."
✅ "Palvelu hoitaa 80 % rutiinikirjanpidosta automaattisesti."

---

## 5. Tiedotteen tyypit ja niiden erityispiirteet

### 5.1 Lanseeraustiedote

- Otsikko: mitä lanseerataan
- Ingressi: mitä, kenelle, milloin, hinta
- Leipäteksti: tarve, ratkaisu, toiminta
- Sitaatti: johtajan kommentti
- Tausta-osa

### 5.2 Talousluvut-tiedote (kvartaali, vuositulos)

- Otsikko: keskeinen luku
- Ingressi: tärkeimmät mittarit
- Leipäteksti: kontekstit, syyt, vertailu
- Sitaatti: toimitusjohtajan tai talousjohtajan kommentti
- Linkki täysraporttiin tai liite

### 5.3 Henkilöstötiedote (rekrytointi, lähtö, palkitseminen)

- Otsikko: kuka, mihin rooliin
- Ingressi: lyhyt taustaesittely
- Leipäteksti: tausta tarkemmin, miksi tämä rooli
- Sitaatti: rekrytoidun tai johdon kommentti
- Tausta-osa

### 5.4 Muutostiedote

- Otsikko: mikä muuttuu
- Ingressi: muutos lyhyesti + aikataulu
- Leipäteksti: vaikutukset eri sidosryhmiin
- Mitä tehdään, mitä odotetaan vastaanottajalta
- Yhteyshenkilö

### 5.5 Kriisitiedote

Vaatii erityistä huolellisuutta. **Älä tee tätä AI:lla yksin.** Kriisiviestintä vaatii ihmisen harkintaa, juridista tarkistusta ja koordinointia organisaation kanssa. Pyydä apua kriisiviestinnän ammattilaiselta.

---

## 6. Sanitoitu malliesimerkki — lehdistötiedote

```markdown
Tiedote
Julkaisuvapaa heti

27.5.2026

# Esimerkki Oy lanseeraa kirjanpidon automaatiopalvelun pk-yrityksille

Esimerkki Oy julkaisi tänään 27.5.2026 Esimerkki Auto -palvelun, joka automatisoi pk-yritysten kirjanpidon ja laskutuksen. Palvelu maksaa 49 € kuukaudessa ja se on tarkoitettu 1–10 hengen yrityksille. Beeta-vaiheessa palvelua käytti 240 yritystä, joiden kirjanpitoon kuluva aika väheni keskimäärin 6 tunnista 1,5 tuntiin kuukaudessa.

## Tarve syntyy aikaa vievästä rutiinista

Tilastokeskuksen mukaan suomalaisia pk-yrityksiä on noin 280 000, ja niistä suurin osa hoitaa kirjanpidon ulkopuolisella tilitoimistolla. Kuukausimaksut alkavat 200 eurosta ja nousevat liikevaihdon mukaan. Esimerkki Auto antaa pienille yrityksille vaihtoehdon, jossa rutiinityö automatisoituu mutta käyttäjä saa tarkistettavakseen lopputuloksen.

Palvelu tunnistaa kuitit, vientit ja arvonlisäveron automaattisesti. Käyttäjä hyväksyy tai korjaa AI:n ehdotukset, ja valmis tilinpäätös syntyy automaattisesti vuoden lopussa.

## Toimitusjohtajan kommentti

"Pk-yritysten kirjanpito on edelleen liian aikaa vievää. Esimerkki Auto hoitaa nyt 80 % rutiinista, ja yrittäjä voi keskittyä asiakkaisiin", sanoo Esimerkki Oy:n toimitusjohtaja Aino Esimerkki.

## Aikataulu ja saatavuus

Esimerkki Auto on saatavilla suomalaisille pk-yrityksille 1.6.2026 alkaen. Palvelu integroituu Verohallinnon järjestelmiin ja pankkien yleisimpiin tiliöintipalveluihin.

---

Lisätietoja:

Aino Esimerkki
Toimitusjohtaja, Esimerkki Oy
+358 40 000 0000
aino.esimerkki@example.fi

Tietoa Esimerkki Oy:stä

Esimerkki Oy on vuonna 2017 perustettu suomalainen ohjelmistoyhtiö, joka kehittää automaation työkaluja pk-yrityksille. Yhtiössä on 24 työntekijää, ja sen pääkonttori sijaitsee Helsingissä. Esimerkki Oy:n omistavat sen perustajat ja henkilökunta.
```

---

## 7. Tarkistuslista ennen lähetystä

```
[ ] "Tiedote" -merkintä ja julkaisuvapaa/embargo yläosassa
[ ] Päiväys selvästi näkyvillä
[ ] Otsikko kuvaileva, ei yliampuvia adjektiiveja
[ ] Ingressi 1–3 virkettä, vastaa kysymyksiin kuka/mitä/missä/milloin/miksi
[ ] Käänteinen pyramidi: tärkein ensin, taustat lopussa
[ ] Sitaatti tunnistettavalta henkilöltä, virallinen titteli, max 2 virkettä
[ ] Sitaatti kuulostaa ihmisen puhumalta, ei AI-fraasilta
[ ] Yritysesittely (boilerplate) lehdistötiedotteessa lopussa, ei alussa
[ ] Lisätietolohko: nimi, titteli, puhelin, sähköposti
[ ] Päivämäärät [[suomi-lokalisaatio-perus]] -muodossa (27.5.2026)
[ ] Numerot suomen muodossa (12 500 €, 25,5 %)
[ ] Ei kolmiosaisia listoja AI-tyyliin
[ ] Ei ajatusviivan ylikäyttöä
[ ] Ei mahtailuretoriikkaa ("vallankumouksellinen", "mullistava", "ainutlaatuinen")
[ ] [[suomi-ei-ai-sloppia]] tarkistus tehty
[ ] [[suomi-kielihuolto]] tarkistus tehty
[ ] [[suomi-anglismit]] tarkistus tehty
```

---

## 8. Mihin tätä skilliä konsultoidaan

- [[suomi-tarkistuslista]] — pipeline H: tiedote
- [[suomi-rekisteri]] — tiedotteen formaaliuden taso
- [[suomi-ei-ai-sloppia]] — myyntipuheen, sitaattien ja kolmiosalistojen karsinta
- [[suomi-anglismit]] — käännöslainat
- [[suomi-kielihuolto]] — mekaniikka
- [[suomi-sahkoposti]] — saateviesti tiedotteen mukana toimittajille
- [[suomi-lokalisaatio-perus]] — päivämäärät, numerot
