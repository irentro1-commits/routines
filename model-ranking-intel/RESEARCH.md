# MODEL RANKING INTEL — i-vory Studio
> Doar generare IMAGINE + VIDEO. Actualizat incremental.
> Ultima actualizare: 2026-05-22

---

## G1: #1 MODEL GENERARE IMAGINE

**VERDICT: GPT Image 2 (high) — #1 cu marja record**

### Clasament text-to-image (Artificial Analysis Arena)
Metodologie: Elo din voturi umane oarbe, comparatii head-to-head fara stire de model.
Date benchmark: Mai 2026 | Sursa: https://artificialanalysis.ai/image/leaderboard/text-to-image

| Rank | Model | Elo (AA) | Elo (Arena.ai) | Disponibil |
|------|-------|----------|----------------|------------|
| 1 | GPT Image 2 (high) | 1339 | 1512 (preliminar) | OpenAI API, ChatGPT |
| 2 | GPT Image 1.5 (high) | 1265 | — | OpenAI API |
| 3 | Nano Banana 2 = Gemini 3.1 Flash Image Preview | 1263 | 1270 | Google AI Studio |
| 4 | Nano Banana Pro = Gemini 3 Pro Image | 1220 | — | Google AI Studio |
| 5 | FLUX.2 [max] | 1196 | — | fal.ai, Replicate |
| 6* | HiDream-O1-Image-Dev-2604 | 1185 | — | open-weight |
| 7* | FLUX.2 [dev] Turbo | 1160 | — | fal.ai |

*open-weight

### Note critice
- **Marja GPT Image 2**: +74 Elo fata de #2 pe AA; +242 pe Arena.ai (4.5M voturi) = cea mai mare marja din istoria leaderboard-ului
- **GPT Image 2 lansat**: 21 aprilie 2026
- **Scor Arena.ai marcat "Preliminary"** la momentul primei capturi (15k voturi vs 95k+ pentru GPT Image 1.5) — suficient de mare incat pozitia sa fie stabila
- **FLUX.2 [max]**: cel mai bun model open-weight proprietar; FLUX.2 [dev] = cel mai bun open-weight gratuit (Elo 1158)
- **Imagen 4 Ultra** (Google DeepMind): citat de surse ca "cel mai fotorealist API public" — nu apare in top 5 AA la data capturii; de urmarit

### Surse credibile utilizate
- Artificial Analysis Image Arena (Elo blind votes): https://artificialanalysis.ai/image/leaderboard/text-to-image
- Arena.ai Text-to-Image Leaderboard (4.5M voturi): https://arena.ai/leaderboard/text-to-image
- Arena.ai anunt oficial GPT Image 2: https://x.com/arena/status/2046670703311884548

---

## G2: #1 MODEL GENERARE VIDEO

**VERDICT: HappyHorse-1.0 (Alibaba) — #1 fara audio; Seedance 2.0 (ByteDance) — #1 cu audio**

### Clasament text-to-video (Artificial Analysis Video Arena)
Metodologie: Elo din voturi umane oarbe. Leaderboard split: cu audio / fara audio.
Date benchmark: Aprilie–Mai 2026 | Sursa: https://artificialanalysis.ai/video/leaderboard/text-to-video

#### FARA AUDIO (text-to-video)
| Rank | Model | Elo (AA) | Disponibil |
|------|-------|----------|------------|
| 1 | HappyHorse-1.0 | ~1332–1357 | fal.ai, Alibaba Cloud Bailian |
| 2 | Dreamina Seedance 2.0 720p | 1273 | CapCut, API (Segmind etc.) |
| 3 | Kling 3.0 1080p (Pro) | 1250 | kling.ai API |
| 4 | grok-imagine-video | 1233 | xAI API |
| 5 | Kling 3.0 Omni 1080p (Pro) | 1232 | kling.ai API |

#### CU AUDIO (text-to-video cu generare audio sincrona)
| Rank | Model | Elo (AA) | Disponibil |
|------|-------|----------|------------|
| 1 | Dreamina Seedance 2.0 720p | 1211 | CapCut, API |
| 1= | HappyHorse-1.0 | 1211 | fal.ai (din 27 apr 2026) |
| 3 | Kling 3.0 Omni 1080p (Pro) | 1099 | kling.ai API |
| 4 | Veo 3.1 | 1095 | Google API |
| 5 | Kling 3.0 1080p (Pro) | 1093 | kling.ai API |

### Note critice
- **HappyHorse-1.0**: model Alibaba (Taotian Future Life Lab), 15B parametri, transformer unificat text+imagine+video+audio intr-un singur forward pass; lansat in Arena la 7 aprilie 2026; API disponibil via fal.ai din 27 aprilie 2026
- **ATENTIE HappyHorse**: sursa https://help.apiyi.com/en/happyhorse-model-mystery-ai-video-lmarena-analysis-en.html raporteaza ca modelul "a disparut misterios din Arena si a reaparat" — disponibilitate API poate fi instabila; de monitorizat
- **Seedance 2.0**: ByteDance, lansat 9 februarie 2026; accepta pana la 9 imagini + 3 clipuri video + 3 fisiere audio per generare (multimodal reference); cel mai bun pentru control de referinte
- **Kling 3.0**: Kuaishou; cel mai bun model pentru scene cu mai multe personaje
- **Scor Elo HappyHorse variabil**: ~1332 (captura mai recenta cu marja 59p fata de Seedance) vs 1357 in alt tabel — valori capturate la date diferite, tendinta ascendenta confirmata
- **Standard profesional 2026**: rutare multi-model per tip de shot — niciun model nu domina toate dimensiunile

### Surse credibile utilizate
- Artificial Analysis Video Arena: https://artificialanalysis.ai/video/leaderboard/text-to-video
- LLM Stats Video Leaderboard (human blind votes): https://llm-stats.com/leaderboards/best-ai-for-video-generation
- HappyHorse fal.ai PR oficial: https://www.prnewswire.com/news-releases/302755003.html
- Seedance 2.0 review cu metodologie: https://aimlapi.com/blog/seedance-2-0-vs-seedance-1-5-pro---bytedances-breakthrough-multimodal-ai-video-models-2026

---

## G4: MODELE NOI APARUTE (10%)

| Model | Tip | Data aparitie | Nota |
|-------|-----|---------------|------|
| GPT Image 2 | Imagine | 21 apr 2026 | Domina imediat ambele leaderboarduri |
| HappyHorse-1.0 | Video | 7 apr 2026 (Arena); API 27 apr | Alibaba; disponibilitate de urmarit |
| Kling 3.0 Omni | Video | ~mar 2026 | Adauga generare audio nativa vs Kling 3.0 standard |
| Veo 3.1 | Video | ~apr 2026 | Google; #4 cu audio |
| MAI-Image-2 | Imagine | ~apr 2026 | Microsoft; intrat in top tier (pozitie exacta neclara) |
| Midjourney V8 Alpha | Imagine | ~apr 2026 | Alpha — benchmark definitiv lipsa |

---

## METODOLOGIE & FIABILITATE SURSE

**CREDIBIL (folosit in clasament):**
- Artificial Analysis Arena — Elo din comparatii oarbe, mii-zeci de mii voturi, metodologie publica
- Arena.ai — 4.5M voturi, metodologie identica; independent de furnizori

**SLAB / EXCLUS:**
- Listicle SEO fara metodologie (usefulai.com, imini.com etc.) — excluse
- Materiale de marketing proprii ale modelelor — excluse
- Orice clasament fara sursa de date si data benchmark-ului — excluse
# Model Ranking Intel — i-vory Studio
**Ultima actualizare:** 2026-05-22
**Scopul:** doar generare IMAGINE + VIDEO. Nu LLM, nu audio.

---

## IMAGINE — Clasament curent

**Sursa primara:** Artificial Analysis Text-to-Image Arena
URL: https://artificialanalysis.ai/image/leaderboard/text-to-image
Metodologie: blind head-to-head voting (utilizatori compara 2 imagini din acelasi prompt fara sa stie ce model le-a generat); scor Elo.
Nr. voturi: ~4.5M cross-platform (Arena.ai) / subset independent Artificial Analysis.
Data benchmark: actualizat continuu, date extrase 2026-05-22.

| Pozitie | Model | Elo (AA Arena) | Disponibilitate | Note |
|---------|-------|---------------|-----------------|------|
| #1 | GPT Image 2 (high) | 1339 | API OpenAI (platit) | Lider curent clar |
| #2 | GPT Image 1.5 (high) | 1265 | API OpenAI (platit) | Acelasi provider |
| #3 | Nano Banana 2 (Gemini 3.1 Flash Image Preview) | 1263 | Google AI Studio / Vertex | La 2 Elo de #2 |
| #4 | Nano Banana Pro (Gemini 3 Pro Image) | 1220 | Google AI Studio / Vertex | |
| #5 | FLUX.2 [max] | 1196 | API platit (BFL/parteneri) | Top open-weight comercial |
| — | HiDream-O1-Image-Dev-2604 | 1185 | HuggingFace / open-weight | **#1 open-weight gratuit** |
| — | FLUX.2 [dev] Turbo | 1160 | open-weight | |
| — | FLUX.2 [dev] | 1158 | open-weight | |

**VERDICT G1:** #1 imagine = **GPT Image 2 (high), Elo 1339** (Artificial Analysis Arena, 2026-05-22).
Benchmark credibil (blind voting, sursa independenta).

**Note importante:**
- Arena.ai (pool mai mare de voturi) poate arata o ordine usor diferita intre pozitiile #2-#3.
- Microsoft MAI-Image-2 (lansat 19 mar 2026) debuta la #3 pe Arena.ai ca familie — nu apare inca in top 5 AA Arena cu Elo individual publicat.
- Midjourney V8 Alpha lansat cu 2K nativ; Elo arena inca necuantificat la data extractiei.

---

## VIDEO — Clasament curent

**Sursa primara:** Artificial Analysis Text-to-Video Arena
URL: https://artificialanalysis.ai/video/leaderboard/text-to-video
Metodologie: Elo din blind comparisons, utilizatori compara 2 video-uri fara sa stie modelul; categorii separate fara audio si cu audio.
Data benchmark: actualizat continuu, date extrase 2026-05-22.

### Fara audio (text-to-video pur)

| Pozitie | Model | Elo | Disponibilitate | Note |
|---------|-------|-----|-----------------|------|
| #1* | HappyHorse-1.0 (Alibaba) | 1357 | **INCERT** — aparut in arena apr 2026, disparut din acces public | Elo cel mai mare dar nu accesibil public stabil |
| #2 | Dreamina Seedance 2.0 720p | 1273 | Runway API (din 17 apr 2026); API parteneri | **#1 practic accesibil** |
| #3 | Kling 3.0 1080p Pro | 1250 | Kling API / platit | |
| #4 | grok-imagine-video | 1233 | xAI API (deschis apr 2026) | |
| #5 | Kling 3.0 Omni 1080p Pro | 1232 | Kling API / platit | |
| — | LTX-2 Pro | 1134 | open-weight | **#1 open-weight** |
| — | LTX-2 Fast | 1130 | open-weight | |

### Cu audio (text-to-video + audio nativ)

| Pozitie | Model | Elo | Note |
|---------|-------|-----|------|
| #1 | Dreamina Seedance 2.0 720p | 1211 | egal cu HappyHorse la aceasta categorie |
| #1 | HappyHorse-1.0 | 1211 | disponibilitate incerta |
| #3 | Kling 3.0 Omni 1080p Pro | 1099 | |
| #4 | Veo 3.1 | 1095 | Google, acces limitat |

**VERDICT G2:** #1 video practic accesibil = **Dreamina Seedance 2.0, Elo 1273** (fara audio) / 1211 (cu audio).
HappyHorse-1.0 tehnic #1 cu Elo 1357 dar disponibilitate publica nestabila — raportat ca a disparut din acces public dupa aparitia in arena.
Sursa: artificialanalysis.ai + llm-stats.com, metodologie Elo blind.

**Sursa secundara (cross-check video):** llm-stats.com/leaderboards/best-ai-for-video-generation
Metodologie alternativa: TrueSkill (μ − 3σ), 186 voturi blind (mai mic ca pool).
Top acolo: LTX-2 Fast (2358 TrueSkill) — diferenta mare fata de AA Arena; posibil sa masoare altceva sau pool prea mic. Benchmark SLAB pentru validare singura.

---

## Modele noi notabile (ultimele 30-60 zile) — G4

| Model | Tip | Data lansare | Note |
|-------|-----|-------------|------|
| GPT Image 2 | Imagine | ~apr-mai 2026 | Noul lider pe AA Arena |
| Krea 2 | Video | 12 mai 2026 | Primul model foundation propriu Krea; #2 pe Contra Labs style-transfer benchmark |
| MAI-Image-2 (Microsoft) | Imagine | 19 mar 2026 | Tinteste fotorealism + text rendering |
| Seedance 2.0 (ByteDance/Dreamina) | Video | API 17 apr 2026 | Disponibil prin Runway + parteneri; exclus SUA direct din cauza IP |
| Kling 3.0 | Video | mar-apr 2026 | Urcat in top 3 video |
| Grok Imagine API (xAI) | Imagine + Video | apr 2026 | $0.02/imagine; video = grok-imagine-video in top 5 |
| HiDream-O1-Image-Dev-2604 | Imagine | apr 2026 | #1 open-weight imagine pe AA Arena |
| OpenAI Sora | Video | — | Consumer app inchis 26 apr 2026; API continua pana sep 2026 |

---

## Surse folosite la aceasta rulare

- https://artificialanalysis.ai/image/leaderboard/text-to-image — AA Image Arena Elo
- https://artificialanalysis.ai/video/leaderboard/text-to-video — AA Video Arena Elo
- https://arena.ai/leaderboard/text-to-image — Arena.ai T2I (pool mai mare)
- https://llm-stats.com/leaderboards/best-ai-for-video-generation — video TrueSkill (pool mic)
- https://awesomeagents.ai/capabilities/image-generation/ — imagine apr 2026
- https://awesomeagents.ai/leaderboards/video-generation-benchmarks-leaderboard/ — video 2026
- https://help.apiyi.com/en/happyhorse-model-mystery-ai-video-lmarena-analysis-en.html — analiza HappyHorse
