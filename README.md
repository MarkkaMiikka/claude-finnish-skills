# Claude Finnish Skills

Fifteen [Claude Code](https://claude.com/claude-code) skills for writing and reviewing Finnish that doesn't read like an AI wrote it. Covers the patterns AI gives itself away on (anglicisms, compound-word breakage, generic marketing formulas, register flattening) across marketing copy, blog posts, applications, social, YMYL, selkokieli, email, proposals, press releases, newsletters, and Finnish localization basics (dates, numbers, addresses, sinuttelu vs. teitittely).

AI-generated Finnish gives itself away in ways English editing tools don't catch. Loaned compounds like "Helsinki-pohjainen" or "X-stack" slip through. The "ei vain X, vaan myös Y" marketing formula reads as suspect by the second comma. Compound words get written apart, partitive and accusative get swapped, foreign proper nouns get declined inconsistently. And the same model that produced "social post" can't tell LinkedIn from TikTok – three different micro-registers collapse into one voice. These skills cover each layer separately, so you only run the checks you need.

## Quick start – just run the orchestrator

If you don't want to remember which skill to invoke when, just use the orchestrator:

```
"Aja täysi suomi-tarkistus" tai "/suomi-tarkistuslista"
```

The orchestrator (`suomi-tarkistuslista`) detects what kind of text you have, picks the right skills, runs them in the right order, and consolidates findings into one report.

## What's included

### Orchestrator (start here)

| Skill | What it does | Trigger phrases |
|---|---|---|
| **suomi-tarkistuslista** | Meta-skill – detects context (markkinointi / hakemus / some / YMYL / selkokieli / lakiteksti / email / tarjous / tiedote / uutiskirje), picks the right pipeline of the 10 available, runs the other skills in correct order, consolidates findings | "aja täysi suomi-tarkistus", "tarkista koko teksti", "suomi-check", "viimeistele suomenkielinen teksti" |

### Universal text-quality skills (used by most pipelines)

| Skill | What it catches | Trigger phrases |
|---|---|---|
| **suomi-anglismit** | Translation loans from English (Helsinki-pohjainen, sukella syvemmälle, X-stack) | "tarkista anglismit", "kuulostaa englannilta", "outo yhdyssana" |
| **suomi-ei-ai-sloppia** | 32 AI writing patterns adapted to Finnish – overstated significance, three-item lists, em-dash overuse, generic positive endings, rigid SVO word order, Finnish humble brag calibration | "humanisoi", "poista AI-fraasit", "kuulostaa AI:lta", "liian mahtipontinen" |
| **suomi-kielihuolto** | Compound words, comma rules, capitalization, abbreviations, dates, numbers, dashes, case endings (partitive vs. accusative), verb government (rektio), foreign proper noun declension | "tarkista yhdyssanat", "pilkutus", "kielihuolto", "oikoluku" |
| **suomi-rekisteri** | Register calibration – formal / professional / customer-facing / colloquial, and consistency within a text | "tarkista rekisteri", "liian virallinen", "liian rento", "rekisteri vaihtelee" |

### Context-specific text-quality skills (used when the situation matches)

| Skill | What it catches | Trigger phrases |
|---|---|---|
| **suomi-some-tyyli** | Channel-specific Finnish social media style – LinkedIn, Instagram, TikTok, Facebook are separate micro-registers, not one "generic social post" | "tee LinkedIn-postaus", "Instagram-caption", "TikTok-hook", "multi-channel some" |
| **suomi-ymyl** | YMYL content rules in Finnish – health, finance, legal, safety. Journalistic framing with authoritative source links, not personal advice | "tarkista YMYL", "terveyssisältö", "taloussisältö", "lainopillinen teksti" |
| **suomi-selkokieli** | Convert complex Finnish (bureaucratic, legal, technical) into plain language (selkokieli) following Selkokeskuksen guidelines | "tee selkokieliseksi", "yksinkertaista", "saavutettava versio" |

### Document templates (new in v0.2 – Finnish document conventions, not just text quality)

| Skill | What it does | Trigger phrases |
|---|---|---|
| **suomi-sahkoposti** | Finnish email conventions – greeting hierarchy, request forms, endings, signature, out-of-office; B2B, B2C, internal, authority and cold outreach categories | "kirjoita sähköposti", "muotoile työsähköposti", "vastaa asiakkaalle", "poissaoloviesti" |
| **suomi-hakemuspaketti** | Tailored Finnish CV + cover letter for a specific job posting; outputs markdown (CV.md + Hakemuskirje.md) with Pandoc/Google Docs conversion instructions | "räätälöi CV", "tee hakemus", "rakenna hakemuspaketti", "kirjoita hakemuskirje" |
| **suomi-tarjous** | Finnish commercial proposal – required elements (Y-tunnus, ALV split, payment terms, validity), scope-in/scope-out, KSE 2013 / IT2022 references. Does NOT give legal advice | "tee tarjous", "muotoile tarjouspohja", "konsultointitarjous", "ALV-erottelu" |
| **suomi-tiedote** | Finnish press release and internal announcement – inverted pyramid, ingressi, sitaatti conventions, lisätietolohko, taustaosa | "kirjoita lehdistötiedote", "tee tiedote", "PR-tiedote", "lanseeraustiedote" |
| **suomi-uutiskirje** | Finnish email newsletter – subject (35–50 chars), preheader, CTA conventions, mandatory unsubscribe link, P.S. used selectively | "tee uutiskirje", "kirjoita newsletter", "email-kampanja", "kuukausikirje" |

### Meta-skills (consulted from other skills – reference libraries, not standalone pipelines)

| Skill | What it does | Trigger phrases |
|---|---|---|
| **suomi-sinuttelu-teitittely** | Decision matrix for Finnish formal vs informal address. Modern Finnish defaults to sinuttelu; teitittely is for authority letters, sensitive contexts, banking, formal representation, 70+ year olds. Corrects mixed-form errors | "sinuttelu vai teitittely", "muotoile teitittelyllä", "kohtelias muoto" |
| **suomi-lokalisaatio-perus** | Finnish formatting reference: dates (`27.5.2026`), times (`klo 14.30`), numbers (`12 500,50`), currency (`12,50 €`), ALV separation, addresses, phone | "muotoile päivämäärä", "numeroformaatti", "ALV-merkintä", "Suomi-osoiteformaatti" |

## Install

These are project-local or user-scope Claude Code skills. Two install paths:

### Option A – drop into your project

```bash
git clone https://github.com/MarkkaMiikka/claude-finnish-skills.git
cp -r claude-finnish-skills/.claude/skills/* your-project/.claude/skills/
```

### Option B – user-scope (available across all projects)

```bash
# Linux/macOS
cp -r claude-finnish-skills/.claude/skills/* ~/.claude/skills/

# Windows PowerShell
Copy-Item -Recurse claude-finnish-skills\.claude\skills\* $env:USERPROFILE\.claude\skills\
```

Once installed, Claude Code surfaces the skills automatically when you mention any of the trigger phrases listed above. You can also invoke them directly:

- Orchestrator: `/suomi-tarkistuslista`
- Universal: `/suomi-anglismit`, `/suomi-ei-ai-sloppia`, `/suomi-kielihuolto`, `/suomi-rekisteri`
- Context-specific text quality: `/suomi-some-tyyli`, `/suomi-ymyl`, `/suomi-selkokieli`
- Document templates: `/suomi-sahkoposti`, `/suomi-hakemuspaketti`, `/suomi-tarjous`, `/suomi-tiedote`, `/suomi-uutiskirje`
- Meta-skills: `/suomi-sinuttelu-teitittely`, `/suomi-lokalisaatio-perus`

All fifteen skills are pure Markdown – no Python or external dependencies. The `suomi-hakemuspaketti` skill produces markdown files and gives Pandoc / Google Docs instructions for converting to .docx or PDF.

## How they relate

Two ways to use this bundle:

### Way 1 – orchestrated (recommended)

```
"Aja suomi-tarkistus" → suomi-tarkistuslista detects context, runs the right pipeline
```

The orchestrator picks one of ten pipelines based on what kind of text you have:

- **Pipeline A** (general text): rekisteri → ei-ai-sloppia → anglismit → kielihuolto
- **Pipeline B** (social media): some-tyyli → ei-ai-sloppia → anglismit → kielihuolto
- **Pipeline C** (YMYL): ymyl → rekisteri → ei-ai-sloppia → anglismit → kielihuolto
- **Pipeline D** (selkokieli): selkokieli → anglismit → kielihuolto
- **Pipeline E** (legal / contract): rekisteri → kielihuolto → anglismit
- **Pipeline F** (application / CV): hakemuspaketti → rekisteri → ei-ai-sloppia → anglismit → kielihuolto
- **Pipeline G** (email): sinuttelu-teitittely → sahkoposti → ei-ai-sloppia → anglismit → kielihuolto
- **Pipeline H** (press release / internal announcement): tiedote → ei-ai-sloppia → anglismit → kielihuolto
- **Pipeline I** (proposal): rekisteri → tarjous → ei-ai-sloppia → anglismit → kielihuolto
- **Pipeline J** (newsletter): rekisteri → uutiskirje → ei-ai-sloppia → anglismit → kielihuolto

The two meta-skills (`suomi-sinuttelu-teitittely` and `suomi-lokalisaatio-perus`) are consulted from within other pipelines where puhuttelumuoto or formatting matters – they don't have standalone pipelines.

### Way 2 – manual

Invoke individual skills when you know which check you need:

```
suomi-anglismit         ──┐
                          ├──> suomi-ei-ai-sloppia ──> suomi-kielihuolto
your draft text         ──┘                           (final mechanic check)
```

When writing fresh content: write the draft, then humanize (`suomi-ei-ai-sloppia`), then check anglicisms (`suomi-anglismit`), then run mechanics (`suomi-kielihuolto`).

## Example – before / after

An AI-generated job application opening, and what it looks like after the writer pulled out the AI tells and put in what they actually did. Note: this goes further than `suomi-ei-ai-sloppia` alone – the skill preserves the core message by design (see SKILL.md, "Säilytä merkitys"). The example pairs humanization with a deliberate reframe from abstract pitch to concrete experience, because that's the realistic move for a job application where the AI version says nothing about the candidate.

**Before (AI):**
> Nykypäivän nopeatempoisessa toimintaympäristössä markkinointiviestintä ei ole pelkästään mainontaa – se on ratkaiseva osa asiakaskokemuksen rakentamista, korostaen brändin sitoutumista ja heijastaen syvempää yhteyttä asiakkaisiin.

**After:**
> Olen tehnyt kaksi vuotta digitaalista markkinointia konsulttitalossa. Keväällä B2C-asiakkaan Meta-kampanjassa konversio nousi 22 % ja raportointi selkeytyi sen sivussa.

Concrete numbers, active voice, no "ei vain X, vaan myös Y", no "korostaen" or "heijastaen" partisiippilauseet, no "nykypäivän nopeatempoisessa" cliché. See `suomi-ei-ai-sloppia/SKILL.md` for the full 32-pattern catalogue with side-by-side fixes.

## Credits and upstream attribution

- **[akunikkola/suomi-finnish-skill](https://github.com/akunikkola/suomi-finnish-skill)** (MIT, © 2026 Aku Nikkola) – `suomi-kielihuolto` in this repo is a derivative work of this upstream skill. The Kielitoimisto-grade rules, example sentences, and the six-phase oikoluku process were originally written by Aku Nikkola. The AI-pattern coverage was expanded into the separate `suomi-ei-ai-sloppia` and `suomi-anglismit` skills in this bundle. Per MIT, upstream copyright is preserved in [LICENSE](LICENSE).
- **[blader/humanizer](https://github.com/blader/humanizer)** (MIT) – original English humanization patterns that informed the Finnish adaptation in `suomi-ei-ai-sloppia`.
- **Wikipedia:Signs of AI writing** – community-curated list of AI tells.
- **[Kielitoimiston ohjepankki](https://kielitoimistonohjepankki.fi/)** – the canonical Finnish-language style reference (Kotimaisten kielten keskus).
- **[Selkokeskus](https://selkokeskus.fi/)** (Kehitysvammaliitto) – guidelines for selkokieli, the Finnish plain-language standard referenced in `suomi-selkokieli`.
- **Kielitoimiston sanakirja, Iso suomen kielioppi, Kielikello** – additional public references.

## Maintenance

Maintained by Miikka Markkanen ([@MarkkaMiikka](https://github.com/MarkkaMiikka)). Issues and PRs welcome – especially:
- New AI-Finnish patterns you've seen in the wild
- Corrections to Kielitoimisto-grade rules
- New trigger phrases that should activate a skill
- Additional verb-rektio entries
- Channel-specific social media style updates as platforms evolve
- New pipeline patterns for the orchestrator (e.g. academic writing, technical documentation)

## License

MIT – see [LICENSE](LICENSE).
