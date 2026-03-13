<div align="center">

<img src="assets/logo.png" alt="Logo" width="120" />

# AI Product Launch Playbook

### Strategie testate sul campo per lanciare prodotti AI a livello globale — Product Hunt, KOL outreach, UGC growth, Reddit marketing

[![GitHub stars](https://img.shields.io/github/stars/dvdzhou/product-launch-playbook?style=social)](https://github.com/dvdzhou/product-launch-playbook/stargazers)
[![GitHub forks](https://img.shields.io/github/forks/dvdzhou/product-launch-playbook?style=social)](https://github.com/dvdzhou/product-launch-playbook/network/members)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](https://opensource.org/licenses/MIT)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](https://github.com/dvdzhou/product-launch-playbook/pulls)
[![Last Commit](https://img.shields.io/github/last-commit/dvdzhou/product-launch-playbook?color=blue)](https://github.com/dvdzhou/product-launch-playbook/commits/main)

</div>

---

## Cos'è questo repository

Fork italiano di [gingiris/gingiris-launch](https://github.com/Gingiris/gingiris-launch), il playbook originale creato da **Iris (生姜iris)**, ex co-fondatrice & COO di [AFFiNE](https://github.com/toeverything/AFFiNE) (60k+ stelle su GitHub).

Rispetto all'originale (v7.0), questo fork ha due obiettivi principali.

Il primo è ottimizzare il playbook per l'uso come **Claude Skill**: ogni file è stato ristrutturato con istruzioni agente nascoste, domande diagnostiche per non scaricare mai le informazioni tutte in una volta, e checkpoint obbligatori che forzano l'agente a verificare l'output dell'utente prima di procedere. L'originale è pensato per essere letto direttamente da un founder; questa versione è pensata per essere usata da un agente AI che accompagna quel founder passo per passo.

Il secondo è aggiornare i contenuti alla realtà del 2026: dati Product Hunt rivisti (Featured sceso a ~16 prodotti/giorno, peso dei commenti sull'algoritmo, dismissione del vantaggio del Hunter), prezzi newsletter e KOL aggiornati, chiarimento su IndexNow e Google, budget esteso con uno scenario a €0, e i casi Manus/Devin riletti per separare cosa è ancora replicabile da cosa non lo è più.

---

## Struttura del repository

```
product-launch-playbook/
├── SKILL.md              ← punto di ingresso per l'agente (leggi questo per primo)
├── strategy.md           ← principi strategici e meccanismi del lancio
├── preparation.md        ← SOP settimana per settimana (L-6 → L-1)
├── product-launch.md     ← piano operativo giorno per giorno (Launch Week)
├── ph-launch.md          ← guida completa al lancio su Product Hunt
├── seo-geo-guide.md      ← SEO e GEO per il traffico organico post-lancio
├── budget.md             ← allocazione del budget per 4 scenari (€0 → €50k)
├── templates.md          ← template pronti: tweet, email, Reddit, DM, KOL
└── tools.md              ← toolbox per fase con stack minimo a budget zero
```

La struttura è piatta (nessuna sottocartella) per compatibilità con il sistema di skill di Claude.

---

## Come si usa come Claude Skill

1. Crea una cartella chiamata esattamente `product-launch-playbook`
2. Copia dentro tutti i file di questo repo (struttura piatta, nessuna sottocartella)
3. Comprimi la cartella in ZIP — lo ZIP deve contenere la cartella come root, non i file direttamente:
   ```
   product-launch-playbook.zip
   └── product-launch-playbook/
       ├── SKILL.md
       ├── strategy.md
       └── ...
   ```
4. Carica lo ZIP su Claude via **Customize → Skills → Upload a skill**

**Trigger phrases:** `"product launch"`, `"Product Hunt"`, `"KOL outreach"`, `"lancio prodotto"`, `"come lancio"`, `"launch strategy"`

L'agente leggerà `SKILL.md` per primo, poi navigherà verso il file pertinente in base alla tua domanda — senza caricare tutto in una volta.

---

## Risultati del playbook originale

I risultati di seguito si riferiscono all'autrice originale Iris e al suo lavoro su AFFiNE:

| Metrica | Risultato |
|:---|:---|
| 🏆 Product Hunt #1 del giorno | 30 volte |
| ⭐ Stelle GitHub in 7 giorni | 6.000+ |
| ⭐ Stelle GitHub in 18 mesi | 33.000+ |
| 🌍 Paesi raggiunti | 100+ |

---

## Panoramica della timeline

| Fase | Quando | Milestone chiave |
|:---|:---|:---|
| Preparazione strategica | L-6 settimane | ICP, value proposition, keyword, budget |
| Creazione materiali | L-5 → L-4 | Sito ottimizzato, launch video, screenshot |
| KOL outreach | L-4 → L-3 | Selezione, primo contatto, content package |
| Preparazione contenuti | L-3 → L-2 | Approvazione bozze, calendar editoriale |
| Verifica finale | L-2 → L-1 | Test tecnici, conferme KOL, lista PH |
| 🚀 **Launch Week** | Giorno del lancio | 5 giorni tematici |
| Mantenimento momentum | L+1 → +4 | Community, SEO, raccolta testimonianze |
| 🎯 **Product Hunt** | Settimana successiva | Piano 24 ore |

---

## Indice dei file

| File | Contenuto |
|:---|:---|
| [`SKILL.md`](SKILL.md) | Punto di ingresso: protocollo di onboarding, routing, dizionario errori, glossario |
| [`strategy.md`](strategy.md) | I 4 meccanismi del lancio con checklist operative e casi reali (Manus, Devin) |
| [`preparation.md`](preparation.md) | SOP settimana per settimana: ICP, value proposition, sito, video, KOL |
| [`product-launch.md`](product-launch.md) | Piano giorno per giorno della Launch Week con gestione crisi |
| [`ph-launch.md`](ph-launch.md) | Algoritmo PH, pagina, hunter, pre-lancio, piano 24 ore |
| [`seo-geo-guide.md`](seo-geo-guide.md) | SEO tecnico, IndexNow, GEO per motori AI, calendario azioni |
| [`budget.md`](budget.md) | 4 scenari (€0 / €1-5k / €10k / €30-50k) con prezzi newsletter e KOL aggiornati |
| [`templates.md`](templates.md) | 7 template: tweet, LinkedIn, Discord, Reddit (3 varianti), email KOL, DM, follow-up |
| [`tools.md`](tools.md) | 30+ strumenti per fase con stack minimo a costo zero |

---

## Crediti e licenza

Lavoro originale: **Iris (生姜iris)** — [@Gingiris_](https://twitter.com/Gingiris_) · [LinkedIn](https://www.linkedin.com/in/yipei-wei-550825105/) · [Telegram](https://t.me/Iris_carrot)

Modifiche (traduzione IT + ottimizzazione skill): **dvdzhou**

Distribuito con licenza MIT — vedi [`LICENSE`](LICENSE) per i dettagli.
