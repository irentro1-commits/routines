# i-vory Studio — Tools Intel RESEARCH
_ultima actualizare: 2026-05-25 | surse: Higgsfield MCP live + WebSearch_

---

## G1 — LANSARI / MODELE NOI

### GPT Image 2 (OpenAI)
- **Status:** ACTIV — API live din mai 2026
- **Lansat:** 21 apr 2026; API deschis ~4 mai 2026
- **DALL-E 2 + DALL-E 3 retrase:** 12 mai 2026 (ireversibil)
- **In catalog Higgsfield:** DA — model separat cu id `gpt_image_2` (distinct de `gpt_image` = GPT Image 1.5)
  - Rezolutii: 1K / 2K / 4K; calitate: low / medium / high
  - **GPT Image 1.5** ramane si el in catalog (editing + text rendering)
- **Features noi:**
  - Reasoning O-series integrat — planifica structura imaginii inainte de generare
  - Acuratete text ~99% (Latin, CJK, Hindi, Bengali)
  - 4K resolution in beta
  - Disponibil pe Microsoft Foundry din 4 mai 2026
- **Sursa:** [mindwiredai.com — GPT Image 2](https://mindwiredai.com/2026/04/22/what-is-gpt-image-2-the-complete-breakdown-features-pricing-and-who-gets-access/), confirmat MCP 2026-05-25

### Higgsfield Cinema Studio 3.5
- **Status:** ACTIV
- **Features noi:**
  - "Mr. Higgs" AI co-director — descompune scene in shots din descriere text
  - @tags pentru personaje / locatii / props reutilizabile (consistenta cross-shot)
  - Simulare optica camera reala: body, lentila, focal length, apertura INAINTE de generare
  - Colaborare real-time in proiecte comune
  - Pre-tuned motion patterns: Noir, Action, Horror, Documentary
- **Powered by:** Seedance 2.0
- **Sursa:** [Higgsfield blog](https://higgsfield.ai/blog/Fresh-Releases), [LinkedIn post](https://www.linkedin.com/posts/higgsfield_introducing-cinema-studio-35-powered-by-activity-7450306219904249858-mqDz)

### Higgsfield Supercomputer (Hermes Agent Stack)
- **Status:** ACTIV
- **Anuntat:** 14 mai 2026
- **Ce este:** Cloud-native agent stack pentru automatizare end-to-end productie media
- **Context:** Dupa pilotul "Hell Grind" — ep 23 min generat in 96h
- **Specs confirmate MCP (2026-05-25):**
  - PLUS: Claude Opus 4.6, 2 scheduled jobs, 3 parallel chats, 2 GB storage, all connectors
  - ULTRA: Claude Opus 4.7, 10 scheduled jobs, 10 parallel chats, 5 GB storage, all connectors
- **Sursa:** [explainx.ai — Higgsfield Supercomputer](https://explainx.ai/blog/higgsfield-ai-supercomputer-hermes-agent-2026), confirmat MCP 2026-05-25

### Higgsfield — Catalog modele LIVE (confirmat MCP 2026-05-25)

#### Modele imagine
| Model | Provider | Rezolutii | Note |
|-------|----------|-----------|------|
| Nano Banana 2 | Google | 1K/2K/4K | fast, photorealistic |
| Nano Banana Pro | Google | 1K/2K/4K | text, diagrame |
| Nano Banana | Google | standard | budget, realistic |
| GPT Image 2 | OpenAI | 1K/2K/4K | **NOU** — separat de v1.5 |
| GPT Image 1.5 | OpenAI | standard | editing + text rendering |
| Seedream 5.0 Lite | ByteDance | 2K/3K | reasoning, editing |
| Seedream 4.5 | ByteDance | 2K/4K | control, transformari |
| Flux 2.0 | Black Forest Labs | 1K/2K | variante: pro/flex/max |
| Flux Kontext Max | Black Forest Labs | standard | **NOU** — context-aware editing, style transfer |
| Kling O1 Image | Kling | 1K/2K | photorealistic |
| Grok Imagine | xAI | standard | **NOU** — high-contrast, editing |
| Soul 2.0 | Higgsfield | 1.5K/2K | UGC, fashion, character |
| Soul Cinema | Higgsfield | 1.5K/2K | cinema stills, concept art |
| Cinema Studio Image 2.5 | Higgsfield | 1K/2K/4K | **NOU** — cinematic stills 4K |
| Marketing Studio Image | Higgsfield | 1K/2K/4K | **NOU** — product ads |
| DTC Ads | Higgsfield | 1K/2K/4K | **NOU** — brand-kit-aware ad gen |
| Z Image | Tongyi-MAI | standard | **NOU** — super fast, stylized |
| Auto | Higgsfield | — | auto-routing pe intent |

#### Modele video
| Model | Provider | Rezolutii | Note |
|-------|----------|-----------|------|
| Seedance 2.0 | ByteDance | 480p/720p/1080p | 4-input multimodal, 4-15s |
| Seedance 1.5 Pro | ByteDance | 480p/720p/1080p | **NOU in catalog** — start/end frame |
| Cinema Studio Video 3.0 | Higgsfield | standard | **NOU** — "most advanced", 4-15s |
| Cinema Studio Video v2 | Higgsfield | standard | genre control (pro/std) |
| Cinema Studio Video v1 | Higgsfield | standard | slow motion, sound |
| Kling 3.0 | Kling | 720p | multi-shot, audio sync, 3-15s |
| Kling 2.6 | Kling | standard | **NOU** — cinematic motion, physics, audio |
| Google Veo 3.1 | Google | — | ultra-realistic, 4/6/8s, variante fast/preview |
| Veo 3.1 Lite | Google | 720p/1080p | budget, 4/6/8s, audio optional |
| Google Veo 3 | Google | — | variante fast/preview, image-to-video |
| Wan 2.6 | Wan | 720p/1080p | **NOU** — open-weight, stylized, 5/10/15s |
| Wan 2.7 | Wan | 720p/1080p | **NOU** — audio sync, character consistent, 2-15s |
| Minimax Hailuo | Hailuo | 512/768/1080 | variante: 2.3, 2.3-fast, 6/10s |
| Grok Imagine | xAI | standard | **NOU** — text + image-to-video, audio, 1-15s |
| Marketing Studio | Higgsfield | 480p-1080p | UGC ads, TikTok/Reels |

### ComfyUI v0.22.0
- **Status:** ACTIV
- **Lansat:** 20 mai 2026
- **Noutati:**
  - Stable Audio 3.0 — suport audio generation
  - MoGe model — enhanced geometry processing
  - HiDream-O1 cu area conditioning — control mai precis al generarii
  - LTXV Enhancements: downscaled IC-LoRA, optional attention_mask input
  - Temporal Processing: `downscale_ratio_temporal` pentru video workflows
  - LTX2.3 Optimization — reducere VRAM peak cand `guide_mask` e activ
  - `Seed2.0` node — ByteDance LLM capabilities
  - `LatentConcat` node — concatenare tensori latent
  - EasyCache/LazyCache: fixes pentru crashes la schimbare proprietati tensori
- **Anterior (v0.21.1, 13 mai):** Flux2ImageNode, GrokImageEditNodeV2, ByteDanceSeedreamNodeV2, Claude LLM node, HiDream-O1-Image, OpenAI Image node
- **Sursa:** [ComfyUI changelog](https://docs.comfy.org/changelog), [GitHub releases](https://github.com/Comfy-Org/ComfyUI/releases)

### Seedance 2.0 (ByteDance)
- **Status:** ACTIV — lansat feb 2026
- **Primul model video cu 4 modalitati de input simultan:** text + imagine + audio + video (pana la 12 fisiere referinta per request)
- **Rezolutie:** pana la 1080p; durata 4-15s; aspect 16:9, 9:16, 1:1, 4:3, 3:4, 21:9
- **Genre modes:** auto, action, horror, comedy, noir, drama, epic
- **API:** BytePlus (international), Volcengine (China), fal.ai, PiAPI
- **Sursa:** [segmind blog Seedance 2.0](https://blog.segmind.com/seedance-2-0-release-date-pricing-key-features-for-developers/)

### Veo 3.1 (Google)
- **Status:** ACTIV — 3 variante in catalog Higgsfield
- **Veo 3.1 Preview + 3.1 Fast** — ultra-realistic, 4/6/8s, durate fixe
- **Veo 3.1 Lite** — 720p/1080p, audio optional, budget batch
- **Veo 3** (regulat) — separate model, image-to-video, variante fast/preview
- **Unic:** singurul model cu audio nativ in output video (Standard)
- **Disponibil in Higgsfield** ca model premium
- **Sursa:** [MindStudio — Veo 3.1 Light](https://www.mindstudio.ai/blog/what-is-google-veo-3-1-light-5-cent-video-model), confirmat MCP 2026-05-25

---

## G2 — PROMO ACTIVE

### Higgsfield — Promourile "Buy until: May 22" — STATUS INCERT

> **!! ATENTIE: Data "Buy until: May 22" a trecut (azi 25 mai). !!**
> MCP live (2026-05-25) inca returneaza aceste features ca "status: included" in config,
> dar nu putem confirma daca sunt inca achizitionabile pentru abonamente noi.
> **Recomandam verificare manuala pe higgsfield.ai inainte de cumparare.**

| Promo | Plus Monthly | Plus Annual | Ultra Monthly | Ultra Annual | Status |
|-------|-------------|-------------|---------------|--------------|--------|
| Soul V2 + Cinema FREE GENS | 3,000 | 5,000 | 5,000 | 10,000 | POSIBIL EXPIRAT |
| Seedream 5.0 Lite — 365-day UNLIMITED | DA | DA | DA | DA | POSIBIL EXPIRAT |
| Flux.2 Pro (1K) — 365-day UNLIMITED | DA | DA | DA | DA | POSIBIL EXPIRAT |
| Seedream 4.5 (2K/4K) — 365-day UNLIMITED | DA | DA | DA | DA | POSIBIL EXPIRAT |
| Nano Banana — 365-day UNLIMITED | DA | DA | DA | DA | POSIBIL EXPIRAT |
| Kling O1 Image — 365-day UNLIMITED | DA | DA | DA | DA | POSIBIL EXPIRAT |
| GPT Image — 365-day UNLIMITED | DA | DA | DA | DA | POSIBIL EXPIRAT |
| Nano Banana 2 (2K) — 7-day UNLIMITED | DA | DA | - | - | POSIBIL EXPIRAT |
| Nano Banana Pro (2K) — 7-day UNLIMITED | NU | NU | DA | DA | POSIBIL EXPIRAT |
| Kling 3.0 (720p/5s) — 7-day UNLIMITED | NU | DA | DA | DA | POSIBIL EXPIRAT |

### Higgsfield Ultra Annual — Feature NOU (confirmat MCP 2026-05-25)
- **"One 365-day Unlimited video model"** — badge SPECIAL, inclus in Ultra Annual
- **Modele disponibile la alegere** (alegerea e fixa dupa cumparare, nu mai poate fi schimbata):
  - Seedance 1.0 Pro Fast 720p (5s)
  - Minimax Hailuo 2.3 Fast 768 (6s)
  - Kling 2.5 Turbo Std 720 (5s)
- **Disponibil si pe 18-month plan si 2-year plan** (mentionat in tooltipsByBillingPeriod)
- **Sursa:** Higgsfield MCP live, 2026-05-25

### Higgsfield — Coduri promo externe (neverificate direct)
| Cod | Discount raportat | Sursa | Status |
|-----|------------------|-------|--------|
| `SPECIAL_OFFER_ULTRA_ANNUAL_23` | ~23% off Ultra Annual | simplycodes.com (15 mai) | POSIBIL EXPIRAT |
| `SPECIAL_OFFER_TEAM_PLAN_ANNUAL_30` | ~30% off Team Annual | simplycodes.com (14 mai) | POSIBIL EXPIRAT |
| `NETGONET_10` | 10% off | coupert.com (mai 2026) | NEVERIFICAT |
| `GENHQ_HIGGSFIELD` | 15% off | WebSearch summary (mai 2026) | NEVERIFICAT |

_Regula anti-halucinare: niciun cod nu a fost verificat direct de noi via checkout. Testeaza inainte de cumparare._

### Discount structural permanent Higgsfield
- Annual billing = 20% off PLUS ($49 → $39/mo), 23% off ULTRA ($129 → $99/mo)
- Confirmat MCP live, fara expirare

---

## G3 — PRICING GATEWAYS

### Higgsfield (confirmat MCP live 2026-05-25)
| Plan | Monthly | Annual/mo | Credite/luna | Economie anuala |
|------|---------|-----------|--------------|-----------------|
| PLUS | $49 | $39 | 1,000 | $120 |
| ULTRA | $129 | $99 | 3,000 | $360 |

- 1,000 credite = ~4,800 imagini sau ~200 videouri sau ~60 generari personaj
  - = 600 generari Nano Banana Pro SAU ~200 videouri Kling 3.0
- 3,000 credite = ~12,000 imagini sau ~500 videouri sau ~100 generari personaj
  - = 1,500 generari Nano Banana Pro SAU ~500 videouri Kling 3.0
- Credit top-up: nu disponibil in workspace-ul curent

### Higgsfield Supercomputer (inclus in plan, fara cost extra)
| Feature | PLUS | ULTRA |
|---------|------|-------|
| Storage | 2 GB | 5 GB |
| Parallel chats | 3 | 10 |
| Scheduled jobs | 2 | 10 |
| Claude model | Opus 4.6 | Opus 4.7 |
| All connectors | DA | DA |

### GPT Image 2 API (OpenAI)
| Calitate | Cost per 1024x1024 |
|----------|-------------------|
| Low | ~$0.006 |
| Medium | ~$0.053 |
| High | ~$0.211 |
- Input tokens: $8/M image input, $2/M cached, $30/M output, $5/M text input
- Edit workflows (cu referinta): 2-3x cost per imagine
- **Sursa:** [wavespeed.ai GPT Image 2 pricing](https://wavespeed.ai/blog/posts/gpt-image-2-pricing-2026/)

### Video API Pricing (mai 2026)
| Model | Cost |
|-------|------|
| Veo 3.1 Standard | $0.50-0.75/sec (cu audio) |
| Veo 3.1 Fast | $0.15/sec |
| Veo 3.1 Light | $0.05/clip |
| Kling API standard | $0.28/5s ($0.056/sec) |
| Seedance 2.0 via fal.ai | ~$0.05/5s (720p) |
| Seedance 2.0 direct | ~$1.21/gen |
| Seedance 2.0 Fast | ~$0.77/gen |
- **Sursa:** [modelslab.com video API comparison](https://modelslab.com/blog/api/veo-3-1-vs-kling-3-sora-2-ai-video-api-cost-2026), [buildmvpfast.com](https://www.buildmvpfast.com/api-costs/ai-video)

### API Gateways
| Gateway | Pozitionare |
|---------|-------------|
| fal.ai | Cel mai ieftin — 985 endpoints, video de la $0.05/sec |
| Replicate | Docs mai bune, catalog mai larg, usor mai scump |
| RunPod H100 SXM | ~$2.69/hr serverless, control GPU complet |
- **Sursa:** [teamday.ai API comparison](https://www.teamday.ai/blog/ai-api-pricing-comparison-2026)

### Kling AI Plans (standalone)
| Tier | Monthly | Annual/mo |
|------|---------|-----------|
| Standard | $8.80 | $6.60 |
| Pro | $25.99 | $24.42 |
| Premier | $64.99 | $60.72 |
| Ultra | $127.99 | $119.17 |
- **Sursa:** [vo3ai.com Kling pricing](https://www.vo3ai.com/kling-ai-pricing)
