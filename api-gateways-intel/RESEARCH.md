# API Gateways Intel - i-vory Studio
> Scop: alternative gri la apiyi.com (gpt-image-2-vip, $0.03/img). ZERO provideri oficiali.
> Productia ramane pe apiyi pana decide Andy.
> Ultima actualizare: 2026-05-25

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
| **laozhang.ai** | gpt-image-2, Veo 3.1 Fast+Standard, Nano Banana 2, Seedance 2.0 | gpt-image-2: $0.03/img; Veo 3.1 Fast: $0.15/video flat (pana 8s); Veo 3.1 Standard: $0.25/video flat; Nano Banana 2: $0.05/img | neclar (probabil card/crypto) | Trust score 71/100 (Scamadviser); fara date proprii de uptime; upstream Gemini a avut 45% fail rate peak; NU se taxeaza request-urile esuate | [blog.laozhang.ai](https://blog.laozhang.ai/en/posts/gpt-image-2-api-pricing) mai-2026; [video cost guide](https://blog.laozhang.ai/en/posts/how-much-does-ai-video-generator-cost) mai-2026 |
| **atlascloud.ai** | gpt-image-2 t2i+edit, Seedance 2.0, Kling 3.0, FLUX, LLM | gpt-image-2: **$0.008/img flat** (t2i si edit, acelasi pret); Seedance 2.0 Fast: $0.081/s; Seedance 2.0 Std: $0.1/s; Kling 3.0 Std: $0.084-0.126/s; FLUX: $0.003/img | pay-per-use, fara subscriptie | SOC 2 certificat; Scamadviser "very likely not a scam"; Trustpilot 3.7/5 (1 review - semnal slab); fara SLA uptime explicit public; PR Newswire confirma Seedance 2.0 apr-2026 = comportament companie legitima | [atlascloud.ai/models gpt-image-2](https://www.atlascloud.ai/models/openai/gpt-image-2/text-to-image) mai-2026; [pricing](https://www.atlascloud.ai/pricing/models) mai-2026 |

**NOTA laozhang.ai Veo 3.1:** CONFIRMAT - $0.15/video Fast (pana 8s), $0.25/video Standard. Official Google Fast = $0.15/s adica $1.2/video 8s -> economie 87.5% la Fast. Nu se taxeaza request-urile esuate (avantaj operational). **NEVERIFICAT prin test de productie.**

**NOTA CRITICA atlascloud.ai gpt-image-2:** $0.008/img flat = 3.75x mai ieftin decat apiyi ($0.03). RISC: neverificat daca $0.008 se aplica indiferent de calitate (low/medium/high) sau doar la low quality. Oficial OpenAI: low ~$0.006, medium ~$0.053, high ~$0.211. Daca atlascloud taxeaza flat $0.008 si livreaza high quality = deal major. Necesita test real cu 4K high quality inainte de migrare.

---

### DE TESTAT

| Gateway | Modele | Pret | Plata | Obs | Sursa + Data |
|---|---|---|---|---|---|
| **wavespeed.ai** | gpt-image-2, Kling (full suite), 700+ modele | gpt-image-2: pret per-img confirmat existent DAR valoare exacta neverificata; Kling: disponibil | pay-per-use, fara subscriptie; $1 trial credit | Singapore-based; 99.9% uptime SLA declarat (neverificat independent); Kling disponibil "exclusive" in unele piete non-CN; comportament platform legitim | [wavespeed.ai/collections/kling](https://wavespeed.ai/collections/kling) mai-2026; [wavespeed.ai/pricing](https://wavespeed.ai/pricing) mai-2026 |
| **kie.ai** | gpt-image-2, Kling, Veo, Seedance, Runway, Claude, GPT, Gemini, Suno | 30-50% sub oficial pe majoritatea modelelor; pana la 80% pe selectie; gpt-image-2 pret exact neverificat | credite prepaid | API unificat; switch instant intre modele; documentatie publica existenta | [kie.ai](https://kie.ai/) mai-2026; [docs.kie.ai](https://docs.kie.ai/) mai-2026 |
| **piapi.ai** | Kling 3.0 (focus principal), alte modele video | Kling 3.0: $0.13/video (5s) vs official $0.14 = 7% economie - MINIMAL | pay-as-you-go, $0 minim | Diferenta pret fata de oficial = nesemnificativa; relevant doar pt workflow Kling specific | [piapi.ai/kling-3-0](https://piapi.ai/kling-3-0) mai-2026 |
| **anyapi.ai** | 400+ modele (OpenAI, Google, Anthropic, DeepSeek) | credite bazate pe consum; pret specific per model neverificat | credite prepaid | API unificat; pret gpt-image-2 specific neverificat | [anyapi.ai](https://anyapi.ai/) mai-2026 |

**NOTA aifreeapi.com:** CONFIRMAT = blog/content site, NU gateway propriu. Publica ghiduri de pricing si comparatii. Nu are pricing page propriu. Eliminat din lista de investigat.

**NOTA wentuo.ai:** CONFIRMAT = blog care recenzeaza apiyi.com si alte gateways. NU are serviciu gateway propriu. Eliminat din cercetare.

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
| **aifreeapi.com** (ca gateway) | CLASIFICAT: blog de comparatii pricing, fara serviciu gateway propriu | mai-2026 |
| **wentuo.ai** (ca gateway) | CLASIFICAT: blog care recenzeaza apiyi si altele, fara serviciu gateway propriu | mai-2026 |

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
| gpt-image-2 low quality | ~$0.006/img | mar-2026 |
| gpt-image-2 1024x1024 high | ~$0.211/img | mar-2026 |
| gpt-image-2 4K high | ~$0.41/img | mar-2026 |
| Veo 3.1 Standard | $0.40/secunda | mar-2026 |
| Veo 3.1 Fast | $0.15/secunda | mar-2026 |
| Veo 3.1 Standard 8s video | ~$3.2/video | mar-2026 |
| Veo 3.1 Fast 8s video | ~$1.2/video | mar-2026 |
| Seedance 2.0 (official ByteDance) | ~69 RMB/luna plan | apr-2026 |
| Kling 3.0 Standard | $0.075/s | feb-2026 |
| Google Veo (enterprise direct) | ~$30/minut video generat | ian-2026 |

Sursa: OpenAI pricing page + [aifreeapi.com Veo 3.1](https://www.aifreeapi.com/en/posts/veo-3-1-pricing) + [laozhang.ai video cost guide](https://blog.laozhang.ai/en/posts/how-much-does-ai-video-generator-cost) + [atlascloud Seedance pricing](https://www.atlascloud.ai/blog/case-studies/seedance-2.0-pricing-full-cost-breakdown-2026)

---

## GOLURI DE CERCETARE (next run)

- [x] ~~laozhang.ai: verificare pret Veo 3.1~~ REZOLVAT: Fast $0.15/video, Standard $0.25/video (mai-2026)
- [x] ~~atlascloud.ai: pret exact gpt-image-2~~ REZOLVAT: $0.008/img flat (mai-2026)
- [x] ~~aifreeapi.com: gateway sau blog?~~ REZOLVAT: blog de comparatii, fara serviciu propriu
- [x] ~~wentuo.ai: pricing propriu?~~ REZOLVAT: blog de recenzii, fara serviciu propriu
- [x] ~~Seedance 2.0 API: pret prin atlascloud~~ REZOLVAT: Fast $0.081/s, Std $0.1/s
- [x] ~~Kling 3.0 API: gateway gri disponibil?~~ REZOLVAT: atlascloud, wavespeed, piapi, kie toate au acces
- [ ] **PRIORITAR** atlascloud.ai gpt-image-2: confirma prin TEST ca $0.008 se aplica la high quality (nu doar low); risc: pot taxeaza flat low quality si livra inferior
- [ ] wavespeed.ai: pret exact per-img pentru gpt-image-2 (exista pe platform, valoare necunoscuta)
- [ ] kie.ai: pret exact per-img pentru gpt-image-2
- [ ] anyapi.ai: pret exact pe model pentru gpt-image-2 (inca neconfirmat)
- [ ] laozhang.ai: test de productie real cu $5-10 credit - calitate output gpt-image-2 si pret efectiv per request
- [ ] atlascloud.ai: uptime real in ultimele 30 zile (Trustpilot 1 review e insuficient)
