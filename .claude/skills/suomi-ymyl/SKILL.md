---
name: suomi-ymyl
description: Suomenkielisen YMYL-sisällön (Your Money or Your Life — terveys, talous, lakiasiat, turvallisuus, ravitsemus, viranomaisasiat) kirjoittaminen journalist-position framingilla. Käytä AINA kun tuotat tai tarkistat suomenkielistä sisältöä jossa lukijan terveys, raha, turvallisuus tai oikeudet voivat olla riippuvaisia tekstin paikkansapitävyydestä. Aktivoituu kun käyttäjä mainitsee terveydellisen ohjeen, lääkkeen, sairauden, oikeudellisen neuvon, sijoituspäätöksen, lainan, vakuutuksen, ruoka-allergian, turvallisuusohjeen, eläinten hoidon, viranomaisasian, tai pyytää sisältöä joka voi vaikuttaa lukijan päätöksiin näissä aiheissa. Skill ohjaa erottamaan suosittelun (mitä virkamies/asiantuntija on sanonut, lähteen anchor-linkillä) referointiin verrattuna omaan suositteluun (mitä kirjoittaja itse väittäisi — kielletty YMYL-sisällössä ilman virallista pätevyyttä). Käytä rinnan [[suomi-kielihuolto]] ja [[suomi-ei-ai-sloppia]] -skillien kanssa.
license: MIT
---

# YMYL-sisältö suomeksi — journalist-position framing

> **Vinkki:** Jos haluat ajaa kaikki suomi-* -skillit yhdessä oikeassa järjestyksessä, käytä `[[suomi-tarkistuslista]]` -orkestraattoria. Se valitsee oikeat skillit ja pipeline-järjestyksen tekstin kontekstin perusteella.

## Mitä YMYL tarkoittaa

YMYL on Googlen sisältöluokitus: **Your Money or Your Life**. Sisältöä jonka virhe voi vahingoittaa lukijaa rahallisesti, terveydellisesti tai turvallisuudellisesti. Suomeksi: terveys, lääkkeet, ravitsemus, talous, sijoittaminen, lainat, vakuutukset, lakiasiat, oikeudet, viranomaisasiat, turvallisuus, eläinten hoito, lasten hoito.

YMYL-sisällön julkaiseminen ilman pätevää lähdettä on:

- **Eettisesti ongelmallista** — lukija voi tehdä päätöksiä virheellisen tiedon perusteella
- **Juridisesti riskialtista** — joissakin maissa korvausvelvollisuus virheellisen ohjeen seurauksista
- **SEO-haitallista** — Google rankittaa AI-slop -YMYL-sisältöä alaspäin (E-E-A-T -kriteerit: Expertise, Experience, Authoritativeness, Trustworthiness)

## Journalist-position vs. consultant-position

**Konsulttipositio (kielletty YMYL:ssä ilman pätevyyttä):**
> "Kannattaa ottaa metformiinia kahdesti päivässä aterian yhteydessä."
> "Suosittelemme sijoittamaan eläke-säästöt indeksirahastoon."
> "Sinun pitäisi pyytää oikeudenkäyntiavustajalta tarkistus ennen sopimuksen allekirjoittamista."

Tämä on **ohjeistus** — kuin terveysasiantuntija, sijoitusneuvoja, juristi tai eläinlääkäri antaisi.

**Journalisti-positio (sallittu kaikille ilman pätevyyttä):**
> "Diabetesliitto kertoo metformiinin tyypilliseksi annokseksi kaksi kertaa päivässä aterian yhteydessä [linkki Diabetesliiton sivulle]."
> "Finanssivalvonnan ohjeen mukaan vähäriskinen pitkän aikavälin sijoittaminen voi sopia eläke-säästöjen kasvattamiseen [linkki]."
> "Suomen Asianajajaliitto suosittelee oikeudellisen tarkistuksen pyytämistä monimutkaisten sopimusten yhteydessä [linkki]."

Tämä on **referointi**: toistat, mitä pätevä taho on sanonut, ja jätät lukijan vastuulle klikata lähteeseen tarkistamaan.

**Erotuksen ydinsääntö:**
- Konsulttipositio: kerrot lukijalle mitä hänen pitäisi tehdä
- Journalisti-positio: kerrot lukijalle mitä pätevä taho on suositellut, jätät päätöksen lukijalle

---

## YMYL-aluekohtaiset säännöt suomeksi

### A. Terveys ja lääketiede

**Pätevät lähteet, joita voi referoida:**
- THL (Terveyden ja hyvinvoinnin laitos)
- Käypä hoito (Duodecim) — kansalliset hoitosuositukset
- Lääketietokeskus (Pharmaca Fennica)
- Fimea (Lääkealan turvallisuus- ja kehittämiskeskus)
- Yliopistojen lääketieteelliset tiedekunnat
- Erikoislääkärijärjestöt (Suomen Kardiologinen Seura jne.)
- Kelan ohjeet etuuksista
- Suomalainen Lääkäriseura Duodecim

**Vältä:**
- "Suosittelemme" — käytä sen sijaan "Käypä hoito -ohjeen mukaan"
- "Lääke vaikuttaa nopeasti" — käytä "valmisteyhteenvedon mukaan vaikutus alkaa..."
- Annosohjeita ilman lähdettä — aina lähde

### B. Talous ja sijoittaminen

**Pätevät lähteet:**
- Finanssivalvonta
- Suomen Pankki
- Valtiokonttori (eläkkeet, asuntolainat)
- Suomen Vakuutusyhtiöiden Keskusliitto
- Verohallinto
- Etua (Eläketurvakeskus)
- Kuluttajaliitto

**Vältä:**
- "Indeksirahasto on hyvä valinta" — käytä "Finanssivalvonnan kuluttajaohjeen mukaan..."
- "Kannattaa nostaa lainaa nyt korkojen takia" — sijoitusneuvonta, vaatii pätevyyden
- Tuotto-odotuksia ilman lähdettä

### C. Lakiasiat ja oikeudet

**Pätevät lähteet:**
- Finlex (säädökset)
- Korkeimman oikeuden päätökset
- Asianajajaliitto
- Oikeusministeriö
- Kuluttajaviranomainen (KKV)
- Tietosuojavaltuutettu

**Vältä:**
- "Voit irtisanoutua kahden viikon irtisanomisajalla" — käytä "Työsopimuslain (55/2001) 6 luvun mukaan..."
- Oikeudellisia tulkintoja monimutkaisista tapauksista
- Sopimuspohjien suoraa suosittelua ilman juristin tarkistusta

### D. Ravitsemus ja allergiat

**Pätevät lähteet:**
- Ruokavirasto
- VRN (Valtion ravitsemusneuvottelukunta)
- Pohjoismaiset ravitsemussuositukset
- Allergia-, iho- ja astmaliitto
- Suomen Sydänliitto

**Vältä:**
- "Tämä ruoka-aine on terveellinen" — käytä "Ruokaviraston ravintosuosituksen mukaan..."
- Allergioiden hoito-ohjeita
- Erityisruokavalion suosittelua ilman ravitsemusterapeuttipätevyyttä

### E. Eläinten hoito

**Pätevät lähteet:**
- Ruokavirasto (eläinlääkintä)
- Suomen Eläinlääkäriliitto
- Tieteelliset eläinlääkärilehdet
- Lainsäädäntö (Eläinsuojelulaki)
- Rotujärjestöt (kun referoit rotutietoa)

**Vältä:**
- "Tämä rotu sopii lapsiperheeseen" — referoi rotujärjestöä
- Sairauden hoito-ohjeita
- Ravinto-ohjeita ilman eläinlääkärin tai virallisen lähteen referointia

### F. Viranomaisasiat

**Pätevät lähteet:**
- Suomi.fi (viranomaispalvelut)
- Kela
- Migri (Maahanmuuttovirasto)
- Verohallinto
- Tulli
- Trafi (Liikenne- ja viestintävirasto)
- Kuntien virkamiesohjeet

**Vältä:**
- "Sinun pitäisi hakea tätä etuutta" — käytä "Kelan ohjeen mukaan etuuteen voi olla oikeutettu, jos..."
- Päätösaikataulujen ennustaminen
- Henkilökohtaisten päätösten suosittelua

---

## Lauserakenteet — journalist-position framing

Käytä näitä rakenteita YMYL-sisällössä:

| Tilanne | Konsulttipositio (vältä) | Journalisti-positio (käytä) |
|---|---|---|
| Yleinen suositus | "Suosittelemme tekemään X" | "[Pätevä taho] suosittelee X-tekemistä [linkki]" |
| Yksilölle ohje | "Sinun pitäisi tehdä X" | "Tarkista omat olosuhteet [pätevältä taholta]" |
| Annos / määrä | "Ota 2 tablettia päivässä" | "[Lähde] kertoo tyypilliseksi annokseksi 2 tablettia päivässä [linkki]" |
| Ajankohta / aikataulu | "Nopeasti / heti / 2 viikon kuluttua" | "[Lähde] kertoo ajankohdan olevan tyypillisesti..." |
| Vaikutus | "Vaikuttaa nopeasti / hyvin / tehokkaasti" | "[Lähde] dokumentoi vaikutuksen alkavan..." |
| Valinta | "Valitse X" | "[Pätevä taho] kuvaa X:n soveltuvan tilanteeseen, jossa..." |
| Vaara | "Älä tee X — se on vaarallista" | "[Lähde] varoittaa X:n yhteydessä [linkki varoituslehteen]" |

---

## Anchor-link-konventio

Joka väite YMYL-tekstissä joka voisi vaikuttaa lukijan päätökseen:

```markdown
Väite + [linkkiteksti viittaa lähteeseen](URL).
```

**Hyvä esimerkki:**
> Käypä hoito -ohjeen mukaan ([linkki Käypä hoito -ohjeeseen](https://www.kaypahoito.fi/...)) tyypin 2 diabeteksen hoito alkaa elämäntapamuutoksilla.

**Huono esimerkki (puuttuva linkki):**
> Tutkimusten mukaan tyypin 2 diabeteksen hoito alkaa elämäntapamuutoksilla.

"Tutkimusten mukaan" ilman tutkimusviittausta on YMYL-sääntö-rikko.

---

## Tarkistuslista per YMYL-väite

```
[ ] Onko väite kirjoitettu journalisti-positiossa, ei konsulttipositiossa?
[ ] Onko lähde nimetty (organisaatio, virasto, lehti, asiantuntija)?
[ ] Onko lähteeseen anchor-linkki samaan virkkeeseen tai välittömästi sen jälkeen?
[ ] Onko väite tarkistettavissa annetussa lähteessä?
[ ] Onko vältetty "minä suosittelen" / "minun kokemus" -framingia (paitsi jos pätevä)?
[ ] Onko aikaleima viittauksessa (jos lähde voi muuttua: lakiteksti, lääkeohje)?
[ ] Onko vastuuvapauslauseke kohdassa jossa väite voi muuttua tai jossa lukijan tilanne vaatii yksilöllistä arviota?
```

---

## YMYL-vastuuvapauslauseke — milloin tarvitaan

Joissakin YMYL-sisällöissä kannattaa lisätä lyhyt vastuuvapauslauseke:

**Terveyssisällössä:**
> "Tämä artikkeli on yleistasoinen tietoesitys. Yksilölliset hoitopäätökset tee lääkärin kanssa."

**Sijoitussisällössä:**
> "Tämä ei ole sijoitusneuvontaa. Sijoituspäätökset tee oman taloudellisen tilanteesi pohjalta tai pätevän sijoitusneuvojan kanssa."

**Lakiasioissa:**
> "Tämä artikkeli ei korvaa yksilöllistä oikeudellista neuvontaa. Monimutkaisissa tapauksissa pyydä juristin tarkistus."

Älä laita vastuuvapauslauseketta jokaiseen YMYL-virkkeeseen — kerran sopivassa kohdassa riittää.

---

## Yleisiä AI-virheitä YMYL-sisällössä suomeksi

### 1. "Suosittelen" / "kannattaa" -tyyliset toimintakehotukset

AI vetää ne sisään koska markkinointi- ja blogitekstit on tyypillisesti kirjoitettu konsulttipositiossa. YMYL-aiheissa nämä rikkovat sääntöä.

### 2. Tutkimusten "yleinen referointi"

"Tutkimusten mukaan", "asiantuntijat sanovat", "yleisesti tiedetään" ilman nimettyä lähdettä. Anglismi: ympäripyöreä viittaus käännetään suoraan suomeksi.

### 3. Lääkkeiden tai annosten ohjeistus ilman lähdettä

Erityisen riskialtis kategoria. AI saattaa tuottaa annosohjeen joka näyttää oikealta mutta jolla ei ole lähdettä — lukija saattaa toimia sen mukaan.

### 4. Tilastojen / lukujen heittäminen ilman lähdettä

"80 % ihmisistä", "joka kolmas suomalainen" ilman lähde-linkkiä. Joko on tutkimus jonka voi linkittää, tai luku poistetaan.

### 5. Trademark-fraasien siteeraaminen ilman attribuointia

Esim. ammattijärjestön suositus jota ei attribuoida järjestölle. "Asiantuntijajärjestön mukaan..." on parempi kuin "asiantuntijat sanovat..."

### 6. Liian rento rekisteri herkässä aiheessa

YMYL-aiheet vaativat yleensä ammattikielistä tai virallista rekisteriä. Liian rento rekisteri herkässä aiheessa (esim. lapsen oireiden hoito) on epäuskottavaa. Vaikka yleinen "asiakaskielinen" tyyli olisi muutoin oikea brändille, YMYL-osiot voivat poiketa sävyltään.

---

## Final-pass YMYL-tarkistus

```
[ ] Jokainen väite jolla on lukijan päätökseen vaikuttava sisältö on attribuoitu nimettyyn lähteeseen
[ ] Jokainen lähde on linkitetty
[ ] Ei "minä suosittelen / kannattaa / sinun pitäisi" -framingia
[ ] Ei tilastoja tai lukuja ilman lähdettä
[ ] Vastuuvapauslauseke on kerran sopivassa kohdassa jos aihe sitä vaatii
[ ] Rekisteri sopii aiheen vakavuuteen
[ ] Lähdelinkit toimivat ja vievät oikealle sivulle (ei kotisivulle yleisesti)
[ ] Aikamääreet (lakitekstin vuosi, lääkeohjeen päivitys) on tarkistettu tuoreiksi
```