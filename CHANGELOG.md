# Changelog

## 0.3.2 – 2026-06-23

Patch release. Two small additions to `suomi-ei-ai-sloppia` drawn from the same English-language AI-tell audits (the keyword-match ranking), adapted to Finnish. No new skills, pipelines or numbered patterns.

### Added

- **suomi-ei-ai-sloppia #32:** new subsection "Sidesanojen ja siirtymäfraasien ylikäyttö" – mechanically stacked connectives (`kuitenkin / näin ollen / lisäksi / edelleen / toisaalta`). This is the single most frequent keyword tell in English (`however / thus / moreover`, 6.3%) yet almost never cited – high prevalence, low salience – so it had no home in the bundle until now.
- **suomi-ei-ai-sloppia #7:** diction list extended with `valjastaa / hyödyntää / virtaviivaistaa / luotsata / navigoida` (leverage/harness, utilize, streamline, navigate) and `vivahteikas / monisyinen / kirjo / kudelma` (nuanced, tapestry) – fancy Finnish renderings of high-frequency English AI diction. Words already covered (comprehensive→kokonaisvaltainen, seamless→saumaton, profound→syvällinen, crucial→ratkaiseva) were left as-is.

### Credits unchanged

Attribution to [`akunikkola/suomi-finnish-skill`](https://github.com/akunikkola/suomi-finnish-skill), [`blader/humanizer`](https://github.com/blader/humanizer), Wikipedia:Signs of AI writing, [Kielitoimiston ohjepankki](https://kielitoimistonohjepankki.fi/) and [Selkokeskus](https://selkokeskus.fi/) preserved.

---

## 0.3.1 – 2026-06-23

Patch release. Adds a salience-ordered triage block to `suomi-ei-ai-sloppia`, informed by empirical English-language AI-tell audits (a human-cited ranking vs. a keyword-match ranking). No new skills, pipelines or rules – the 32 patterns are unchanged; this only foregrounds the highest-signal ones and the mechanical-vs-judgment split.

### Added

- **suomi-ei-ai-sloppia:** new top section "Korkeimman signaalin tunnusmerkit – tarkista nämä ensin" – a Finnish-weighted priority order (em dash, anglisms, over-hype/humble-brag, "ei vain X vaan Y", uniform sentence rhythm, sycophancy/chatbot residue) that foregrounds the em dash as the single most-cited tell (→ pattern #14). Includes the caveat that a keyword pass over-flags frequent-but-rarely-cited diction (bolded bullets, "in conclusion", connectives like "however/thus") and misses the structural tells humans actually cite (uniform rhythm, formulaic shape, triads) – those need human reading, not grep. The Finnish-specific top tells (anglisms, over-hype, SVO-rigidity) are weighted above the English ranking because they are invisible to English-language audits.

### Credits unchanged

Attribution to [`akunikkola/suomi-finnish-skill`](https://github.com/akunikkola/suomi-finnish-skill), [`blader/humanizer`](https://github.com/blader/humanizer), Wikipedia:Signs of AI writing, [Kielitoimiston ohjepankki](https://kielitoimistonohjepankki.fi/) and [Selkokeskus](https://selkokeskus.fi/) preserved.

---

## 0.3.0 – 2026-06-21

Adds field-tested verification discipline and a class of mechanical check the LLM pass cannot self-detect, drawn from production use of the bundle on a Finnish content site (pSEO, heavy YMYL). No new skills or pipelines.

### Added

- **suomi-kielihuolto:** new section "Näkymättömät ohjausmerkit" – soft hyphen (U+00AD), zero-width space (U+200B), directional marks (U+200E/U+200F) and word joiner (U+2060), with the explicit note that an LLM pass can't see them (they often vanish at tokenization), plus ripgrep and JavaScript sweeps. U+FEFF/BOM is excluded by design. Codepoints are documented as text rather than embedded as live characters, so the file passes its own sweep.
- **suomi-ymyl:** new section "Sitaatin verifiointi ≠ sitaatin lainaaminen" – independent, adversarial source verification for quotes, statute references and numbers; the "attribution leak" sister failure mode; two new checklist lines (one per checklist).
- **suomi-ei-ai-sloppia:** pattern #14 expanded – the em-dash character (U+2014) is itself a Finnish artifact (normalize to the en-dash U+2013), plus a mechanical "count, don't eyeball" density heuristic with an exception for dashes inside verbatim foreign-language source titles. Also adds a one-line pointer to the orchestrator's new series-level check.
- **suomi-tarkistuslista:** new "Sisältösarjan toistotarkistus" note – per-text passes structurally can't see a formula (closing paragraph, intro hook, justification phrase) reused across a content series; run a series-level comparison pass over the whole set.
- **README:** "Operationalizing the mechanical checks" appendix with an optional pre-commit grep example.

### Changed

- **Em-dash normalization (repo-wide):** all em-dashes (U+2014) across the 15 skills, the README and this changelog were normalized to the Finnish ajatusviiva, the en-dash (U+2013) – 484 occurrences in total. Deterministic, meaning-preserving glyph swap so the bundle passes its own new pattern #14 rule (the project invariant is that each skill passes its own checks).
- **suomi-ymyl:** the default attribution form shifted from "[taho] suosittelee X" to "[taho]:n mukaan X". "Suosittelee" is kept only where the source verifiably publishes that exact recommendation (for example a Käypä hoito -suositus). Rationale: a bare endorsement verb puts a recommendation in a named body's mouth and carries a verification and trademark risk; attributing a fact to a named source document is safer.

### Credits unchanged

Attribution to [`akunikkola/suomi-finnish-skill`](https://github.com/akunikkola/suomi-finnish-skill), [`blader/humanizer`](https://github.com/blader/humanizer), Wikipedia:Signs of AI writing, [Kielitoimiston ohjepankki](https://kielitoimistonohjepankki.fi/) and [Selkokeskus](https://selkokeskus.fi/) preserved.

---

## 0.2.1 – 2026-06-03

Patch release. Correctness and consistency fixes across all 15 skills and the README – no new skills or pipelines. The skills were run through their own rules (anglism, AI-slop, grammar, and factual checks) and the findings applied.

### Fixed

- **Authoritative sources (YMYL and meta-skills):** corrected outdated or wrong Finnish authorities – `Trafi` → `Traficom`, the defunct `Suomen Vakuutusyhtiöiden Keskusliitto` → `Finanssiala ry`, `Maistraatti` / `Ulkomaalaisvirasto` → `Digi- ja väestötietovirasto (DVV)` / `Maahanmuuttovirasto`, and Valtiokonttori's scope (added `Keva` for public-sector pensions; `Eläketurvakeskus` already listed for earnings-related).
- **Standard contract references (`suomi-tarjous`):** updated to current editions – `KSE 2013`, `IT2022`, `JIT 2015` – with a note to verify the latest version.
- **VAT:** general rate shown as `25,5 %`; reduced-rate examples aligned with rates current for 2026.
- **Localization (`suomi-lokalisaatio-perus`):** the service-number example now matches its stated pattern, and the byte abbreviation leads with `B`.
- **Grammar and mechanics:** missing commas before `että`, object-case agreement, compound spelling (`kohderekisteri`), and `ei käännetä` → `ei käänny`.
- **Organization spellings:** `YLE` / `KELA` → `Yle` / `Kela` (inflected directly, not as initialisms).

### Changed

- **Anglisms in the skills' own prose** replaced with Finnish equivalents (e.g. `em-dash` → `ajatusviiva`, `disclaimer` → `vastuuvapauslauseke`, `#produktiivisuus` → `#tuottavuus`).
- **Consistency:** `suomi-hakemuspaketti` frontmatter now lists all three mandatory chained skills; the README context list and pipeline count are aligned; `ALV` capitalization standardized in proposal templates.
- **Factual softening:** removed the claim that Google down-ranks AI content as such (reframed around quality/spam) and an unsourced training-data statistic.

### Credits unchanged

Attribution to [`akunikkola/suomi-finnish-skill`](https://github.com/akunikkola/suomi-finnish-skill), [`blader/humanizer`](https://github.com/blader/humanizer), and Wikipedia:Signs of AI writing preserved.

---

## 0.2.0 – 2026-05-27

Second release. Seven new skills covering Finnish business documents (email, application package, proposal, press release, newsletter), basic localization (dates, numbers, currency, addresses) and a decision matrix for sinuttelu/teitittely. The repo grows from 8 to 15 skills. The orchestrator (`suomi-tarkistuslista`) gains four new pipelines (G–J) and references two new meta-skills.

### New skills

**Primary skills (own context-specific pipeline step):**

- **suomi-sahkoposti** – Finnish email conventions: greeting hierarchy (`Hei [Etunimi]` / `Hyvä [Titteli]`), request forms (`Voitko` / `Voisitko` / `Voisitteko`), endings (`Ystävällisin terveisin` / `Terveisin`), signature block, out-of-office. Five categories (B2B, B2C, internal, authority, cold outreach) with example emails.
- **suomi-hakemuspaketti** – tailored Finnish CV + cover letter for a specific job posting, output as markdown (CV.md + Hakemuskirje.md) with Pandoc/Google Docs conversion instructions. Bullet convention: concrete action + measured outcome. Avoids "Olen erittäin kiinnostunut" -opening and similar AI tells.
- **suomi-tarjous** – Finnish commercial proposal: required elements (Y-tunnus, ALV split, payment terms, validity), B2B vs B2C pricing, standard contract reference (KSE 2013, IT2022), scope-in/scope-out separation. Does not provide legal advice – refers to Asianajajaliitto for contract clauses.
- **suomi-tiedote** – Finnish press release and internal announcement: inverted pyramid, 1–3-sentence ingressi, quote conventions (max 2 sentences, no "Olemme erittäin iloisia..."), boilerplate placement at end. Covers five sub-types (launch, financials, personnel, change, crisis).
- **suomi-uutiskirje** – Finnish email newsletter: subject line (35–50 chars), preheader (80–130 chars, complements not repeats), CTA conventions (`Lue lisää` not `Klikkaa tästä`), mandatory unsubscribe link, P.S. used selectively not mechanically.

**Meta-skills (consulted from other skills, no standalone pipeline):**

- **suomi-sinuttelu-teitittely** – decision matrix for Finnish formal/informal address. Modern Finnish defaults to sinuttelu; teitittely is the exception (authority letters, sensitive contexts, banking, formal representation, people over 70). Includes verb conjugation rules and corrects mixed-form errors like "Olette saanut sinun hakemuksesi".
- **suomi-lokalisaatio-perus** – reference library for Finnish formatting: dates (`27.5.2026`), times (`klo 14.30` with period), numbers (`12 500,50`), currency (`12,50 €` with space), ALV separation, addresses (postinumero before city), phone (`+358 40 123 4567`).

### New pipelines (in suomi-tarkistuslista)

- **Pipeline G – Email** (`suomi-sinuttelu-teitittely` → `suomi-sahkoposti` → cleanup chain)
- **Pipeline H – Press release / internal announcement** (`suomi-tiedote` → cleanup chain)
- **Pipeline I – Proposal** (`suomi-rekisteri` → `suomi-tarjous` → cleanup chain)
- **Pipeline J – Newsletter** (`suomi-rekisteri` → `suomi-uutiskirje` → cleanup chain)

### Changed

- **Pipeline F (application / CV)** now begins with `suomi-hakemuspaketti` for tailoring, then runs the standard cleanup chain.
- **Pipeline A (general text)** description updated – sähköposti moved out to its own Pipeline G; uutiskirje to Pipeline J.
- **suomi-tarkistuslista frontmatter** triggers expanded with new document types (sähköposti, tarjous, tiedote, uutiskirje).
- **Context detection (Vaihe 0)** in orchestrator extended with new text-type questions and auto-detection rules.

### Calibration note

The bundle's anglicism handling (in `suomi-anglismit` and the cleanup chain) was clarified during v0.2 development: domain jargon that has a precise technical meaning in marketing, sales, and AI fields is **kept**, not "translated away". Examples kept as canonical: `orgaaninen kasvu` (marketing), `brieffata` (advertising), `inbound` (B2B sales), `konversio` (digital marketing), `kuvageneraatio` (AI). These have specific meanings that translations like "maksuton jakelu", "ohjeistaa", or "saapuva yhteydenotto" lose.

### Credits unchanged

`suomi-kielihuolto` remains a derivative of [`akunikkola/suomi-finnish-skill`](https://github.com/akunikkola/suomi-finnish-skill). Attribution preserved.

---

## 0.1.0 – 2026-05-25

Initial release. Eight skills for Finnish text quality, plus an orchestrator that picks the right pipeline for the text you have.

### Included skills

**Orchestrator (recommended entry point):**

- **suomi-tarkistuslista** – meta-skill that detects context, picks the right pipeline of sub-skills (A–F), runs them in correct order, and consolidates findings into one report. Removes the need to remember which skill to invoke when.

**Universal text-quality skills:**

- **suomi-anglismit** – 7 patterns for catching translation loans from English
- **suomi-ei-ai-sloppia** – 32 patterns for humanizing AI-generated Finnish, including dedicated coverage of Finnish word order (teema-reema vs. SVO) and the Finnish humble brag calibration
- **suomi-kielihuolto** – Kielitoimiston-grade orthography, grammar, punctuation, expanded with case-system rules (partitive vs. accusative, locative cases), verb government (rektio), and foreign proper noun declension
- **suomi-rekisteri** – register calibration (formal / professional / customer-facing / colloquial) and consistency checking

**Context-specific skills:**

- **suomi-some-tyyli** – channel-specific Finnish social media style for LinkedIn, Instagram, TikTok, Facebook
- **suomi-ymyl** – YMYL (Your Money or Your Life) content rules in Finnish, journalistic framing with authoritative source links
- **suomi-selkokieli** – Finnish plain-language conversion following Selkokeskuksen guidelines

### Six pipelines covered by orchestrator

- **A – General text** (marketing, blog, email, internal comms)
- **B – Social media** (LinkedIn / Instagram / TikTok / Facebook)
- **C – YMYL** (health, finance, legal, safety, nutrition, animals, government)
- **D – Selkokieli** (plain-language conversion)
- **E – Legal / contract / terms of service**
- **F – Application / CV** (Finnish recruitment conventions)

### Credits

`suomi-kielihuolto` is a derivative work of [`akunikkola/suomi-finnish-skill`](https://github.com/akunikkola/suomi-finnish-skill) (MIT, © 2026 Aku Nikkola) – Kielitoimisto-grade kielihuolto patterns, oikoluku process, and many examples were originally written by Aku Nikkola. The AI-pattern section was expanded into `suomi-ei-ai-sloppia` and `suomi-anglismit` as separate skills. The case-system, verb-rektio, and foreign-name-declension sections were added in this bundle.

`suomi-ei-ai-sloppia` also incorporates patterns from [`blader/humanizer`](https://github.com/blader/humanizer) (MIT) and Wikipedia:Signs of AI writing.

Kielitoimiston ohjepankki is the canonical Finnish-language reference. Selkokeskus (Kehitysvammaliitto) is the authoritative source for Finnish plain-language standards.
