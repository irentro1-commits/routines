# GPT-IMAGE-2 RESEARCH — i-vory Studio

Ultima actualizare: 2026-05-28
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

**NUANTA CRITICA LUNGIME PROMPT (actualizat 2026-05-28):**

Exista doua clustere distincte confirmate empiric:

- **Cluster A — Photorealism / hero shots / porterete / lifestyle:** optimal 150-300 cuvinte
  - Anil-matcha repo: medie empirica ~215 cuvinte din 15 prompts de succes (fotorealism, UI, lifestyle)
  - Pixo.video (single-source, 2026-04): "sweet spot = 100-300 cuvinte Instant Mode, max 500 Thinking Mode"
  - YouMind GitHub (2026-04): "150-800 cuvinte, 800+ numai pentru infografice complexe"
  - Logica confirmata: "model incepe sa ignore instructiunile timpurii dupa cateva sute de tokeni"

- **Cluster B — UI mockups / infografice complexe / JSON-structurate:** optimal 800-1200+ cuvinte
  - gpt-image2/awesome-gptimage2-prompts (GitHub, 179 stars, 3000+ prompts, 2026-04): medie prompts "Featured" = ~1100 cuvinte (JSON structurat cu callouts)
  - Prompts simple (poster de oras): 15-20 cuvinte; Prompts UI mockup complex: 1500-2000+ cuvinte
  - CONCLUZIE: lungimea mare e justificata NUMAI cand e JSON-structurata cu specificatii precise per element

- **VERDICT FINAL G1 LUNGIME:** Baseline v4 (850-1100 cuvinte) este VALID dar CONDITIONAT — functioneaza pentru infografice/UI cu 14 sectiuni etichetate. NU este optim universal. Pentru hero shots / lifestyle / fotorealism: taie la 200-350 cuvinte. Contradictia aparenta din rularea 1 (850-1100 vs 150-300) era de fapt o distinctie de tip-continut.

### DE TESTAT

**"7-Part Prompt Formula" / "8-Element Framework":**
- Mentionat de Felo AI si alte surse dar fara autor verificabil
- Single-source, nu include exemple reale
- SKIP pana la confirmare independenta

### RESPINS

- "Prompt scurt (<50 cuvinte) functioneaza la fel de bine" — contrazis de toate sursele comunitare (subutilizeaza modelul)
- "Keyword stuffing" (lista de buzzwords fara structura) — respins de cookbook + community
- "Vague quality adjectives" (stunning, hyper-realistic, amazing) — respins de cookbook si community
- "850-1100 cuvinte e optim universal" — PARTIAL RESPINS; e optim pentru JSON/UI, nu pentru fotorealism/hero

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

**Tehnica art-movement pentru tipografie (actualizat 2026-05-28):**
- Confirmat prin multiple snippets de search (2026): inlocuieste numele fontului cu miscare artistica sau stil de design
- Mecanism: modelul activeaza un "sistem estetic complet" (font + layout + culori + proportii) in loc de o singura proprietate
- Exemple confirmate functional: "minimalist Bauhaus sans-serif", "Art Deco geometric lettering", "Swiss International Typographic Style grid", "gritty street graffiti letterform"
- Avantaj vs naming direct: evita copyright + activeaza context vizual mai bogat
- Tehnica din baseline v4 ("in the spirit of [font clasic]") este o forma a acestei abordari — acum SUSTINUTA conceptual de multiple surse
- NIVEL: confirmat din snippet-uri multiple (2026) dar fara autori individuali cu handle verificabil; considerat solid conceptual, DE VERIFICAT cu test propriu pentru formula exacta "in the spirit of"
- Surse: search snippets din apiyi.com, gpt-image2 repo (Momotaro prompt: "fuses the gentle atmosphere of 'Irasutoya' with the overwhelming information density of 'Kasumigaseki slides'"), multiple blog snippets 2026

### DE TESTAT

**Diacritice RO (ș, ț, ă, â, î) — GAP MAJOR:**
- Thread DALL-E pe OpenAI Developer Community identificat (community.openai.com/t/dall-e-does-not-correctly-place-diacritics.../1250658) dar inaccessibil (403) si inca relevant pentru DALL-E nu gpt-image-2 specific
- Problema documentata pentru DALL-E: cedilla (ş/ţ) in loc de comma-below (ș/ț) — diferenta Unicode: gresit U+015F/U+0163, corect U+0219/U+021B
- gpt-image-2 promite ~95-99% text accuracy pentru Latin + CJK + Hindi + Bengali — Eastern European cu diacritice comma-below neconfirmat in testare publica
- Workaround de testat: "render Romanian text using proper comma-below diacritics (ș U+0219, ț U+021B), NOT cedilla variants"
- **ACTIUNE NECESARA:** Test local cu ș/ț/ă — fotografie rezultat, noteaza daca model foloseste cedilla (gresit) vs comma-below (corect)

**"in the spirit of [font clasic]" formula exacta:**
- Tehnica mai larga (art movement) e sustinuta; formula exacta cu "in the spirit of" neconfirmata direct de useri cu output fotografiat
- DE TESTAT: "in the spirit of Bodoni" vs "Bodoni-style geometric serif" vs "Didot-inspired high-contrast serif" — care formula produce rezultat mai fidel

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

**input_fidelity parameter (API):**
- "high" fidelity pentru logo, fata, brand asset care trebuie sa ramana identice
- Sursa: snippet search (single-source, 2026) — confirma existenta parametrului; verifica in API docs

### DE TESTAT

**Text-only consistency (FARA imagine de referinta) — partial progres (2026-05-28):**
- Prima tehnica identificata: "detailed specification language" = descriere exacta de material + geometrie + textura pentru a bloca un produs vizual consistent intre generari
- Exemplu din gpt-image2/awesome-gptimage2-prompts: "Form-fitting cream or ivory bodycon midi dress with elegant draping and ruching, featuring an asymmetrical neckline with 1 shoulder strap" — consistent across generations fara imagine sursa
- Alt exemplu: caracter cu "long flowing pale blonde hair with soft layers and long front bangs" — repetat identic in fiecare prompt din serie
- Principiu: "consistency through restrictive style definitions rather than visual references"
- NIVEL: single-source (gpt-image2 repo, 179 stars) — DE TESTAT local

**Promptul "LOCKED PRODUCT" din baseline v4:**
- Termenul exact "LOCKED PRODUCT" ca eticheta in prompt — logic consistent cu tehnicile confirmate dar nu am gasit confirmarea acestei formule exacte in teste comunitare
- DE TESTAT: "LOCKED: [produs]" vs "PRESERVED: [produs]" vs "DO NOT CHANGE: [produs]" — care etichetare raspunde mai bine

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
- `No influencer styling. Faces and postures must look like real pedestrians, not overly polished.` — Anil-matcha/Awesome-GPT-Image-2-API-Prompts (Convenience Store Night Scene prompt, 2026-04)

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

**CANDID / AMATEUR FRAMING — CONFIRMAT SOLID (actualizat 2026-05-28):**
- Tehnica: adauga "a candid photo" sau "amateur photo" ca sufix simplu la sfarsitul promptului
- Efect confirmat: previne hyperpolish artifacts care tradeaza AI ("paradoxically improves photorealism by preventing hyperpolish artifacts")
- Confirmat de 4+ autori in 2 repo-uri independente:
  - ZeroLu GitHub: @AntCaveClub — "A beautiful woman looking at her phone on the subway; a candid photo" (sufix simplu, tehnica minima)
  - ZeroLu GitHub: @patrickassale — "Amateur iPhone photo at Apple Park during the iPhone 20 keynote, Tim Cook presenting on stage"
  - ZeroLu GitHub: @patrickassale — "Amateur photo of an open notebook lying flat, filled with handwritten notes... natural imperfections"
  - Anil-matcha GitHub: "No influencer styling. Faces and postures must look like real pedestrians, not overly polished" + "The image should look like an authentic life slice captured by a photographer in the city"
- FORMULA OPTIMA: [prompt principal] + "; a candid photo" SAU "amateur [device] photo of" la inceput
- Varianta negativa: "No influencer styling. Not overly polished." in sectiunea Negative

**Timestamp overlay pentru digital camera simulation (actualizat 2026-05-28):**
- gpt-image2/awesome-gptimage2-prompts (179 stars, 2026-04): "timestamp in the bottom-right corner reading '02 18 04'" — simuleaza metadata de camera digitala veche
- Consistent cu era-photography technique (@pangyusio ZeroLu: "photo from 2003")
- NIVEL: single-source (gpt-image2 repo); consistent cu G4 pattern = DE TESTAT pentru aplicatii

### DE TESTAT

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

**7. Subway Candid** — @AntCaveClub (X, ZeroLu GitHub)
- Prompt core: "A beautiful woman looking at her phone on the subway; a candid photo."
- Tehnica: prompt minimal + candid sufix = result autentic
- Aplicare i-vory: UGC lifestyle, social content organic-looking

**8. Apple Keynote Amateur** — @patrickassale (X, ZeroLu GitHub)
- Prompt core: "Amateur iPhone photo at Apple Park during the iPhone 20 keynote, Tim Cook presenting on stage"
- Tehnica: "amateur" framing + context real specific = credibilitate maxima
- Aplicare i-vory: event/behind-scenes content pentru brand story

**9. Convenience Store Night Scene** — (Anil-matcha GitHub, 2026-04)
- Prompt core: "Create an ultra-realistic urban street group photo at a convenience store entrance at 10 PM on a summer night... No influencer styling. Faces and postures must look like real pedestrians, not overly polished... The image should look like an authentic life slice captured by a photographer in the city."
- Tehnica: negative anti-polish + "authentic life slice" framing + specificatii de ambient real (freezer stickers, glass reflections, shared bikes)
- Aplicare i-vory: lifestyle brand photo cu produs in scena urbana

### DE TESTAT

**Prompturi carusel 3:4 vs hero 3:2 din baseline v4:**
- Tehnica aspect ratio specifica mentionata in baseline dar nu am gasit confirmare din teste comunitare ca 3:4 vs 3:2 afecteaza semnificativ calitatea compositiei
- DE TESTAT local

**"Letterpress physics cu masuratori" din baseline v4:**
- Tehnica specifica mentionata in baseline, interesanta pentru packaging print
- Nu am gasit confirmare comunitara directa (poate exista in forumuri de print design)
- DE TESTAT: "letterpress printed, subtle deboss, slight ink squish at edges, impression depth 0.3mm"

**Design showcase Western/European cu prompt real si autor verificabil:**
- GAP: nu am gasit exemple cu handle de X + prompt real + output pentru design European/Western
- Toate exemplele verificate sunt CJK-heavy sau US-focused
- DE CAUTAT: Reddit r/ChatGPT, r/OpenAI, r/graphic_design, X creators europeni

### RESPINS

- Nimic confirmat respins inca pentru G5

---

## NOTE METODOLOGICE

**Surse accesate cu succes:**
- GitHub raw content: ZeroLu/awesome-gpt-image, Anil-matcha/Awesome-GPT-Image-2-API-Prompts, YouMind-OpenLab/awesome-gpt-image-2, openai/openai-cookbook, gpt-image2/awesome-gptimage2-prompts (NOU rulare 2)
- Web search snippets: multiple surse (fragmentar)

**Surse blocate (403):**
- OpenAI Developer Community forum (threads specifice)
- VentureBeat, TechCrunch, Pixo, Phygital+, Fotor, DataCamp, MagicShot, Seaart, etc.
- weshop.ai, pixnova.ai, chatgptimages.app, fal.ai/learn, morphic.com, sentisight.ai, james-palm.medium.com, atlascloud.ai, apiyi.com
- Motivul probabil: bot detection / paywall

**Surse SKIP (blogspam/afiliat fara autor):**
- notegpt.io, a2a-mcp.org, apiyi.com, pixverse.ai, imini.com, tenorshare.ai, noviai.ai, mindstudio.ai — ghiduri SEO fara autor verificabil si fara dovezi de testare proprie

**Criterii confirmare:**
- "solid": tehnica mentionata/demonstrata de 2+ autori independenti (handle X verificabil, cookbook oficial, sau repo GitHub cu contributii multiple)
- "single-source de testat": tehnica plausibila dar un singur autor/sursa
