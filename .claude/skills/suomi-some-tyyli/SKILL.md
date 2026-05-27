---
name: suomi-some-tyyli
description: Kirjoita suomenkielisiä some-postauksia kanavakohtaisilla mikrorekistereillä. Käytä kun käyttäjä sanoo "tee LinkedIn-postaus", "kirjoita Instagram-caption", "TikTok-hook", "Facebook-postaus", "tee multi-channel some", "samaan viestiin eri kanavaversiot", tai antaa raakaviestin joka pitäisi muotoilla kanavakohtaisesti. Skill tunnistaa että LinkedIn, Instagram, TikTok ja Facebook ovat omia mikrorekisterejään suomeksi — yhden geneerisen some-version kirjoittaminen ei toimi. Tuottaa per-kanava -versiot oikealla pituudella, sävyllä, rakenteella ja CTA-konventiolla. Käytä rinnan [[suomi-ei-ai-sloppia]] -humanisointi-skillin ja [[suomi-kielihuolto]] -mekaniikkaskillin kanssa final-passissa.
license: MIT
---

# Suomalaiset some-kanavakohtaiset mikrorekisterit

> **Vinkki:** Jos haluat ajaa kaikki suomi-* -skillit yhdessä oikeassa järjestyksessä, käytä `[[suomi-tarkistuslista]]` -orkestraattoria. Se valitsee oikeat skillit ja pipeline-järjestyksen tekstin kontekstin perusteella.

## Lähtökohta

Yksi viesti = neljä erilaista some-postausta. Kanavat eivät ole vaihtoehtoisia muotoja samasta viestistä, vaan omia mikrorekisterejään. AI:n yleinen virhe on tuottaa "geneerinen some-postaus", jonka voi laittaa minne tahansa. Tällainen postaus ei sovi minnekään.

Jokaisella kanavalla on:

- **Oma pituus-konventio** (LinkedIn pidempi, TikTok lyhyempi)
- **Oma hook-tapa** (LinkedIn: kysymys tai oivallus; Instagram: visuaali + caption; TikTok: ensimmäiset 2 sek)
- **Oma rekisteri** (LinkedIn: ammattikieli + persoona; Instagram: yleiskieli + tunne; TikTok: puhekielinen + dynaaminen; Facebook: vaihtelee yleisön mukaan)
- **Oma CTA-konventio** (LinkedIn: keskusteluun kutsuva; Instagram: tallenna/jaa; TikTok: kommentoi/seuraa; Facebook: linkki kommentteihin)
- **Oma hashtag-käytäntö**
- **Oma kappalerakenne**

---

## Kanavakohtaiset säännöt

### LinkedIn — suomenkielinen ammattilainen

**Pituus:** 800–1300 merkkiä (näytetään ilman "näytä lisää" -klikkausta noin 200 merkkiä, joten alkupään pitää koukuttaa).

**Hook (ensimmäinen rivi):**
- Kysymys joka aktivoi tunnistamisen ("Mietitkö joskus, miksi...")
- Oivallus tai kontraindikaatio ("Markkinointitiimit luulevat että X. Se ei ole totta.")
- Henkilökohtainen tarinan alku ("Eilen tein virheen jonka maksoin myöhemmin.")
- Konkreettinen numero alussa ("Käytin viikossa 18 tuntia raporttiin, jonka kukaan ei lukenut.")

**Rakenne:**

```
1. Hook (1–2 riviä)
[tyhjä rivi]
2. Tausta tai konteksti (2–3 lyhyttä riviä)
[tyhjä rivi]
3. Ydin / oivallus / opetus (3–5 lyhyttä riviä, voi olla listamuotoinen)
[tyhjä rivi]
4. Yhteenveto tai kysymys lukijalle (1–2 riviä, kutsuu kommenttiin)
```

**Rekisteri:** Ammattikieli + henkilökohtainen sävy. Ei mainospuhetta. Ei "intohimoinen tuloksentekijä" -kliseitä. Suora ja konkreettinen.

**Hashtagit:** Suomessa hashtagien arvo LinkedInissä on laskenut — 0–3 olennaista tagia loppuun. Älä laita 10. Älä laita yhtä hashtagia per rivi.

**CTA:** Ei "kommentoi 🚀-emojilla" -tyyppisiä. Avoin kysymys joka kutsuu keskusteluun ("Miten teidän tiimissä tämä on ratkaistu?").

**Vältä LinkedInissä:**
- 🚀💡✅-emojien yliannostus
- "PSA:" tai "FRESH TAKE:" -alkukirjoitukset (anglismia)
- "Hot take:" (anglismia)
- Liian pitkä postaus ilman luettavuusrakennetta
- Itsekehu-sävy ("Olen ylpeä, että...")

### Instagram — visuaali + caption

**Pituus:** Caption 100–300 merkkiä optimi. Kun pidempi, taita tyhjillä riveillä luettavaksi.

**Hook:** Captionin ensimmäiset 125 merkkiä näkyvät syötteessä — laita avain sinne.

**Rakenne:**

```
1. Hook / pääviesti (1–2 riviä, ensimmäinen näkyvä)
[tyhjä rivi]
2. Konteksti tai laajennus (2–4 riviä jos tarvitaan)
[tyhjä rivi]
3. CTA (1 rivi, tarkka: "Tallenna myöhempää varten", "Lue lisää linkistä biossa", "Kommentoi alle")
[tyhjä rivi]
4. Hashtagit (5–15 olennaista, voi laittaa myös ensimmäiseen kommenttiin)
```

**Rekisteri:** Yleiskieli + tunne. Visuaalin tukena. Lyhyemmät virkkeet kuin LinkedInissä.

**Hashtagit:** 5–15 olennaista. Sekoita laajaa (#markkinointi) ja kapeaa (#B2B-markkinointi-suomi). Ei kaikki hashtagit samalla rivillä Captioniin — ensimmäiseen kommenttiin tai erotettuna tyhjillä riveillä.

**Vältä Instagramissa:**
- Liian pitkä caption ilman tyhjiä rivejä (lukijaystävällisyys)
- Geneeriset hashtagit (#love #life) jotka eivät kuvaa sisältöä
- CTA ilman selkeää ohjeistusta ("klikkaa biota" → "Linkki biossa")
- LinkedIn-tyylinen ammattikielinen virke

### TikTok — caption + hook (videon kanssa)

**Pituus:** 80–150 merkkiä Captionissa. Hook on itse videon ensimmäiset 2 sekuntia, ei Caption.

**Caption-rooli:** Vahvistaa hookia, ei toista videota. Lisää konteksti, esittää kysymyksen, antaa kommenttisysäys.

**Rakenne:**

```
[Caption: 1 lyhyt rivi joka tukee videon hookia tai kontekstoi sen]
[Tyhjä rivi]
[CTA: 1 lause joka kutsuu sitoutumaan — kommentti, seuraaminen, tallennus]
[Tyhjä rivi]
[Hashtagit: 3–6 olennaista, ei spämmiä]
```

**Rekisteri:** Puhekielisempi kuin Instagram. Lyhyt, suora. Tunnustetaan että lukija on lyhyellä huomiokyvyllä.

**Hashtagit:** 3–6 — ei enempää. TikTok-algo painottaa muita signaaleja enemmän kuin hashtageja. Käytä mieluummin 1 trendaava + 2 niche + 1 brändi.

**Vältä TikTokissa:**
- Liian pitkä Caption (TikTokin Caption-näkyvyys on rajallinen)
- LinkedIn-tyylinen pitkä rakenne
- Hashtag-spämmi 20+ tagia
- "Linkki biossa" ilman selkeää syytä lukijalle klikata

### Facebook — vaihteleva yleisö, kontekstin mukaan

**Pituus:** Vaihtelee. Yritystilien postaukset 100–500 merkkiä. Pidemmät tarinat-tyyliset 500–1200 merkkiä.

**Rakenne:** Vähemmän formaalia rakennetta kuin muilla. Yksi suora viesti + linkki + CTA.

**Rekisteri:** Yleiskielinen, lähempänä asiakaskieltä. Vanhempi yleisö → vähemmän anglismeja, ei TikTok-puhekielisyyttä.

**Hashtagit:** Facebook-hashtagit ovat heikkoja. 0–3 jos käytetään.

**CTA:** Suora linkki + lyhyt selitys ("Lue koko juttu täältä:").

**Vältä Facebookissa:**
- TikTok-tyylinen puhekielisyys (yleisö vanhempi keskimäärin)
- Instagram-tyylinen visuaalikeskeisyys ilman tekstin tukea
- LinkedIn-tyylinen ammattijargon kuluttajalle

---

## Multi-channel prosessi

Kun pyydetään yksi viesti → 4 kanavaa:

### Vaihe 1 — Ydinviesti

Tunnista mikä on **se yksi asia** jonka jokaisen kanavan version lukijan pitää saada. Tämä on lähtö-kapseli kaikkiin neljään.

### Vaihe 2 — Kohdeyleisö per kanava

| Kanava | Tyypillinen suomalainen yleisö |
|---|---|
| LinkedIn | B2B-ammattilainen, esihenkilö, asiantuntija, työnhakija |
| Instagram | Sekoittunut B2C-yleisö, brändifaneja, visuaalisia päätöksiä tekeviä |
| TikTok | Nuorempi keskimäärin, viihdettä, lyhyt huomiokyky, mobiili |
| Facebook | Vanhempi keskimäärin, yhteisölliset jaot, tarinat, suorat ostopäätökset |

### Vaihe 3 — Per-kanava kirjoitus

Kirjoita kanavakohtaiset versiot tyhjästä. Älä käännä yhtä versiota toisesta. Joka versio:

- Käyttää kanavan rakenne-konventiota
- Käyttää kanavan rekisteriä
- Optimoi kanavan algoritmisille signaaleille (LinkedIn: kommentit; Instagram: tallennukset; TikTok: katseluaika; Facebook: jaot)

### Vaihe 4 — Hashtag-strategia per kanava

Kuten yllä — eri kanavat = eri hashtag-strategiat. Ei copy-paste samaa hashtag-listaa kaikille.

### Vaihe 5 — Final-pass per versio

Aja jokainen versio läpi:
- [[suomi-ei-ai-sloppia]] (poistaa AI-fraasit + kliseet)
- [[suomi-kielihuolto]] (mekaniikka)
- [[suomi-anglismit]] (jos teksti voi sisältää käännöslainoja)

---

## Yhden viestin esimerkki neljässä kanavassa

**Lähtöviesti:** "Tein tällä viikolla tutkimuksen oman aikataulun käytöstä — kolme tuntia päivässä menee kokouksiin joista 40 % olisi voitu hoitaa sähköpostilla."

### LinkedIn-versio (1100 merkkiä)

```
Mietin koko viikon: miksi en saa mitään aikaiseksi.

Pidin kirjaa kalenteristani 5 työpäivän ajan. Joka tunti, mihin se meni.

Lopputulos: kokouksia 3 tuntia per päivä. Niistä 40 % olisi pystytty hoitamaan sähköpostilla.

Tämä ei ole uutta — kaikki tietävät että kokouksia on liikaa. Mutta numero tekee siitä konkreettista:

— 15 tuntia viikossa kokouksissa
— 6 tuntia viikossa kokouksissa jotka eivät tarvinneet kokousta
— Yksi työpäivä, jolla olisin tehnyt todellista työtä

Kolme muutosta jotka teen ensi viikolla:

1. Oletus uusiin kokouspyyntöihin: "Voiko tämän hoitaa sähköpostilla?"
2. 15 min kokoukset 30 min sijasta paikkalla missä mahdollista
3. Ei tiistain kokouksia ennen klo 13:00 — aamupäivä syvä työpäivä

Onko teidän tiimissä tehty samaa harjoitusta? Mitä tuli ilmi?
```

### Instagram-versio (250 merkkiä Captionissa + hashtagit)

```
Pidin kirjaa kokouksistani viikon ajan. Tulos: 40 % niistä olisi voitu hoitaa sähköpostilla.

15 tuntia viikossa kokouksissa. 6 tuntia hukattua.

Tallenna myöhempää varten. Kerro kommenteissa: missä SINUN aika menee?
```

[Hashtagit ensimmäiseen kommenttiin: #työelämä #produktiivisuus #etätyö #kokoukset #ajanhallinta #urakehitys #suomi]

### TikTok-versio (Caption, oletus että video sisältää itse keskeisen)

```
Pidin kirjaa kokouksistani viikon. Numero jonka huomasin: 40 %.

Kommentoi alle: oletko itse mitannut?

#työ #ajanhallinta #kokoukset
```

### Facebook-versio (paikallinen B2B-ryhmä)

```
Tein viikon kokeen: pidin kirjaa kalenterista tunti kerrallaan. Lopputulos: 15 tuntia viikossa kokouksissa, joista lähes 6 tuntia olisi pystytty hoitamaan sähköpostilla.

Kolme muutosta seuraavaan viikkoon — kirjoitin tästä pidemmin LinkedInissä, linkki kommentteihin.

Onko muilla samanlaisia kokemuksia? Mitä työkaluja kalenterin analyysiin?
```

---

## Yhteenveto: per-kanava tarkistus

```
[ ] Pituus oikea per kanava (LinkedIn 800–1300, Instagram 100–300, TikTok 80–150, Facebook 100–1200)
[ ] Hook sopii kanavalle (LinkedIn: kysymys/oivallus; IG: ensimmäiset 125 merkkiä; TikTok: video-hook; Facebook: suora)
[ ] Rekisteri kanavakohtainen (LinkedIn ammattikieli, IG yleiskieli + tunne, TikTok puhekielinen, Facebook yleiskielinen)
[ ] CTA kanavakohtainen (LinkedIn: keskustelu; IG: tallenna/jaa; TikTok: kommentti/seuraa; Facebook: linkki)
[ ] Hashtagit kanavakohtaiset (LinkedIn 0–3, IG 5–15, TikTok 3–6, Facebook 0–3)
[ ] Ei copy-paste samaa tekstiä kaikkiin kanaviin
[ ] Anglismit + AI-slop + kielihuolto -tarkistukset tehty jokaiselle versiolle erikseen
```
