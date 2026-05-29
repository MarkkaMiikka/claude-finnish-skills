---
name: suomi-rekisteri
description: Kalibroi suomenkielisen tekstin rekisteri tarkoituksenmukaiseksi — yleiskieli, ammattikieli, asiakaskieli, puhekieli — ja varmistaa että rekisteri pysyy yhtenäisenä tekstin sisällä. Käytä kun käyttäjä sanoo "tarkista rekisteri", "kuulostaa liian viralliselta", "kuulostaa liian rennolta", "rekisteri vaihtelee", "sopimaton sävy", "muuta yleiskielelle", "muuta ammattikielelle", "muuta asiakaskielelle", tai kun teet sisältöä, jossa eri osioilla on eri sävyvaatimukset (esim. brändin pääsivu = ammattikieli, FAQ = lähempänä asiakaskieltä, blogikommentti = puhekielisempi). Skill tunnistaa rekisterit, ehdottaa kalibrointia ja korjaa rekisterivaihtelua. Ei käsittele mekaniikkaa (yhdyssanat, pilkutus) — käytä siihen [[suomi-kielihuolto]]. Ei käsittele AI-slop -kuvioita — käytä siihen [[suomi-ei-ai-sloppia]].
license: MIT
---

# Suomen rekisterin kalibrointi

> **Vinkki:** Jos haluat ajaa kaikki suomi-* -skillit yhdessä oikeassa järjestyksessä, käytä `[[suomi-tarkistuslista]]` -orkestraattoria. Se valitsee oikeat skillit ja pipeline-järjestyksen tekstin kontekstin perusteella.

## Mitä rekisteri tarkoittaa

Rekisteri on tekstin **kielellinen muotoilu** suhteessa lukijaan ja viestintätilanteeseen. Sama asiasisältö voidaan ilmaista eri rekistereissä, ja jokainen rekisteri viestii lukijalle erilaista suhdetta kirjoittajan ja kohteen välillä.

Suomi käyttää neljää päärekisteriä:

1. **Virallinen / hallinnollinen** — viranomaisteksti, lait, asetukset, viralliset päätökset
2. **Ammattikieli** — asiantuntijatyö, ammattijulkaisut, koulutus, raportointi
3. **Yleiskieli / asiakaskieli** — markkinointi kuluttajille, journalismi, ohjeet, käyttöoppaat, FAQ
4. **Puhekieli / arkikieli** — some-postaukset rennoilla kanavilla, kommentit, henkilökohtainen kirjoittaminen

## Yleisin AI-virhe rekisterissä

AI valitsee usein **yhden rekisterin** ja pitää sen koko tekstin läpi, vaikka teksti vaatii rekisterivaihtelua. Esimerkki: yrityksen verkkosivu, jonka pääsivu on ammattikielinen, mutta FAQ-osa on **kirjoitettu samalla rekisterillä**, vaikka FAQ:n pitäisi olla lähempänä yleiskieltä, koska sen lukijat ovat eri vaiheessa ostopolkua ja eri kielitaidolla.

Toinen yleinen virhe: AI sekoittaa rekistereitä sattumanvaraisesti samassa tekstissä. Yksi virke on virallinen, seuraava puhekielinen, kolmas mainosmainen.

---

## Rekisterin tunnistustestit

Kysy jokaisesta virkkeestä tai kappaleesta:

### 1. Sanaston rekisterimerkki

| Rekisteri | Tyypilliset sanavalinnat |
|---|---|
| Virallinen | "edellä mainittu", "asianomainen", "asiaan kuuluva", "viranomaistaho", "selvitettäväksi" |
| Ammattikieli | "asiantuntija", "toteuttaa", "hyödyntää", "menetelmä", "kokemus" |
| Yleiskieli / asiakaskieli | "auttaa", "käyttää", "tehdä", "saada", "kertoa" |
| Puhekieli | "kattoo", "haluu", "duuni", "hommata", "tsekata" |

### 2. Lauserakenne

| Rekisteri | Lauserakenne |
|---|---|
| Virallinen | Pitkät virkkeet, sivulauseita ketjuissa, passiivi-vahvuus, nominaalimuodot (-minen, -uus, -isuus) |
| Ammattikieli | Keskipitkiä virkkeitä, sekarakenteet, asioiden välisiä suhteita ilmaistaan |
| Yleiskieli | Lyhyemmät virkkeet, aktiivinen ääni, suora ja konkreettinen |
| Puhekieli | Lyhyet virkkeet, ellipsit, kysymyksiä, huokaisuja, kontaktin haku lukijaan ("mietitkö joskus...") |

### 3. Puhuttelutapa

| Rekisteri | Puhuttelu |
|---|---|
| Virallinen | "asianomaisen on", "henkilö voi" — ei suoraa puhuttelua |
| Ammattikieli | "Voitte", "Te" (joissain yhteyksissä), "asiakas" |
| Yleiskieli | "Sinä", "te-kohteliaisuusmuoto valinnainen", suora puhuttelu |
| Puhekieli | "Sä", "sun", "muista että..." |

### 4. Persoonan käyttö

| Rekisteri | Persoona |
|---|---|
| Virallinen | Persoonaton, passiivi, "todetaan", "nähdään" |
| Ammattikieli | "Olemme", "ratkaisemme", harvoin yksittäinen "minä" |
| Yleiskieli | "Me autamme", "kerromme", joskus minä-muoto |
| Puhekieli | "Mä mietin että...", suora ensimmäinen persoona |

---

## Rekisteri-prosessi tekstin tarkastukseen

### Vaihe 1 — Päätä kohderekisteri ennen tekstin lukemista

Kysy itseltäsi (tai pyydä käyttäjältä jos epäselvää):

- **Kuka lukee?** Asiantuntija samalta alalta vs. kuluttaja vs. viranomainen vs. opiskelija
- **Mitä tarkoitusta varten?** Päätöksenteko vs. tutustuminen vs. viihtyminen vs. ohjeen seuraaminen
- **Missä kanavassa?** Verkkosivun pääsivu (ammattikieli yleensä), FAQ (yleiskielinen), some-postaus (puhekielisempi), uutiskirje (asiakaskieli + ammattikieli sekoitus)

### Vaihe 2 — Tarkista yhtenäisyys

Lue teksti läpi ja merkitse:

- **Sanat, jotka eivät kuulu** valittuun rekisteriin (esim. virallinen "edellä mainittu" yleiskielisessä asiakassivulla)
- **Virkkeet, jotka ovat liian raskaita** (pitkät sivulauseet ja nominaalimuodot yleiskielisessä tekstissä)
- **Lauseet, jotka ovat liian rentoja** (puhekielisiä elementtejä ammattikielisessä tekstissä)

### Vaihe 3 — Tarkista rekisterivaihtelu eri osioiden välillä

Joillain teksteillä on legitiimi syy vaihtaa rekisteriä eri osioissa. Esim:

| Tekstin osio | Tyypillinen rekisteri |
|---|---|
| Yrityksen pääsivun hero | Ammattikieli, voi olla mainosmainen |
| Tuotekuvauksen otsikko + ingressi | Ammattikieli |
| Tuotekuvauksen "miten käytät" | Yleiskieli / asiakaskieli |
| FAQ | Yleiskieli / asiakaskieli — vastaa lukijan kysymystä lukijan tasolla |
| Käyttöehdot / tietosuojaseloste | Virallinen (laillinen vaatimus) |
| Asiakaspalvelun chat-bot | Asiakaskieli, jopa puhekielisempi |
| Blog-artikkeli | Ammattikieli + persoona |
| Some-postaus | Puhekielisempi, vaihtelee kanavan mukaan |

Jos teksti on koko ajan yhdessä rekisterissä mutta sen pitäisi vaihdella → korjaa.

### Vaihe 4 — Korjaa

Jokaisen rekisterirajaa rikkovan kohdan kohdalla:

- Tunnista kohderekisteri
- Kirjoita uudelleen kohderekisterissä
- Säilytä asiasisältö

---

## Esimerkit kalibrointitilanteista

### Tilanne 1: Virallinen → Yleiskieli (asiakassivu)

**Ennen (liian virallinen):**
> Edellä mainittujen ehtojen täytyttyä asiakkaan tilauksenmuutosoikeutta voidaan käsitellä. Käsittelyaika muodostuu kahdesta arkipäivästä saapumishetkestä laskettuna.

**Jälkeen (yleiskielinen, asiakaspalvelun FAQ):**
> Kun ehdot täyttyvät, käsittelemme tilauksesi muutoksen. Käsittely kestää tyypillisesti kaksi arkipäivää.

### Tilanne 2: Ammattikieli → Asiakaskieli (verkkosivun "miten käytät")

**Ennen (liian ammattikielistä):**
> Käyttäjä toteuttaa rekisteröitymisen palvelun aloitussivulla ja hyödyntää saamiaan tunnuksia kirjautumiseen.

**Jälkeen (asiakaskielistä):**
> Luot tunnuksen aloitussivulla. Saamillasi tunnuksilla kirjaudut sisään.

### Tilanne 3: Sekarekisteri (epäjohdonmukainen)

**Ennen (rekisteri vaihtelee tarpeettomasti):**
> Mietitkö jos meidän palvelu sopii sulle? No, palvelun käyttöönotto edellyttää sopimuksen tekemistä ja tilausvahvistuksen vastaanottamista. Anyway, ota yhteyttä jos haluat lisätietoja!

**Jälkeen (johdonmukainen yleiskieli):**
> Mietitkö, sopiiko palvelumme sinulle? Käyttöönotto on suoraviivainen: teemme sopimuksen yhdessä ja saat tilausvahvistuksen. Otatko yhteyttä lisätietoja varten?

### Tilanne 4: Puhekielen oikea käyttö (some-kanava)

**Sopiva LinkedIn-puhekielisyys:**
> Mietin tätä eilen kun tein asiakkaalle Q3-raporttia: miksi me kirjoitamme markkinoinnin tuloksista aina samalla tylsällä tavalla? Tässä kolme ajatusta, jotka muuttivat sen.

**Sopiva Instagram-puhekielisyys (samasta aiheesta):**
> Tylsää markkinointiraportointia? Kokeile näitä kolmea.

---

## Tyypillisiä AI-rekisterivirheitä

### 1. Liian-virallinen kuluttajateksti

AI valitsee oletusrekisterinään ammatti- tai virallisen rekisterin, koska harjoitusdataa on enemmän tällaisesta. Lopputulos: kuluttajille suunnattu teksti kuulostaa viranomaisilta.

### 2. Liian-rento ammattilukijoille suunnattu teksti

Ammattijulkaisussa, joka käsittelee teknisiä asioita, kirjoitetaan kuin some-postauksessa. Asiantuntijalukija kokee tekstin epäuskottavaksi.

### 3. Sekaisin rekistereitä samassa tekstissä

Yksi virke on ammattikielistä, seuraava puhekielistä, kolmas mainosmaista. Lopputulos: lukijalla ei ole selvää käsitystä siitä, kenelle teksti on suunnattu.

### 4. Anglismeilla rekisterin rentouttaminen

"Hei guys", "tsekkaa tää", "killer feature" suomenkielisessä tekstissä, jonka muuten pitäisi olla ammattikielinen. Anglismi-rekisteririkko on yleisin some-postauksissa.

### 5. Vääränlainen me-/sinä-puhuttelu

Markkinointitekstissä äkillinen "te-muoto" vaihtaminen sinä-puhutteluun ja takaisin. Joko valitse yksi tai vaihtele harkitusti.

---

## Yhteenveto: rekisteri-tarkistuslista

```
[ ] Kohde-rekisteri valittu ja kirjattu (virallinen / ammattikieli / yleiskieli / puhekieli)
[ ] Sanasto kuuluu kohderekisteriin (ei "edellä mainittu" yleiskielessä, ei "tsekkaa" ammattikielessä)
[ ] Virkerakenne sopii kohderekisteriin (pitkät vs lyhyet, passiivi vs aktiivi)
[ ] Puhuttelutapa johdonmukainen (sä/te/persoonaton — pidä yhtä koko teksti)
[ ] Persoonan käyttö johdonmukainen (me/minä/passiivi — sekoittaminen ei satunnaista)
[ ] Eri osiot (hero, FAQ, käyttöehdot, blogi) ovat omissa rekistereissään mutta jokainen osio on yhtenäinen
[ ] Ei tarpeettomia anglismi-rekisteririkkoja ("guys", "killer", "tsekkaa")
[ ] Lukija tunnistaa selkeästi kenelle teksti on suunnattu pelkän ensimmäisen kappaleen perusteella
```
