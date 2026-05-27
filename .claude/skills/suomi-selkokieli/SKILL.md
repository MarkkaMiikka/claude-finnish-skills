---
name: suomi-selkokieli
description: Muunna monimutkainen suomenkielinen teksti (virastokieli, ammattikieli, lainopillinen teksti, sopimusteksti) selkokielelle tai sen lähimmäksi vastineeksi. Käytä kun käyttäjä sanoo "tee tästä selkokielinen", "yksinkertaista", "muunna virastokielestä", "tee tästä luettavampi", "saavutettava versio", "selkokielistä", tai antaa monimutkaisen tekstin joka pitää avata laajemmalle lukijakunnalle. Skill noudattaa Selkokeskuksen ohjeita: lyhyt virke, yksi ajatus per virke, tuttu sanasto, konkreettiset esimerkit, looginen jäsentely. Ei kata pelkkää oikolukua — käytä siihen [[suomi-kielihuolto]]. Ei kata AI-slop -kuvioita — käytä siihen [[suomi-ei-ai-sloppia]]. Ei kata rekisterin tunnistamista — käytä siihen [[suomi-rekisteri]].
license: MIT
---

# Suomenkielisen tekstin selkokielistäminen

> **Vinkki:** Jos haluat ajaa kaikki suomi-* -skillit yhdessä oikeassa järjestyksessä, käytä `[[suomi-tarkistuslista]]` -orkestraattoria. Se valitsee oikeat skillit ja pipeline-järjestyksen tekstin kontekstin perusteella.

## Mitä selkokieli on

Selkokieli on suomen kielen muoto, joka on tarkoituksellisesti yksinkertaisempi rakenteeltaan, sanastoltaan ja sisällöltään kuin yleiskieli. Selkokielen viralliset ohjeet löytyvät Selkokeskuksesta (Kehitysvammaliitto). Tarkoitus: tieto on ymmärrettävä laajalle lukijakunnalle.

Lukijoita joille selkokieli on tarpeellista:

- Maahanmuuttajat ja suomea toisena kielenä opiskelevat
- Lukivaikeudesta kärsivät
- Vanhempi väestö
- Kognitiivisesti haastavissa elämäntilanteissa olevat
- Lapset jotka oppivat itsenäistä lukemista
- Kuka tahansa kiireinen joka haluaa tiedon nopeasti

Selkokielistäminen on rakenteellinen muunnos, joka säilyttää sisällön mutta avaa muodon. Pelkkä virkkeiden lyhentäminen ei riitä.

Tämä skill tähtää **selkokielen lähimmäksi vastineeksi**, ei välttämättä viralliseen Selkokeskuksen sertifioituun selkokieleen. Jos haluat virallisen selkomerkin, hae se Selkokeskuksen tarkastamana.

---

## Selkokielen ydinsäännöt

### 1. Yksi ajatus per virke

Pitkä virastokielinen virke joka sisältää 3–5 ajatusta jaetaan 3–5 virkkeeseen.

**Ennen (yleiskielinen):**
> Asiakkaan tulee toimittaa allekirjoitettu sopimus alkuperäisenä kahden viikon kuluessa siitä, kun se on hänelle lähetetty, jotta käsittely voidaan aloittaa ilman lisäselvityksiä.

**Jälkeen (selkokielisempi):**
> Sopimus pitää allekirjoittaa.
> Lähetä allekirjoitettu sopimus takaisin meille.
> Lähetä sopimus kahden viikon sisällä siitä, kun sait sen.
> Sen jälkeen voimme aloittaa käsittelyn.

### 2. Lyhyet virkkeet

Pyri 5–10 sanaan per virke. Pidempi virke on aina ehdokas pilkkomiselle.

### 3. Aktiivinen ääni, ei passiivi

| Vältä | Käytä |
|---|---|
| "Hakemus käsitellään" | "Käsittelemme hakemuksen" |
| "Asiakkaalle lähetetään" | "Lähetämme asiakkaalle" |
| "Päätöstä voidaan hakea" | "Voit hakea päätöstä" |

### 4. Tuttu sanasto

Vältä:
- Hallinnollinen sanasto (asianomainen, mainittu, kuuluva, säätelemä)
- Tieteellinen sanasto ilman selitystä
- Ammattisanasto ilman selitystä
- Anglismit (implementoida, optimoida)
- Vanhahtava sanasto (toimittaa, ilmoittaa, lausua)

Käytä:
- Tuttu, jokapäiväinen sanasto
- Lyhyet sanat
- Suorat verbit (tehdä, antaa, ottaa)

### 5. Konkretiat abstrakteiden sijaan

| Abstrakti | Konkreettinen |
|---|---|
| "Tukea tarvitsevat henkilöt" | "Ihmiset joilla on vaikeuksia" |
| "Toimintaa edistävät toimet" | "Asiat jotka auttavat" |
| "Sopeutumisaikaa edellytetään" | "Tarvitset aikaa tottua" |

### 6. Yksi näkökulma per kappale

Kappale ei sisällä useita aiheita. Yksi pääajatus, jota tukee 2–3 selittävää virkettä.

### 7. Looginen järjestys

- Aika-järjestyksessä jos kuvataan prosessi (ensin tämä, sitten tämä, sitten tämä)
- Tärkein ensin, vähemmän tärkeä sitten
- Yleinen ensin, yksityiskohdat sitten

### 8. Suora puhuttelu sinä-muodolla

| Yleiskieli | Selkokieli |
|---|---|
| "Henkilö voi hakea" | "Sinä voit hakea" |
| "Asiakkaan tulee" | "Sinun pitää" |
| "Hakijalle ilmoitetaan" | "Saat tietää" |

### 9. Vältä metafora-puhetta

- Vältä: "vahva pohja", "rohkea askel", "polkua eteenpäin"
- Käytä: konkreettinen kuvaus mitä tapahtuu

### 10. Apusanat ovat sallittuja, jopa suositeltavia

Selkokielessä pienet selventävät sanat eivät ole "täytettä" — ne auttavat lukijaa:

- "Tämä tarkoittaa..."
- "Esimerkiksi..."
- "Toisin sanoen..."
- "Yksinkertaisesti sanottuna..."

---

## Selkokielistämisen prosessi

### Vaihe 1 — Tunnista kohdelukija

Jos selkokielistät tekstin "maahanmuuttajille" se voi vaatia eri valintoja kuin "lukivaikeudesta kärsiville". Jos kohde on yleinen "saavutettava versio", noudata yleisiä selkokielen sääntöjä.

### Vaihe 2 — Etsi raskaat rakenteet

Lue alkuteksti ja merkitse:

- Virkkeet joissa on enemmän kuin 15 sanaa
- Sanat jotka voivat olla tuntemattomia
- Lauseet jotka sisältävät useita ajatuksia
- Passiivit
- Abstraktit ilmaisut

### Vaihe 3 — Pilko virkkeet

Jokainen merkitsemäsi pitkä virke = useampi lyhyt virke. Kirjoita alkuperäinen ajatus uudelleen niin että jokainen virke sisältää vain yhden ajatuksen.

### Vaihe 4 — Vaihda sanasto

Vaihda tuntemattomat sanat tuttuihin. Jos ammattisanasta ei pääse eroon (esim. lakitermi), selitä sana välittömästi:

> "Asianajopalkkio. Se tarkoittaa rahaa jonka maksat juristille."

### Vaihe 5 — Vaihda passiivi aktiiviksi

Tunnista kuka tekee. Kirjoita siinä muodossa.

### Vaihe 6 — Lisää lukijaystävällisyyttä

- Otsikoita jokaiselle uudelle aiheelle
- Listoja jos asioita on monta
- Tyhjiä rivejä kappaleiden väliin
- Tummennuksia avain-sanoille

### Vaihe 7 — Lue ääneen

Selkokielinen teksti pitää voida lukea ääneen sujuvasti. Jos kompastelet, vielä yksi kierros.

---

## Esimerkit kokonaisista muunnoksista

### Esimerkki A: Virkainfo lainoista

**Ennen (virkainfo, yleiskielinen):**
> Lainan myöntäminen edellyttää säännöllistä tuloa ja vakavaraisuusarvion läpäisyä. Hakemus käsitellään 14 arkipäivän kuluessa siitä, kun kaikki tarvittavat liitteet ovat saapuneet käsittelijälle. Negatiivisen päätöksen yhteydessä on mahdollista pyytää lisäselvitystä tai tehdä uusi hakemus muutetuilla tiedoilla.

**Jälkeen (selkokielisempi):**
> ## Lainan saaminen
>
> Tarvitset säännölliset tulot saadaksesi lainan.
>
> Tutkimme myös taloudellista tilannettasi.
>
> ## Käsittelyaika
>
> Käsittelemme hakemuksen 14 arkipäivässä.
>
> Käsittely alkaa sen jälkeen kun olemme saaneet kaikki liitteet.
>
> ## Jos saat kielteisen päätöksen
>
> Voit pyytää meiltä selvitystä.
> Voit myös tehdä uuden hakemuksen.
> Uudessa hakemuksessa voit antaa lisää tietoja.

### Esimerkki B: Sosiaaliturvan etuusohje

**Ennen (yleiskielinen):**
> Yleisen asumistuen myöntäminen edellyttää, että hakija asuu vakituisesti Suomessa ja että hänen kotitaloutensa kuukausitulot eivät ylitä asuntotyypille ja perhekoolle määriteltyjä tulorajoja. Asumistuen määrä lasketaan hyväksyttävien asumismenojen, perusomavastuun ja tulojen perusteella.

**Jälkeen (selkokielisempi):**
> ## Voitko saada asumistukea?
>
> Asumistukea voi saada kun:
>
> - Asut Suomessa vakituisesti.
> - Tulosi eivät ole liian suuria.
>
> Tulorajat ovat erilaisia eri perheille ja asunnoille.
>
> ## Kuinka paljon asumistukea voit saada?
>
> Asumistuki riippuu kolmesta asiasta:
>
> - Kuinka paljon vuokra maksaa.
> - Mikä on omavastuusi (osa jonka maksat itse).
> - Kuinka paljon tienaat.

### Esimerkki C: Sopimusehto

**Ennen (lainopillinen):**
> Sopimuksen voimassaolo on jatkuva, kunnes jompikumpi sopimusosapuoli irtisanoo sen kirjallisesti vähintään yhden kuukauden irtisanomisaikaa noudattaen.

**Jälkeen (selkokielisempi):**
> Sopimus on voimassa jatkuvasti.
>
> Kumpikin voi lopettaa sopimuksen.
>
> Lopettamisesta pitää ilmoittaa kirjallisesti.
>
> Sopimus loppuu kuukauden kuluttua ilmoituksesta.

---

## Selkokielen rajat — mitä se EI ole

Selkokielistäminen ei ole:

- **Lapsille kirjoittamista.** Selkokieli on aikuislukijan tekstiä jonka ymmärrettävyyttä on parannettu.
- **Sisällön köyhdyttämistä.** Kaikki olennainen säilyy.
- **Slangia tai puhekieltä.** Selkokieli on kirjakieltä, vaikkakin yksinkertaista.
- **Mainospuhetta.** Se ei voi olla "innostavaa" tai "vetävää" tavalla joka peittäisi sisältöä.
- **Käännöstä.** Se on suomesta suomeen muunnos.

---

## Selkokielen tarkistuslista

```
[ ] Yksi ajatus per virke
[ ] Virkkeet keskimäärin 5–10 sanan pituisia
[ ] Aktiivinen ääni hallitseva
[ ] Tuttu sanasto, ammattisanat selitetty
[ ] Konkreettisia ilmaisuja abstraktien sijaan
[ ] Sinä-muotoinen puhuttelu (jos sopiva)
[ ] Selventäviä apusanoja ("tämä tarkoittaa", "esimerkiksi")
[ ] Otsikoita uudelle aiheelle
[ ] Listat jos asioita on monta
[ ] Looginen järjestys (aika tai tärkeys)
[ ] Ei metafora-puhetta
[ ] Voi lukea ääneen ilman kompastelua
[ ] Sisältö on säilynyt, vaikka muoto on muuttunut
```

---

## Virallinen selkomerkki

Suomessa selkokielisellä tekstillä voi olla virallinen Selkokeskuksen myöntämä selkomerkki. Se vaatii Selkokeskuksen tarkastuksen ja yleensä kustannukset. Jos tarvitset virallisen merkin (esim. julkisen sektorin sisältö, jolle saavutettavuusvaatimukset koskevat), ohjaa lopullinen versio Selkokeskukseen tarkastettavaksi. Tämä skill auttaa pääsemään läheltä selkomerkin tasoa mutta ei myönnä merkkiä.

Selkokeskus: [selkokeskus.fi](https://selkokeskus.fi/)
