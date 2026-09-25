# Fit by Chezan

Generator de antrenamente și nutriție cu AI, 100% static — fără server, fără cont, fără login.

## Cum funcționează

Aplicația rulează în întregime în browser. Nu există niciun backend: datele tale (antrenamente, greutăți, progres) se salvează doar în `localStorage`-ul browserului tău, pe acest dispozitiv.

Pentru funcțiile bazate pe AI (generare antrenamente, nutriție, transcriere poze), aplicația apelează direct din browser API-urile Cerebras și/sau Groq, folosind cheia ta proprie de API.

## Configurare cheie API

1. Deschide aplicația și mergi la tab-ul **Setări**.
2. Introdu cheia ta de la [Cerebras](https://cloud.cerebras.ai/) și/sau [Groq](https://console.groq.com/keys) (ai nevoie de cel puțin una).
3. Apasă **Salvează setările**.

Cheia rămâne doar în browser-ul tău (localStorage) — nu este trimisă niciodată către vreun server al aplicației, pentru că aplicația nu are server.

> Notă: Cerebras blochează apelurile directe din browser (CORS) pentru unele conturi — dacă se întâmplă asta, aplicația trece automat pe Groq.

## Rulare locală

Fiind un site static, orice server HTTP simplu merge:

```bash
python -m http.server 8090
```

apoi deschide `http://localhost:8090`.

## Găzduire

Aplicația e gândită pentru GitHub Pages — servește direct `index.html` din rădăcina repo-ului/branch-ului configurat.
