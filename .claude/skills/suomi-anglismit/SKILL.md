---
name: suomi-anglismit
description: Etsi ja korjaa suoraan englannista käännettyjä sanoja ja rakenteita suomenkielisestä tekstistä. Käytä kun viimeistelet julkaistavaa suomenkielistä sisältöä ja epäilet käännöslainoja, kun käyttäjä sanoo "kuulostaa englannilta", "AI-makuinen sana", "outo yhdyssana", "tämä ei kuulosta suomelta", "tarkista anglismit", "X-laina-sana", tai kun teet final-passin suomenkieliselle markkinointikopiolle, blogiartikkelille, sivuston sisällölle, hakemuksille tai some-julkaisuille. Spesifimpi kuin [[suomi-ei-ai-sloppia]] joka kattaa koko AI-slop-listan — tämä keskittyy vain käännöslainoihin ja anglismeihin. Aktivoituu erityisesti yhdyssanojen kohdalla, joiden alkuosa on erisnimi/lyhenne + jälkimerkitysosa, joka näyttää suoralta käännökseltä englannista (esim. "Helsinki-pohjainen", "eläinlaina", "lähde-stack").
license: MIT
---

# Suomi-anglismit — käännöslainojen tunnistaja ja korjaaja

> **Vinkki:** Jos haluat ajaa kaikki suomi-* -skillit yhdessä oikeassa järjestyksessä, käytä `[[suomi-tarkistuslista]]` -orkestraattoria. Se valitsee oikeat skillit ja pipeline-järjestyksen tekstin kontekstin perusteella.

## Mitä tämä skilli tekee

Käyt suomenkielisen tekstin läpi ja **etsit vain yhden tyyppisiä ongelmia**: sanoja ja rakenteita, jotka ovat suoria käännöksiä englannista ja jotka eivät kuulosta luonnollisilta suomalaiselle korvalle.

Tämä skilli ei kata kaikkea AI-slop-listaa (kolmiosalistat, "edistää"-verbi, mahtipontinen tyyli) — niihin käytä [[suomi-ei-ai-sloppia]]. Tämä skilli ei kata kielioppia (yhdyssanat, pilkutus, sijamuodot) — niihin käytä [[suomi-kielihuolto]].

**Yhden lauseen tunnistustesti:** *"Kun käännän tämän sanan/rakenteen englanniksi sanasta sanaan, kuulostaako alkuperäinen englanniksi? Jos kyllä → todennäköinen anglismi."*

---

## Prosessi

1. **Lue teksti läpi** ja merkitse jokainen sana tai rakenne, joka tuntuu raskaalta, kankealta tai vieraalta suomalaiselle
2. **Käy alla olevat kuviot järjestyksessä** — etsi osumia
3. **Jokaisen osuman kohdalla:** kirjoita uudelleen luontevammalla suomalaisella rakenteella
4. **Vertaa lopuksi:** lukeeko teksti nyt kuin suomalaisen kirjoittamaa?

---

## Kuvio 1: X-pohjainen / X-stack / X-laina / X-import -yhdyssanat

Erisnimen tai lyhenteen + jälkimerkitysosan yhdyssanat ovat tämän skillin **kärkihavainto**. Englannin "X-based / X-stack / X-borrowing / X-import" -rakenne ei toimi suomeksi.

| Anglismi | Korjaus |
|---|---|
| "Helsinki-pohjainen opas" (Helsinki-based guide) | "Helsingin opas" / "Opas Helsinkiin" |
| "Eläinlaina" (animal borrowing) | "Eläinten nimet" / "Eläinaiheinen" |
| "Lähde-stack" (source stack) | "Lähteet" / "Lähde-kombinaatio" |
| "Tech-stack" suomenkielisessä bloggauksessa | "Teknologiat" / "Käytetyt välineet" |
| "Brand-import" | "Tuotu brändi" / "Ulkomainen brändi" |
| "Use-case" suomeksi | "Käyttötapa" / "Esimerkki" / "Sovelluskohde" |
| "Open-source" sellaisenaan | "Avoimen lähdekoodin" (ei "open-source-pohjainen") |
| "Stub-pohja" (stub base) | "Raakaversio" / "Luonnos" / "Alustava versio" |

**Tunnistustesti:** Jos yhdyssanan ALKUOSA on erisnimi tai lyhenne ja JÄLKIOSA on substantiivi, joka kuvaa lähdettä/perustaa/tyyppiä ("-pohjainen", "-stack", "-laina", "-import", "-source", "-base") — todennäköinen anglismi.

---

## Kuvio 2: Verbit käännöslainoina

Englannin verbit, joiden suomalainen vastine on lyhyempi/luontevampi.

| Anglismi | Korjaus |
|---|---|
| "Tehdä päätös" (make a decision) | "Päättää" |
| "Olla sitä mieltä, että" (be of the opinion) | "Uskoa, että" / "Mielestäni" |
| "Ottaa askeleita kohti" (take steps toward) | "Edetä" / "Pyrkiä" |
| "Sukella syvemmälle" (dive deeper) | "Tutustua tarkemmin" / "Syventyä" |
| "Pureutua aiheeseen" (dive into) | "Käsitellä" / "Käydä läpi" |
| "Adressoida ongelma" (address) | "Käsitellä ongelma" / "Puuttua ongelmaan" |
| "Implementoida" (implement) | "Toteuttaa" / "Ottaa käyttöön" |
| "Operoida" (operate) | "Toimia" / "Liikennöidä" / "Hoitaa" |
| "Kannustaa X tekemään" (encourage to) | "Auttaa X tekemään" / "Tukea X:ää" |
| "Innostaa" (inspire) kun ei oikeasti innostua | "Saada kiinnostumaan" |
| "Valtuuttaa" (empower) | "Antaa mahdollisuus" / "Tukea" |
| "Ohjata viralliseen lähteeseen" (we guide) — toistuvasti | "Viittaamme X:ään" / "Lue lisää X:stä" / vaihtele |
| "Antaa neuvoja" (give advice) | "Neuvoa" |
| "Tarjota palvelua" (provide service) | "Palvella" / lyhyemmin |
| "Hahmottaa kokonaisuus" (grasp the whole) | "Ymmärtää" / "Saada käsitys" |

---

## Kuvio 3: Adjektiivit ja kuvalliset substantiivit

| Anglismi | Korjaus |
|---|---|
| "Tarttumapinta" (kuvallisesti — touchpoint) | "Yhteys" / "Kontakti" / poista |
| "Lisäarvo" (added value) | "Hyöty" / poista (usein tyhjä sana) |
| "Saumaton kokemus" (seamless) | "Sujuva" / "Yhtenäinen" |
| "Vaivaton" mainoslauseessa | "Helppo" / "Yksinkertainen" |
| "Intuitiivinen" tuotekuvauksessa | "Selkeä" / "Helppokäyttöinen" |
| "Skaalautuva" sellaisenaan | "Joustava" / "Kasvaa tarpeen mukaan" |
| "Räätälöity" jokaiselle X:lle | "Sovitettu" / "Tehty juuri X:lle" |
| "Kokonaisvaltainen" (holistic) | "Laaja" / "Monipuolinen" — usein poista |
| "Moninainen / monipuolinen" mainoslauseessa | konkreettinen kuvaus mistä on kyse |
| "Rikas" kuvallisesti (rich content) | konkreettinen sana (laaja, syvä, monitahoinen) |
| "Elävä" abstraktista asiasta | "Aktiivinen" / "Toimiva" |
| "Syvällinen" pinnallisesta sisällöstä | konkreettinen sana |
| "Risteyskohta" kuvallisesti (intersection) | "Yhtymäkohta" / "Kohtaamispaikka" |
| "Yhdistyä luontevasti" (connect naturally) | "Sopia hyvin yhteen" / "Jatkua" |
| "Yhdessä näkymässä" (in one view) | "Yhdessä paikassa" / "Samalla sivulla" |
| "Sisältöalue / sisältö-osio" (content area/section) | "Aihealue" / "Osio" |
| "Datapohjaiset" (data-driven) | "Lukuihin perustuva" / "Numeroiden mukaan" |

---

## Kuvio 4: Lauserakenteet käännöslainoina

| Anglismi | Korjaus |
|---|---|
| "Tämä toimii hyvin sekä X että Y" (this works well in both) | "Toimii sekä X:ssä että Y:ssä" / suoraan |
| "Tämä on merkittävä ero" (this is a significant difference) | "Tämä on iso/selvä/olennainen ero" |
| "Tämä korostaa X:n merkitystä" (this highlights) | suoraan kerro X:stä |
| "Tämä heijastaa Y:tä" (this reflects) | "Tämä kertoo Y:stä" / "Y näkyy tässä" |
| "Nimi kantaa 10 vuotta" (the name carries) | "Nimi on 10 vuoden valinta" |
| "Avaa viranomaislähde →" (open source) | "Lue virallinen ohje →" / "Siirry kunnan sivulle →" |
| "Käytännön ongelma, ei teoreettinen" (practical, not theoretical) | poista "ei teoreettinen" — käytännön ongelma riittää |
| "On tärkeää huomata, että" (it's important to note) | suoraan kerro asia |
| "Käytettävissä olevien tietojen perusteella" (based on available info) | konkreettinen lähdeviittaus / poista |

---

## Kuvio 5: Idiomit ja kliseet

| Anglismi | Korjaus |
|---|---|
| "Olla samalla aaltopituudella" (on the same wavelength) | "Ymmärtää toisiaan" / "Sopia yhteen" |
| "Katsoa peiliin" (look in the mirror) — mahtailussa | "Miettiä omaa toimintaa" |
| "Olla tilanteen tasalla" (be on top of things) | "Olla ajan tasalla" / "Tietää" |
| "Ottaa kantaa" jatkuvasti | "Sanoa" / "Kommentoida" |
| "Tuoda esiin" (bring forth) | "Kertoa" / "Esittää" |
| "Pilari" / "kulmakivi" kuvallisesti (pillar/cornerstone) | konkreettinen kuvaus, esim. "tukipuoli" / "perusta" |

---

## Kuvio 6: Omakeksitty terminologia virallisen sijaan

Kun käännät englannin termiä suomeksi, älä keksi käännöstä — tarkista, käytetäänkö Suomessa virallista termiä samasta asiasta. Omakeksitty käännös voi muuttaa merkitystä tai luoda lukijalle harhakuvan.

**Periaate:** Jos asialla on virallinen suomenkielinen termi (laki, viranomainen, ammattisanasto), käytä sitä. Älä käännä englanninkielisestä lähteestä, vaikka käännös vaikuttaisi suoraviivaiselta.

**Tunnistustesti:** Tarkista virallinen lähde (Finlex, viranomaisen sivut, ammattisanakirja, Kielitoimiston sanakirja). Käytetäänkö sanaa sellaisenaan? Jos virallinen termi on toinen, oman muodon käyttäminen heikentää tekstin uskottavuutta ja E-E-A-T:tä.

Esimerkkejä asiayhteyksistä, joissa pitää tarkistaa virallinen termi:
- Lakikäsitteet (Finlex)
- Terveydenhuollon termit (THL, Käypä hoito)
- Veroterminologia (vero.fi)
- Tekniset standardit (SFS)

---

## Kuvio 7: Suomelle vieraat yhdyssana-ketjut

Suomen kielessä yhdyssana voi olla 2–3 osaa, mutta englannin tyyppiset 4+ osaiset (process improvement initiative manager) ovat raskaita.

**Vältä:**
- "Asiakaspalvelukokonaisuuden parantamishanke"
- "Markkinointiviestintästrategiakokonaisuus"
- "Koulutuksenkehittämisaloite"

**Korjaa:**
- Pilko sanaliitoksi: "Hanke asiakaspalvelun parantamiseksi"
- Yksinkertaista: "Strategia markkinointiviestintään"

---

## Työnkulku

### Vaihe 1 — pikalukeminen
Lue teksti läpi normaalisti. Merkitse sanat ja lauseet, jotka pysähdyttävät tai kuulostavat raskailta tai vierailta.

### Vaihe 2 — kuviotarkistus
Käy 7 kuviolistaa läpi järjestyksessä. Etsi osumia.

### Vaihe 3 — tunnistustesti
Jokaisen epäillyn osuman kohdalla: *"Kun käännän tämän englanniksi sanasta sanaan, kuulostaako se englanniksi luontevalta? Entä alkuperäinen suomeksi?"* Jos englannin versio on luonteva ja suomalaisen versio kankea → anglismi.

### Vaihe 4 — korjaus
- Käytä suomen oman ilmaisun rakennetta
- Vaihda raskaat yhdyssanat sanaliitoiksi tai genetiivirakenteiksi
- Lyhennä — suomi on usein lyhyempi kuin englanninkielinen vastine

### Vaihe 5 — viimeistelytarkistus
Lue korjattu teksti ääneen. Jos lause kompastelee tai painottaa väärää sanaa, vielä yksi kierros.

---

## Mitä tämä skilli EI tee

- **Ei kielioppia** (yhdyssana-säännöt, pilkutus, kongruenssi) → [[suomi-kielihuolto]]
- **Ei AI-slop kokonaisuudessaan** (kolmiosalistat, mahtipontinen tyyli, kliseet, "edistää"-verbi) → [[suomi-ei-ai-sloppia]]
- **Ei tyylillistä editointia** (kappalerakenne, rytmi, lukijaystävällisyys)
- **Ei suomen oikolukua sellaisenaan** — keskittyy vain käännöslainakuvioiden tunnistukseen

Käytä rinnan muiden suomenkielisten skillien kanssa kun teet ison viimeistelytarkistuksen.

---

## Tulosmuoto

Jokaisesta löydöksestä:

```
Tiedosto: [polku:rivi]
Anglismi: "[suora sitaatti]"
Selitys: [miksi tämä on käännöslaina — mihin englannin rakenteeseen viittaa]
Korjaus: "[suomalainen vaihtoehto]"
```

Yhteenveto lopussa: kuinka monta osumaa kuvioittain (1–7), kolme yleisintä kuviotyyppiä tekstissä.
