# LOG RULARI — GPT-IMAGE-2 RESEARCH

---

## [2026-05-23] RULARE 2 — Goluri din run 1; surse max 30 zile (apr-mai 2026)

**Data rulare:** 2026-05-23 (TZ Europe/Bucharest)
**Surse cautate:** ultimele 30 zile (mai 2026) + 3 luni (feb-mai 2026)
**Status goaluri inainte:** 6 goluri din run 1

### DELTA adaugat:

**G4 — Candid/amateur framing → PROMOVAT DIN DE TESTAT in BEST PRACTICE:**
- Confirmat de 4 handles independente in magiccreator-ai GitHub: @phasE89, @WolfRiccardo, @Masimo_Blue, @mark_k
- Phrazing confirmat: "amatérská kompozice, momentka", "Realistic smartphone snapshot", "like an iPhone concert photo", "slightly amateur", "uneven spacing, natural ink pressure"
- Sursa: github.com/magiccreator-ai/awesome-gpt-image-2-prompts, activ mai 2026
- Nivel: SOLID (4 handles independente in acelasi repo + YouMind din run anterior = 5+ surse)

**G1 — Prompt length → ACTUALIZAT (mai tare evidence pentru 300-500 cuvinte):**
- Pixo.video: testat 150/300/600 cuvinte; "600-word version quietly dropped constraints from top" + 100-300 optim Instant, 500 Thinking
- tokenmix.ai / dev.to: "over 500 tokens diminishing returns" — al doilea domeniu independent
- Doua surse acum converg pe 300-500 cuvinte. 850-1100 baseline v4 = PROBABIL SUBOPTIMAL single-shot Instant Mode
- Nota: Thinking Mode tolereaza mai mult, dar +30-90 sec latenta
- Tot DE TESTAT local (nu exista confirmare din teste publice cu acelasi prompt la 3 lungimi)

**G5 — Letterpress/deboss → CONFIRMAT PARTIAL (single curated source):**
- Morphic prompt library: "cream recycled cardstock, letterpress printed, subtle deboss on logo" — testat si publicat
- "MERIDIAN & SONS debossed into the matte slate case lid" — testat si publicat
- Sursa: morphic.com/resources/how-to/chatgpt-images-2.0-prompts, 2026
- Nivel: single-source dar curated/tested; nu e inca SOLID (lipseste al doilea handle independent)

**G5 — Exemple Western European noi (3 exemple cu autori):**
- @WolfRiccardo: Amalfi Coast vintage travel poster, 1950s style + screen print texture
- @phasE89: Yorkshire pub scene, prompt in ceha, framing amator
- @Masimo_Blue: rough colored-pencil sketch cu "slightly amateur" look
- Sursa: github.com/magiccreator-ai/awesome-gpt-image-2-prompts, mai 2026

**G2 — Font "in the spirit of" → REAJUSTAT:**
- Community repos (magiccreator-ai + ZeroLu + Anil-matcha): NIMENI nu foloseste "in the spirit of"
- Practica comunitara = descriptori directi de era/echipament/stil: "retro 1950s", "35mm film", "CCD compact camera", "Kodak Portra 400 film simulation"
- Verdict: era/style descriptors directi = confirmat solid; "in the spirit of" = netestat public
- Ramane DE TESTAT: "in the spirit of Bodoni" vs "1920s Italian poster typeface" comparativ

**G2 — Diacritice RO → INCA GAP:**
- @phasE89 a folosit prompt in ceha ("amatérská fotka") implicit cu diacritice "é" — dar fara raport explicit despre acuratete
- Nu exista confirmare publica pentru comma-below RO (ș/ț U+0219/U+021B) vs cedilla (ş/ţ)
- Support oficial pentru "Latin scripts" = teoretic ar include, dar neverificat in practica

**G3 — Text-only product consistency → PARTIAL DATE NOI:**
- @SRKDAN (magiccreator-ai): constraint-based approach: "no zip, no buttons, no fastening — closes perfectly" + "no crown, no buttons — a sealed case that sets itself"
- Tehnica functioneaza pentru concept design dar nu pentru branding/logo consistency
- Inca GAP pentru: cum mentii un logo/brand consistent cross-generatii fara image reference

### Goluri ramase pentru urmatoarea rulare:
1. **G1 PRIORITAR:** Test local 300 vs 600 vs 1000 cuvinte acelasi prompt
2. **G2 PRIORITAR:** Test local diacritice RO (ș/ț/ă comma-below) + "in the spirit of" vs era descriptor
3. **G3:** Consistenta brand/logo text-only cross-generatii fara image reference — cauta tehnici confirmate
4. **G5:** Al doilea handle pentru letterpress/deboss ca sa treaca la SOLID
5. **G4 INCHIS** (nu mai are gap)

### Surse accesate cu succes:
- github.com/magiccreator-ai/awesome-gpt-image-2-prompts (raw README) — mai 2026, activ
- github.com/ZeroLu/awesome-gpt-image (raw README) — confirmat inca activ
- Multiple web search snippets: pixo.video, tokenmix.ai/dev.to, morphic.com, magiccreator-ai

### Surse blocate (403) in run 2:
- fal.ai, morphed.app, picsart.com, community.openai.com, pixnova.ai, evolink.ai, atlascloud.ai
- mindwiredai.com, framia.pro, wavespeed.ai, skywork.ai, befreed.ai, thenewstack.io, buildfastwithai.com
- openai.com/index/introducing-chatgpt-images-2-0/, pixo.video/blog (direct)
- Nota metodologica: ~70% din paginile incercate 403; informatia extrase in principal din GitHub raw + search snippets

### Nivel incredere general run 2:
- G4 candid/amateur: SOLID (4+ handles independente confirmate)
- G1 length: CONTESTAT cu doua surse (Pixo + tokenmix) dar lipsa test independent cu screenshot
- G5 letterpress: single-source curated (Morphic) — nu inca SOLID
- G2 diacritice: inca GAP complet

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
