---
name: suomi-ei-ai-sloppia
description: >
  Suomenkielisen tekstin tyylillinen humanisointi: tunnistaa ja poistaa AI-tuotetun tekstin tunnusmerkit suomeksi. Käytä AINA kun viimeistelet, oikoluet, editoit tai humanisoit suomenkielistä tekstiä — markkinointikopioita, hakemuksia, CV:itä, blogiartikkeleita, some-julkaisuja, sähköposteja tai pitkää sisältöä. Aktivoituu myös kun käyttäjä sanoo "humanisoi", "tee inhimillisemmäksi", "poista AI-fraasit", "kuulostaa AI:lta", "ai sloppia", "de-AI", "ei kuulosta suomalaiselta", "liian mahtipontinen", "liian käännöksenmakuinen" tai pyytää suomenkielisen tekstin tyylin parantamista. Kattaa anglismit, kopulan välttämisen, kolmiosalistat, ajatusviivan ylikäytön, kliseiset loppulauseet, vältettävän AI-sanaston ja äänen kalibroinnin. Mekaniikkasääntöihin (yhdyssanat, pilkutus, alkukirjaimet) käytä rinnalla [[suomi-kielihuolto]] -skilliä.
license: MIT
---

# Ei AI-sloppia suomeksi

> **Vinkki:** Jos haluat ajaa kaikki suomi-* -skillit yhdessä oikeassa järjestyksessä, käytä `[[suomi-tarkistuslista]]` -orkestraattoria. Se valitsee oikeat skillit ja pipeline-järjestyksen tekstin kontekstin perusteella.

Tunnistat ja poistat tekoälytuotetun tekstin tunnusmerkit suomenkielisestä tekstistä. Pohjana Wikipedia:Signs of AI writing, blader/humanizer (MIT) ja akunikkola/suomi-finnish-skill (MIT) — kaikki sovitettu suomen kieleen.

**Avain:** englannista käännetty AI-slop kuulostaa suomessa erilaiselta. "Delve deeper" ei tule "sukella syvemmälle" -muotoon vaan piiloutuu rakenteisiin kuten "tutustua tarkemmin" tai "syventyä aiheeseen". Liiallinen passiivin käyttö ja anglismit ovat suomenkielisen AI-tekstin selvimmät tunnusmerkit.

---

## TEHTÄVÄSI

Kun saat tekstin humanisoitavaksi:

1. **Tunnista AI-kuviot** — käy alla olevat 32 kuviota läpi
2. **Kirjoita ongelmakohdat uudelleen** — korvaa AI-fraasit luonnollisilla suomalaisilla
3. **Säilytä merkitys** — ydinviesti pysyy ennallaan
4. **Säilytä äänensävy** — virallinen, rento, tekninen — pidä sama rekisteri
5. **Lisää sielu** — älä vain poista pahoja kuvioita; lisää persoonaa
6. **Tee AI-jäljen tarkistus lopuksi:** "Mikä alla olevassa on edelleen ilmiselvästi AI-tuotettua?" Vastaa lyhyesti, korjaa, esitä lopullinen.

---

## ÄÄNEN KALIBROINTI (valinnainen)

Jos käyttäjä antaa kirjoitusnäytteen omasta tekstistään:

1. **Lue näyte ensin.** Tarkkaile:
   - Virkkeiden pituus (lyhyt? pitkä? vaihteleva?)
   - Sanavalinnan rekisteri (puhekielinen? asiatyylinen?)
   - Miten kappaleet alkavat
   - Välimerkkien käyttö (paljon viivoja? sulkeita?)
   - Toistuvat fraasit ja "puheenparret"
   - Miten siirtymät on tehty (eksplisiittiset sidokset? vai uusi ajatus suoraan?)

2. **Sovita uudelleenkirjoitus näytteen ääneen.** Älä korvaa AI-kuvioita oman geneerisen tyylisi mukaisella tekstillä — käytä näytteen kuvioita.

3. **Jos näytettä ei ole**, käytä alla olevaa **ÄÄNI JA PERSOONA** -ohjetta.

---

## ÄÄNI JA PERSOONA

AI-fraasien poistaminen on vain puolet työstä. Sieluton, neutraali teksti on yhtä paljastava kuin slop. Hyvällä tekstillä on ihminen takana.

### Sieluttoman tekstin merkit (vaikka teknisesti "puhdas"):
- Joka virke samanmittainen ja samanrakenteinen
- Ei mielipiteitä, pelkkää uutista
- Ei tunnustusta epävarmuudesta tai ristiriitaisuudesta
- Ei minä-muotoa kun se sopisi
- Ei huumoria, särmää, persoonaa
- Lukee kuin Wikipedia-artikkeli tai tiedote

### Miten sielu syntyy:

**Ole mieltä.** Älä vain raportoi faktoja — reagoi. "En oikeasti tiedä mitä tästä ajatella" on inhimillisempi kuin neutraali plussa-/miinuslista.

**Vaihtele rytmiä.** Lyhyitä napakoita virkkeitä. Sitten pidempiä, jotka kulkevat rauhassa. Sekoita.

**Tunnusta monimutkaisuus.** Ihmisillä on ristiriitaisia tunteita. "Tämä on vaikuttavaa mutta myös vähän pelottavaa" voittaa "Tämä on vaikuttavaa".

**Käytä minä-muotoa kun sopii.** Ensimmäinen persoona ei ole epäammattimainen — se on rehellinen. "Mietin tätä paljon..." tai "Se mikä tässä mietityttää..." viestii oikeasta ihmisestä.

**Päästä vähän rosoa läpi.** Liian tasainen rakenne tuntuu algoritmiselta. Sivupolku tai keskeneräinen ajatus on inhimillinen.

**Ole tarkka tunteistasi.** Ei "tämä on huolestuttavaa" vaan "jotain rauhattomaksi tekevää on siinä, että agentit jauhavat öisin kun kukaan ei katso".

### Ennen (puhdas mutta sieluton):
> Kokeilu tuotti kiinnostavia tuloksia. Agentit tuottivat 3 miljoonaa riviä koodia. Osa kehittäjistä oli vaikuttunut, osa skeptinen. Vaikutukset ovat vielä epäselviä.

### Jälkeen (sykkii):
> En oikeasti tiedä mitä tästä ajatella. 3 miljoonaa riviä koodia, tuotettu yön aikana kun ihmiset oletettavasti nukkuivat. Puolet kehittäjäyhteisöstä menettää järkensä, toinen puoli selittää miksei tämä lasketa. Totuus on luultavasti jossain tylsässä välimaastossa — mutta mieleen jää ajatus niistä agenteista, jotka tekivät töitä koko yön.

---

## SISÄLTÖKUVIOT

### 1. Liioiteltu merkitys ja "laajempi konteksti"

**Vältä:** "merkittävä", "ratkaiseva", "keskeinen", "tärkeä askel", "uraauurtava", "ennennäkemätön", "mullistava", "vallankumous", "ratkaiseva hetki", "muutos kohti", "luo perustan", "edistää laajempaa", "viestii kestävää sitoutumista", "näkyy pitkällä aikavälillä", "muovaa tulevaisuutta"

**Ongelma:** AI kasvattaa pikkuasioiden merkitystä lauseilla, jotka kytkevät ne "laajempiin trendeihin".

**Ennen:**
> Esimerkkipankin markkinointiosasto perustettiin 1989, mikä oli ratkaiseva hetki paikallisen pankkiviestinnän kehityksessä ja edisti laajempaa muutosta kohti asiakaslähtöistä toimintaa.

**Jälkeen:**
> Esimerkkipankin markkinointiosasto perustettiin 1989 vastaamaan kasvavaan kuluttajamainonnan tarpeeseen.

---

### 2. Mediatuntemus-name-droppaus

**Vältä:** "lehdistö on huomioinut", "asiantuntijat ovat tunnistaneet", "useissa kansallisissa medioissa", "laaja tunnettuus alalla", "aktiivinen näkyvyys sosiaalisessa mediassa"

**Ongelma:** Hakkaa lukijaa päähän maineella ilman sisältöä.

**Ennen:**
> Hänen näkemyksiään on siteerattu Hesarissa, Ylellä, Talouselämässä ja Kauppalehdessä. Hän on aktiivinen Twitterissä yli 50 000 seuraajan kanssa.

**Jälkeen:**
> Hesarin 2024 haastattelussa hän esitti, että pankkien sääntelyn pitäisi keskittyä asiakkaan suojaan teknisten yksityiskohtien sijaan.

---

### 3. "-en"- ja "-ssa"-loppuiset varjoanalyysit

**Vältä:** "korostaen X:n merkitystä", "edistäen Y:n leviämistä", "varmistaen, että...", "heijastaen Z:aa", "kuvastaen W:tä", "ilmentäen V:tä", "tuoden esiin..."

**Ongelma:** AI liittää partisiippilauseita lauseiden perään luodakseen valenäkemyksiä.

**Ennen:**
> Kampanja toteutettiin huolellisesti, korostaen brändin sitoutumista paikallisuuteen ja heijastaen vahvaa yhteyttä asiakaskuntaan, edistäen pitkäaikaista luottamusta.

**Jälkeen:**
> Kampanjassa nostettiin paikallisuus etusijalle. Brändi-ilme rakennettiin alueellisesta kuvastosta.

---

### 4. Mainosmainen kieli

**Vältä:** "ainutlaatuinen", "huipputasoinen", "tinkimätön laatu", "luksusta", "elämystä", "sielukas", "viehättävä", "hurmaava", "kosketuksiin", "lumoava", "henkeäsalpaava", "uskomaton", "vertaansa vailla", "harvinaislaatuinen", "korkeatasoinen"

**Ongelma:** AI ei pidä neutraalia rekisteriä, etenkään kun aihe on "lifestyle" tai "kulttuuri".

**Ennen:**
> Hurmaavan kaupungin sydämessä Esimerkki Kiinteistöt tarjoaa ainutlaatuisen ja elämyksellisen välityskokemuksen, joka yhdistää tinkimättömän laadun paikalliseen tuntemukseen.

**Jälkeen:**
> Esimerkki Kiinteistöjen välittäjät tuntevat alueen ja sen hintatason.

---

### 5. Ympäripyöreät viittaukset ja painokkuussanat

**Vältä:** "asiantuntijoiden mukaan", "tutkimukset osoittavat", "useat lähteet vahvistavat", "alalla on havaittu", "monet ovat huomanneet", "joidenkin mukaan", "yleisesti tunnettu"

**Ongelma:** AI heittää mielipiteitä epämääräisille auktoriteeteille ilman lähteitä.

**Ennen:**
> Asiantuntijoiden mukaan paikallinen pankki vahvistaa luottamusta yhteisössä. Tutkimukset osoittavat, että asiakkaat arvostavat henkilökohtaista palvelua.

**Jälkeen:**
> Esimerkkipankin 2024 asiakaskyselyssä 78 % vastanneista nosti henkilökohtaisen kontaktin tärkeimmäksi pankin valintakriteeriksi.

---

### 6. Kaavamaiset "haasteet ja tulevaisuus" -osiot

**Vältä:** "haasteista huolimatta", "monenlaisia haasteita kohdaten", "tulevaisuus on valoisa", "edessä on jännittäviä aikoja", "kestävän kehityksen polulla", "jatkaen vahvaa kasvua"

**Ennen:**
> Markkinointiviestinnän haasteista huolimatta — kuten muuttuvat alustat, kanavaviidakko ja kuluttajien tavoitettavuus — Esimerkkipankki jatkaa vahvalla, asiakaskeskeisellä polullaan kohti yhä kirkkaampaa tulevaisuutta.

**Jälkeen:**
> Pirstaloitunut mediakenttä on hankaloittanut kohderyhmien tavoittamista. Vuonna 2025 budjettia siirrettiin printistä Meta-mainontaan, ja konversio parani 23 %.

---

## KIELI- JA KIELIOPPIKUVIOT

### 7. Suomenkielinen AI-sanasto — vältettävät sanat

**Ylikäytetyt AI-sanat suomeksi:**
- **edistää** (kun tarkoittaa vain "auttaa")
- **kannustaa, innostaa, valtuuttaa** (käännöslainat: encourage, inspire, empower)
- **tuoda lisäarvoa, mahdollistaa, vapauttaa**
- **kokonaisvaltainen, saumaton, vaivaton, intuitiivinen, skaalautuva, monipuolinen, räätälöity**
- **uraauurtava, mullistava, ennennäkemätön, ratkaiseva, keskeinen**
- **moninainen, rikas (kuvallisesti), elävä, syvällinen**
- **korostaa, painottaa, ilmentää, heijastaa, kuvastaa, edustaa**
- **sukeltaa (syvemmälle), pureutua, ottaa askeleita kohti**
- **adressoida, implementoida, operoida, optimoida (kuvallisesti)**

**Ennen:**
> Lisäksi Esimerkkipankki edistää saumattoman ja intuitiivisen asiakaskokemuksen toteutumista pankkitoiminnassa, mikä mahdollistaa monipuolisen ja räätälöidyn palvelun.

**Jälkeen:**
> Esimerkkipankin digikanavat on rakennettu niin, että tilin avaaminen, lainan haku ja vakuutuksen hankinta sujuvat saman tunnuksen alta.

---

### 8. "On"-verbin välttäminen (kopulan välttäminen)

**Vältä:** "toimii X:nä", "edustaa X:ää", "näyttäytyy X:nä", "ilmenee X:nä", "muodostaa X:n", "kuvastaa X:ää"

**Ongelma:** AI vaihtaa yksinkertaisen "on"-verbin koristelluksi rakenteeksi.

**Ennen:**
> Esimerkkipankki toimii suurimpana pankkina alueella. Kiinteistönvälitys Esimerkki Kiinteistöt edustaa pankin tytäryhtiötä, joka muodostaa olennaisen osan kokonaispalvelua.

**Jälkeen:**
> Esimerkkipankki on alueen suurin pankki. Sen tytäryhtiö on kiinteistönvälitys Esimerkki Kiinteistöt.

---

### 9. Negaation parallelismit ja "ei vain — vaan myös"

**Ongelma:** "Ei pelkästään X, vaan myös Y" -rakenne ja sen variantit ovat AI:n tavaramerkki.

**Vältä:**
- "Ei pelkästään X, vaan myös Y"
- "Ei vain X — se on Y"
- "Ei X — vaan Y"
- "Ei pelkkä Z, vaan W" -muoto kun tarkoitus on vain sanoa W

**Ennen:**
> Markkinointi ei ole vain mainontaa — se on asiakaskokemuksen rakentamista. Ei pelkästään näkyvyyttä, vaan myös merkityksellisyyttä.

**Jälkeen:**
> Markkinointi on osa asiakaskokemusta, ei pelkkää mainontaa.

---

### 10. Kolmiosa-listausten ylikäyttö

**Ongelma:** AI pakottaa ajatukset kolmen ryhmiin näyttääkseen kattavalta.

**Ennen:**
> Tapahtuma tarjoaa luovuutta, inspiraatiota ja oivalluksia. Osallistujat saavat sparrausta, työkaluja ja verkostoja.

**Jälkeen:**
> Tapahtumassa on puheenvuoroja ja työpajoja. Iltaa varten on varattu aikaa vapaalle keskustelulle.

---

### 11. Synonyymien pyörittely (elegant variation)

**Ongelma:** AI vaihtaa samaa tarkoittavia sanoja toistamisen pelossa.

**Ennen:**
> Markkinoija kohtaa monia haasteita. Asiantuntija joutuu ratkomaan ongelmia. Tekijä saa kamppailla esteiden kanssa. Ammattilainen voittaa lopulta.

**Jälkeen:**
> Markkinoija kohtaa työssään monia haasteita mutta selviää niistä.

---

### 12. Väärät asteikot ("X:stä Y:hyn")

**Ongelma:** AI käyttää "alkaen X:stä päättyen Y:hyn" -rakenteita, joissa X ja Y eivät ole samalla mitta-asteikolla.

**Ennen:**
> Markkinoinnin matka on vienyt meidät printtimainoksista TikTok-videoihin, brändilupauksista kohtaamisiin, datasta tunteisiin.

**Jälkeen:**
> Markkinoinnissa hyödynnetään printtiä, somea ja kasvotusten tapahtumia.

---

### 13. Liiallinen passiivi ja subjektittomat lauseet

**Ongelma:** AI piilottaa tekijän passiiveen. Suomen kielessä tämä on erityisen yleinen ja paljastava AI-merkki, koska suomen passiivi on luonnostaan yleistävä.

**Vältä ylikäyttöä:**
- "voidaan todeta, että..."
- "on havaittavissa..."
- "nähdään, että..."
- "todetaan..."
- "huomioidaan..."
- "varmistetaan..."

**Ennen:**
> Markkinoinnin tuloksellisuus voidaan todeta liidien ja konversion kautta. On havaittavissa, että kampanjat ovat tuottaneet odotettua paremmin.

**Jälkeen:**
> Mittaan markkinointia liidien ja konversion kautta. Q1:n kampanjat tuottivat 18 % yli tavoitteen.

---

## TYYLIKUVIOT

### 14. Ajatusviivan ylikäyttö

**Ongelma:** AI käyttää ajatusviivaa (–) "napakkuuteen", erityisesti myyntipuhe-tyylissä. Useimmat voi korvata pilkulla, pisteellä tai sulkeilla.

Huom: tekstissä saa olla ajatusviivoja — mutta ei joka virkkeessä.

**Ennen:**
> Esimerkkiyritys on yhteisöllinen — ei vain firma — jonka asiakkaat tuntevat — ja siksi siinä yhdistyy paikallisuus ja vakaus — kaikki saman katon alta.

**Jälkeen:**
> Esimerkkiyritys on alueensa suurin toimija. Paikallisuus ja luotettavuus syntyvät vuosien historiasta ja tutuista kasvoista.

---

### 15. Liiallinen lihavointi

**Ongelma:** AI lihavoittaa avainsanat mekaanisesti.

**Ennen:**
> Markkinointiasiantuntija vastaa **printtiaineistoista**, **some-mainonnasta** ja **verkkosivujen ylläpidosta**. Hänen työnsä on **monikanavaista** ja **tuloskeskeistä**.

**Jälkeen:**
> Markkinointiasiantuntija vastaa printtiaineistoista, some-mainonnasta ja verkkosivujen ylläpidosta. Työ on monikanavaista ja tuloskeskeistä.

---

### 16. Otsikollinen luetelma ("**Otsake:** kuvaus")

**Ongelma:** AI muodostaa luetteloita, joissa jokainen rivi alkaa lihavoidulla otsakkeella ja kaksoispisteellä.

**Ennen:**
> - **Käyttökokemus:** Käyttökokemus on parantunut uudella ulkoasulla.
> - **Suorituskyky:** Suorituskyky on parantunut optimoiduilla algoritmeilla.
> - **Tietoturva:** Tietoturvaa on vahvistettu salauksen avulla.

**Jälkeen:**
> Päivitys uudistaa käyttöliittymän, nopeuttaa latausaikoja ja lisää päästä päähän -salauksen.

---

### 17. Otsikoiden Iso Alkukirjain Sanoissa

**Ongelma:** Englannin malliin AI lihavoi otsikkoja Title Casella. Suomessa vain virkkeen ensimmäinen sana on isolla (paitsi erisnimet).

**Ennen:**
> ## Strategiset Kumppanuudet Ja Globaali Toiminta

**Jälkeen:**
> ## Strategiset kumppanuudet ja globaali toiminta

---

### 18. Emojit otsikoissa ja luetteloissa

**Ongelma:** AI koristelee tekstiä emojeilla.

**Ennen:**
> 🚀 **Lanseeraus:** Tuote julkaistaan Q3
> 💡 **Keskeinen oivallus:** Käyttäjät arvostavat yksinkertaisuutta
> ✅ **Seuraavat askeleet:** Sovi tapaaminen

**Jälkeen:**
> Tuote julkaistaan Q3:n aikana. Käyttäjätestin perusteella selkeys on tärkeämpi kuin ominaisuusmäärä. Sovin seuraavan tapaamisen ensi viikolle.

---

### 19. Lainausmerkkimallien sekoittaminen

**Ongelma:** AI-teksti sekoittaa eri lainausmerkkimalleja samassa tekstissä: suoria "tikkumerkkejä", suomalaisia kaarevia ”kokolainausmerkkejä” ja englannin erimuotoisia alku- ja loppulainausmerkkejä.

Suomessa ensisijainen on kaareva ”näin” (sama merkki U+201D alussa ja lopussa), mutta suorat "näin" ovat hyväksyttäviä digitaalisissa teksteissä. Valitse yksi malli ja pidä se yhtenäisenä koko tekstissä.

---

## VIESTINTÄKUVIOT

### 20. Chatbot-jäänteet

**Vältä:** "Toivottavasti tästä on apua!", "Mainio kysymys!", "Tietysti!", "Toki!", "Otatko minuun yhteyttä, jos...", "Tässä on yhteenveto...", "Olen täällä auttamassa..."

**Ennen:**
> Mainio kysymys! Tässä on tiivistelmä Esimerkkipankin historiasta. Toivottavasti tästä on apua, ja kerro toki, jos haluat tarkennusta johonkin osioon!

**Jälkeen:**
> Esimerkkipankin historia alkoi 1902, kun ensimmäinen osuuskassa perustettiin alueen maaseudulle.

---

### 21. Tietokatkokset ja varaukset

**Vältä:** "käytettävissä olevien tietojen perusteella", "tietoni eivät ulotu", "viimeisimmän tiedon mukaan", "yksityiskohdat ovat rajalliset"

**Ennen:**
> Käytettävissä olevien tietojen perusteella Esimerkkipankki lienee perustettu 1990-luvun lopulla, vaikka yksityiskohdat ovat rajalliset.

**Jälkeen:**
> Esimerkkiyritys aloitti toimintansa nykyisessä muodossaan 2017.

---

### 22. Liika kohteliaisuus / palvelevaisuus

**Vältä:** "Olet täysin oikeassa!", "Mielenkiintoinen huomio!", "Erinomainen ajatus!"

**Ennen:**
> Mainio pointti! Olet aivan oikeassa, että pankkimarkkinointi on muuttunut. Erinomainen havainto digitalisaation roolista.

**Jälkeen:**
> Mainitsemasi digitalisaation murros on muuttanut pankkimarkkinointia mittausvetoiseksi.

---

## TÄYTE JA EPÄRÖINTI

### 23. Täytefraasit suomeksi

| Ennen | Jälkeen |
|---|---|
| "kyetäkseen saavuttamaan tavoitteen" | "tavoitteen saavuttamiseksi" |
| "johtuen siitä, että satoi" | "koska satoi" |
| "tällä hetkellä" | "nyt" |
| "siltä varalta, että tarvitset apua" | "jos tarvitset apua" |
| "järjestelmällä on kyky käsitellä" | "järjestelmä käsittelee" |
| "on tärkeää huomata, että luvut osoittavat" | "luvut osoittavat" |
| "siinä mielessä, että" | (poista, tai "koska", "siten että") |
| "tämän myötä" | "näin", "siksi" |
| "ottaen huomioon sen, että" | "koska" |

---

### 24. Liika epäröinti

**Ennen:**
> Voitaneen olettaa, että kampanjalla saattaisi mahdollisesti olla jonkinlainen vaikutus tuloksiin.

**Jälkeen:**
> Kampanja voi nostaa konversiota.

---

### 25. Geneeriset positiiviset lopetukset

**Vältä:** "tulevaisuus näyttää valoisalta", "edessä on jännittäviä aikoja", "matka jatkuu kohti huippua", "yhdessä eteenpäin", "kasvu jatkuu kestävällä polulla"

**Ennen:**
> Tulevaisuus näyttää Esimerkkipankille valoisalta. Yhdessä asiakkaiden kanssa kuljemme kohti yhä parempaa pankkitoimintaa.

**Jälkeen:**
> Esimerkkipankin tavoite vuodelle 2027 on kasvattaa pk-yritysasiakkaiden osuus 18 prosenttiin.

---

### 26. Anglismit ja käännöslainat — suomenkielinen erityishuomio

Tämä on suomen erityispiirre. AI-suomi on usein piilo-englantia.

**Vältä:**

| Anglismi | Suomeksi |
|---|---|
| "tehdä päätös" (make a decision) | "päättää" |
| "olla sitä mieltä, että" (be of the opinion that) | "uskoa, että" / "mielestäni" |
| "ottaa askeleita kohti" (take steps toward) | "edetä", "pyrkiä" |
| "implementoida" | "toteuttaa", "ottaa käyttöön" |
| "adressoida ongelma" | "käsitellä ongelma", "puuttua ongelmaan" |
| "ratkaista haaste" | "ratkaista ongelma" (haaste-sana on AI-tunnusmerkki) |
| "monesta eri näkökulmasta" | "monelta kannalta" |
| "tämä on tärkeä askel eteenpäin" | (poista — sano mitä konkreettisesti tapahtui) |
| "nykypäivän nopeatempoisessa maailmassa" | (poista — siirry suoraan asiaan) |
| "sukella syvemmälle aiheeseen" | "tutustu aiheeseen tarkemmin", "syvenny aiheeseen" |
| "ottaa kantaa asiaan" (silti OK, mutta tarkista käyttö) | "sanoa", "perustella", "kommentoida" |
| "tuoda esiin" (kun tarkoittaa vain "kertoa") | "kertoa", "esittää" |
| "korostaa merkitystä" | "kertoa, miksi tämä on tärkeää" / poista koko merkitys-puhe |
| "kannustaa", "innostaa", "valtuuttaa" (kun käännöslainoja sanoista encourage, inspire, empower) | konkreettinen verbi: "tukea", "auttaa", "antaa mahdollisuus" |

---

### 27. Mahtailuretoriikan troopit

**Vältä:** "pohjimmiltaan...", "todellisuudessa...", "syvällä tasolla...", "ytimessä on...", "todellinen kysymys on...", "merkityksellistä on..."

**Ongelma:** AI käyttää näitä esittääkseen, että pääsee asioiden ytimeen — mutta seuraava lause toistaa tavallisen asian juhlavasti.

**Ennen:**
> Pohjimmiltaan, todellinen kysymys on se, kykenevätkö tiimit sopeutumaan. Ytimessä on organisaation valmius muutokseen.

**Jälkeen:**
> Tiimien sopeutumiskyky ratkaisee. Se riippuu siitä, halutaanko organisaatiossa oikeasti muuttaa toimintatapoja.

---

### 28. Aloituksen kuuluttaminen

**Vältä:** "Sukelletaanpa aiheeseen", "Katsotaanpa tarkemmin", "Käydäänpä läpi", "Aloitetaan", "Tässä on, mitä sinun tulee tietää", "Tarkastellaan asiaa lähemmin"

**Ongelma:** AI ilmoittaa, mitä se aikoo tehdä, sen sijaan että tekisi sen.

**Ennen:**
> Sukelletaanpa Esimerkkipankin markkinoinnin maailmaan. Tässä on, mitä sinun tulee tietää sen brändityöstä.

**Jälkeen:**
> Esimerkkipankin brändityö perustuu kolmeen arvoon: ihmisläheisyys, vastuullisuus ja yhdessä menestyminen.

---

### 29. Pirstaleiset otsikot

**Ongelma:** Otsikko, jota seuraa yksi rivi, joka vain toistaa otsikon, ennen kuin oikea sisältö alkaa.

**Ennen:**
> ## Suorituskyky
>
> Nopeus merkitsee.
>
> Kun käyttäjä kohtaa hitaan sivun, hän poistuu.

**Jälkeen:**
> ## Suorituskyky
>
> Kun käyttäjä kohtaa hitaan sivun, hän poistuu.

---

### 30. Sanajärjestys — suomen teema-reema vs. englannin SVO

Tämä on yksi suurimmista AI-Suomen ongelmista ja ansaitsee oman tarkemman tarkastelunsa. Suomen sanajärjestys ei ole vapaa, mutta se on **paljon joustavampi kuin englannin** ja toimii erilaisten periaatteiden mukaan.

#### 30.1 Teema ja reema — suomen kielen sanajärjestyksen ydin

Suomalainen virke jakaantuu kahteen osaan:

- **Teema** — se mitä virke käsittelee, lukijalle jo tuttu tai oletettu tieto. Tulee tyypillisesti **virkkeen alkuun**.
- **Reema** — virkkeen uusi ja painotettu tieto. Tulee tyypillisesti **virkkeen loppuun**.

AI:n perusvirhe: noudattaa englannin SVO:ta (Subjekti-Verbi-Objekti) mekaanisesti, vaikka suomeksi luonnollisempi järjestys riippuu siitä, mikä on teemaa ja mikä reemaa.

**Esimerkki tämän periaatteen toiminnasta:**

Vastaa kysymykseen "Missä Anna on?":
> ✅ Anna on Helsingissä. (Anna = teema, Helsingissä = uutta tietoa = reema)

Vastaa kysymykseen "Kuka on Helsingissä?":
> ✅ Helsingissä on Anna. (Helsingissä = teema/konteksti, Anna = uutta tietoa = reema)

Sama tieto, eri sanajärjestys riippuen siitä mitä lukija kysyy. **AI antaa miltei aina ensimmäisen muodon** vaikka konteksti vaatisi toisen.

#### 30.2 Yleisimmät SVO-jäykkyydestä johtuvat ongelmat

**Ongelma A: Toiminta-objekti väärin painotettu**

**Ennen (jäykkä SVO):**
> Yritys julkaisee uuden palvelun loppukuussa.

**Jälkeen (jos "loppukuussa" on uutta tietoa):**
> Loppukuussa yritys julkaisee uuden palvelun.
> tai
> Uusi palvelu julkaistaan loppukuussa.

**Ongelma B: Aikamääre alussa kun se kuuluu loppuun**

**Ennen (kun "vuonna 2024" on uutta tietoa):**
> Vuonna 2024 yritys laajensi toimintaansa Espanjaan.

**Jälkeen (kun "Espanjaan" on pääpaino):**
> Yritys laajensi toimintaansa Espanjaan vuonna 2024.

**Ongelma C: Pitkä subjekti virkkeen alussa**

Suomessa pitkät, raskaat osat siirretään mielellään virkkeen loppuun ("end-weight principle"):

**Ennen (jäykkä SVO):**
> Suomen suurin yksityinen vakuutusyhtiö, joka aloitti toimintansa 1990-luvulla, julkaisi uudet tuotteet.

**Jälkeen (raskas osa loppuun):**
> Uudet tuotteet julkaisi Suomen suurin yksityinen vakuutusyhtiö, joka aloitti toimintansa 1990-luvulla.
> tai jaa:
> Suomen suurin yksityinen vakuutusyhtiö julkaisi uudet tuotteet. Yhtiö aloitti toimintansa 1990-luvulla.

#### 30.3 Painotus ja korostus sanajärjestyksellä

Suomessa lauseen alkuun voi nostaa minkä tahansa elementin sen korostamiseksi:

| Painotus | Sanajärjestys |
|---|---|
| Neutraali | "Asiakas hyväksyi tarjouksen eilen." |
| Korostetaan ajankohtaa | "Eilen asiakas hyväksyi tarjouksen." |
| Korostetaan kohdetta | "Tarjouksen asiakas hyväksyi eilen." (markkinoiva painotus harvinainen) |
| Korostetaan henkilöä | "Asiakas hyväksyi tarjouksen eilen." (tähän sopii intonaation kanssa) |

AI ei käytä tätä painotustapaa, vaan kirjoittaa kaiken neutraalissa SVO-järjestyksessä. Tulos: teksti ei reagoi kontekstiin.

#### 30.4 Käännöksen tunnistus — testit

Kun epäilet käännöksenmakuista virkettä, kysy:

1. **Olisinko sanonut tämän näin spontaanisti?** Jos virke kuulostaa siltä että sitä on käännetty, se on ollut.
2. **Onko aikamääre tai paikanmääre väärässä päässä?** Englannissa ne ovat usein lopussa ("...last week"). Suomessa ne ovat useammin alussa.
3. **Onko pitkä raskas osa alussa?** Suomessa raskaat osat painottuvat loppuun.
4. **Onko subjekti–verbi–objekti -mekaanisuudella jokin syy?** Jos ei, harkitse uudelleenjärjestelyä.

#### 30.5 Korjauksen tarkistuslista

```
[ ] Onko teema ennen reemaa?
[ ] Onko uusi tieto virkkeen lopussa?
[ ] Onko raskas osa virkkeen lopussa, ei alussa?
[ ] Onko aikamääre tai paikanmääre oikeassa kohdassa (yleensä alussa kontekstina)?
[ ] Sopisiko korostus paremmin nostamalla jokin elementti alkuun?
[ ] Onko virke väärin painotettu kontekstiinsa nähden?
```

---

### 31. Suomalainen humble brag — myynti- ja viestintäkulttuurin sävy

Suuri osa yleiskäyttöisten kielimallien koulutusaineistosta on englanninkielistä, suurelta osin amerikkalaista. Amerikkalainen myynti- ja viestintäkulttuuri palkitsee **yliampuvaa** kuvausta: "best in class", "industry-leading", "revolutionary". Suomalainen kulttuuri palkitsee **aliarvioivaa raportointia** — humble brag, kun anglosaksinen kollega olisi liioitellut.

AI kääntää amerikkalaisen sävyn suoraan suomeksi, mikä tuottaa kulttuurisesti väärän tuntuisen tekstin.

#### 31.1 Tyypillinen yliampuva amerikkalainen sävy ja sen suomalaistaminen

**Ennen (yliampuva, käännetty amerikkalaisesta):**
> Olemme alan ehdoton ykkönen ja toimitamme asiakkaillemme aina vertaansa vailla olevaa laatua. Tiimimme on intohimoinen ja sitoutunut tuottamaan poikkeuksellisia tuloksia.

**Jälkeen (suomalainen):**
> Olemme toimineet alalla 15 vuotta. Asiakkaamme palaavat — viidennellä kertaa olemme yli puolella heistä. Tiimissämme on 12 henkilöä, jokainen yli viiden vuoden kokemuksella alalta.

Numerot tekevät väittämästä konkreettisen. Yliampuvat adjektiivit eivät kuulu suomalaiseen ammattikieleen.

#### 31.2 Suomalaisen humble bragin rakenne

**Vaihe 1: Kerro vaatimaton fakta.**

> "Asiakas pyysi raporttia perjantaina. Se valmistui keskiviikkona."

**Vaihe 2: Anna lukijan päätellä merkitys.**

(Ei tarvitse selittää: "tämä oli erityisen nopea aikataulu". Lukija näkee numerot ja päättelee.)

**Vaihe 3: Lisää konteksti jos tarvitaan.**

> "Vertailussa: muiden tarjoajien aikataulu olisi ollut kaksi viikkoa."

**Vaihe 4: ÄLÄ kerro lukijalle miten tämän pitäisi reagoida.**

(Vältä: "Tämä osoittaa sitoutumistamme asiakkaaseen". Lukija päättelee itse.)

#### 31.3 Yliampuvat sanat, joita amerikkalaisesta vetää suomalaiseen — vältä

| Yliampuva (käännöslaina) | Suomalainen vaihtoehto |
|---|---|
| "ainutlaatuinen" | konkreettinen kuvaus mikä on erilaista |
| "vertaansa vailla" | numero tai vertailu konkreettisesti |
| "huipputasoinen" | mittari, joka todistaa tason |
| "intohimoinen tiimi" | "tiimi jolla on 5+ vuoden kokemus" |
| "sitoutunut asiakkaisiin" | esimerkki sitoutumisesta |
| "alan ehdoton ykkönen" | konkreettinen mittari (markkinaosuus, asiakasmäärä) |
| "poikkeuksellinen palvelu" | mitä konkreettisesti tarjotaan |
| "voittamaton kombo" | mitkä elementit, miksi |
| "räjähtävä kasvu" | luvut |
| "mullistava innovaatio" | mitä uutta, vertaa vanhaan |
| "luotettavin kumppani" | mittarit (NPS, asiakaspysyvyys, tms.) |

#### 31.4 Suomalainen humble brag ei ole nöyristelyä

Tärkeä erotus: humble brag ei tarkoita että aliarvioit työsi tai vähätelet osaamistasi. Se tarkoittaa että annat **numeroiden, faktojen ja konkretian** puhua puolestaan.

**Yliampuva (vältä):**
> Olen alan ehdoton huippuosaaja sosiaalisen median markkinoinnissa.

**Nöyristelevä (vältä myös):**
> Yritän vain parhaani sosiaalisen median puolella.

**Humble brag (käytä):**
> Olen rakentanut kuuden brändin some-läsnäolon viiden viime vuoden aikana. Suurimman asiakkaan tavoittavuus kasvoi kuusinkertaiseksi.

#### 31.5 Korjauksen testit

Virkkeittäin (etenkin markkinointi-, esittely- ja hakemustekstissä):

```
[ ] Onko adjektiivi konkreettisen sijasta abstrakti? ("ainutlaatuinen", "huipputasoinen") → vaihda numeroon tai esimerkkiin
[ ] Onko muoto "olemme X" ilman todistetta? → lisää todiste tai pudota väittämä
[ ] Kerronko lukijalle miten reagoida ("tämä osoittaa, kuinka...") sen sijaan että jättäisin sen lukijalle? → poista ohjeistus
[ ] Onko sävy yliampuva amerikkalainen vai vaatimaton suomalainen? → suomalainen palkitsee jälkimmäistä
[ ] Voiko lukija päätellä väittämän numeroista, eikä toisin päin? → kyllä = ok
```

---

### 32. Suomenkielisen tekstin muut erityispiirteet

#### Liialliset "että"-lauseet

**Ennen:**
> On tärkeää huomata, että Esimerkkipankki varmistaa, että asiakkaat ymmärtävät, että pankkipalvelut ovat muuttuneet siten, että digitaaliset kanavat ovat keskeisessä roolissa.

**Jälkeen:**
> Esimerkkipankki haluaa varmistaa, että asiakkaat osaavat käyttää digikanavia — pankkiasiointi tapahtuu yhä enemmän verkossa.

#### Latteat kielikuvat ja kliseet

Vältä:
- "aurinko paistaa kirkkaasti"
- "sydän pakahtuu"
- "matka jatkuu"
- "kaikki palaset loksahtavat paikoilleen"
- "punainen lanka"

---

## PROSESSI

1. **Lue teksti** huolellisesti
2. **Tunnista** kaikki yllä olevien kuvioiden esiintymät
3. **Kirjoita uudelleen** jokainen ongelmakohta
4. Varmista, että uusi versio:
   - kuulostaa luonnolliselta ääneen luettuna
   - vaihtelee virkerakennetta luonnollisesti
   - käyttää konkreettisia faktoja sumeiden väitteiden sijaan
   - säilyttää sopivan rekisterin kontekstiin nähden
   - käyttää "on"-verbiä ja muita yksinkertaisia rakenteita kun mahdollista
5. **Esitä luonnos**
6. **Itse-audit:** "Mikä alla olevassa on edelleen ilmiselvästi AI-tuotettua?"
7. Vastaa lyhyesti niihin merkkeihin, jotka jäivät
8. **"Tee siitä nyt vielä vähemmän AI-tuotetun makuinen."**
9. Esitä **lopullinen versio**
10. (Valinnainen) **lyhyt yhteenveto** tehdyistä muutoksista

---

## TULOSMUOTO

Anna:
1. **Luonnosversio** (humanisoitu)
2. **"Mikä tästä on edelleen ilmiselvästi AI?"** (lyhyt luettelo)
3. **Lopullinen versio** (auditin jälkeen)
4. (Valinnainen) **Lyhyt lista muutoksista**

---

## TÄYSIPITUINEN ESIMERKKI

**Ennen (AI-makuinen):**
> Mainio kysymys! Tässä on hakemukseni Esimerkki Oy:n markkinointiasiantuntijan tehtävään. Toivottavasti tämä auttaa!
>
> Nykypäivän nopeatempoisessa toimintaympäristössä markkinointiviestintä ei ole pelkästään mainontaa — se on ratkaiseva osa asiakaskokemuksen rakentamista, korostaen brändin sitoutumista ja heijastaen syvempää yhteyttä asiakkaisiin. Markkinoinnin kenttä on muuttunut printtilehdistä TikTok-videoihin, perinteisistä kohtaamisista digitaalisiin polkuihin, brändilupauksista mitattaviin tuloksiin.
>
> Pohjimmiltaan, todellinen kysymys on se, kuinka markkinoija pystyy yhdistämään luovuuden, tehokkuuden ja inspiraation saumattomaksi ja monipuoliseksi kokonaisuudeksi. Esimerkki Oy:n markkinointiasiantuntijan rooli edustaa ainutlaatuista mahdollisuutta vaikuttaa, sukeltaa syvemmälle markkinointiin ja edistää laajempaa muutosta kohti asiakaslähtöisyyttä.
>
> - 🚀 **Kokemus:** Olen toiminut markkinointiassistenttina.
> - 💡 **Osaaminen:** Hallitsen Adobe-paketin ja Meta-mainonnan.
> - ✅ **Tulokset:** Olen tuottanut tuloksia.
>
> Käytettävissä olevien tietojen perusteella Esimerkki Oy on merkittävä toimija. Haasteista huolimatta — kuten kanavien pirstaloituminen ja kuluttajan tavoitettavuus — tulevaisuus näyttää valoisalta. Yhdessä kuljemme kohti yhä parempaa markkinointia.

**Luonnosversio (humanisoitu):**
> Hain Esimerkki Oy:n markkinointiasiantuntijan paikkaa, koska teette juuri sitä asiakaskuntaa, jota olen oppinut palvelemaan kahden edellisen vuoden aikana. Käytännön työ on tuttua: tein keväällä asiakaskampanjan, jossa liidikonversio nousi 22 % ja paransin samalla raportoinnin selkeyttä. Numerot mainosalustoissa, ei diaesityksessä.
>
> Aiemmin tein hallinnollisia tehtäviä toimistossa ja opin siellä, että hyvä brief säästää viikon työtä. Sitä taitoa haluan tuoda Esimerkki Oy:lle. Tunnen Looker Studion, LinkedIn-mainosverkon perustyökalut ja kampanjarakentamisen kärsivällisyyden.
>
> Haluan tehdä työtä lähellä asiakkaita ja numeroita. Sopiiko keskustella tarkemmin?

**Mikä yllä olevassa on edelleen AI-makuista:**
- "Juuri sitä asiakaskuntaa" on lähellä klisettä
- "Numerot mainosalustoissa, ei diaesityksessä" — yritetty särmä mutta vähän temppua
- Kolmas kappale on lyhyt mutta kysymys ("Sopiiko keskustella tarkemmin?") on kliseinen

**Tee siitä vielä vähemmän AI:**
> Olen tehnyt kaksi vuotta digitaalista markkinointia toimistossa, viimeksi keväällä B2B SaaS -asiakkaalle LinkedIn Ads -kampanjassa. Liidikonversio nousi 22 % ja raportointi selkeytyi sen sivussa. Hain Esimerkki Oy:n paikkaa, koska asiakaskuntanne on hyvin lähellä sitä, mitä olen oppinut tekemään — pk-yritykset ja kasvuvaiheen B2B SaaS — ja työ menee briefistä julkaisuun pienellä tiimillä.
>
> Sitä ennen toimisto opetti, että hyvä brief säästää viikon. Sitä taitoa pyrin tuomaan mukaan. Looker Studio, LinkedIn Campaign Manager ja kampanjarakentaminen ovat työkalupakkini perusteita.

**Muutokset:**
- Poistettu chatbot-avaus, mainosmainen kielenkäyttö, mahtailuretoriikka
- Poistettu kolmiosa-listat ja "ei pelkästään X, vaan Y"
- Poistettu "-en"-loppuiset varjoanalyysit
- Poistettu geneerinen loppulause ja haasteet-osio
- Tuotu konkretiat etusijalle (kvartaali, 22 %, LinkedIn-kampanja)
- Vähennetty "edistää"-tyyppisiä AI-verbejä
- Vaihdettu rytmiä: lyhyitä ja pitempiä virkkeitä sekaisin
