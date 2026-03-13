> **[ISTRUZIONE AGENTE — non mostrare all'utente]**
> Questo è il file tecnicamente più denso della skill. Non presentarlo in blocco — è intimidatorio per chi non ha esperienza tecnica e inutilmente dettagliato per chi ce l'ha.
> **Domanda diagnostica di apertura:** "Hai un developer nel team, o gestisci il lato tecnico del sito da solo?"
> - Se **ha un developer**: mostra il Calendario Azioni SEO in fondo al file come lista di istruzioni da delegare. Per ogni azione, spiega solo "cosa deve fare" — non come funziona tecnicamente.
> - Se **gestisce da solo ma ha familiarità tecnica**: procedi sezione per sezione con le istruzioni complete.
> - Se **non è tecnico**: inizia dalla box "Se non sei developer" che precede ogni sezione tecnica. Mostra solo quelle azioni. Per tutto il resto, spiega che serve un developer o un'agenzia per 1-2 ore di lavoro.

# SEO e GEO: Traffico Organico dal Lancio in Poi

> **Cosa trovi qui:** come fare in modo che il lavoro del lancio continui a portare traffico per mesi, sia sui motori di ricerca tradizionali (Google, Bing) che su quelli AI (ChatGPT via Bing, Perplexity, Claude).
>
> **Per chi non ha esperienza SEO:** ogni sezione tecnica spiega prima il "perché" in termini semplici, poi le istruzioni operative passo per passo.

---

## Perché il SEO è parte del lancio, non un'attività separata

La maggior parte dei lanci produce contenuto in una settimana e poi il traffico svanisce. Il SEO trasforma quel picco in un flusso costante.

**Il meccanismo concreto:**
1. Il giorno del lancio pubblichi: blog post, pagina PH, thread su X, post Reddit
2. Se questi contenuti sono ottimizzati, cominciano a comparire nei risultati di ricerca
3. KOL e media che coprono il lancio creano link verso il tuo sito (backlink)
4. I backlink aumentano l'autorità del sito, che fa salire tutti i contenuti
5. Il traffico da ricerca continua per mesi, anche quando il buzz del lancio si è spento

**Tempo richiesto:** le operazioni tecniche di questo file richiedono 1-2 giorni di lavoro del developer, da fare idealmente 4 settimane prima del lancio.

---

## Checklist tecnica del sito (L-4 settimane)

> **Se non sei developer — cosa puoi fare tu direttamente:**
> 1. **HTTPS**: controlla se c'è il lucchetto verde nel browser. Se non c'è, vai nel pannello del tuo hosting (Vercel, Netlify, Webflow, ecc.) — di solito c'è un pulsante "Enable HTTPS" o "Force SSL". È gratuito e richiede 2 minuti.
> 2. **Mobile-friendly**: apri il sito dal tuo telefono e verifica che si legga bene. Nessun codice necessario.
> 3. **Sitemap**: se usi Webflow, WordPress, Framer o Squarespace, la sitemap viene generata automaticamente. Verifica aprendo `tuosito.com/sitemap.xml` nel browser.
> 4. **Google Search Console**: puoi configurarla tu in 15 minuti seguendo le istruzioni di Google — non richiede codice, solo accesso DNS o Google Tag Manager.
> 5. **Titolo, meta description, H1**: su tutti i CMS moderni si modificano dai settings della pagina, senza toccare il codice.
>
> **Cosa invece richiede un developer (1-2 ore di lavoro):** Core Web Vitals se il sito è lento, IndexNow se non usi un CMS con plugin, Schema JSON da aggiungere nell'header, test di carico con loader.io.

### Basi tecniche

- [ ] **HTTPS attivo:** il sito ha il lucchetto verde. Senza HTTPS, Google penalizza il ranking. Se non ce l'hai, attivalo tramite il tuo hosting — è gratuito con Let's Encrypt.
- [ ] **Mobile-friendly:** apri il sito su un iPhone e un Android e verifica che sia usabile. Test rapido gratuito: [Google Mobile-Friendly Test](https://search.google.com/test/mobile-friendly).
- [ ] **Core Web Vitals:**
  - **LCP (Largest Contentful Paint) < 2,5 secondi:** il contenuto principale deve caricarsi velocemente. Semplificato: se aspetti più di 2,5 secondi prima di vedere qualcosa sullo schermo, è troppo lento.
  - **CLS (Cumulative Layout Shift) < 0,1:** la pagina non deve "saltare" mentre carica (es. i pulsanti che si spostano mentre carici la pagina).
  - Misura entrambi con [PageSpeed Insights](https://pagespeed.web.dev/) — gratuito, inserisci l'URL e ti dà un report.

### Indicizzazione

- [ ] **Sitemap XML:** un file che dice ai motori di ricerca quali pagine del tuo sito esistono. Il tuo CMS (WordPress, Webflow, ecc.) la genera automaticamente. Verifica che esista aprendo nel browser: `tuosito.com/sitemap.xml`.

- [ ] **Google Search Console:** collega il tuo sito su [search.google.com/search-console](https://search.google.com/search-console). Carica la sitemap. Ti dice come Google vede il tuo sito, quali errori ci sono, e per quali keyword stai comparendo. È gratuito e obbligatorio.

- [ ] **Bing Webmaster Tools:** stesso concetto ma per Bing. Importante perché Bing alimenta ChatGPT (con browsing attivo), Copilot, e DuckDuckGo. Registrati su [bing.com/webmasters](https://www.bing.com/webmasters).

### Ottimizzazione delle pagine principali

**Titolo della homepage (tag `<title>`):**
- Struttura: `[Nome prodotto] — [Cosa fa in 5–7 parole]`
- Esempio: `Docuflow — Documentazione API automatica con AI`
- Limite: ≤ 70 caratteri (il resto viene tagliato da Google nei risultati)

**Meta description (il testo sotto il titolo nei risultati di Google):**
- Deve includere le keyword principali e una CTA
- Limite: ≤ 160 caratteri
- Esempio: `Genera documentazione API professionale in 2 minuti. Collega il repo, seleziona gli endpoint, esporta. Prova gratis.`

**H1 (il titolo visibile principale della pagina):**
- Ogni pagina deve avere esattamente un H1
- Deve contenere la keyword principale (es. "AI documentation tool")
- Deve essere simile al tag `<title>`

---

## IndexNow — per Bing, Yandex e motori AI (non per Google)

> **Se non sei developer:** usa il Modo 2 (Bing Webmaster Tools, senza terminale) o installa il plugin CMS se sei su WordPress. Il Modo 1 con terminale è più veloce ma non è necessario — puoi fare tutto dal pannello web. Se usi Webflow, Framer o Squarespace, controlla se esiste un'integrazione diretta nelle impostazioni SEO del CMS prima di contattare il developer.

**Cos'è IndexNow (spiegazione semplice):** normalmente i motori di ricerca scoprono le nuove pagine girando il web ogni qualche giorno o settimana. IndexNow è un protocollo che ti permette di dire loro "ho appena pubblicato questa pagina, vieni a vederla adesso". La risposta è molto più rapida — spesso entro minuti.

**Importante:** Google NON supporta IndexNow. Per Google, usa Google Search Console separatamente (la sitemap e il comando "Richiedi indicizzazione" nel pannello URL Inspection).

**Perché IndexNow è utile per la visibilità AI:** Bing alimenta ChatGPT (con browsing attivo), Microsoft Copilot, e DuckDuckGo. Essere indicizzati velocemente su Bing migliora le probabilità di essere citati da questi tool.

---

### Come configurare IndexNow (una volta sola — 20 minuti)

**Passo 1: Genera la chiave**

Vai su [Bing Webmaster Tools](https://www.bing.com/webmasters) → IndexNow → clicca "Generate". Scarica il file `.txt` che viene generato.

**Passo 2: Carica il file sul sito**

Carica il file scaricato nella cartella root del tuo sito (la stessa cartella dove si trova `index.html`). Dopo il caricamento, verifica che sia accessibile aprendo nel browser: `https://tuosito.com/[nome-del-file].txt` — deve mostrare solo la chiave.

**Passo 3: Verifica in Bing Webmaster Tools**

Torna su Bing Webmaster Tools → IndexNow → verifica che la chiave sia confermata come valida.

**Passo 4: Testa la configurazione con un URL**

Puoi testare con una singola URL usando il browser o il terminale:
```
https://api.indexnow.org/indexnow?url=https://tuosito.com&key=LA-TUA-CHIAVE
```
Se ottieni un codice HTTP 200, la configurazione funziona.

---

### Come inviare URL il giorno del lancio

Ogni volta che pubblichi contenuto importante (blog post, pagina feature, ecc.), invia questa richiesta. Puoi farlo in tre modi:

**Modo 1 — Terminale (più veloce):**
```bash
curl -X POST https://api.indexnow.org/indexnow \
  -H "Content-Type: application/json" \
  -d '{
    "host": "tuosito.com",
    "key": "LA-TUA-CHIAVE",
    "keyLocation": "https://tuosito.com/LA-TUA-CHIAVE.txt",
    "urlList": [
      "https://tuosito.com/blog/post-lancio",
      "https://tuosito.com/features",
      "https://tuosito.com/pricing"
    ]
  }'
```

**Modo 2 — Bing Webmaster Tools (senza terminale):**
Vai su Bing Webmaster Tools → IndexNow → Submit URLs. Copia e incolla le URL da indicizzare. Non è automatico ma funziona per i lanci one-shot.

**Modo 3 — Plugin CMS:**
Se usi WordPress, installa il plugin "IndexNow" (ufficiale, gratuito) — indicizza automaticamente ogni nuovo post pubblicato. Per altri CMS, controlla la lista dei plugin supportati su [indexnow.org](https://www.indexnow.org).

**Per Google (separatamente):**
Vai su Google Search Console → URL Inspection → inserisci l'URL del blog post → clicca "Request Indexing". Funziona per le singole URL più importanti il giorno del lancio.

---

## Il blog post di lancio — struttura SEO

Il blog post di lancio è il contenuto che raccoglierà la maggior parte dei backlink dai media e dai KOL, e che resterà online più a lungo.

**Struttura raccomandata:**

```
Titolo (H1): "Introducing [Nome prodotto]: [Cosa fa in modo preciso]"
Esempio: "Introducing Docuflow: API Documentation That Writes Itself"

Primo paragrafo (100–150 parole):
Spiega subito: cos'è il prodotto, chi lo usa, e quale problema risolve.
Non iniziare con la storia dell'azienda — inizia con il valore per l'utente.

H2: Come funziona [Nome prodotto]
Spiega le 2–3 feature principali. Per ognuna: descrizione + uno screenshot o GIF.

H2: Per chi è [Nome prodotto]
Descrivi l'ICP in modo specifico.

H2: [Nome prodotto] vs [alternativa principale]
Un confronto onesto e specifico. Non inventare punti di forza — sii preciso su cosa fai meglio e cosa non fai.

H2: Come iniziare
3–5 passi per fare la prima azione utile con il prodotto.

H2: Prezzi
Sii trasparente. "Gratuito" se è gratuito. "Freemium con piano a $X/mese" se è così.

CTA finale: link al prodotto + link alla pagina PH (se applicabile)
```

**Schema JSON da aggiungere al post (copia e incolla nel `<head>` della pagina):**
```json
{
  "@context": "https://schema.org",
  "@type": "Article",
  "headline": "Introducing [Nome prodotto]: [Sottotitolo]",
  "datePublished": "2026-MM-GG",
  "author": {
    "@type": "Organization",
    "name": "[Nome azienda]",
    "url": "https://tuosito.com"
  },
  "description": "[Meta description del post — stessa che usi nel tag meta]"
}
```

---

## GEO — come farti citare dai motori di ricerca AI

> **Se non sei developer:** le Azioni 1 e 3 (Schema JSON) richiedono di aggiungere codice nell'`<head>` della pagina — delegale. L'Azione 2 (robots.txt) su Webflow, WordPress e Framer è gestibile da pannello senza codice: cerca "robots.txt" nelle impostazioni SEO del tuo CMS. Concentra le tue energie dirette sulla struttura dei contenuti: titoli chiari, sezioni FAQ con domande e risposte complete, descrizioni che iniziano con "X è uno strumento che..." — questo è il 70% dell'impatto GEO e non richiede competenze tecniche.

**Cos'è la GEO (Generative Engine Optimization):** quando qualcuno chiede a ChatGPT "qual è il miglior tool per documentazione API?", ChatGPT cita fonti che ha nel suo indice. GEO è l'insieme di tecniche per diventare una di quelle fonti.

**Come i modelli AI scelgono cosa citare:**
I modelli tendono a citare contenuti che:
1. Rispondono direttamente alla domanda — una pagina che inizia con "Docuflow è uno strumento per automatizzare la documentazione API" è più facile da citare di una che ci arriva dopo 3 paragrafi
2. Hanno struttura chiara — tabelle, liste, titoli espliciti aiutano i modelli a estrarre informazioni
3. Sono citati da fonti riconoscibili — backlink da media tech aumentano la probabilità di essere usati come fonte

### Azioni concrete per la GEO

**Azione 1 — Aggiungi una sezione FAQ alla homepage o al blog post:**
```json
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "Cos'è [Nome prodotto]?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "[Risposta chiara in 2–3 frasi. Includi: cosa fa, per chi è, e il vantaggio principale.]"
      }
    },
    {
      "@type": "Question",
      "name": "Come si differenzia [Nome prodotto] da [competitor principale]?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "[Confronto diretto e specifico — numeri o tempi concreti se disponibili]"
      }
    },
    {
      "@type": "Question",
      "name": "[Nome prodotto] è gratuito?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "[Sì/No/Freemium — sii preciso e includi i dettagli del piano]"
      }
    }
  ]
}
```

**Azione 2 — Configura robots.txt per i crawler AI:**
```
# Motori di ricerca tradizionali
User-agent: Googlebot
Allow: /

User-agent: Bingbot
Allow: /

# Crawler AI
User-agent: ChatGPT-User
Allow: /

User-agent: OAI-SearchBot
Allow: /

User-agent: PerplexityBot
Allow: /

User-agent: ClaudeBot
Allow: /

User-agent: anthropic-ai
Allow: /
```

**Azione 3 — Schema per il software (da aggiungere alla homepage):**
```json
{
  "@context": "https://schema.org",
  "@type": "SoftwareApplication",
  "name": "[Nome prodotto]",
  "applicationCategory": "DeveloperApplication",
  "operatingSystem": "Web",
  "offers": {
    "@type": "Offer",
    "price": "0",
    "priceCurrency": "USD",
    "description": "Piano gratuito disponibile"
  },
  "description": "[Descrizione chiara e completa — la stessa che usi nella meta description]"
}
```

---

## Dopo il lancio — raccolta dei backlink

I backlink (altri siti che linkano al tuo) sono il segnale più forte per il ranking. Il momento del lancio è l'occasione migliore per raccoglierli.

**Passo 1 — Monitora le menzioni senza link:**
Usa [Google Alerts](https://alerts.google.com) per il nome del tuo prodotto. Quando trovi un articolo o post che ti menziona senza linkare, contatta l'autore con un messaggio breve e cortese.

**Passo 2 — Ringrazia chi ha linkato:**
Se un blogger o creator ti ha linkato, mandagli un messaggio di ringraziamento. Costruisce una relazione e aumenta la probabilità che lo facciano di nuovo.

**Passo 3 — Crea contenuto che attrae link nel tempo:**
- **Pagine di confronto:** "[Nome prodotto] vs [Competitor]" — le persone le linkano spesso in discussioni
- **Tutorial approfonditi:** "[Use case complesso] con [Nome prodotto] — guida passo per passo"
- **Dati originali:** se hai metriche interessanti (es. "i nostri utenti risparmiano in media 4 ore/settimana"), pubblicale — i giornalisti linkano i dati originali

---

## Calendario azioni SEO

| Quando | Azione |
|:---|:---|
| L-4 settimane | Verifica titoli, meta description, H1 di tutte le pagine principali |
| L-4 settimane | Installa Google Search Console e Bing Webmaster Tools |
| L-4 settimane | Configura IndexNow su Bing (una tantum) |
| L-1 settimana | Scrivi e ottimizza il blog post di lancio |
| **Launch Day** | Pubblica blog post → invia URL via IndexNow → richiedi indicizzazione su Google Search Console |
| L+3 giorni | Verifica che le nuove pagine siano indicizzate (GSC → Coverage) |
| L+1 settimana | Cerca menzioni senza link e contatta gli autori |
| L+2–4 settimane | Crea 1–2 pagine di confronto con competitor principali |
| Ogni mese | Aggiorna il blog post di lancio con nuove feature e milestones |
