# LOG RULARI — GPT-IMAGE-2 RESEARCH

---

## [2026-05-25] RULARE 2 — Delta incremental (3 zile de la rulare 1)

**Data rulare:** 2026-05-25 09:11 (TZ Europe/Bucharest)
**Surse cautate:** ultimele 30 zile (mai 2026) + 3 luni (feb-mai 2026)
**Goluri de la rularea 1 atacate:** G1 (lungime prompt), G2 (diacritice RO + font style), G3 (text-only consistency), G4 (candid framing), G5 (exemple Western)

### DELTA adaugat:

**SURSA NOUA DESCOPERITA:**
- github.com/magiccreator-ai/awesome-gpt-image-2-prompts — living collection curated din X, ~40+ creatori cu handles verificabile. Adaugat la tracked sources.
- ZeroLu/awesome-gpt-image: update detectat 2026-05-25 04:18 UTC (actualizat azi dimineata!)

**G1 — Lungime prompt (partial clarificat, NU rezolvat):**
- magiccreator-ai (multi-creator): @BubbleBrain foloseste 800+ cuvinte in practica reala pentru portrait/product complex cu rezultate bune
- Interpretare actualizata: contradictia e use-case-dependent (simplu=100-400, complex=800+), nu una sau alta. 850-1100 viabil pt complex dar NU "optim universal".
- Stare: ramane DE TESTAT local

**G2 — Diacritice (partial inchis):**
- ZeroLu (2026-05-25, multi-creator): diacritice FR/DE/ES confirmate
- magiccreator-ai (@phasE89, creator ceh): diacritice cehesti renderate corect in prompt real — cel mai apropiat de Eastern European confirmat pana acum
- Gap RO (comma-below ș/ț): PERSISTA — INCA NECONFIRMAT specific in testare publica
- G2 "in the spirit of": nicio confirmare noua, ramane DE TESTAT

**G3 — Text-only consistency (partial, single-source):**
- Anil-matcha: descriere textuala extrem de detaliata = "absolutely consistent in appearance and coloring" pt personaj/animal. Tehnica validata single-source. Ramane DE TESTAT pt produs fizic.

**G4 — Candid/amateur framing (UPGRADE MAJOR → BEST PRACTICE):**
- CONFIRMAT SOLID (2+ surse independente):
  1. magiccreator-ai multi-creator (@WolfRiccardo, @BubbleBrain, @mark_k, @phasE89): CCD compact camera, harsh direct flash, smartphone photo realism, "amatérská fotka"
  2. Anil-matcha multi-contributor: "CCD Camera Flash Candid", "candid snapshot feeling, slight motion blur", "faces look like real pedestrians"
- Tehnica specifica NOUA: "CCD compact camera + harsh on-camera direct flash" = snapshot autentic
- Formula adaugata in BEST PRACTICE G4
- First-person POV/bodycam: single-source, adaugat ca DE TESTAT separat

**G5 — Exemple Western/European (4 noi adaugate):**
- Amalfi Coast vintage travel poster (@WolfRiccardo, magiccreator-ai)
- Boston Spring 2026 poster (@BubbleBrain, magiccreator-ai)
- Yorkshire pub scene (@phasE89, magiccreator-ai)
- Irish countryside coastal portrait (creator neverificat, nivel incredere mai mic)

### Goluri ramase pentru urmatoarea rulare:
1. **G2 PRIORITAR (persistent):** Test local diacritice RO ș/ț comma-below — gap critic nerezolvat
2. **G1:** Test local 300 vs 600 vs 1000 cuvinte acelasi subject — contradictia nu e rezolvata complet
3. **G3:** A doua sursa pentru text-only product consistency (fara referinta); test local pt produs fizic
4. **G4:** Confirmare a doua sursa pentru first-person POV/bodycam
5. **G2:** Confirmare "in the spirit of [font clasic]" vs specificare directa — 2+ useri
6. **G5:** Cauta prompturi cu diacritice RO in exemple showcase (daca exista)

### Surse accesate in aceasta rulare:
- github.com/magiccreator-ai/awesome-gpt-image-2-prompts (raw README, nou) — 2026-05, activ
- github.com/ZeroLu/awesome-gpt-image (raw README, update detectat 2026-05-25) — activ
- github.com/Anil-matcha/Awesome-GPT-Image-2-API-Prompts (raw README) — 2026-04, activ
- Web search snippets: multiple (fragmentar, blocate 403: fal.ai, aivideobootcamp.com, james-palm.medium.com, picsart.com)

### Nivel incredere rulare 2:
- G4 "candid framing": SOLID (2 surse independente, multiple creator handles verificabile)
- G1 partial clarificare: single-source direction (magiccreator-ai)
- G2 diacritice Eastern EU: solid indirect (ceh confirmat); RO direct: nula
- G3 text-only: single-source, DE TESTAT

---

## [2026-05-22] RULARE 1 — Prima populare (prima rulare, toate goalurile erau goale)

**Data rulare:** 2026-05-22 (TZ Europe/Bucharest)
**Surse cautate:** ultimele 30 zile (mai 2026) + 3 luni (feb-mai 2026)
**Status goaluri inainte:** toate goale (prima rulare)

### DELTA adaugat:

**G1 — Structura prompt:**
- SOLID: structura Scene→Subject→Style→Lighting→Constraints→Negative confirmata (cookbook + ZeroLu + Anil-matcha)
- SOLID: etichete/line breaks bate bloc dens (3 surse independente)
- SOLID: limbaj concret > adjective vagi
- SOLID: negative prompt la final
- CONTESTAT: lungimea 850-1100 cuvinte din baseline v4 — community zice 100-400 optimal; cookbook nu da limita fixa; flagat ca DE TESTAT

**G2 — Text + diacritice RO:**
- SOLID: text exact in ghilimele (cookbook + multiple)
- SOLID: quality=medium/high pentru text mic (cookbook)
- SOLID: spell-out pentru cuvinte dificile (cookbook)
- GAP MAJOR: diacritice RO comma-below (ș/ț) — fara confirmare in testare publica; thread DALL-E identificat dar inaccesibil; workaround Unicode propus pentru test

**G3 — Locked product / img2img:**
- SOLID: etichetare rol imagini de referinta (multiple)
- SOLID: "change only X, keep everything else the same" (cookbook + multiple)
- SOLID: "preserve list" repeta fiecare iteratie (cookbook)
- SOLID: "product = locked layer, scene = editable layer" framing (multiple)
- SOLID: character sheet three-view (ZeroLu + Anil-matcha)

**G4 — Anti-AI fotorealism:**
- SOLID: film stock specific (Kodak Portra 400, Fujifilm Classic Chrome) confirmat (getimg.ai + ZeroLu multiple creators)
- SOLID: negative anti-AI explicit (ZeroLu multiple X handles)
- SOLID: imperfection language (ZeroLu + Anil-matcha)
- SOLID: equipment anchors (ZeroLu @WolfRiccardo + multiple)
- SOLID: era photography — 2003 camera, 90s point-and-shoot (ZeroLu + YouMind)

**G5 — Showcase design-uri:**
- 6 exemple verificate cu autori X reali din ZeroLu GitHub
- Handles: @WolfRiccardo, @patrickassale, @pangyusio, @BubbleBrain, @flowersslop, 卡尔的AI沃茨

### Goluri ramase pentru urmatoarea rulare:
1. **G2 PRIORITAR:** Test local diacritice RO (ș/ț/ă) — nu exista confirmare publica
2. **G1:** Clarificare contradictie lungime prompt — test 300 vs 600 vs 1000 cuvinte
3. **G3:** Consistenta text-only fara imagine de referinta (locked product no ref image)
4. **G4:** "candid mood / amateur framing" confirmare 2+ useri
5. **G5:** Exemple Western / European design (vs heavy CJK focus din sursele gasite)
6. **G2:** "in the spirit of [font clasic]" confirmare vs specificare directa

### Surse accesate:
- github.com/ZeroLu/awesome-gpt-image (raw README) — 2026-04, activ
- github.com/Anil-matcha/Awesome-GPT-Image-2-API-Prompts (raw README) — 2026-04, activ
- github.com/YouMind-OpenLab/awesome-gpt-image-2 (GitHub page) — 2026-04, activ
- github.com/openai/openai-cookbook (raw .ipynb) — 2026-04, oficial
- Multiple web search snippets (fragmentar, 2026-04/05)

### Nivel incredere general rulare 1:
- Tehnicile SOLID sunt bazate pe surse cu autori reali verificabili
- Tehnicile DE TESTAT sunt plausibile dar single-source sau neconfirmate pentru gpt-image-2 specific
- ~60% din pages incercate au returnat 403 — limita metodologica semnificativa
