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
