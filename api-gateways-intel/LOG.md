# LOG - API Gateways Intel
> Cel mai recent sus. Format: [data] scurt verdict + gateways top + flag riscuri.

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
