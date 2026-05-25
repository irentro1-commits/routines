# LOG - API Gateways Intel
> Cel mai recent sus. Format: [data] scurt verdict + gateways top + flag riscuri.

---

## [2026-05-25] - RULARE 2 (delta pricing major)

**SURSE CAUTATE:** atlascloud.ai/pricing, atlascloud.ai/models/gpt-image-2, blog.laozhang.ai, wavespeed.ai, piapi.ai, kie.ai, scamadviser, prnewswire, aifreeapi.com, wentuo.ai
**PERIOADA DATE:** apr-mai 2026

### DELTA fata de [2026-05-22]

**PRETUL ZILEI - ATLASCLOUD.AI GPT-IMAGE-2: $0.008/img flat** (confirmat din mai multe pagini ale atlascloud.ai, mai-2026).
Asta e 3.75x mai ieftin decat apiyi.com ($0.03). Daca se confirma ca taxeaza flat indiferent de quality (LOW/MED/HIGH) = cel mai ieftin gateway confirmat pentru gpt-image-2.
RISC NEVERIFICAT: posibil $0.008 = low quality implicit, nu high. **TEST OBLIGATORIU inainte de migrare.**

**NOU CONFIRMATE:**
- laozhang.ai Veo 3.1: $0.15/video Fast, $0.25/video Standard; fara taxa pe request esuat
- atlascloud.ai Seedance 2.0: $0.081/s Fast, $0.1/s Standard (anuntat PR Newswire apr-2026)
- aifreeapi.com = BLOG ONLY, nu gateway (inchis din lista de investigat)
- wentuo.ai = BLOG ONLY, nu gateway (inchis din lista de investigat)

**GATEWAYURI NOI IDENTIFICATE:**
- wavespeed.ai (Singapore; 700+ modele; 99.9% SLA declarat; gpt-image-2 disponibil, pret necunoscut)
- kie.ai (30-80% sub oficial; gpt-image-2, Kling, Veo, Seedance; pret exact neconfirmat)
- piapi.ai (Kling 3.0: $0.13/video = 7% sub oficial = nesemnificativ)

### TOP GATEWAYS IEFTINE (verificate cu sursa)

1. **atlascloud.ai** - gpt-image-2: **$0.008/img flat** | Seedance 2.0 Fast: **$0.081/s**
   - Sursa: [atlascloud.ai/models/openai/gpt-image-2/text-to-image](https://www.atlascloud.ai/models/openai/gpt-image-2/text-to-image) - mai 2026
   - Trust: SOC 2; Scamadviser "very likely not a scam"; Trustpilot 3.7 (1 review - insuficient)
   - Status: PROMOVAT la IEFTINE VERIFICATE - pret confirmat pe pagini proprii; test calitate necesar

2. **laozhang.ai** - gpt-image-2: **$0.03/img**; Veo 3.1 Fast: **$0.15/video** (8s, fara taxa pe fail)
   - Sursa: [blog.laozhang.ai](https://blog.laozhang.ai/en/posts/gpt-image-2-api-pricing) - mai 2026
   - Trust: Scamadviser 71/100
   - Status: VERIFICAT - pret egal cu apiyi pe imagine dar superior pe video

3. **apiyi.com** (productia curenta) - gpt-image-2-vip: **$0.03/img flat** orice rezolutie
   - Status: CONFIRMAT, in productie

### FLAG RISCURI

- **[CRITIC PRIORITAR] atlascloud.ai calitate neconfirmata**: $0.008 poate insemna low quality implicit. Daca dai high quality in request si primesti low = substitutie silentioasa de parametru. Testeaza explicit cu `quality: high` si masura output vs apiyi.
- **[IMPORTANT] Sora API**: DEFUNCT din apr-2026. Eliminat din calcule.
- **[GENERAL] Toate gateways gri**: fara SLA garantat, depind de upstream

### NEXT ACTIONS (pentru Andy)
1. **TEST URGENT**: atlascloud.ai cu $5-10 credit - cere explicit `quality: high`, `size: 4096x4096` si compara cu apiyi output. Daca e identic = migrare economiseste 75% pe imagine.
2. Test laozhang.ai $5: verifica calitate gpt-image-2 si confirma Veo 3.1 $0.15 in practica
3. Verifica wavespeed.ai pret exact gpt-image-2 (au pricing page public)
4. Verifica kie.ai pret exact gpt-image-2

---

## [2026-05-22] - PRIMA RULARE (bootstrap)

**SURSE CAUTATE:** apiyi.com, laozhang.ai, atlascloud.ai, anyapi.ai, aifreeapi.com, wentuo.ai, Taobao/Xianyu resellers, Scamadviser, Tom's Hardware, arxiv
**PERIOADA DATE:** ian-mai 2026

### DELTA fata de anterior
Prima rulare - nu exista baseline. Totul e nou.

### TOP GATEWAYS IEFTINE (verificate cu sursa)

1. **apiyi.com** (productia curenta) - gpt-image-2-vip: **$0.03/img flat** orice rezolutie pana la 4K
   - Sursa: [help.apiyi.com](https://help.apiyi.com/en/gpt-image-2-vip-size-resolution-complete-guide-en.html) - mai 2026
   - Status: CONFIRMAT, in productie

2. **laozhang.ai** - gpt-image-2: **$0.03/img**; Veo 3.1: **$0.15/video flat** (pana 8s = 87-97% sub oficial)
   - Sursa: [blog.laozhang.ai gpt-image-2](https://blog.laozhang.ai/en/posts/gpt-image-2-api-pricing) - mai 2026
   - Sursa Veo: [laozhang.ai video cost guide](https://blog.laozhang.ai/en/posts/how-much-does-ai-video-generator-cost) - mai 2026
   - Trust: Scamadviser 71/100 - [scamadviser.com](https://www.scamadviser.com/check-website/laozhang.ai)
   - Status: DE TESTAT - pret egal cu apiyi pe imagine, potential mai bun pe video

3. **atlascloud.ai** - FLUX: **$0.003/img** (nu gpt-image-2 confirmat); video API exista, pret neverificat
   - Sursa: [atlascloud.ai](https://www.atlascloud.ai/blog/case-studies/unlock-the-cheapest-ai-image-generation-api-2026-today) - mai 2026
   - Status: DE INVESTIGAT - FLUX foarte ieftin, dar modelele noastre (gpt-image-2) neverificate

### FLAG RISCURI CRITICE

- **[CRITIC] Taobao/Xianyu reselleri**: EVITA. Chei furate + substitutie model + date exfiltrate + injectie malware confirmata in studiu arxiv apr-2026. Sursa: [Tom's Hardware](https://www.tomshardware.com/tech-industry/artificial-intelligence/chinese-grey-market-sells-claude-api-access-at-90-percent-off-through-proxy-networks-that-harvest-user-data)
- **[IMPORTANT] Sora API**: DEFUNCT din apr-2026. OpenAI a oprit complet accesul API.
- **[ATENTIE] laozhang.ai Veo $0.15**: pretul e foarte atractiv dar NEVERIFICAT prin test real. Posibil expirat sau conditional.
- **[GENERAL] Toate gateway-urile gri**: fara SLA explicit, depind de conturile upstream care pot fi banate de OpenAI/Google

### NEXT ACTIONS (pentru Andy)
- Test laozhang.ai cu $5-10 credit: verifica gpt-image-2 calitate + pret real per request
- Verifica atlascloud.ai daca suporta gpt-image-2 (nu doar FLUX)
- Daca video generation e in plan: laozhang.ai Veo 3.1 $0.15/video e cel mai atractiv de testat

---
