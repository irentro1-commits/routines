# VIDEO INTEL - i-vory Studio Research Base
> Ultima actualizare: 2026-05-28 | Rulare 2

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

**[NOU 2026-05-28] Kling O3 Multi-Shot Storyboard:**
- Pana la 6 shot-uri distincte intr-un clip de 15 sec
- Fiecare shot are propriul prompt, durata, unghi camera si miscare
- "AI Director" mode: interpreteaza instructiuni bazate pe script (shot-reverse-shot, cross-cutting)
- Arhitectura "Omni One" - acelasi motor pentru T2V, I2V si editare
- Sursa: GenAIntel (feb 2026), MindStudio, vidofy.ai

### DE TESTAT

- Runway "Director Mode" pentru camera control separat de miscarea subiectului
- Generare in off-peak (noapte) reduce erorile de server la Kling
- Kling O3 multi-shot storyboard pentru procedura dentara (implant in 4 shot-uri: preparatie → implant → sutura → radiografie)

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

**[NOU 2026-05-28] Wan 2.7 workflow alternativ pentru consistenta:**
- First frame + last frame control: definesti starea initiala SI finala a obiectului
- 9-grid multi-referinta: combini pana la 9 imagini referinta simultan
- Subject referencing: produs sau personaj de referinta in paralel cu scena
- Mai bun decat Seedance la scene multi-subiect; Seedance mai bun la subiect unic expresiv
- Open-weight (Alibaba) = potential self-hosted
- Sursa: MindStudio blog (mar 2026), Technology.org 25 mai 2026, LaoZhang AI Blog

### DE TESTAT

- IP Adapter + Face-lock pentru personaj recurent in mai multe scenarii
- Wan 2.7 first+last frame pt produs dentar: imagine produs curat → imagine dupa utilizare (tranzitie)
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

**[NOU 2026-05-28] Kling O3 "AI Director" camera blocking:**
- Script-based camera instructions: "shot 1: wide establishing, shot 2: close-up macro, shot 3: pull back reveal"
- Cross-cutting si shot-reverse-shot intelese nativ
- Wan 2.7: camera control avansat + first/last frame = control complet traiectorie

### DE TESTAT

- Kling O3 AI Director pentru procedura dentara multi-shot (script narativ)
- Runway Motion Brush pentru scene cu multiple elemente (ex: dinte + instrument + mana)
- Wan 2.7 first+last frame pentru animatii cu endpoint definit precis (implant: start=gol → end=implantat)
- Veo 3.1 physics simulation pentru lichide/fluide (relevanta pentru proceduri detartraj)

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

| Model | Pret/sec API | Abonament (lunar) | Durata max | Note |
|-------|-------------|-------------------|------------|------|
| Kling 3.0 (API direct) | $0.10 | - | 15 sec | - |
| Kling 3.0 via Higgsfield PLUS | ~$0.039/sec | $39/mo annual | 15 sec | 61% mai ieftin vs API direct |
| Kling 3.0 via Higgsfield ULTRA | ~$0.033/sec | $99/mo annual | 15 sec | Best value volum mare |
| Seedance 2.0 (API) | ~$0.05-0.09 | incl. Higgsfield | 15 sec | Best value overall |
| Wan 2.7 (open-weight) | gratuit (self-host) / API | - | 15 sec | NOU mar 2026, open source |
| Sora 2 (API) | $0.10-0.50 | - | ~25 sec | SHUTDOWN sep 2026 |
| Veo 3.1 Lite | sub $0.15 | - | 4/6/8 sec | NOU, budget batch |
| Veo 3.1 Fast | $0.15 | - | 4/6/8 sec | Rapid prototyping |
| Veo 3.1 Standard | $0.75 | $19.99/mo Google | 4/6/8 sec | 4K, best lip-sync |
| Runway Gen-4.5 | ~$1.50/clip | $12-76/mo | - | Pro advertising |

**[NOU 2026-05-28] Higgsfield - pricing real (verificat direct prin MCP):**
- PLUS: $49/mo sau **$39/mo annual** → 1000 credite = ~200 Kling 3.0 videos (5s/720p)
- ULTRA: $129/mo sau **$99/mo annual** → 3000 credite = ~500 Kling 3.0 videos
- Inclus in PLUS/ULTRA: Seedance 2.0 (Full Access), Kling 3.0, Wan 2.7, Veo 3.1, Veo 3.1 Lite, Grok Video (xAI), Cinema Studio Video 3.0 (proprietary SOTA)
- Cinema Studio Video 3.0: modelul propriu Higgsfield, tagat "best-quality/sota/film"
- Marketing Studio: one-click produs ads, TikTok/Reels ready, cu avatar + produs
- Concurenta: 6 videouri paralele (PLUS), 8 videouri paralele (ULTRA)
- Sursa: Higgsfield MCP API (verificat direct 28 mai 2026)

**[NOU 2026-05-28] Wan 2.7 (Alibaba, mar 2026):**
- Open-weight (~27B param, Diffusion Transformer + Flow Matching)
- Self-hosted = cost zero daca ai GPU (unic pe piata printre top modele)
- Durata: 2-15 sec, 720p/1080p
- Sursa: MindStudio blog, Technology.org 25 mai 2026

**Recomandare i-vory Studio [ACTUALIZAT]:**
- Prototipare rapida + volum: Higgsfield PLUS annual ($39/mo) → acces toate modelele
- Productie finala calitate: Veo 3.1 Standard sau Cinema Studio 3.0 (Higgsfield)
- EVITA Sora (shutdown progresiv 2026)
- INVESTIGHEAZA: Wan 2.7 self-hosted daca volum > 500 clipuri/luna

### DE TESTAT

- Higgsfield PLUS vs abonament direct Kling la calitate identica (sunt acelasi model?)
- Cinema Studio Video 3.0 (Higgsfield SOTA) la macro procedura clinica
- Wan 2.7 self-hosted pentru volum mare → cost efectiv?
- Veo 3.1 Lite pentru batch social media dentar (4/6/8 sec → ideal Reels)

### RESPINS

- Sora pentru proiecte noi (shutdown confirmat API sep 2026)
- Veo 3.1 Standard pentru draft/prototip (prea scump la $0.75/sec)
- API direct Kling cand Higgsfield ofera acelasi model la 61% mai ieftin

**Surse:**
- BuildMVPFast API pricing apr 2026: https://www.buildmvpfast.com/api-costs/ai-video
- LaoZhang cost guide 2026: https://blog.laozhang.ai/en/posts/how-much-does-ai-video-generator-cost
- Wan 2.7 vs Seedance (LaoZhang 2026): https://blog.laozhang.ai/en/posts/wan-2-7-vs-seedance-2-0
- Technology.org Wan 2.7 (25 mai 2026): https://www.technology.org/2026/05/25/wan-2-7-vs-wan-2-2-what-changed-in-alibaba-s-flagship-video-model/

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

**[NOU 2026-05-28] Romana in audio AI video - NEGATIV confirmat:**
- Seedance 2.0: limbi suportate EN/CN/JP/KR/ES/ID + dialecte chineze. Romana = ABSENT.
- Kling O3: EN/CN/JP/KR/ES. Romana = ABSENT.
- WORKAROUND: genereaza video fara audio → dubbing exterior cu ElevenLabs (romana suportata)
- Sursa: Seedance official site (seed.bytedance.com), Cutout.pro blog, GenAIntel feb 2026

**[NOU 2026-05-28] Wan 2.7 pentru tranzitii anatomice:**
- First frame = dinte sanatos / Last frame = dinte cu carie → animeaza procesul de degradare
- Prima data posibil nativ in orice model (anterior necesita multi-pass)
- Workflow: fotografie macro dinte sanatoase (input 1) + fotografie sau imagine AI dinte cariot (input 2) → Wan 2.7 I2V
- Sursa: MindStudio blog (mar 2026)

**[NOU 2026-05-28] Higgsfield Marketing Studio pentru social media dentar:**
- One-click product ads cu avatar + produs
- TikTok/Reels ready (format vertical nativ)
- Produs: poza periuta/pasta/implant → ad animat direct
- Potential pentru "inainte/dupa" detartraj cu avatar AI prezentator

### DE TESTAT

- Wan 2.7 first+last frame: dinte sanatoase → carie (tranzitie anatomica)
- Cinema Studio Video 3.0 (Higgsfield SOTA) pentru macro procedura clinica
- Veo 3.1 Lite pentru batch Reels dentare (4/6/8 sec, mai ieftin)
- Veo 3.1 physics pentru apa/spray detartraj
- Kling O3 multi-shot storyboard: procedura implant in 4 shot-uri narative
- Prompt "cross-section view dental anatomy" cu Kling O3 AI Director
- Higgsfield Marketing Studio: produs dentar (pasta/periuta) → ad animat

### RESPINS

- Seedance 2.0 / Kling O3 pentru audio in romana: CONFIRMAT NEGATIV
- Generare directa T2V "show tooth decay process microscopically" → halucinatii anatomice garantate
- Footage clinic real ca I2V input fara consent pacient → risc GDPR + etic
- Asteptarea unui tool specializat medical → nu exista in 2026, cel mai bun e workflow I2V cu referinte proprii

**Surse:**
- ZSky AI dental marketing blog: https://zsky.ai/blog/ai-video-for-dental-practices
- VideoAI.me healthcare 2026: https://videoai.me/blog/ai-video-healthcare-medical-practices-patient-education-2026
- VOKA dental animation portfolio: https://voka.io/our-medical-animation-video-portfolio/what-is-dental-caries-and-how-does-it-develop/

---

## MODEL LANDSCAPE (mai 2026) [ACTUALIZAT 2026-05-28]

| Model | Puncte forte | Slab la | Acces |
|-------|-------------|---------|-------|
| Kling 3.0 / O3 | Motion Control, AI Director 6-shot, 15s, 4K | Pret API ridicat direct | API, Higgsfield |
| Veo 3.1 Standard | Calitate vizuala top, lip-sync, physics | Scump ($0.75/sec) | Google AI Pro, Higgsfield |
| Veo 3.1 Lite | Ieftin, batch, 4/6/8s | Durata mica | Higgsfield |
| Seedance 2.0 | Consistenta identitate, multi-SKU, audio nativ | Romana audio absent | Higgsfield, ByteDance API |
| Wan 2.7 | First+last frame, open-weight, camera avansat | Mai nou, mai putin testat | Higgsfield, self-host |
| Cinema Studio 3.0 | SOTA Higgsfield, film-grade | Proprietary, doar pe Higgsfield | Higgsfield |
| Runway Gen-4.5 | Director Mode, Motion Brush, commercial | Scump, fara audio nativ | Runway.com |
| Minimax Hailuo 2.3 | Physics natural, emotii faciale, 1080p | Durate fixe (6/10s) | Higgsfield |
| Grok Imagine (xAI) | T2V + I2V, audio, pana 15s | Inca neacoperit in tests | Higgsfield |
| Sora 2 | - | SHUTDOWN progresiv, evita pentru proiecte noi | - |
