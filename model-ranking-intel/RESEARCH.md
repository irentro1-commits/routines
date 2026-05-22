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
