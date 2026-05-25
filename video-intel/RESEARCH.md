# VIDEO INTEL - i-vory Studio Research Base
> Ultima actualizare: 2026-05-25 | Rulare #2

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

**WAN 2.7 (Alibaba, open source, #1 leaderboard mai 2026) - NOU:**
- First+Last frame control: definesti exact primul si ultimul cadru, modelul genereaza tranzitia
- V2V editing cu instructiuni text: "schimba fundalul", "modifica culoarea obiectului"
- Multi-image input: 9 imagini simultan in grid
- UTIL pentru dental: definesti start (dinte intact) si end (implant montat), generezi animatia procedurii
- Sursa: MindStudio WAN 2.7 guide (2026): https://www.mindstudio.ai/blog/wan-2-7-ai-video-model-features-release-timeline

### DE TESTAT

- WAN 2.7 first+last frame pentru animatie procedura dentara (start=dinte intact, end=dinte tratat)
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

**Runway Gen-4.5 vs Kling 3.0 - CLARIFICAT (mai 2026):**
- Runway Gen-4.5: #1 Artificial Analysis leaderboard (Elo 1247), fizica lichide/materie superioara
  → OPTIM pentru: detartraj (spray apa), fluide, textile, miscare organica
  → MINUS: audio nu e nativ, se adauga in post; 30-90 sec generare per 10 sec clip
- Kling 3.0: audio nativ integrat (EN/ZH/JA/KO/ES), 4K nativ, cost mai mic
  → OPTIM pentru: tot ce nu necesita fizica lichide; workflow rapid complet (video+audio intr-o generare)
- CONCLUZIE: Runway pentru detartraj/proceduri cu spray, Kling pentru tot restul

**Kling Motion Control 3.0 - UPDATE occlusion recovery:**
- Skeletal anchoring: miscare ancorata pe schelet, nu deriva
- Occlusion recovery: cand mana acopera instrumentul sau fata, modelul reconstituie logic miscarea
  → DIRECT UTIL pentru dental: scena mana + instrument + dinte → nu mai pierde coerenta
- Motion Transfer: clipuri pana la 30 sec continuu (vs 15 sec anterior)
- Sursa: BananaProAI Motion Control guide 2026: https://bananaproai.com/blog/kling-motion-control-complete-guide-2026-transfer-real-motion-to-ai-characters-in-seconds/

### DE TESTAT

- WAN 2.7 first+last frame pe procedura dentara (start=dinte intact, end=implant montat)
- Runway Motion Brush pentru scene cu multiple elemente (ex: dinte + instrument + mana)
- Kling Motion Transfer cu occlusion recovery pe instrument chirurgical in mana

### RESPINS

- Prompturi fara specificare camera → model alege aleator
- Miscare subiect + miscare camera in aceeasi fraza → conflict, rezultat imprevizibil
- "complex scene" fara Motion Brush in Runway → artefacte

**Surse:**
- Wiro AI Kling v3 motion transfer test: https://wiro.ai/blog/kling-v3-motion-control-motion-transfer-in-3-tests/
- Atlabs Kling 3.0 prompt guide: https://www.atlabs.ai/blog/kling-3-0-prompting-guide-master-ai-video-generation
- MindStudio Kling 2.6 motion control: https://www.mindstudio.ai/blog/what-is-kling-2-6-pro-motion-control-video
- AtlasCloud Runway vs Kling (2026): https://www.atlascloud.ai/blog/guides/runway-gen-4-vs-kling-3-0-which-image-to-video-ai-wins-for-professional-filmmaking
- BananaProAI Motion Control 2026: https://bananaproai.com/blog/kling-motion-control-complete-guide-2026-transfer-real-motion-to-ai-characters-in-seconds/

---

## G4 - COST + DURATA PER MODEL

### BEST PRACTICE

**Tabel pret per secunda (API, mai 2026):**

| Model | Pret/sec | 10 sec clip | Durata max | Note |
|-------|----------|-------------|------------|------|
| Kling 3.0 | $0.10 | $1.00 | 120 sec | Cel mai bun raport calitate/pret |
| Seedance 2.0 | ~$0.05-0.09 | ~$0.90 | 15 sec | Best value overall |
| Sora 2 (API) | $0.10 base / $0.30-0.50 pro | $1-5 | ~25 sec | SHUTDOWN sep 2026 |
| Veo 3.1 Fast | $0.15 | $1.50 | - | Rapid prototyping |
| Veo 3.1 Standard | $0.75 | $7.50 | - | 4K, best lip-sync |
| Runway Gen-4.5 | ~$1.50/clip | $1.50 | - | Pro advertising |

**Abonamente lunare:**
- Kling Standard: $10/mo (entry cel mai ieftin, acces nelimitat Kling direct)
- Seedance 2.0: ~$9/mo (cel mai bun raport volum/calitate)
- Runway Standard: $12/mo (~62 clipuri de 10 sec)
- Runway Pro: $76/mo (volum mare, features avansate)
- Google AI Pro (Veo 3.1): $19.99/mo

**Higgsfield - ADAUGAT (mai 2026) - agregator 15+ modele:**

| Plan | Pret/mo (anual) | Credite/mo | Kling 3.0 videos | Veo 3.1 videos |
|------|-----------------|------------|-----------------|----------------|
| Starter | $15 | 200 | ~33 | ~4 |
| Plus | $39 | 1.000 | ~142 | ~20 |
| Ultra | $99 | 3.000 | ~428 | ~51 |

- Kling 3.0 pe Higgsfield: ~6 credite/video
- Sora 2 / Veo 3.1 pe Higgsfield: 40-70 credite/video
- Extra credite: $5 per 100 credite (expira in 90 zile)

**VERDICT Higgsfield vs direct:**
- Higgsfield ARE SENS daca folosesti MIX de modele (Veo + Kling + Seedance) sub un cont
- Higgsfield NU ARE SENS daca folosesti DOAR Kling ($10/mo direct = nelimitat vs $15/mo = 33 videos)
- Pentru i-vory Studio: Higgsfield Plus ($39) = 142 Kling + 120 Seedance + 20 Veo intr-un singur abonament

**Recomandare i-vory Studio (actualizata):**
- Prototipare rapida: Kling Standard ($10/mo direct)
- Mix productie: Higgsfield Plus ($39/mo) = acces multi-model
- Productie finala calitate: Veo 3.1 Standard sau Kling 3.0 Pro
- EVITA Sora (shutdown progresiv 2026)

**Nota WAN 2.7:** open source, rulat local = cost 0 daca ai GPU; fara abonament comercial simplu deocamdata.

### DE TESTAT

- Higgsfield Plus ($39/mo) vs abonamente separate pentru mix de modele
- WAN 2.7 local pentru volum mare fara cost per generare
- API direct vs abonament pentru volume lunare > 100 clipuri

### RESPINS

- Sora pentru proiecte noi (shutdown confirmat API sep 2026)
- Veo 3.1 Standard pentru draft/prototip (prea scump la $0.75/sec)
- Higgsfield Starter ($15/mo) pentru Kling-only (mai scump si limitat vs $10/mo direct)

**Surse:**
- BuildMVPFast API pricing apr 2026: https://www.buildmvpfast.com/api-costs/ai-video
- LaoZhang cost guide 2026: https://blog.laozhang.ai/en/posts/how-much-does-ai-video-generator-cost
- Vo3AI comparison: https://www.vo3ai.com/ai-video-generator-pricing-comparison
- Higgsfield pricing oficial (2026): https://higgsfield.ai/pricing
- Imagine.art Higgsfield pricing breakdown: https://www.imagine.art/blogs/higgsfield-ai-pricing

---

## G5 - DENTAL - Videoclipuri Anatomice (pentru Cezar)

### BEST PRACTICE

**Tipuri de continut care functioneaza deja (confirmat 2026):**

1. **Explainer procedura** - AI presenter explica procedura (voce + miscare), fara footage clinic real
   - Tool: Seedance 2.0 (audio nativ sync) sau Veo 3.1 (lip-sync <120ms)
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

**CLARIFICAT (mai 2026) - Romana nu e suportata nativ in niciun model major:**
- Seedance 2.0 audio nativ: EN, ZH, JA, KO + dialecte chineze. ROMANA = NU
- Kling 3.0 (O3) audio nativ: EN, ZH, JA, KO, ES. ROMANA = NU
- Veo 3.1: cel mai bun in EN; alte limbi prin prompt ("speak Romanian"), acuratete neconfirmata
- CONCLUZIE: pentru explainere in romana → ElevenLabs Multilingual v2 + video fara audio → mixaj post
- Sursa: AtlasCloud native audio comparison 2026: https://www.atlascloud.ai/blog/guides/ai-video-models-native-audio-compared

**Workflow recomandat pentru anatomie dentara (actualizat):**
```
1. Fotografiezi model 3D sau macrofoto dinte/jaw
2. Genereaza imagine de referinta curata (fundal alb, iluminare clinica)
VARIANTA A (I2V clasic - Kling 3.0):
3. I2V cu prompt: "[instrument/fenomen] se misca lent pe [structura anatomica],
   macro shot, clinical white background, slow dolly in, [end state]"
VARIANTA B (WAN 2.7 first+last frame - NOU):
3. Definesti frame_start = dinte intact + frame_end = dinte tratat
4. WAN 2.7 genereaza tranzitia (animatia procedurii)
5. Adauga voiceover separat (ElevenLabs Multilingual v2 pentru romana)
6. Post-procesare minima in CapCut/Premiere
```

**Fenomene animate posibile cu AI video actual:**
- Carie: "bacteria [vizibila] erodeaza suprafata smaltului, time-lapse slow"
- Detartraj: "instrument ultrasonic vibrand indeparteaza tartru de pe dinte, water spray"
- Implant: "implant insurubat lent in os, cross-section view, clinical light"
- Inflamatie gingivala: "gingiva se inroseste progresiv, close-up macro"

### DE TESTAT

- WAN 2.7 first+last frame: frame_start=dinte intact → frame_end=implant montat (testa tranzitia)
- Runway Motion Brush pentru detartraj (spray apa + instrument + dinte = 3 elemente viteze diferite)
- Kling Motion Transfer cu occlusion recovery pe instrument chirurgical
- Prompt cu "cross-section view dental anatomy" - cat de bine intelege modelele anatomice (neconfirmat)

### RESPINS

- Seedance 2.0 / Kling O3 audio pentru romana → nu e suportata, pierzi timp
- Generare directa T2V "show tooth decay process microscopically" → halucinatii anatomice garantate
- Footage clinic real ca I2V input fara consent pacient → risc GDPR + etic
- Asteptarea unui tool specializat medical → nu exista in 2026, cel mai bun e workflow I2V cu referinte proprii

**Surse:**
- ZSky AI dental marketing blog: https://zsky.ai/blog/ai-video-for-dental-practices
- VideoAI.me healthcare 2026: https://videoai.me/blog/ai-video-healthcare-medical-practices-patient-education-2026
- VOKA dental animation portfolio: https://voka.io/our-medical-animation-video-portfolio/what-is-dental-caries-and-how-does-it-develop/

---

## MODEL LANDSCAPE (actualizat mai 2026)

| Model | Puncte forte | Slab la | Audio nativ (romana) |
|-------|-------------|---------|---------------------|
| Kling 3.0 / O3 | Motion Control + occlusion recovery, 4K, durata 120s, pret OK | Uneori suprarealist | EN/ZH/JA/KO/ES (NU ROM) |
| WAN 2.7 | #1 leaderboard, first+last frame, V2V edit, open source | Fara API comercial simplu | EN+altele |
| Veo 3.1 | Calitate vizuala top, fizica lichide, lip-sync | Scump la Standard | EN best, rest prin prompt |
| Runway Gen-4.5 | #1 Artificial Analysis Elo, fizica lichide superioare, Director Mode | Fara audio nativ, generare lenta | NU (post-productie) |
| Seedance 2.0 | Raport calitate/pret, audio nativ, multi-frame | Durata max 15s | EN/ZH/JA/KO (NU ROM) |
| Sora 2 | - | SHUTDOWN progresiv, evita pentru proiecte noi | N/A |

**NOTA ROMANA:** Niciun model major nu genereaza audio in romana nativ (mai 2026).
→ Solutie validata: ElevenLabs Multilingual v2 + video muted → sync manual sau auto in CapCut/Premiere.
