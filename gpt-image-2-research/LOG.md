# LOG RULARI — GPT-IMAGE-2 RESEARCH

---

## [2026-05-27] RULARE 2 — Delta incremental (goluri din rularea 1)

**Data rulare:** 2026-05-27 (TZ Europe/Bucharest)
**Surse cautate:** ultimele 30 zile (mai 2026) prioritar; 3 luni (feb-mai 2026)
**Goluri atacate:** G4 candid/amateur, G3 consistenta text-only, G2 font "in the spirit of", G1 lungime prompt, G2 diacritice RO, G5 exemple Western

### DELTA adaugat:

**G4 — Candid/amateur framing: MUTAT DIN DE TESTAT IN SOLID**
- @AntCaveClub (X, ZeroLu 2026-05-27, NOU): "a beautiful woman looking at her phone on the subway; a candid photo" — confirma explicit keyword "candid"
- @patrickassale (X, ZeroLu 2026-05-27, NOU): "Amateur iPhone photo at Apple Park during the iPhone 20 keynote" — "amateur iPhone photo" ca framing distinct
- Acum 3 handles X independenti (@WolfRiccardo + @patrickassale x2 + @AntCaveClub) cu 4 exemple verificate
- VERDICT: SOLID — inclus in BEST PRACTICE

**G5 — Showcase: 2 exemple noi**
- @patrickassale: Apple Park event photography (URL verificabil)
- @AntCaveClub: urban subway candid (URL verificabil)

**G3 — Thinking Mode: NOU DE TESTAT**
- Thinking Mode (Plus/Pro/Business) = 8 imagini coerente dintr-un prompt, reasoning step inainte de generare
- Relevant pentru batch product consistency fara drift
- Sursa: OpenAI launch + AVB benchmark April 2026 (nu din useri reali cu handles)

**G2 — Font "art movement approach": CLARIFICAT**
- Conceptul "art movement / design style" in loc de font specific confirmat in surse tehnice (Apiyi single-source)
- Aliniat cu "in the spirit of" din baseline v4, dar neverificat de useri reali

### Goluri RAMASE pentru urmatoarea rulare:
1. **G2 PRIORITAR:** Diacritice RO comma-below — zero confirmare publica (thread OpenAI Community tot 403)
2. **G1:** Contradictia lungime prompt (850-1100 vs 100-500) — nerezolvata, Oakgen.ai "500 generatii" inaccesibil
3. **G2:** "in the spirit of [font]" confirmare 2+ useri cu handles (nu single-source)
4. **G5:** Exemple design Western/European (repo-urile disponibile sunt CJK-heavy)
5. **G3:** Consistenta text-only fara imagine de referinta — "Preserve list" framework gasit dar neverificat

### Surse accesate cu succes:
- github.com/ZeroLu/awesome-gpt-image (raw README, 2026-05-27 — cel mai recent) — SURSA PRINCIPALA DELTA
- Multiple web search snippets (fragmentar, mai 2026)
- YouMind GitHub (summary rezumat, limitat)

### Surse 403 (persistente):
- community.openai.com/t/dall-e-does-not-correctly-place-diacritics... — tot blocat
- pixo.video, promptolis.com, morphed.app, oakgen.ai, vibedex.ai, analyticsvidhya.com, pixverse.ai, fal.ai, wavespeed.ai, thenewstack.io, arxiv.org/2511.13182 — toate 403

### Nivel incredere rulare 2:
- Delta G4 = SOLID (3 handles X verificabili, 4 exemple cu URL-uri)
- Delta G3 Thinking Mode = single-source (OpenAI) confirmat de benchmark, netestat de comunitate
- Delta G2 font = conceptual aliniat dar single-source blogspam
- ~70% din pagini incercate = 403

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
