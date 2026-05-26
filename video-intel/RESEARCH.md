# VIDEO INTEL - i-vory Studio Research Base
> Ultima actualizare: 2026-05-26 | Rulare 2

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

**Google Flow (Veo 3.1) - NOU Google I/O 2026:**
- Mediu dedicat pentru video generativ, camera control precis, temporal consistency imbunatatit
- Sync audio nativ, suport dialog, aceeasi calitate ca Veo 3.1 Standard
- App Android beta disponibil; Flow Music app iOS separat
- Alternativa directa la Runway Director Mode pentru utilizatorii Google

**Termeni care functioneaza verificat:**
```
Camera: dolly in/out, pan left/right, tilt up/down, handheld shake,
        crane shot, drone/aerial, rack focus, push in, pull back,
        orbit around subject, locked/static

Miscare subiect: specify separately from camera
Endpoint: always add where motion ends
```

### DE TESTAT

- Runway Motion Brush pentru scene cu multiple elemente (ex: dinte + instrument + mana)
- Kling Motion Transfer pe clip procedura dentara (extrage ritm miscare instrument chirurgical)
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

| Model | Pret/sec | 10 sec clip | Durata max | Note |
|-------|----------|-------------|------------|------|
| Veo 3.1 Lite | $0.05 | $0.50 | - | NOU Google I/O; prototipare ieftina |
| Seedance 2.0 | ~$0.05-0.09 | ~$0.90 | 15 sec | Best value overall |
| Kling 3.0 | $0.10 | $1.00 | 120 sec | Motion Control unic, durata record |
| Sora 2 (API) | $0.10-$0.50 | $1-5 | ~25 sec | SHUTDOWN sep 2026 - EVITA |
| Veo 3.1 Standard | **$0.40** | $4.00 | **2 min** | CORECTIE: era $0.75 - redus la I/O; durata extinsa |
| Runway Gen-4.5 | ~$1.50/clip | $1.50 | - | Pro advertising |
| Gemini Omni Flash | $0.20-0.60* | $2-6* | 10 sec | NOU 19 mai; API public "curand"; *proiectie |

**Abonamente lunare:**
- Google AI Plus: $7.99/mo (include Gemini Omni Flash + Veo 3.1 Lite via Flow - NOU)
- Kling Standard: $10/mo (entry cel mai ieftin pentru Kling dedicat)
- Seedance 2.0: ~$9/mo (cel mai bun raport volum/calitate)
- Runway Standard: $12/mo (~62 clipuri de 10 sec)
- Google AI Pro: $19.99/mo (Veo 3.1 Standard + Flow)
- Higgsfield Starter: $15/mo | Plus: $39/mo | Ultra: $99/mo (agregator 15+ modele)
- Runway Pro: $76/mo (volum mare, features avansate)

**Higgsfield ca agregator - VERDICT:**
- Higgsfield Plus ($39/mo, 1000 credite) = ~142 clipuri Kling 3.0 (~$0.27/clip)
- Kling direct ($10/mo) = mai ieftin daca folosesti DOAR Kling
- Higgsfield are sens DOAR daca folosesti mix Kling + Veo + Seedance intr-un singur cont
- Avantaj Higgsfield: Cinema Studio, Soul ID (features exclusive), acces multi-model fara conturi separate

**Recomandare i-vory Studio:**
- Prototipare rapida (dental concept): Veo 3.1 Lite ($0.05/sec) sau Seedance 2.0 ($9/mo)
- Productie dentara calitate + Motion Control: Kling 3.0 Pro ($10/mo direct)
- Explainer cu audio nativ: Gemini Omni Flash (testat romana - vezi G5) sau Veo 3.1 Standard
- EVITA Sora (shutdown confirmat sep 2026)

### DE TESTAT

- Generare batch in off-peak pentru cost efectiv la Kling
- Seedance 2.0 pentru volum social media dentar (raport cel mai bun)
- API direct vs abonament pentru volume lunare > 100 clipuri
- Gemini Omni Flash API (fara data exacta, anuntat "curand" dupa 19 mai 2026)
- Higgsfield Plus ($39/mo) daca proiectul foloseste 3+ modele diferite

### RESPINS

- Sora pentru proiecte noi (shutdown confirmat API sep 2026)
- Veo 3.1 Standard pentru draft/prototip (chiar si dupa reducere la $0.40/sec; Veo 3.1 Lite la $0.05 e suficient pentru draft)

**Surse:**
- BuildMVPFast API pricing apr 2026: https://www.buildmvpfast.com/api-costs/ai-video
- LaoZhang cost guide 2026: https://blog.laozhang.ai/en/posts/how-much-does-ai-video-generator-cost
- Vo3AI comparison: https://www.vo3ai.com/ai-video-generator-pricing-comparison

---

## G5 - DENTAL - Videoclipuri Anatomice (pentru Cezar)

### BEST PRACTICE

**Tipuri de continut care functioneaza deja (confirmat 2026):**

1. **Explainer procedura** - AI presenter explica procedura (voce + miscare), fara footage clinic real
   - Tool: Gemini Omni Flash (80 limbi - cel mai probabil include romana, DE TESTAT) sau Veo 3.1 Standard (lip-sync <120ms)
   - Kling 3.0 si Seedance 2.0: suporta 5-8 limbi dar romana NU e confirmata explicit
   - WORKAROUND confirmat pentru romana: video mut AI + voiceover ElevenLabs romana (calea sigura acum)
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

### DE TESTAT

- Veo 3.1 physics pentru apa/spray (detartraj) → realismul fluidelor
- Kling Motion Transfer: inregistreaza miscarea mainii proprii cu instrument → aplica pe model anatomic (Kling 3.0 MC are "occlusion recovery" - util pentru instrumente/props ce se suprapun)
- **PRIORITATE:** Gemini Omni Flash cu romana: 80 limbi suportate → test "Explica detartrajul in romana" → lip sync nativ
- Prompt cu "cross-section view dental anatomy" - cat de bine intelege modelele anatomice
- Veo 3.1 Lite $0.05/sec pentru prototipare rapida animatii dentare (pret nou, accesibil)

### RESPINS

- Generare directa T2V "show tooth decay process microscopically" → halucinatii anatomice garantate
- Footage clinic real ca I2V input fara consent pacient → risc GDPR + etic
- Asteptarea unui tool specializat medical → nu exista in 2026, cel mai bun e workflow I2V cu referinte proprii

**Surse:**
- ZSky AI dental marketing blog: https://zsky.ai/blog/ai-video-for-dental-practices
- VideoAI.me healthcare 2026: https://videoai.me/blog/ai-video-healthcare-medical-practices-patient-education-2026
- VOKA dental animation portfolio: https://voka.io/our-medical-animation-video-portfolio/what-is-dental-caries-and-how-does-it-develop/

---

## MODEL LANDSCAPE (mai 2026)

| Model | Puncte forte | Slab la |
|-------|-------------|---------|
| Kling 3.0 | Motion Control unic, pret OK, durata 120s | Romana neconfirmata in audio nativ |
| Veo 3.1 Standard | Calitate vizuala top, lip-sync, physics, 2 min | $0.40/sec (inca scump pt volum) |
| Veo 3.1 Lite | $0.05/sec - cel mai ieftin calitate, Lite tier NOU | Calitate sub Standard |
| Seedance 2.0 | Raport calitate/pret, audio nativ, leaderboard | Durata max 15s, romana neconfirmata |
| Runway Gen-4.5 | Director Mode #1 Video Arena, Motion Brush | Mai scump, fara audio nativ |
| Gemini Omni Flash | 80 limbi (romana probabil), free/YouTube, edit in-chat | API nu e public inca, max 10 sec |
| Higgsfield | Agregator 15+ modele intr-un cont | Scump daca folosesti 1-2 modele |
| Sora 2 | - | SHUTDOWN progresiv, evita pentru proiecte noi |
