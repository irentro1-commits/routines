# GPT-IMAGE-2 RESEARCH — i-vory Studio

Ultima actualizare: 2026-05-25
Versiune baseline referinta: FURAT v4 (850-1100 cuvinte, 14 sectiuni, img2img "LOCKED PRODUCT")

---

## G1 — STRUCTURA MAXIMA SINGLE-SHOT (cea mai mare structura care pastreaza calitatea)

### BEST PRACTICE ACTUALA (solid 2+ useri)

**Structura confirmata:** `[Scene/Background] → [Subject] → [Style/Medium] → [Lighting] → [Constraints] → [Negative]`
- Sursa 1: OpenAI Cookbook oficial (raw GitHub, 2026-04): "background/scene → subject → key details → constraints"
- Sursa 2: ZeroLu/awesome-gpt-image (GitHub, culegere de X creators confirmati: @BubbleBrain, @WolfRiccardo, @flowersslop, etc.)
- Sursa 3: Anil-matcha/Awesome-GPT-Image-2-API-Prompts (GitHub, multiple X handle credits)
- VERDICT: **Structura sectionate cu line breaks / etichete bate blocul dens** — confirmat independent de cookbook + doua repos comunitare cu autori reali

**Etichete > blob:** "use short labeled segments or line breaks instead of one long paragraph" — cookbook oficial
- Confirmat de ZeroLu (prompts cu "Title | Visual Requirements | Technical Specs | Content Elements")
- Confirmat de Anil-matcha (prompts modulate cu aspect ratio, lighting, exclusions separate)

**Limbaj concret > adjective vagi:**
- Cookbook: "Be concrete about materials, shapes, textures, and the visual medium"
- Community (ZeroLu + Anil-matcha): spec de camera, film stock, sursa de lumina, textura de suprafata bate "stunning" / "beautiful" / "amazing"

**Negative prompt la final:** "no plastic skin, no digital over-sharpening, no airbrushing, no watermark, no extra text, no logos"
- Confirmat de ZeroLu (multiple X creators)
- Confirmat de Anil-matcha
- Confirmat de cookbook: "no watermark, no extra text, no logos/trademarks"

### DE TESTAT

**CONTRADICTIE CRITICA — Lungimea promptului (partial clarificata 2026-05-25):**
- Baseline FURAT v4 zice 850-1100 cuvinte optimal
- Pixo.video ("15 field-tested techniques", 2026-04, single source): "sweet spot = 100-300 cuvinte Instant Mode, max 500 Thinking Mode"
- GitHub Anil-matcha: "GPT-Image-2 handles long, detailed prompts better than shorter ones." — fara limita superioara fixata
- GitHub YouMind: 150-800 cuvinte, 800+ numai pentru infografice complexe/UI mockups
- Cookbook oficial: nu da limita fixa, "long prompts can work but debugging harder"
- **NOU 2026-05-25 (magiccreator-ai, ~40+ creator credits):** @BubbleBrain foloseste prompts ce depasesc 800 cuvinte in practica reala (detaliere granulara piele/pose/lighting) si obtine rezultate. @WolfRiccardo si @mark_k: prompts moderate 50-150 cuvinte pt lifestyle/travel.
- **INTERPRETARE ACTUALA:** Contradictia e probabil use-case-dependent — 100-400 cuvinte = use case simplu (lifestyle, travel); 800+ cuvinte = portrait complex, product cu multe specificatii. 850-1100 e viabil pt complex single-shot dar nu e "optim universal".
- **ACTIUNE NECESARA:** Testat local cu acelasi subject la 300 / 600 / 1000 cuvinte pe acelasi tip de output. Contradictia nu e rezolvata complet.

**"7-Part Prompt Formula" / "8-Element Framework":**
- Mentionat de Felo AI si alte surse dar fara autor verificabil
- Single-source, nu include exemple reale
- SKIP pana la confirmare independenta

### RESPINS

- "Prompt scurt (<50 cuvinte) functioneaza la fel de bine" — contrazis de toate sursele comunitare (subutilizeaza modelul)
- "Keyword stuffing" (lista de buzzwords fara structura) — respins de cookbook + community
- "Vague quality adjectives" (stunning, hyper-realistic, amazing) — respins de cookbook si community

---

## G2 — FIDELITATE TEXT + DIACRITICE RO

### BEST PRACTICE ACTUALA (solid 2+ useri)

**Text exact in ghilimele:**
- Cookbook oficial: "Put literal text in quotes or ALL CAPS and specify typography details (font style, size, color, placement) as constraints"
- Confirmat de ZeroLu (multiple creators: Chinese text fara "garbled characters, typos")
- Confirmat de Anil-matcha (text placement + hierarchy ca design element)
- FORMULA: `exact text: "TEXTUL TAU" in [pozitie], [culoare], [font style], [dimensiune relativa]`

**Calitate medie/inalta pentru text mic:**
- Cookbook: "Use medium or high quality for small text, dense information panels, and multi-font layouts"
- Single-source oficial, logic consistent cu alte recomandari

**Spell-out pentru cuvinte dificile:**
- Cookbook: "For difficult words, spell them out letter-by-letter to improve character accuracy"
- EXEMPLU: "S-O-L-I-D-A-R-I-T-A-T-E" in loc de "SOLIDARITATE" pentru cuvinte lungi

**Ierarhie tipografica explicita:**
- Confirmat de ZeroLu + Anil-matcha: "Primary title + subtitle + introduction" cu pozitionare
- Adjectivele de tipografie functioneaza: "clean kerning, tight tracking, flush left, justified"

**Fiecare rand de text pe rand separat in prompt:**
- Confirmat de multiple surse: split textul in linii separate, nu un bloc

### DE TESTAT

**Diacritice RO (ș, ț, ă, â, î) — GAP MAJOR (partial inchis 2026-05-25):**
- Thread DALL-E OpenAI Community (community.openai.com/t/dall-e-does-not-correctly-place-diacritics.../1250658): inaccesibil 403
- GPT-Image-2 CONFIRMAT oficial: "high-fidelity text in Japanese, Korean, Chinese, Hindi, Bengali" — limbile Europene NU sunt in lista de "high-fidelity" din comunicatul oficial
- **NOU 2026-05-25:** ZeroLu/awesome-gpt-image (update 25 mai 2026, multiple X creator credits): diacritice CONFIRMATE pentru franceza, germana, spaniola in testare reala
- **NOU 2026-05-25:** magiccreator-ai/awesome-gpt-image-2-prompts (@phasE89, creator ceh): prompt cu "Amatérská fotka" (foto amatoreasca), diacritice cehesti (á, é, í, ů, č etc.) renderate corect — cel mai apropiat de RO confirmat pana acum
- **INFERENTA (nu confirmare):** Daca diacriticele cehesti (Eastern European) si cele franco-germane merg, sansa buna ca ă/â/î sa mearga. Comma-below (ș/ț U+0219/U+021B) INCA NECONFIRMAT — diferit de cedilla si mai rar in training data.
- Workaround de testat: "render Romanian text: [TEXTUL] using proper comma-below diacritics, NOT cedilla variants" + specificare Unicode explicit
- **ACTIUNE NECESARA (PRIORITARA):** Test local ș/ț — confirma daca reda comma-below corect (U+0219/U+021B) sau cedilla gresit (U+015F/U+0163)

**"in the spirit of [font clasic]" pentru evitare copyright:**
- Tehnica din baseline v4, logica din punct de vedere legal
- Nu am gasit confirmare directa 2+ useri ca functioneaza mai bine decat specificarea font-ului direct
- DE TESTAT: "in the spirit of Bodoni" vs "Bodoni style" vs "Bodoni" — care produce rezultat mai fidel

### RESPINS

- Nimic confirmat respins inca pentru G2

---

## G3 — LOCKED PRODUCT / IMG2IMG CONSISTENTA MAXIMA

### BEST PRACTICE ACTUALA (solid 2+ useri)

**Etichetare explicita a rolului fiecarei imagini de referinta:**
- "Image 1 is the product. Image 2 is the style reference." — confirmat de multiple ghiduri comunitare April 2026
- Cookbook: "State exclusions and invariants explicitly"
- FORMULA: `[Image 1] = product reference (LOCKED). [Image 2] = background/scene style. Change only: [X]. Keep locked: [Y, Z, W].`

**"Change only X, keep everything else the same":**
- Cookbook: "change only X + keep everything else the same"
- Confirmat de multiple surse comunitare
- Nota: "also say not to alter saturation, contrast, layout, arrows, labels, camera angle" — cookbook

**"Preserve list" — repeta la fiecare iteratie:**
- Cookbook: "repeat the preserve list on each iteration to reduce drift"
- Tehnica anti-drift, critica pentru sesiuni multi-iteratie

**Produs = strat blocat, scena = strat editabil:**
- "telling GPT Image 2 that the product is the locked layer and the scene is the editable layer matters more than adding style adjectives" — confirmat de multiple surse
- FORMULA: `LOCKED PRODUCT: [descriere]. EDITABLE SCENE: [descriere noua].`

**Character sheet three-view pentru personaje:**
- Confirmat de ZeroLu + Anil-matcha: "three-view drawings: front, side, and back" + "facial expression variations" pe fundal alb
- Foloseala: IP character consistency, storyboard generation

**Maxim 16 imagini de referinta per call:**
- Confirmat de multiple surse tehnice April 2026

**Pentru packaging:** "preserve the input product exactly" sau "plain packaging" cand modelul inventeaza detalii
- Confirmat de multiple ghiduri comunitare

### DE TESTAT

**Promptul "LOCKED PRODUCT" din baseline v4:**
- Termenul exact "LOCKED PRODUCT" ca eticheta in prompt — logic consistent cu tehnicile confirmate dar nu am gasit confirmarea acestei formule exacte in teste comunitare
- DE TESTAT: "LOCKED: [produs]" vs "PRESERVED: [produs]" vs "DO NOT CHANGE: [produs]" — care etichetare raspunde mai bine

**Consistenta cross-generatii fara imagine de referinta (text-only img2img):**
- **NOU 2026-05-25 (Anil-matcha, single-source):** "The same pet (absolutely consistent in appearance and coloring)" — descriere textuala extrem de detaliata a aparentei (culoare, markings, textura) functioneaza pentru personaj/animal. Tehnica: nu "consistent with previous" ci descrierea COMPLETA a obiectului la fiecare prompt.
- DE TESTAT pt produs fizic (packaging, sticla, etc.) — mai greu decat personaj
- GAP partial acoperit, confirmare a 2-a sursa necesara

### RESPINS

- "Simply say keep consistent" fara a lista explicit ce e blocat — respins de cookbook (drift inevitabil fara lista)

---

## G4 — ANTI-AI-TELL PENTRU FOTOREALISM HERO

### BEST PRACTICE ACTUALA (solid 2+ useri)

**Film stock specific in loc de "photorealistic" generic:**
- "Kodak Portra 400 look", "Fujifilm Classic Chrome", "35mm film grain" — confirmat de getimg.ai review + ZeroLu GitHub (multiple X creators)
- Cookbook: "be concrete" + "include 'photorealistic' to strongly engage photorealistic mode" — AMBELE pot fi adevarate: "photorealistic, shot on Kodak Portra 400, 35mm"
- Grain specific la film stock bate grain generic: "grain that matches specified film stock, not a generic noise overlay" — confirmat de getimg.ai + community

**Negative explicit anti-AI:**
- `no plastic skin, no digital over-sharpening, no airbrushing, no AI-synthetic look` — confirmat de ZeroLu (creditat la @WolfRiccardo, @BubbleBrain si altii) + YouMind GitHub
- `Negative: Low quality, unnatural hands, extra fingers, excessive skin retouching, text artifacts` — YouMind GitHub (pattern consistent across multiple prompts)

**Limbaj de imperfectiune:**
- "visible micro pores", "subtle skin texture", "natural imperfections", "slight blurriness", "fingerprints, smudges, scratches" — ZeroLu + Anil-matcha (multiple creator credits)
- CONFIRMAT: imperfection language > "perfect skin" language pentru anti-AI

**Ancore de echipament real:**
- "RAW quality, unprocessed, unedited image with full iPhone camera quality" — @WolfRiccardo (ZeroLu)
- "shot on iPhone", "35mm film photography", "Sony α7R V" — multiple surse si creatori
- Cookbook: "prompt the model as if a real photo is being captured in the moment. Use photography language"

**Era photography pentru autenticitate temporala:**
- "2003 digital camera family snapshot" — @pangyusio (ZeroLu) — grain si compresie specifica epocii
- "90s point-and-shoot camera quality" — YouMind GitHub
- TEHNICA: specificarea unui device/era veche adauga imperfectii caracteristice = mai greu de identificat ca AI

**Lighting realism:**
- "harsh direct on-camera flash, specular highlights" — ZeroLu
- "natural window light", "tungsten-vs-neon color mixing" — confirmat de multiple surse

**"Candid mood" / "amateur photo" framing — CONFIRMAT SOLID 2026-05-25:**
- **magiccreator-ai** (curated de la @WolfRiccardo, @BubbleBrain, @mark_k, @phasE89 + 40 creatori): "smartphone photo realism", "CCD compact camera + harsh on-camera direct flash" pentru snapshot autentic, "authentic phone or travel-camera photos", "amatérská fotka / amatérská kompozice, momentka" (creator ceh)
- **Anil-matcha** (multiple contributor prompts): "CCD Camera Flash Candid" cu "candid snapshot feeling, slight motion blur"; "Faces and postures must look like real pedestrians, not overly polished"
- CONFIRMAT: 2 surse independente (magiccreator-ai multi-creator + Anil-matcha multi-contributor). Mutat din DE TESTAT.
- FORMULA: `shot on CCD compact camera, harsh on-camera direct flash, candid snapshot feeling, slight motion blur, faces and postures look like real pedestrians not overly polished`
- VARIANTA: `first-person POV / bodycam perspective` pentru anti-posed look (single-source magiccreator-ai, DE TESTAT)

**Anonimizare cu censor blocks:**
- YouMind GitHub: "opaque rectangular masks covering faces while preserving identity context"
- Interesant dar use-case limitat pentru hero product
- DE TESTAT pentru lifestyle photography fara fata completa

### DE TESTAT

**First-person POV / bodycam perspective:**
- magiccreator-ai (single-source direction): driver's seat, bodycam perspective pentru intimitate candid
- Logica: elimina "posed for camera" look complet
- DE TESTAT: adaugat la hero lifestyle shots

### RESPINS

- "Hyper-realistic, stunning, ultra-detailed" ca substitute pentru specificatii concrete — respins de cookbook si community
- "Perfect lighting, perfect skin" — contrazice tehnica imperfectiunii

---

## G5 — DESIGN-URI SMECHERE CU PROMPTUL REAL (showcase)

### BEST PRACTICE ACTUALA (solid 2+ useri)

Exemple verificate cu autori reali din ZeroLu/awesome-gpt-image (GitHub, colectie din X/Twitter):

**1. RAW iPhone Street Photo** — @WolfRiccardo (X)
- Prompt core: "Completely RAW quality, unprocessed, unedited image with full iPhone camera quality...momentary blur. The subway is in motion."
- Tehnica: equipment anchor + motion blur + "unprocessed"
- Aplicare i-vory: hero lifestyle cu produs in scena reala

**2. Handwritten Notebook** — @patrickassale (X)
- Prompt core: "casual and slightly messy, like personal notes, natural imperfections, crossed out words, underlined headings...no flash"
- Tehnica: imperfectiune + sans flash = autentic
- Aplicare i-vory: packaging mock-up "scris de mana"

**3. 2003 Digital Camera Family Snapshot** — @pangyusio (X)
- Prompt core: "Generate a photo from 2003, shot with a digital camera"
- Tehnica: era photography = grain + compresie JPEG specifica = imposibil de identificat ca AI
- Aplicare i-vory: testimonial fake UGC cu produs

**4. 35mm Onsen Portrait** — @BubbleBrain (X)
- Prompt core: "35mm film photography, warm vintage Japanese onsen ryokan aesthetic, soft ambient wooden lantern lighting"
- Tehnica: film + lumina specifica de sursa + ambient cald
- Aplicare i-vory: lifestyle foto produs beauty/wellness

**5. Movie Theater Celebrity Scene** — @flowersslop (X)
- Tehnica: ancorare reala (cinema) + personaj compus
- Aplicare i-vory: social proof visual cu brand placement

**6. Pet x Brand Collab (KFC)** — 卡尔的AI沃茨 (WeChat)
- Prompt core: "77 (cat's name) X KFC — absolutely consistent in appearance and coloring"
- Tehnica: cross-brand collab cu consistenta fortata explicit
- Aplicare i-vory: collab campaign visual

**7. Amalfi Coast Vintage Travel Poster** — @WolfRiccardo (X, via magiccreator-ai, 2026-05)
- Tehnica: "1950s travel poster style" + era descriptori + retro palette
- Aplicare i-vory: packaging insert / gift card cu aesthetic mediteraneean

**8. Boston Spring 2026 Event Poster** — @BubbleBrain (X, via magiccreator-ai, 2026-05)
- Tehnica: localitate reala + sezon + granularitate imbracaminte/lighting 800+ cuvinte
- Aplicare i-vory: poster campaign sezonier cu text

**9. Yorkshire Pub Scene** — @phasE89 (X, creator ceh, via magiccreator-ai, 2026-05)
- Tehnica: candid interior + "authentic pub atmosphere" + CCD aesthetic
- Aplicare i-vory: lifestyle shot produs in context European autentic

**10. Irish Countryside Coastal Portrait** (creator neverificat, magiccreator-ai, 2026-05)
- Tehnica: locatie specifica + lumina naturala nord-atlantica + film stock cald
- NOTA: creator handle neverificat — nivel incredere mai mic, dar tehnica consistenta cu alte exemple confirmate

### DE TESTAT

**Prompturi carusel 3:4 vs hero 3:2 din baseline v4:**
- Tehnica aspect ratio specifica mentionata in baseline dar nu am gasit confirmare din teste comunitare ca 3:4 vs 3:2 afecteaza semnificativ calitatea compositiei
- DE TESTAT local

**"Letterpress physics cu masuratori" din baseline v4:**
- Tehnica specifica mentionata in baseline, interesanta pentru packaging print
- Nu am gasit confirmare comunitara directa (poate exista in forumuri de print design)
- DE TESTAT: "letterpress printed, subtle deboss, slight ink squish at edges, impression depth 0.3mm"

### RESPINS

- Nimic confirmat respins inca pentru G5

---

## NOTE METODOLOGICE

**Surse accesate cu succes:**
- GitHub raw content: ZeroLu/awesome-gpt-image (update 2026-05-25), Anil-matcha/Awesome-GPT-Image-2-API-Prompts, YouMind-OpenLab/awesome-gpt-image-2, openai/openai-cookbook
- **NOU 2026-05-25:** github.com/magiccreator-ai/awesome-gpt-image-2-prompts — living collection curated din X, ~40+ creatori confirmati (@WolfRiccardo, @BubbleBrain, @mark_k, @itnavi2022, @phasE89 si altii). Adaugat la surse tracked.
- Web search snippets: multiple surse (fragmentar)

**Surse blocate (403):**
- OpenAI Developer Community forum (threads specifice)
- VentureBeat, TechCrunch, Pixo, Phygital+, Fotor, DataCamp, MagicShot, Seaart, etc.
- Motivul probabil: bot detection / paywall

**Surse SKIP (blogspam/afiliat fara autor):**
- notegpt.io, a2a-mcp.org, apiyi.com, pixverse.ai, imini.com, tenorshare.ai, noviai.ai, mindstudio.ai — ghiduri SEO fara autor verificabil si fara dovezi de testare proprie

**Criterii confirmare:**
- "solid": tehnica mentionata/demonstrata de 2+ autori independenti (handle X verificabil, cookbook oficial, sau repo GitHub cu contributii multiple)
- "single-source de testat": tehnica plausibila dar un singur autor/sursa
