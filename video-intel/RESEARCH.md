# VIDEO INTEL - i-vory Studio Research Base
> Ultima actualizare: 2026-05-23 | Rulare 2

---

## G1 - STRUCTURA PROMPT VIDEO (t2v / i2v / v2v)

### BEST PRACTICE

**Formula universala validata (4 straturi):**
```
SUBIECT (detalii specifice)
+ ACTIUNE (miscare precisa)
+ CONTEXT (max 3-5 elemente: locatie, lumina, ora)
+ STIL (camera, mood, tip shot)
```

**T2V** - prompt lung 50-80 cuvinte, descriere completa scena + camera + lumina.
**I2V** - prompt scurt 20-40 cuvinte, DOAR instructiuni de miscare. Nu redescrie ce e deja in imagine.
**V2V** - upload referinta, extrage pattern miscare, aplica pe subiect nou (Motion Transfer Kling).

**Reguli anti-fail:**
- Adauga endpoint clar: "parul se misca in vant, apoi revine la loc" (nu lasa actiunea deschisa)
- I2V: clip 5 sec > 10 sec (mai putine erori)
- Specifica ce NU se misca: "fundalul ramane static, doar mana se misca"
- Termeni cinematografici functioneaza: "medium close-up", "dolly in", "rack focus", "tracking shot"

**Structura prompta testata (Kling 3.0):**
> "A [SUBJECT] [ACTION], shot as a [CAMERA MOVE], [LIGHTING], [SETTING]. [END STATE]."
> Exemplu: "A dentist's gloved hand places an implant into a jawbone model, shot as a slow push-in macro, warm clinical lighting, clean white surface. Hand retracts gently, leaving implant in place."

### DE TESTAT

- Sora 2 API (activ pana sep 2026) pentru T2V calitate cinematica inainte de shutdown complet
- Runway "Director Mode" pentru camera control separat de miscarea subiectului
- Generare in off-peak (noapte) reduce erorile de server la Kling

### RESPINS

- Prompturi vagi cu relatii spatiale ambigue ("langa", "in spatele") → distorsiuni
- Redescrierea imaginii in I2V → confuzie model, rezultate aleatorii
- Clipuri I2V > 10 sec ca prima incercare → rata fail ridicata

**Surse:**
- Artlist prompting tips (fara data exacta): https://help.artlist.io/hc/en-us/articles/31558164653213
- Medium Kristopher Dunham (2026): https://medium.com/@creativeaininja/how-to-actually-control-next-gen-video-ai-runway-kling-veo-and-sora-prompting-strategies-92ef0055658b
- Veed Kling guide (2026): https://www.veed.io/learn/kling-ai-prompting-guide

---

## G2 - CONSISTENTA PRODUS / PERSONAJ

### BEST PRACTICE

**Workflow standard 2026:**
1. Genereaza imagini REFERINTA mai intai (3-5 unghiuri: fata, 3/4, profil, close-up)
2. Foloseste I2V (image-to-video) nu T2V pentru consistenta
3. Limiteaza durata clipului per generare (mai scurt = mai consistent)
4. Multi-frame aware systems (Kling 3.0, Veo 3.1) mentin identitatea automat

**Rate consistenta atinsa:**
- Kling 3.0: ~95%+ consistenta pentru usecase standard (testat 5 clipuri acelasi personaj)
- Veo 3.1: cel mai bun la consistenta referinta → frame (testat cu imagini produs)

**Produs fizic (ex: cabinet dentar):**
- Fotografie unica produs → suita video in setari diferite posibila cu I2V
- Detalii fine (textura, culoare exacta) pastrate daca referinta e clara si mare

### DE TESTAT

- IP Adapter + Face-lock pentru personaj recurent in mai multe scenarii
- Kling 3.0 "story mode" pentru personaj consistent in 5+ clipuri scurte
- Veo 3.1 vs Kling 3.0 la consistenta brand (produs clinic, culori exacte)

### RESPINS

- T2V pur pentru personaje recurente → inconsistenta garantata
- Clipuri lungi (>10 sec) ca strategie principala → mai mult drift

**Surse:**
- Magic Hour blog (2026): https://magichour.ai/blog/how-to-keep-characters-consistent-in-ai-video
- RenderFire blog (2026): https://renderfire.com/blog/character-consistency-ai-generation
- PixVerse (fara data): https://pixverse.ai/en/blog/ai-video-generator-with-character-consistency

---

## G3 - CONTROL CAMERA / MISCARE

### BEST PRACTICE

**Kling 3.0 Motion Control** - #1 ELO benchmark, control camera precis:
- Accepta terminologie cinematica standard
- "dolly in", "tracking shot following from side", "rack focus", "handheld", "drone"
- 8/10 generari nimeresc camera la prima incercare cu termeni precisi
- Motion Transfer: upload video referinta → extrage miscare → aplica pe alt subiect (unic pe piata)

**Runway Gen-4.5 Director Mode:**
- Camera control independent de miscarea subiectului
- Motion Brush pentru scene complexe cu elemente la viteze diferite
- Optim pentru productie comerciala si advertising

**Termeni care functioneaza verificat:**
```
Camera: dolly in/out, pan left/right, tilt up/down, handheld shake,
        crane shot, drone/aerial, rack focus, push in, pull back,
        orbit around subject, locked/static

Miscare subiect: specify separately from camera
Endpoint: always add where motion ends
```

**Kling vs Runway pentru scene dentare multi-element (clarificat mai 2026):**
- Scene cu UN singur subiect (ex: instrument pe dinte) → Kling 3.0 (native 4K, audio nativ, camera control precis)
- Scene complexe cu 3+ elemente la viteze diferite (ex: dinte + instrument + mana + apa) → Runway Gen-4.5 Motion Brush (control per-pixel, cel mai granular din piata)

### DE TESTAT

- Kling Motion Transfer pe clip procedura dentara (extrage ritm miscare instrument chirurgical)
- Veo 3.1 physics simulation pentru lichide/fluide (relevanta pentru proceduri detartraj)
- WAN 2.7 R2V (reference-to-video) pentru miscare personaj din referinta

### RESPINS

- Prompturi fara specificare camera → model alege aleator
- Miscare subiect + miscare camera in aceeasi fraza → conflict, rezultat imprevizibil
- "complex scene" fara Motion Brush in Runway → artefacte

**Surse:**
- Wiro AI Kling v3 motion transfer test: https://wiro.ai/blog/kling-v3-motion-control-motion-transfer-in-3-tests/
- Atlabs Kling 3.0 prompt guide: https://www.atlabs.ai/blog/kling-3-0-prompting-guide-master-ai-video-generation
- MindStudio Kling 2.6 motion control: https://www.mindstudio.ai/blog/what-is-kling-2-6-pro-motion-control-video

---

## G4 - COST + DURATA PER MODEL

### BEST PRACTICE

**Tabel pret per secunda (API, mai 2026):**

| Model | Pret/sec | 10 sec clip | Durata max | Note |
|-------|----------|-------------|------------|------|
| WAN 2.7 (Alibaba) | $0.08-0.12 | ~$1.00 | 15 sec | #1 leaderboard mai 2026, T2V+I2V+R2V+edit |
| Kling 3.0 | $0.10 | $1.00 | 120 sec | Cel mai bun raport calitate/pret + durata |
| Seedance 2.0 | ~$0.05-0.09 | ~$0.90 | 15 sec | Best value, audio nativ |
| Sora 2 (API) | $0.10 base / $0.30-0.50 pro | $1-5 | ~25 sec | SHUTDOWN sep 2026 |
| Veo 3.1 Lite | $0.05-0.08 | ~$0.65 | - | NOU mai 2026, tier buget Veo |
| Veo 3.1 Fast | $0.15 | $1.50 | - | Rapid prototyping |
| Veo 3.1 Standard | $0.75 | $7.50 | - | 4K, best lip-sync |
| Gemini Omni Flash | TBD (~$0.05-0.08) | TBD | ~10 sec | Anuntat mai 2026, API inca nelive |
| Runway Gen-4.5 | ~$1.50/clip | $1.50 | - | Pro advertising, Motion Brush |

**Abonamente lunare:**
- Kling Standard: $10/mo (entry cel mai ieftin)
- Seedance 2.0: ~$9/mo (cel mai bun raport volum/calitate)
- Higgsfield Starter: $15/mo (200 cr) | Plus: $39/mo (1000 cr) | Ultra: $99/mo (3000 cr)
- Runway Standard: $12/mo (~62 clipuri de 10 sec)
- Runway Pro: $76/mo (volum mare, features avansate)
- Google AI Pro (Veo 3.1): $19.99/mo

**Recomandare i-vory Studio:**
- Prototipare rapida: Seedance 2.0 ($9/mo) sau Kling Standard ($10/mo)
- Best value API: WAN 2.7 ($0.08/sec, #1 leaderboard) sau Veo 3.1 Lite ($0.05-0.08/sec)
- Productie finala calitate: Veo 3.1 sau Kling 3.0 Pro
- EVITA Sora (shutdown progresiv 2026)
- Gemini Omni: asteapta lansarea API (proiectat: saptamanile urmatoare dupa mai 2026)

### DE TESTAT

- WAN 2.7 R2V (reference-to-video) pentru consistenta personaj - feature unic
- Generare batch in off-peak pentru cost efectiv la Kling
- Veo 3.1 Lite vs Veo 3.1 Fast: calitate vs cost la draft medical
- API direct vs abonament pentru volume lunare > 100 clipuri

### RESPINS

- Sora pentru proiecte noi (shutdown confirmat API sep 2026)
- Veo 3.1 Standard pentru draft/prototip (prea scump la $0.75/sec)
- Higgsfield pentru medical: nu e specializat, pret similar Kling fara avantaje clare

**Surse:**
- BuildMVPFast API pricing apr 2026: https://www.buildmvpfast.com/api-costs/ai-video
- LaoZhang cost guide 2026: https://blog.laozhang.ai/en/posts/how-much-does-ai-video-generator-cost
- Wan 2.7 API pricing mai 2026: https://moderndiplomacy.eu/2026/05/03/wan-2-7-text-to-video-api-balancing-high-fidelity-output-with-0-08-sec-efficiency/
- MindStudio Wan 2.7 features: https://www.mindstudio.ai/blog/wan-2-7-ai-video-model-features-release-timeline
- Higgsfield pricing 2026: https://higgsfield.ai/pricing
- Gemini Omni API pricing mai 2026: https://techsy.io/en/blog/gemini-omni-api-pricing

---

## G5 - DENTAL - Videoclipuri Anatomice (pentru Cezar)

### BEST PRACTICE

**Tipuri de continut care functioneaza deja (confirmat 2026):**

1. **Explainer procedura** - AI presenter explica procedura (voce + miscare), fara footage clinic real
   - Tool: Veo 3.1 (lip-sync <120ms, calitate top) sau Gemini Omni (anuntat mai 2026, excelent educational)
   - ATENTIE: Seedance 2.0 NU suporta romana (confirmat mai 2026: EN/ZH/JP/KO/ES/FR/DE/PT)
   - Use case: "Ce se intampla la detartraj", "Cum functioneaza implantul"

2. **Animatie macro procedura** - instrument + dinte/model anatomic, miscare lenta
   - Tool: Kling 3.0 I2V (fotografiezi modelul → animezi)
   - Prompt pattern: macro shot, slow push-in, warm clinical light, instrumente in miscare

3. **Marketing cabinet** - tur virtual, introducere echipa, "ce sa te astepti la prima vizita"
   - Tool: orice T2V (Seedance sau Kling)
   - Nu necesita acuratete anatomica stricta

4. **Social media scurt (Reels/TikTok)** - 5-8 sec, impact vizual, fara voce
   - Tool: Kling 3.0 sau Seedance 2.0
   - Format vertical nativ

**Workflow recomandat pentru anatomie dentara:**
```
1. Gaseste/fotografiezi model 3D sau macrofoto dinte/jaw
2. Genereaza imagine de referinta curata (fundal alb, iluminare clinica)
3. I2V cu prompt: "[instrument/fenomen] se misca lent pe [structura anatomica],
   macro shot, clinical white background, slow dolly in, [end state]"
4. Adauga voiceover separat (ElevenLabs sau similar)
5. Post-procesare minima in CapCut/Premiere
```

**Fenomene animate posibile cu AI video actual:**
- Carie: "bacteria [vizibila] erodeaza suprafata smaltului, time-lapse slow"
- Detartraj: "instrument ultrasonic vibrand indeparteaza tartru de pe dinte, water spray"
- Implant: "implant insurubat lent in os, cross-section view, clinical light"
- Inflamatie gingivala: "gingiva se inroseste progresiv, close-up macro"

**Gemini Omni pentru dental educational (NOU mai 2026):**
- Demo oficial: claymation proteina-folding explainer - exact tipul de continut anatomic vizat
- Puncte forte relevante: text rendering on-screen curat, blackboard equations, consistenta intre frame-uri
- Optim pentru: "ce e caria" cu elemente vizuale clare, diagrame animate, structuri anatomice stilizate
- Status: API nelive inca (anuntat mai 2026, urmatoarele saptamani)

**Kling castiga la anatomie in benchmark (confirmat mai 2026):**
- In testul Vidguru VEO 3.1 vs Kling v2.6, Kling castiga categoria "anatomy"
- Implicatie: pentru animatie macro structuri dentare, Kling poate depasi Veo la acuratete anatomica

### DE TESTAT

- Veo 3.1 physics pentru apa/spray (detartraj) → realismul fluidelor
- Kling Motion Transfer: inregistreaza miscarea mainii proprii cu instrument → aplica pe model anatomic
- Prompt cu "cross-section view dental anatomy" - cat de bine intelege modelele anatomice (Kling favorit)
- Gemini Omni (cand API devine live) pentru explainer dental stilizat

### RESPINS

- Generare directa T2V "show tooth decay process microscopically" → halucinatii anatomice garantate
- Footage clinic real ca I2V input fara consent pacient → risc GDPR + etic
- Asteptarea unui tool specializat medical → nu exista in 2026, cel mai bun e workflow I2V cu referinte proprii
- Seedance 2.0 pentru voiceover in romana → romana NU e inclusa in cele 8 limbi suportate

**Surse:**
- ZSky AI dental marketing blog: https://zsky.ai/blog/ai-video-for-dental-practices
- VideoAI.me healthcare 2026: https://videoai.me/blog/ai-video-healthcare-medical-practices-patient-education-2026
- VOKA dental animation portfolio: https://voka.io/our-medical-animation-video-portfolio/what-is-dental-caries-and-how-does-it-develop/
- Vidguru VEO 3.1 vs Kling v2.6 benchmark: https://www.vidguru.ai/blog/veo-3.1-vs-kling-v2.6-comparison-benchmark.html
- Gemini Omni Google I/O mai 2026: https://blog.google/innovation-and-ai/models-and-research/gemini-models/gemini-omni/
- Seedance audio limbi confirmate: https://www.cutout.pro/learn/blog-seedance-2-0-audio-guide/

---

## MODEL LANDSCAPE (mai 2026)

| Model | Puncte forte | Slab la |
|-------|-------------|---------|
| WAN 2.7 (Alibaba) | #1 leaderboard, T2V+I2V+R2V+edit, $0.08/sec | Durata max 15s |
| Kling 3.0 | Motion Control unic, anatomie benchmark, durata 120s | Uneori suprarealist |
| Veo 3.1 | Calitate vizuala top, lip-sync, physics | Scump la Standard |
| Veo 3.1 Lite | Budget Veo $0.05-0.08/sec | NOU, inca putin documentat |
| Gemini Omni | Educational/anatomical explainers, text curat | API nelive inca (mai 2026) |
| Seedance 2.0 | Raport calitate/pret, audio nativ 8 limbi | Romana NU inclusa, durata max 15s |
| Runway Gen-4.5 | Director Mode, Motion Brush per-pixel, commercial | Mai scump, fara audio nativ |
| Higgsfield | Creative marketing general | Nu e specializat, credit system opac |
| Sora 2 | - | SHUTDOWN progresiv, evita pentru proiecte noi |
