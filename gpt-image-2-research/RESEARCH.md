# GPT-IMAGE-2 RESEARCH — i-vory Studio

Ultima actualizare: 2026-05-26
Versiune baseline referinta: FURAT v4 (850-1100 cuvinte, 14 sectiuni, img2img "LOCKED PRODUCT")

---

## G1 — STRUCTURA MAXIMA SINGLE-SHOT (cea mai mare structura care pastreaza calitatea)

### BEST PRACTICE ACTUALA (solid 2+ useri)

**Structura confirmata:** `[Intended Use] → [Scene/Background] → [Subject] → [Style/Medium] → [Lighting] → [Constraints] → [Negative]`
- Sursa 1: OpenAI Cookbook oficial (developers.openai.com/cookbook, 2026-04): "background/scene → subject → key details → constraints" + "include the intended use (ad, UI mock, infographic) to set the mode and level of polish"
- Sursa 2: ZeroLu/awesome-gpt-image (GitHub, culegere de X creators confirmati: @BubbleBrain, @WolfRiccardo, @flowersslop, @MrLarus, @sunyunran, etc.)
- Sursa 3: Anil-matcha/Awesome-GPT-Image-2-API-Prompts (GitHub, multiple X handle credits)
- Sursa 4: fal.ai/learn/tools/prompting-gpt-image-2 + MindStudio blog (2026-04/05): "name the intended use up front so the model sets the right polish level"
- VERDICT: **Structura sectionata cu line breaks / etichete bate blocul dens** — confirmat independent de cookbook + doua repos comunitare + doua ghiduri tehnice cu testare proprie

**[NOU 2026-05-26] "Intended Use" prefix = sectiunea 0 a promptului:**
- `"pitch deck slide" / "product ad" / "infographic" / "hero banner" / "carousel post"` pus LA INCEPUTUL promptului semnaleaza modelului nivelul de finisaj si contextul vizual
- Cookbook oficial + fal.ai + MindStudio (3 surse independente, 2026-04/05) = SOLID
- Exemplu aplicat: `"Product ad for Instagram carousel. Background: marble texture..."`

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

**CONTRADICTIE LUNGIME PROMPT — clarificare partiala [actualizat 2026-05-26]:**
- Baseline FURAT v4 zice 850-1100 cuvinte optimal
- Pixo.video (2026-04, single source): sweet spot = 100-300 Instant Mode, max 500 Thinking Mode
- GitHub Anil-matcha: 100-400 cuvinte optim; 500+ = risc incoerenta
- GitHub YouMind: 150-800 cuvinte, 800+ numai infografice complexe
- Cookbook: nu da limita fixa; "long prompts can work but debugging harder"
- ZeroLu (actualizat 2026-05-26, @sunyunran): prompt de 5 cuvinte ("90s + point-and-shoot camera quality") = rezultat impecabil pentru atmosfera simpla
- ZeroLu (2026-05-26, @MrLarus): prompt 500+ cuvinte = Silhouette Universe poster cu rezultate confirmate
- MindStudio (2026-05): "GPT Image 2 parses each clause rather than blending elements" = modelul NU ignora parti din prompturi lungi
- **CLARIFICARE ACTUALA:** Lungimea optima e RELATIVA LA COMPLEXITATEA TASK-ULUI. Ultra-scurt (sub 50 cuvinte) = ok pt atmosfera/stil simplu. Lung (500+) = ok pt infografice/poster cu multe elemente. Structura cu etichete ramane critica indiferent de lungime.
- **RAMANE DE TESTAT local:** acelasi brief complex la 300 / 600 / 1000 cuvinte cu structura identica

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

**Diacritice RO (ș, ț, ă, â, î) — GAP MAJOR:**
- Exista un thread vechi pe OpenAI Developer Community despre probleme DALL-E cu diacriticele romanesti (URL identificat: community.openai.com/t/dall-e-does-not-correctly-place-diacritics.../1250658) dar nu am putut accesa continutul (403)
- GPT-Image-2 promite ~99% text accuracy si suport multilingual CONFIRMAT pentru: CJK, Arabic, Hindi, Bengali
- Suport Eastern European / Romano / comma-below (ș/ț vs cedilla s/t) — **NECONFIRMAT in testare publica**
- Workaround potential de testat: specificare explicita "text with correct Romanian diacritics: comma-below s (ș U+0219), comma-below t (ț U+021B)" sau scris Unicode explicit
- Alt workaround de testat: "render Romanian text: [TEXTUL] using proper comma-below diacritics, NOT cedilla variants"
- **ACTIUNE NECESARA:** Test local cu ș/ț/ă - fotografiaza rezultatul, noteaza daca model foloseste cedilla (gresit: ş/ţ U+015F/U+0163) vs comma-below (corect: ș/ț U+0219/U+021B)

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
- Nu am gasit tehnici confirmate de 2+ useri pentru a bloca un produs fara imagine sursa
- GAP de cercetat la urmatoarea rulare

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

**Era photography pentru autenticitate temporala — CONFIRMARE DUBLA [actualizat 2026-05-26]:**
- "2003 digital camera family snapshot" — @pangyusio (ZeroLu, 2026-04)
- "90s + point-and-shoot camera quality" — @sunyunran (ZeroLu, actualizat 2026-05-26) — prompt de 5 cuvinte, confirmat ca produce rezultat distinct si autentic
- "90s point-and-shoot camera quality" — YouMind GitHub (2026-04)
- ACUM 3 SURSE INDEPENDENTE pentru era photography (2 autori X + 1 repo GitHub)
- TEHNICA CONFIRMATA SOLID: specificarea unui device/era veche adauga imperfectii caracteristice (grain, compresie JPEG, color cast specific) = mai greu de identificat ca AI

**Lighting realism:**
- "harsh direct on-camera flash, specular highlights" — ZeroLu
- "natural window light", "tungsten-vs-neon color mixing" — confirmat de multiple surse

### DE TESTAT

**"Candid mood" / "amateur photo" framing [actualizat 2026-05-26]:**
- Keywords confirmate de cookbook oficial + multiple ghiduri (2026-04/05): "slightly blurry," "off-center," "awkward angle," "candid," "snapshot," "phone photo," "harsh flash," "slightly tilted horizon"
- EXEMPLU din cookbook: "candid and unposed, 35mm film aesthetic, shallow depth of field, photorealistic"
- DE TESTAT: cookbook = singura sursa cu autor verificabil; ghidurile multiple care citeaza acelasi cookbook nu sunt surse independente. Nicio confirmare directa de la 2 useri X cu dovezi vizuale.
- ACTIUNE: test local cu aceste keywords adaugate la un hero shot standard

**Anonimizare cu censor blocks:**
- YouMind GitHub: "opaque rectangular masks covering faces while preserving identity context"
- Interesant dar use-case limitat pentru hero product
- DE TESTAT pentru lifestyle photography fara fata completa

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

**[NOU 2026-05-26 — din ZeroLu actualizat 260526 04:04 UTC]**

**7. "90s Point-and-Shoot Camera"** — @sunyunran (X, ZeroLu 2026-05-26)
- Prompt: `"90s + point-and-shoot camera quality"` — 5 cuvinte, zero detalii extra
- Tehnica: ultra-minimalist era anchor; modelul infereste tot ce tine de grain, color, compresie
- Aplicare i-vory: lifestyle UGC rapid fara sa construiesti prompt elaborat de fotorealism

**8. "Silhouette Universe Narrative Poster"** — @MrLarus (X, ZeroLu 2026-05-26)
- Prompt: ~500+ cuvinte, structura modulara: silhouette selection → internal world → texture → color palette → final quality
- Tehnica: prompt lung (500+) structurat pe sectiuni = colectiv poster editorial de inalta estetica
- Aplicare i-vory: poster campanie cu mesaj narativ complex; dovedeste ca prompturi lungi NU afecteaza calitatea daca sunt structurate

**9. "Museum Catalog-Style Infographic"** — @MrLarus (X, ZeroLu 2026-05-26)
- Prompt: ~400+ cuvinte; structura: layout → material descriptions → pattern meanings → aesthetic
- Tehnica: "museum catalog" ca intended use prefix = nivelul de finisaj editorial impus modelului
- Aplicare i-vory: product education card, ingrediente packaging vizualizate ca exponate

**10. "Eight-Panel Manga Concept"** — @venturetwins (X, ZeroLu 2026-05-26)
- Prompt: `"Create an eight-panel manga about GPT-Image-2 launching today"`
- Tehnica: storytelling secvential single-shot; modelul compune naratiunea
- Aplicare i-vory: product story carusel cu personaj/naratiune

**11. "Where is [Name] Crowd Poster"** — @icreatelife (X, ZeroLu 2026-05-26)
- Prompt: `"Create a 'Where is [Your Name]' crowd search poster set in the city of your choosing"`
- Tehnica: template cu variabila deschisa; mass crowd + easter egg product placement
- Aplicare i-vory: awareness campaign visual cu brand ascuns

**12. "100 Pixel Art Items Grid"** — @ProperPrompter (X, ZeroLu 2026-05-26)
- Prompt: `"Create a single image containing a grid of 100 completely unique pixel art items, each with a meaningful label"`
- Tehnica: density stress-test pentru text + consistency la scara mare (100 elemente distincte)
- Aplicare i-vory: icon pack, product variety showcase pixel-style

### DE TESTAT

**Prompturi carusel 3:4 vs hero 3:2 din baseline v4:**
- Tehnica aspect ratio specifica mentionata in baseline dar nu am gasit confirmare din teste comunitare ca 3:4 vs 3:2 afecteaza semnificativ calitatea compositiei
- DE TESTAT local

**"Letterpress physics cu masuratori" din baseline v4:**
- Tehnica specifica mentionata in baseline, interesanta pentru packaging print
- Nu am gasit confirmare comunitara directa (poate exista in forumuri de print design)
- DE TESTAT: "letterpress printed, subtle deboss, slight ink squish at edges, impression depth 0.3mm"

**Western/European design cu autor X verificabil:**
- Vintage Lisbon travel poster (1960s screen-print, gouache) circula in ghiduri (morphic.com, picsart.com, 2026-04) dar fara autor X confirmat — posibil OpenAI demo original
- DE TESTAT: cine e autorul real? Cautare directa pe X pentru "Lisbon travel poster gpt-image-2"

### RESPINS

- Nimic confirmat respins inca pentru G5

---

## NOTE METODOLOGICE

**Surse accesate cu succes:**
- GitHub raw content: ZeroLu/awesome-gpt-image, Anil-matcha/Awesome-GPT-Image-2-API-Prompts, YouMind-OpenLab/awesome-gpt-image-2, openai/openai-cookbook
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
