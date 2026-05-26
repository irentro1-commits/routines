# LOG RULARI — GPT-IMAGE-2 RESEARCH

---

## [2026-05-26] RULARE 2 — Delta incremental (goluri din rularea 1)

**Data rulare:** 2026-05-26 09:02 TZ Europe/Bucharest
**Surse cautate:** 2026-05-22 → 2026-05-26 + goluri neacoperite din rularea 1
**Status goaluri inainte:** G1 (contradictie lungime, "intended use" necercetata), G2 (diacritice RO gap), G3 (text-only consistency gap), G4 (candid framing single-source), G5 (Western design, noi autori)

### DELTA adaugat:

**G1 — Structura prompt:**
- SOLID NOU: "Intended use" prefix la inceputul promptului (ex: "Product ad for Instagram carousel.") — cookbook oficial + fal.ai + MindStudio = 3 surse independente. Structura devine: [Intended Use] → [Scene] → [Subject] → [Style] → [Lighting] → [Constraints] → [Negative]
- CLARIFICARE CONTRADICTIE LUNGIME: Lungimea optima e relativa la task. Ultra-scurt (<50 cuvinte) = ok pt atmosfera simpla (@sunyunran, ZeroLu). 500+ cuvinte = ok pt infografice/poster complex (@MrLarus, ZeroLu). "GPT Image 2 parses each clause" (MindStudio) = nu ignora instructiunile din promputri lungi DACA sunt structurate cu etichete. Contradictia baseline v4 (850-1100 cuvinte "optimal") ramane NECONFIRMATA pentru toate use case-urile dar NERESPINSA pentru infografice.

**G4 — Anti-AI fotorealism:**
- SOLID CONSOLIDAT: Era photography tehnica acum are 3 surse (@pangyusio ZeroLu, @sunyunran ZeroLu 2026-05-26, YouMind GitHub) — mutata din "2 surse" la "3 surse confirmate"
- SINGLE-SOURCE UPDATE: "candid" keywords ("slightly blurry," "off-center," "awkward angle") = cookbook oficial + multiple ghiduri care il citeaza. NU sunt surse independente — ramane DE TESTAT pana la confirmare de la useri X cu dovezi vizuale

**G5 — Showcase design-uri:**
- 6 autori noi verificabili din ZeroLu (actualizat 2026-05-26 04:04 UTC):
  - @sunyunran: "90s + point-and-shoot camera quality" (5 cuvinte, Photography)
  - @MrLarus: "Silhouette Universe Narrative Poster" (500+ cuvinte, Typography)
  - @MrLarus: "Museum Catalog-Style Infographic" (400+ cuvinte, Typography)
  - @venturetwins: "eight-panel manga about GPT-Image-2" (Video/Animation)
  - @icreatelife: "Where is [Name] crowd search poster" (Video/Animation)
  - @ProperPrompter: "100 unique pixel art items grid" (Game/Entertainment)

### Goluri RAMASE pentru urmatoarea rulare:
1. **G2 PRIORITAR:** Diacritice RO (ș/ț comma-below) — inca 0 confirmare publica in gpt-image-2
2. **G3:** Product consistency text-only (fara imagine de referinta) — inca 0 tehnica confirmata
3. **G4:** "candid" framing keywords — confirmare de la 2 useri X cu dovezi vizuale (nu doar cookbook echo)
4. **G2:** "in the spirit of [font]" vs specificare directa — neconfirmat cu teste comparate
5. **G5:** Vintage Lisbon poster — identificare autor X original
6. **G1:** Test local comparativ 300 / 600 / 1000 cuvinte, acelasi brief

### Surse accesate cu succes:
- github.com/ZeroLu/awesome-gpt-image (raw README, 2026-05-26 actualizat AZI)
- developers.openai.com/cookbook/examples/multimodal/image-gen-models-prompting-guide (web snippet, 2026-04)
- fal.ai/learn/tools/prompting-gpt-image-2 (web snippet, 2026-04)
- mindstudio.ai blog (web snippet, 2026-05)
- Multiple web search snippets (fragmentar, 2026-04/05)

### Surse blocate (403):
- community.openai.com (Romanian diacritics thread)
- medium.com/@0xmega (infographics article)
- morphic.com, tharindumanujaya.com, the-decoder.com, segmind.com
- fal.ai/learn direct fetch (functioeaza doar snippet prin search)

### Nivel incredere general rulare 2:
- "Intended use" prefix = SOLID (3 surse independente cu autor verificabil)
- Era photography consolidata = SOLID (3 surse, 2 autori X distinti)
- Restul delta = clarificari pe date existente, nu tehnici complet noi

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
