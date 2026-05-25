# MODEL RANKING INTEL — i-vory Studio
> Doar generare IMAGINE + VIDEO. Actualizat incremental.
> Ultima actualizare: 2026-05-25

---

## G1: #1 MODEL GENERARE IMAGINE

**VERDICT: GPT Image 2 (high) — #1 cu marja record (neschimbat)**

### Clasament text-to-image (Artificial Analysis Arena)
Metodologie: Elo din voturi umane oarbe, comparatii head-to-head fara stire de model.
Date benchmark: Mai 2026 | Sursa: https://artificialanalysis.ai/image/leaderboard/text-to-image

| Rank | Model | Elo (AA) | Disponibil |
|------|-------|----------|------------|
| 1 | GPT Image 2 (high) | 1339 | OpenAI API, ChatGPT |
| 2 | GPT Image 1.5 (high) | 1266 | OpenAI API |
| 3 | Nano Banana 2 = Gemini 3.1 Flash Image Preview | 1264 | Google AI Studio |
| 4 | Nano Banana Pro = Gemini 3 Pro Image | 1220 | Google AI Studio |
| **5** | **grok-imagine-image-quality** | **1210** | **xAI API ($0.02/img)** |
| 6 | FLUX.2 [max] | ~1196 | fal.ai, Replicate |
| 7* | HiDream-O1-Image-Dev-2604 | 1185 | open-weight |
| 8* | FLUX.2 [dev] Turbo | 1160 | fal.ai |

*open-weight

### Note critice
- **DELTA 2026-05-25**: grok-imagine-image-quality (Elo 1210) a urcat la #5, impingand FLUX.2 [max] (1196) pe pozitia 6.
- **GPT Image 2 neschimbat**: Elo 1339, marja +74 fata de #2 — pozitie stabila.
- **Arena.ai** (pool mai mare ~4.5M voturi): GPT Image 2 la 1512 (preliminar); top 5 consistent cu AA.
- **grok-imagine-image-quality** = modul "Quality" al xAI Grok Imagine API, disponibil din ~apr 2026.
- **Midjourney V8 Alpha**: inca fara Elo arena publicat.
- **Imagen 4 Ultra** (Google): citat ca "cel mai fotorealist API" dar fara Elo independent confirmat.

### Surse credibile utilizate
- Artificial Analysis Image Arena (Elo blind votes): https://artificialanalysis.ai/image/leaderboard/text-to-image
- Arena.ai Text-to-Image Leaderboard: https://arena.ai/leaderboard/text-to-image
- xAI Grok Imagine Quality Mode: https://x.ai/news/grok-imagine-quality-mode

---

## G2: #1 MODEL GENERARE VIDEO

**VERDICT: HappyHorse-1.0 (Alibaba) — #1 fara audio; Seedance 2.0 (ByteDance) — #1 cu audio (solo)**

### Clasament text-to-video (Artificial Analysis Video Arena)
Metodologie: Elo din voturi umane oarbe. Leaderboard split: cu audio / fara audio.
Date benchmark: Mai 2026 | Sursa: https://artificialanalysis.ai/video/leaderboard/text-to-video

#### FARA AUDIO (text-to-video)
| Rank | Model | Elo (AA) | Disponibil |
|------|-------|----------|------------|
| 1 | HappyHorse-1.0 | 1357 | fal.ai, Alibaba Cloud Bailian |
| 2 | Dreamina Seedance 2.0 720p | 1273 | CapCut, API (Segmind etc.) |
| 3 | Kling 3.0 1080p (Pro) | 1250 | kling.ai API |
| 4 | grok-imagine-video | 1233 | xAI API |
| 5 | Kling 3.0 Omni 1080p (Pro) | 1232 | kling.ai API |
| — | LTX-2 Pro* | 1134 | open-weight — #1 open-weight fara audio |
| — | LTX-2 Fast* | 1130 | open-weight |

#### CU AUDIO (text-to-video cu generare audio sincrona)
| Rank | Model | Elo (AA) | Disponibil |
|------|-------|----------|------------|
| **1** | **Dreamina Seedance 2.0 720p** | **1213** | CapCut, API |
| 2 | HappyHorse-1.0 | 1212 | fal.ai |
| 3 | Kling 3.0 Omni 1080p (Pro) | 1099 | kling.ai API |
| 4 | Veo 3.1 | 1095 | Google API |
| 5 | Kling 3.0 1080p (Pro) | 1093 | kling.ai API |
| — | LTX-2.3 Fast* | 973 | open-weight — **#1 open-weight CU audio** |
| — | LTX-2.3 Pro* | 958 | open-weight |

*open-weight

### Note critice
- **DELTA 2026-05-25 (cu audio)**: Seedance 2.0 acum solo #1 cu Elo 1213, HappyHorse 1212 — inainte erau egale la 1211. Separare minima (1 punct) dar tendinta confirmata.
- **DELTA 2026-05-25 (open-weight cu audio)**: LTX-2.3 Fast (Elo 973) = noul #1 open-weight cu audio, inlocuind LTX-2 in aceasta subcategorie. LTX-2.3 lansata 5 mar 2026, 22B param, 4K+audio nativ.
- **HappyHorse**: acces public inca inconsistent pe unele platform — prioritizeaza Seedance 2.0 pentru pipeline productie.
- **Gemini Omni Flash** (Google I/O, 19 mai 2026): nu are Elo arena inca; evaluari calitative plasate sub Seedance la calitate video pura.
- **Standard profesional 2026**: rutare multi-model per tip de shot; niciun model nu domina toate dimensiunile.

### Surse credibile utilizate
- Artificial Analysis Video Arena: https://artificialanalysis.ai/video/leaderboard/text-to-video
- Medium — Gemini Omni vs Seedance: https://medium.com/ai-analytics-diaries/googles-omni-video-model-impressive-but-does-it-beat-seedance-2-1d2cd3d23dc2
- LTX-2.3 lansare: https://www.kombitz.com/2026/03/05/ltx-2-3-new-open-source-ai-video-generation-model-released/

---

## G4: MODELE NOI APARUTE (10%)

| Model | Tip | Data aparitie | Nota |
|-------|-----|---------------|------|
| GPT Image 2 | Imagine | 21 apr 2026 | Domina ambele leaderboarduri |
| HappyHorse-1.0 | Video | 7 apr 2026 (Arena); API 27 apr | Alibaba; disponibilitate de urmarit |
| Kling 3.0 Omni | Video | ~mar 2026 | Adauga generare audio nativa |
| Veo 3.1 | Video | ~apr 2026 | Google; #4 cu audio |
| Veo 3.1 Lite | Video | 31 mar 2026 | Google; API $0.05/sec (720p); mai ieftin, fara Elo arena inca |
| MAI-Image-2 | Imagine | ~apr 2026 | Microsoft; intrat in top tier (pozitie exacta neclara) |
| Midjourney V8 Alpha | Imagine | ~apr 2026 | Alpha — benchmark definitiv lipsa |
| LTX-2.3 (Fast + Pro) | Video | 5 mar 2026 | Lightricks; 22B, 4K, audio nativ; #1 open-weight video CU audio |
| Runway Gen-4 update | Video | 3 mai 2026 | Audio nativ adaugat (lip sync + SFX) la Gen-4 |
| Gemini Omni Flash | Video | 19 mai 2026 (Google I/O) | Multimodal in+out; nu apare inca in arena; sub Seedance calitativ conform evaluari timpurii |

---

## METODOLOGIE & FIABILITATE SURSE

**CREDIBIL (folosit in clasament):**
- Artificial Analysis Arena — Elo din comparatii oarbe, mii-zeci de mii voturi, metodologie publica
- Arena.ai — 4.5M voturi, metodologie identica; independent de furnizori

**SLAB / EXCLUS:**
- Listicle SEO fara metodologie — excluse
- Materiale de marketing proprii ale modelelor — excluse
- Orice clasament fara sursa de date si data benchmark-ului — excluse
- Benchmark slab: llm-stats.com video (186 voturi TrueSkill) — cross-check doar, nu sursa primara
