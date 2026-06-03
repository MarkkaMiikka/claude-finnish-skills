---
name: suomi-lokalisaatio-perus
description: >
  Suomenkielisen lokalisaation perussäännöt: päivämäärät, kellonajat, numerot, valuutta, prosentit, yksiköt, osoitteet ja puhelinnumerot. Käytä kun muotoilet päivämäärää tai kellonaikaa, kun lokalisoit numerot suomeksi, kun teet hintamerkintöjä, tai kun käyttäjä sanoo "lokalisaatio", "muotoile päivämäärä", "numeroformaatti", "ALV-merkintä", "klo aikamerkintä" tai "Suomi-osoiteformaatti". Tämä on ohjekirjasto, jota muut suomi-* -skillit kuten [[suomi-tarjous]] ja [[suomi-uutiskirje]] konsultoivat.
license: MIT
---

# Suomenkielisen lokalisaation perussäännöt

> **Vinkki:** Jos haluat ajaa kaikki suomi-* -skillit yhdessä oikeassa järjestyksessä, käytä `[[suomi-tarkistuslista]]` -orkestraattoria.

Tämä skill on **ohjekirjasto**. Se ei korjaa tekstiä itse vaan tarjoaa muotoilusäännöt, joihin muut skillit ja käyttäjä voivat tarttua. Lähteenä Kotimaisten kielten keskuksen suositukset sekä SFS-standardit ja Verohallinnon ohjeet.

---

## 1. Päivämäärät

### 1.1 Vakiomuoto eri konteksteissa

| Konteksti | Muoto | Esimerkki |
|---|---|---|
| Lyhyt (UI, lomake, taulukko) | `pp.kk.vvvv` | `27.5.2026` |
| Ilman etunollia (suomalainen vakio) | `p.k.vvvv` ilman etunollia | `27.5.2026`, ei `27.05.2026` |
| Tekstissä | sama lyhyt | `Tapaaminen on 27.5.2026.` |
| Kalenterimainen | `pp. [kuukausi taivutettuna] vvvv` | `27. toukokuuta 2026` |
| Viikonpäivän kanssa | `[viikonpäivä] pp. [kuukausi] vvvv` | `keskiviikko 27. toukokuuta 2026` |
| Tekninen (ISO 8601) | `vvvv-kk-pp` | `2026-05-27` (vain teknisessä yhteydessä) |

**Vältä englannin muotoja:** `5/27/2026`, `27/5/2026`, `May 27, 2026`, `27th May 2026`.

### 1.2 Päivämäärävälit

Käytä ajatusviivaa (en dash, `–`), ei yhdysmerkkiä (`-`):

- `25.–27.5.2026` (sama kuukausi)
- `30.4.–3.5.2026` (eri kuukausi)
- `28.12.2025–2.1.2026` (eri vuosi)

### 1.3 Avoimet välit

- `alkaen 25.5.2026`
- `25.5.2026 alkaen`
- `viimeistään 31.12.2026`

### 1.4 Kuukauden nimi taivutuksessa

Päivämäärässä kuukausi on **partitiivissa**: `27. toukokuuta`, `1. tammikuuta`, `15. helmikuuta`.

---

## 2. Kellonaika

### 2.1 Perusmuoto

| Konteksti | Muoto | Esimerkki |
|---|---|---|
| UI ja teksti | 24h, **piste** erottimena | `14.30` |
| Lähetä-tekstissä | `klo HH.MM` | `klo 14.30` |
| Tekninen logitus, IDE, API | `HH:MM:SS` sallittu | `14:30:00` |

**Vältä:** `14:30` UI:ssa (englanti-konventio), `2:30 PM`, `02:30 pm`, `14.30 h`.

### 2.2 Yhdistetty päivämäärä + kellonaika

- Tekstissä: `27.5.2026 klo 14.30`
- Lyhyessä UI:ssa: `27.5.2026, 14.30`
- Teknisessä: `2026-05-27T14:30:00+03:00` (ISO 8601, vain järjestelmien välisessä siirrossa)

### 2.3 Aikavälit

- `klo 9.00–16.30`
- `klo 14–17` (kun täysien tuntien välejä, minuutit pois)
- `klo 14.30–15.00` (kun minuutteja, molemmissa päissä sama tarkkuus)

---

## 3. Numerot

### 3.1 Desimaalierotin: pilkku

| Oikein | Väärin |
|---|---|
| `12,5` | `12.5` |
| `0,75` | `0.75` |
| `3,14159` | `3.14159` |

Tämä on suomen tärkein eroavuus englannista. Piste on tuhaterotin tai päivämäärässä.

### 3.2 Tuhaterotin: välilyönti (kapea, ei piste)

| Oikein | Väärin |
|---|---|
| `1 234` | `1,234` |
| `1 234 567` | `1.234.567` |
| `12 500 €` | `12,500 €` |

Vakaa välilyönti (`&nbsp;` HTML:ssä, ` ` koodissa) estää rivin katkeamisen luvun keskeltä.

### 3.3 Luvun ja yksikön väli: aina välilyönti

| Oikein | Väärin |
|---|---|
| `25 %` | `25%` |
| `12,50 €` | `12,50€` |
| `25 °C` | `25°C` |
| `5 kg` | `5kg` |
| `100 km/h` | `100km/h` |
| `2 GB` | `2GB` |

### 3.4 Lukujen kirjoittaminen tekstissä

| Konteksti | Konventio | Esimerkki |
|---|---|---|
| Alle 10 yleisessä tekstissä | Sanoin | `kolme asiakasta`, `viisi kertaa` |
| 10 ja yli yleisessä tekstissä | Numeroin | `12 asiakasta`, `47 kertaa` |
| Tekninen / taulukko | Aina numeroin | `3 kg`, `2 m` |
| Rahasummat | Aina numeroin | `5 €`, `12,50 €` |
| Prosentit | Aina numeroin | `5 %`, `25 %` |
| Virkkeen alussa | Sanoin tai uudelleenjäsentelyssä | `Vuonna 2025...`, ei `2025 oli...` |

### 3.5 Järjestysluvut

- Pisteen kanssa: `3.`, `27.`, `100.`
- Taivutusliite, jos taivutusmuoto: `3:n`, `5:nteen` (tämä on kankea — sanoin parempi)
- Suosi sanoja taivutuksessa: `kolmas`, `kolmanteen`, ei `3:nteen`

---

## 4. Valuutta

### 4.1 Euron merkitseminen

| Konteksti | Muoto | Esimerkki |
|---|---|---|
| Tekstissä ja hinnoissa | numero + välilyönti + `€` | `12,50 €` |
| Taulukoissa | sama | `1 250,00 €` |
| Lyhennetyssä viestinnässä | `12,5 €` (jos tarkkuus riittää) | |

**Älä kirjoita:** `€12,50` (englanti-tyyli), `12,50EUR` (ilman välilyöntiä), `12,50 e`.

### 4.2 ALV-erottelu

Suomessa yleinen ALV (arvonlisävero) on 25,5 % (alkaen 1.9.2024). Aiemmin 24 %. Tarkista voimassa oleva taso.

**B2C-hinnoittelu** (kuluttaja-asiakkaat): hinta sisältää ALV:n. Mainoksissa ja hinnastoissa loppuhinta riittää, mutta erottelu lisää selkeyttä.

```
Tuote: 125,50 €
(sis. ALV 25,5 %)
```

**B2B-hinnoittelu** (yritysasiakkaat): hinta ilmoitetaan ilman ALV:tä, ALV eritellään.

```
Konsultointi:       100,00 €/h (ALV 0 %)
ALV 25,5 %:          25,50 €
Yhteensä:           125,50 €
```

**Tarjouksessa**: ks. [[suomi-tarjous]] täydellinen rakenne.

### 4.3 Muut valuutat

- `12,50 USD` tai `12,50 $`
- `10,00 SEK` tai `10,00 kr`
- `100,00 NOK` tai `100,00 kr`

Vältä englannin sijoittelua: `$12.50` muuttuu suomeksi muotoon `12,50 $` tai `12,50 USD`.

---

## 5. Prosentit, lämpötila ja yksiköt

### 5.1 Prosentti

- `25 %` (välilyönti pakollinen)
- Promille: `0,5 ‰`
- Promille-merkki: pikemmin `‰` kuin `%o`

### 5.2 Lämpötila

- `25 °C` (välilyönti astemerkin edessä)
- Pakkasella: `−5 °C` (miinusmerkki on `−`, ei yhdysmerkki `-`)

### 5.3 SI-yksiköt

| Yksikkö | Lyhenne | Esimerkki |
|---|---|---|
| Metri | m | `2 m` |
| Kilometri | km | `100 km` |
| Sekunti | s | `30 s` |
| Tunti | h | `2 h` |
| Kilogramma | kg | `5 kg` |
| Litra | l (tai L) | `2 l`, `2 L` |
| Watt | W | `60 W` |
| Voltti | V | `230 V` |

### 5.4 Tietoyksiköt

| Yksikkö | Lyhenne | Huom |
|---|---|---|
| Tavu | B (tai t) | `1024 B` tai `1 KB` (kontekstista) |
| Kilotavu | KB | `4 KB` |
| Megatavu | MB | `2 MB` |
| Gigatavu | GB | `500 GB` |
| Teratavu | TB | `1 TB` |
| Megabitti / s | Mbit/s | `100 Mbit/s` |

Suomeksi käytetään yleisesti kansainvälisiä lyhenteitä `KB`, `MB`, `GB`.

---

## 6. Osoite

### 6.1 Vakiomuoto kotimaisessa kirjeessä

```
Aino Esimerkki
Esimerkkikatu 12 A 5
00100 HELSINKI
```

Säännöt:
1. Vastaanottajan nimi ensimmäisellä rivillä
2. Katuosoite + numero + porras + huoneisto (kun on)
3. Postinumero (5 numeroa) + välilyönti + kaupungin nimi
4. Kaupungin nimi versaalein on vakiintunut konventio
5. Ei pilkkua postinumeron ja kaupungin välissä

### 6.2 Ulkomaisessa kirjeessä

Lisää maa viimeiselle riville:

```
Aino Esimerkki
Esimerkkikatu 12 A 5
00100 HELSINKI
SUOMI
```

### 6.3 Yrityksen osoite

```
Esimerkki Oy
Aino Esimerkki / Markkinointi
Esimerkkikatu 12 A 5
00100 HELSINKI
```

### 6.4 Porras- ja huoneistomerkinnät

- Porras: iso kirjain ilman pistettä — `A`, `B`, `C`
- Huoneisto: numero porraskirjaimen jälkeen — `A 5`
- Vältä englannin `Apt 5` -muotoa
- "Asunto" sanana ei kuulu osoiteriville suomeksi

---

## 7. Puhelinnumero

### 7.1 Vakiomuodot

| Konteksti | Muoto | Esimerkki |
|---|---|---|
| Kotimainen | `0XX XXX XXXX` | `040 123 4567` |
| Kansainvälinen (Suomi) | `+358 XX XXX XXXX` | `+358 40 123 4567` |
| Lankaverkko | `0X XXX XXXX` | `09 123 4567` (Helsinki) |
| Yleinen palvelunumero | `0XXX XXX XXXX` | `0200 123 4567` |

### 7.2 Säännöt

1. Kotimaisessa muodossa **nolla on alussa**, kansainvälisessä se jätetään pois (`+358 40 ...`, ei `+358 040 ...`)
2. Numero erotetaan välilyönnein luettavuuden vuoksi
3. Sulkeita ei käytetä suuntanumeron ympärillä suomalaisessa konventiossa (`(040) 123 4567` on englanti-tyyli)

---

## 8. Henkilön nimi

### 8.1 Järjestys

Yleinen konventio: `Etunimi Sukunimi`. Vältä englannin `Sukunimi, Etunimi` -järjestystä paitsi listassa, jossa aakkostus vaatii sen.

### 8.2 Tittelin paikka

- Sähköpostissa ja kirjeessä: titteli erilliselle riville nimen alle
- Hakemuksessa: titteli nimen kanssa samalla rivillä on hyväksyttävä: `Aino Esimerkki, KTM`
- Allekirjoituksessa: titteli nimen alla

---

## 9. Mihin tätä skilliä konsultoidaan

Tämä skill on **ohjekirjasto**, ei suora editoija. Muut skillit hakevat täältä säännöt:

- [[suomi-tarjous]] — ALV-erottelu, hinnoittelu
- [[suomi-uutiskirje]] — päivämäärät otsikoissa
- [[suomi-sahkoposti]] — yhteystiedot allekirjoituksessa
- [[suomi-tiedote]] — päivämäärät ja numerot tiedotteessa

---

## 10. Tarkistuslista

Käytä tätä kun viimeistelet suomenkielistä tekstiä, jossa on numeerista tai aikatietoa:

```
[ ] Päivämäärät muodossa pp.kk.vvvv (ei englannin järjestyksessä)
[ ] Kellonajat pisteellä (14.30), 24h
[ ] Desimaali pilkulla (12,5 — ei 12.5)
[ ] Tuhaterotin välilyönnillä (1 234 — ei 1,234)
[ ] Välilyönti luvun ja yksikön välissä (25 %, 12,50 €, 25 °C)
[ ] ALV eritelty B2B-hinnoissa
[ ] Postinumero ennen kaupunkia, ilman pilkkua
[ ] Puhelinnumero ilman sulkeita suuntanumeron ympärillä
[ ] Alle 10 luvut sanoin yleisessä tekstissä
[ ] Ulkomaiset valuutat numero + lyhenne, ei symboli edessä
```
