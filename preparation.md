# Preparazione al Lancio: SOP Settimana per Settimana (L-6 → L-1)

> **Come usare questo file:** segui la sequenza settimanale dall'alto verso il basso. Ogni settimana ha un obiettivo preciso e una checklist. Non saltare avanti se non hai completato la settimana corrente — le fasi sono interdipendenti.

> **Se hai meno di 6 settimane:** vai alla sezione "Piano accelerato" in fondo al file.

---

## Settimana 1 (L-6 settimane): Fondamenta strategiche

**Obiettivo:** capire chi sei, per chi stai costruendo, e cosa vuoi ottenere. Senza queste risposte, tutto il lavoro successivo rischia di essere nella direzione sbagliata.

### Passo 1 — Definisci il tuo ICP (Ideal Customer Profile)

L'ICP non è "chiunque possa usare il mio prodotto". È la descrizione precisa della persona che trae il massimo valore dal tuo prodotto **oggi**, nella versione attuale.

**Come compilarlo — rispondi a queste domande:**
- Che lavoro fa questa persona? (titolo, settore, dimensione azienda)
- Qual è il problema specifico che risolve con il tuo prodotto? (non "risparmia tempo" — ma "non riusciva a fare X in meno di 3 ore, ora lo fa in 10 minuti")
- Che strumenti usa già? Quali odia?
- Dove passa il tempo online? (Reddit, X, LinkedIn, forum specifici?)
- Cosa lo fa decidere di provare un nuovo tool? (raccomandazione di un collega, un thread su X, un video su YouTube?)

**Esempio di ICP ben definito:** "Marco, 32 anni, sviluppatore backend freelance, costruisce API per startup italiane. Usa Python e FastAPI. Odia scrivere documentazione. Paga di tasca propria i tool, quindi è sensibile al prezzo sotto i $30/mese. Scopre i nuovi tool su X e su Hacker News."

**Segnale che il tuo ICP non è ancora definito:** se la tua descrizione si applica a più di 3 milioni di persone nel mondo, è troppo vaga.

### Passo 2 — Definisci la Value Proposition

La value proposition risponde a: "Perché il tuo utente ideale dovrebbe usare il tuo prodotto invece dell'alternativa che usa già?"

**Formula pratica:**
> [Nome prodotto] aiuta [ICP] a [raggiungere risultato specifico] senza [frustrazione/costo attuale], a differenza di [alternativa principale] che [limitazione dell'alternativa].

**Esempio:** "Docuflow aiuta i developer freelance a generare documentazione API professionale in 2 minuti senza scrivere una riga di testo, a differenza di Swagger UI che richiede configurazione manuale e produce output poco leggibile."

### Passo 3 — Stabilisci obiettivi misurabili

Per ogni obiettivo, stabilisci un numero preciso. "Aumentare la visibilità" non è un obiettivo — è un'aspirazione.

| Obiettivo | Metrica | Target realistico (early-stage) |
|:---|:---|:---|
| Awareness | Impression totali nei primi 7 giorni | 50K–500K |
| Interesse | Visite al sito nel Launch Week | 5K–20K |
| Prova | Nuovi sign-up nel Launch Week | 500–2.000 |
| Community | Membri Discord/Telegram al termine del lancio | 200–1.000 |
| PH (se applicabile) | Posizione finale | Top 10 di giornata |

### Passo 4 — Fai la ricerca delle keyword

Le keyword ti dicono come i tuoi utenti cercano soluzioni ai loro problemi — e ti aiutano a capire il linguaggio da usare nei tuoi materiali.

**Come fare la ricerca (strumento gratuito):**
1. Vai su [AITDK.com](https://aitdk.com) — inserisci il nome di 3 tuoi competitor
2. Guarda le keyword per cui rankano: queste sono le parole che il tuo ICP usa
3. Fai una lista di: 10 keyword di prodotto (es. "AI documentation tool"), 10 keyword di problema (es. "how to automate API docs")

**Checklist settimana 1:**
- [ ] ICP documentato in un paragrafo
- [ ] Value proposition scritta con la formula sopra
- [ ] 3 KPI scelti con target numerico
- [ ] Lista di 20 keyword (10 prodotto + 10 problema)
- [ ] Budget approssimativo deciso (vedi `budget.md`)

---

## Settimana 2 (L-5): Ottimizzazione del sito web

**Obiettivo:** il sito deve convertire i visitatori in sign-up. Un visitatore che arriva dal lancio e non si registra è un'opportunità persa per sempre.

### Standard minimi del sito prima del lancio

**Sezione above the fold (quello che si vede senza scrollare):**
- Titolo principale: deve rispondere in meno di 5 secondi alla domanda "questo a cosa serve?"
- Sottotitolo: espandi con il beneficio concreto (non le feature)
- CTA (call to action): un solo pulsante principale, ben visibile, con testo attivo ("Prova gratis" > "Scopri di più")
- Screenshot o video breve del prodotto in azione

**Segnale che il titolo è sbagliato:** se leggi il titolo a voce alta a qualcuno che non conosce il tuo settore e non capisce a cosa serve il prodotto, riscrivilo.

**Metrica di riferimento per la conversion rate:**
- Sotto il 10%: qualcosa non funziona (titolo vago, UX rotta, proposta poco chiara)
- 10–25%: nella norma
- 25–40%: ottimo per un prodotto early-stage
- Sopra 40%: eccellente, probabilmente hai un pubblico già ben targetizzato

**Come testare prima del lancio:**
Condividi il link a 5–10 persone che corrispondono al tuo ICP e chiedi: "Guardando questa pagina per 10 secondi, riesci a dirmi cosa fa questo prodotto e a chi si rivolge?" Se non ci riescono, il problema è il sito, non le persone.

**Opzioni di login — in ordine di preferenza per conversion rate:**
1. Google OAuth (riduce il friction al minimo)
2. GitHub OAuth (se il tuo ICP è developer)
3. Email + password (richiede più passaggi, ma dà dati più puliti)
> Offri almeno 2 opzioni. Non obbligare a creare un nuovo account con email+password se puoi evitarlo.

**Checklist settimana 2:**
- [ ] Titolo e sottotitolo riscritti e testati con 5 persone
- [ ] CTA principale visibile senza scrollare
- [ ] Almeno un video o GIF che mostra il prodotto in azione
- [ ] Login con Google e/o GitHub funzionante
- [ ] Google Analytics (o Mixpanel/PostHog) installato e verificato
- [ ] UTM parameters configurati per ogni canale di lancio

---

## Settimane 3–4 (L-4): Video di lancio e materiali visivi

**Obiettivo:** produrre il Launch Video — il materiale più importante dell'intero lancio.

### Perché il Launch Video è così critico

Il Launch Video è l'unico contenuto che:
- Viene guardato da chi non ti conosce ancora (abbassa la barriera di ingresso)
- Viene condiviso dai KOL senza doverlo riscrivere (è autonomo)
- Rimane utile per mesi dopo il lancio (evergreen)

Uno studio del 2025 di Demand Curve ha rilevato che i lanci con un video nella pagina PH ottengono in media il 34% di upvote in più rispetto a quelli senza. Non è decorativo — è funzionale.

### Struttura del Launch Video (60–90 secondi)

```
[0–5 sec]   HOOK — mostra il problema o il risultato finale
            Non iniziare con il logo o con "Ciao, siamo [nome]"
            Inizia con: "Fai X ogni giorno e ci vuole un'ora?" oppure mostra
            direttamente il prodotto che risolve il problema
            
[5–15 sec]  SOLUZIONE — nomina il prodotto e la proposta di valore in una frase
            
[15–60 sec] DIMOSTRAZIONE — mostra le 2–3 feature principali in azione
            Usa lo schermo reale del prodotto, non mockup generici
            
[60–75 sec] CTA + LOGO — "Prova gratis su [URL]" + logo finale
```

### Quale stile scegliere

| Stile | Quando usarlo | Esempio di riferimento |
|:---|:---|:---|
| Screen recording con voiceover | Prodotto complesso, molte funzionalità | Loom, Linear |
| Demo live con musica | Prodotto visivamente bello, UX intuitiva | Figma, Notion |
| Fondatore in camera | Prodotto con forte componente narrativa/mission | 37Signals, Basecamp |
| Animazione + screen | Prodotto astratto, difficile da mostrare direttamente | Stripe, Vercel |

**Budget per il video:**
- $0 (fai da te): usa ScreenStudio (Mac) o Loom per registrare lo schermo. Microfono decente ($50–$100). Risultato: sufficiente se il prodotto parla da solo.
- $1.000–$4.000: un editor freelance su Upwork o Fiverr che monti il tuo screen recording con testo animato e musica.
- $5.000+: agenzia o video professional. Necessario solo se il prodotto richiede effetti complessi o attori.

> **Nota per chi parte da zero:** non serve spendere $8.000 per un video. Wordware ha vinto Product of the Year su PH con un video registrato sul laptop con ScreenStudio. Il contenuto batte la produzione.

### Materiali aggiuntivi da preparare

- **5 screenshot/GIF per PH** (una per ogni feature principale)
- **3–5 GIF brevi** per i post sui social (5–10 secondi, no audio, mostrano una singola feature)
- **Logo in alta risoluzione** (PNG con sfondo trasparente, almeno 512×512px)
- **Palette colori ufficiale** (hex codes) per dare ai KOL materiali coerenti

**Checklist settimane 3–4:**
- [ ] Script del Launch Video scritto e approvato
- [ ] Launch Video registrato e montato
- [ ] 5 screenshot/GIF per PH pronti
- [ ] GIF per social pronte
- [ ] Tutti i materiali raccolti in un Google Drive condivisibile (il "Content Package" per i KOL)

---

## Settimane 4–5 (L-3): KOL outreach e media

**Obiettivo:** identificare e contattare le persone giuste che amplificheranno il lancio. Questo richiede più tempo di quanto pensi — non aspettare l'ultima settimana.

### Come identificare i KOL giusti

**Processo pratico in 3 passi:**
1. Cerca su X: `"[nome del tuo tool principale competitor]" lang:en` e guarda chi ne parla con engagement alto
2. Cerca chi ha twittato su prodotti simili negli ultimi 3 mesi e ha ricevuto molti retweet
3. Vai su [nanoinfluencer.ai](https://www.nanoinfluencer.ai) e filtra per settore + follower count 10K–100K

**Criteri di valutazione di un KOL:**
- Engagement rate effettivo: il numero di impression/follower deve essere >10% (es. se ha 20K follower, un tweet medio deve avere 2K+ visualizzazioni)
- I commenti sono conversazioni reali o emoji e "great post"? I commenti reali indicano un pubblico attivo
- Ha già parlato di prodotti simili al tuo? Ha mostrato interesse genuino nel settore?
- Attenzione ai "matrix account" (account AI): post sempre in inglese perfetto, nessuna personalità, tweettano ogni 30 minuti. Questi non portano valore reale.

### Priorità dei canali KOL

| Canale | Priorità | Note |
|:---|:---|:---|
| Newsletter AI (Rundown, TLDR AI, Ben's Bites) | ⭐⭐⭐⭐⭐ | Pubblico pre-qualificato, alta conversione |
| X/Twitter tech community | ⭐⭐⭐⭐⭐ | Seeding, discussione tecnica, viralità |
| LinkedIn (B2B, tool professionali) | ⭐⭐⭐⭐ | Migliore per conversioni su target business |
| YouTube (tutorial/review) | ⭐⭐⭐⭐ | Contenuto evergreen, alta intenzione d'acquisto |
| TikTok | ⭐⭐⭐ | Utile per awareness, conversioni più basse |

### Il Content Package — quello che mandi ai KOL

Non mandargli solo il link al sito. Mandagli un pacchetto completo che riduce il loro lavoro al minimo:

```
📦 [Nome prodotto] — Content Package per il lancio [data]

🔗 Link utili:
- Sito: [URL]
- Video demo: [URL]
- PH launch page: [URL]
- Prova gratuita: [URL con codice accesso]

📝 Tagline: [Una frase]
📝 Descrizione breve (50 parole): [testo]
📝 3 punti chiave da comunicare:
  1. [Feature/beneficio 1] — [come si spiega a parole semplici]
  2. [Feature/beneficio 2] — ...
  3. [Feature/beneficio 3] — ...

🖼 Asset scaricabili: [link Google Drive con logo, GIF, screenshot]

📅 Data di pubblicazione richiesta: [data e ora specifiche]
🔗 UTM link personalizzato per te: [URL con ?utm_source=nome_kol]

💬 Tono suggerito: [autentico e diretto / tecnico / casual]
⚠️ Non usare: [frasi che vuoi evitare, es. "rivoluzionario", "game-changer"]
```

**Checklist settimane 4–5:**
- [ ] Lista di 15–20 KOL potenziali identificati
- [ ] Engagement rate verificato per ognuno (>10%)
- [ ] Primo contatto inviato ai KOL Tier 1 (almeno 6 settimane prima del lancio per Newsletter)
- [ ] Content Package preparato e su Google Drive
- [ ] Hunter per Product Hunt contattato (se applicabile)

---

## Settimane 5–6 (L-2 e L-1): Finalizzazione e pre-lancio

**Obiettivo:** verificare che tutto funzioni, raccogliere le prime conferme, creare anticipazione.

### Lista di verifica tecnica (L-2)

- [ ] Il sito regge 1.000 visitatori simultanei? (testalo con un load test)
- [ ] Il flusso di registrazione funziona su mobile? (testa su iPhone e Android)
- [ ] Tutti i link UTM reindirizzano correttamente e vengono registrati in Analytics?
- [ ] La email di benvenuto viene inviata entro 60 secondi dalla registrazione?
- [ ] Il canale Discord/Telegram è pronto con regole, canali organizzati e un messaggio di benvenuto automatico?

### Pre-lancio: costruisci anticipazione (L-1 settimana)

- Pubblica 1–2 "teaser" su X e LinkedIn: "Lancio qualcosa venerdì. Se lavori in [settore], ne parleremo."
- Se hai già utenti beta, mandagli una email personale (non broadcast): chiedi se vogliono supportare il lancio su PH e come li puoi aiutare a farlo
- Controlla i profili di tutti i membri del team su PH: devono essere completi, con foto reale, bio, e almeno qualche upvote recente su altri prodotti

---

## Piano accelerato — se hai meno di 2 settimane

**Settimana 1 (tutto in urgenza):**
1. Scrivi ICP e value proposition in 2 ore
2. Ottimizza il titolo e la CTA del sito (1 giorno)
3. Registra un video grezzo con Loom o ScreenStudio (2–3 ore)
4. Contatta 5 persone della tua rete che conosci di persona e che potrebbero supportare il lancio
5. Crea la pagina PH in bozza

**Settimana 2 (lancio):**
- Non fare Product Hunt la settimana stessa — rimandalo di 2–3 settimane
- Lancia il prodotto con un annuncio essenziale su X e nella tua community
- Raccolta feedback e prime testimonianze

**Cosa NON fare se hai poco tempo:** non pagare KOL senza averli selezionati con cura, non pubblicare su tutti i canali contemporaneamente senza materiali pronti, non forzare Product Hunt senza rete di supporto.
