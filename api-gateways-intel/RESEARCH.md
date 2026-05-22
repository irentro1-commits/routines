# API Gateways Intel - i-vory Studio
> Scop: alternative gri la apiyi.com (gpt-image-2-vip, $0.03/img). ZERO provideri oficiali.
> Productia ramane pe apiyi pana decide Andy.
> Ultima actualizare: 2026-05-22

---

## BENCHMARK CURRENT - apiyi.com (productie)

| Model | Pret | Note |
|---|---|---|
| gpt-image-2-vip | $0.03/imagine (flat, orice rezolutie 1K/2K/4K) | reverse route |
| gpt-image-2 (official proxy) | -15% vs OpenAI oficial | pay-as-you-go, token-based |
| Sora 2 / Veo 3.1 | listat, pret neverificat direct | |

Sursa: [apiyi.com blog](https://help.apiyi.com/en/gpt-image-2-vip-size-resolution-complete-guide-en.html) + [gpt-image-2-all $0.03](https://help.apiyi.com/en/gpt-image-2-all-api-launch-003-per-call-tutorial-en.html) - mai 2026

---

## TABEL GATEWAYS

### IEFTINE VERIFICATE

| Gateway | Modele | Pret | Plata | Fiabilitate | Sursa + Data |
|---|---|---|---|---|---|
| **apiyi.com** (PRODUCTIE) | gpt-image-2-vip, gpt-image-2, Claude, Gemini, Nano Banana | $0.03/img (VIP flat), -15% (official proxy) | card, crypto, Alipay | MEDIE - depinde de upstream OpenAI; fara SLA explicit | [help.apiyi.com](https://help.apiyi.com/en/gpt-image-2-vip-size-resolution-complete-guide-en.html) mai-2026 |
| **laozhang.ai** | gpt-image-2, Veo 3.1, Sora 2, Nano Banana 2, Seedance 2.0 | gpt-image-2: $0.03/img; Veo 3.1: $0.15/video flat (pana 8s); Nano Banana 2: $0.05/img | neclar (probabil card/crypto) | Trust score 71/100 (Scamadviser); fara date proprii de uptime; upstream Gemini a avut 45% fail rate peak | [blog.laozhang.ai](https://blog.laozhang.ai/en/posts/gpt-image-2-api-pricing) mai-2026 |

**NOTA laozhang.ai Veo 3.1:** Official Google = $0.15/s (Standard) - laozhang ofera $0.15/video FLAT (pana 8s) = economie 87-97%. Daca oferta e reala, e cea mai buna din piata pentru video. **NEVERIFICAT prin test real.**

---

### DE TESTAT

| Gateway | Modele | Pret | Plata | Obs | Sursa + Data |
|---|---|---|---|---|---|
| **atlascloud.ai** | FLUX, video API, LLM agregat | FLUX: de la $0.003/img; video: nespecificat | pay-per-use, fara subscriptie | Agregator smart - routing la cel mai ieftin server global; full-modal (img+video+audio+LLM) | [atlascloud.ai](https://www.atlascloud.ai/) mai-2026 |
| **anyapi.ai** | 400+ modele (OpenAI, Google, Anthropic, DeepSeek) | credite bazate pe consum; pret specific neverificat | credite prepaid | Un singur API key, switch instant intre modele | [anyapi.ai](https://anyapi.ai/) mai-2026 |
| **aifreeapi.com** | OpenAI image, Veo 3.1, Gemini | Veo 3.1 "cheapest" - pret exact neverificat | neclar | Blog activ cu ghiduri pricing; gateway propriu posibil existent | [aifreeapi.com](https://www.aifreeapi.com/en/posts/cheapest-veo3-api) mai-2026 |

---

### RISC MARE - NU FOLOSI IN PRODUCTIE

| Sursa | Model pret | Risc documentat | Sursa |
|---|---|---|---|
| **Taobao / Xianyu reselleri** | 90-97% off oficial (ex. Claude Opus la 3-10% din pret) | CHEI FURATE: OpenAI/Anthropic bancheaza conturile upstream -> outage instant; SUBSTITUTIE MODEL: platesti Claude Opus, primesti alt model mai ieftin fara sa stii; EXFILTRARE DATE: prompt-urile si output-urile tale sunt vandute ca training data; INJECTIE MALWARE: 8 din routerele analizate injecteaza cod malitios in tool calls; fara obligatii de data handling | [Tom's Hardware](https://www.tomshardware.com/tech-industry/artificial-intelligence/chinese-grey-market-sells-claude-api-access-at-90-percent-off-through-proxy-networks-that-harvest-user-data) + [Threads AI post](https://www.threads.com/@artificialintelligence.co/post/DYe_tw0iepI/chinese-students-buy-cheap-claude-and-gpt-api-access-on-taobao-and-xianyu-for) mai-2026 |

---

### DEPRECATE / DEFUNCT

| Serviciu | Status | Data |
|---|---|---|
| **Sora API (OpenAI)** | OPRIT - OpenAI a inchis Sora API, web si app in aprile 2026 | [aionda.blog](https://aionda.blog/en/posts/openai-sora-2-pricing-update) apr-2026 |

---

## RISCURI GENERALE - GATEWAYS GRI

### R1 - Exfiltrare date (CRITIC)
Toate gatewayurile gri ruteaza request-urile prin servere proprii. Prompt-urile, imaginile generate, input-ul clientilor trec prin un tert fara obligatii GDPR sau contractuale. Taobao reselleri documentat vand prompt-urile ca training data.

### R2 - Substitutie model (CRITIC)
Platesti pentru gpt-image-2, primesti un model mai ieftin sau local. Fara audit tehnic (fingerprinting de output), nu poti detecta. Documentat pe Taobao; risc neexclus pe orice gateway gri.

### R3 - Instabilitate upstream (MARE)
Gatewayurile depind de conturile lor la OpenAI/Google. Daca OpenAI bancheaza contul reseller-ului (frecvent), serviciul pica fara avertisment. Apiyi mentioneaza explicit ca nu garanteaza SLA deoarece depinde de upstream.

### R4 - Injectie cod malitios (MARE - specific tool calls)
Studiu arxiv (apr 2026): 8 routere gratuite si 1 platit injecteaza cod in tool calls returnate. Relevant daca folosim API in pipeline agentic. Mitigare: inspectare output + sandbox executie.

### R5 - ToS violation (MEDIU - risc legal)
Toate aceste gateways violeaza ToS OpenAI/Google/Anthropic. Risc direct pentru i-vory: daca OpenAI detecteaza us-ul indirect, poate bloca accesul la contul oficial daca il ai. In practica rareori aplicat indirect.

### R6 - Key compromise (MEDIU)
Daca gateway-ul e compromis sau e scam, API key-ul tau la gateway e expus. Mitigare: rotate chei periodic, limite de buget pe key.

---

## PRETURI DE REFERINTA - OFICIAL (pentru comparatie)

| Model | Pret oficial | Data |
|---|---|---|
| gpt-image-2 1024x1024 high | ~$0.211/img | mar-2026 |
| gpt-image-2 4K high | ~$0.41/img | mar-2026 |
| Veo 3.1 Standard | $0.40/secunda | mar-2026 |
| Veo 3.1 Fast | $0.15/secunda | mar-2026 |
| Google Veo (enterprise direct) | ~$30/minut video generat | ian-2026 |

Sursa: OpenAI pricing page + [aifreeapi.com Veo 3.1](https://www.aifreeapi.com/en/posts/veo-3-1-pricing) + [laozhang.ai video cost guide](https://blog.laozhang.ai/en/posts/how-much-does-ai-video-generator-cost)

---

## GOLURI DE CERCETARE (next run)

- [ ] laozhang.ai: verificare pret Veo 3.1 $0.15/video prin test real sau screenshot pricing page
- [ ] atlascloud.ai: pret exact gpt-image-2 si video (nu FLUX)
- [ ] anyapi.ai: pret exact pe model pentru imagine
- [ ] aifreeapi.com: este gateway propriu sau doar blog? pricing page daca exista
- [ ] Seedance 2.0 API: pret prin laozhang vs official ByteDance
- [ ] Kling 3.0 API: gateway gri disponibil?
- [ ] wentuo.ai: pricing propriu (par sa aiba serviciu separat de blog)
