# SEO e GEO: Traffico Organico dal Lancio in Poi

> **Cosa trovi qui:** come fare in modo che il lavoro del lancio continui a portare traffico nei mesi successivi, sia sui motori di ricerca tradizionali (Google, Bing) che su quelli AI (ChatGPT, Perplexity, Claude).

> **Per chi non ha esperienza di SEO:** ogni sezione tecnica include una spiegazione del "perché" prima delle istruzioni operative.

---

## Perché il SEO è parte del lancio, non un'attività separata

La maggior parte dei lanci produce contenuto in una settimana e poi il traffico svanisce. Il SEO è il modo per trasformare quel picco in un flusso costante.

**Il meccanismo concreto:**
1. Il giorno del lancio pubblichi: un blog post, la pagina PH, un thread su X, 5 post Reddit
2. Se questi contenuti sono ottimizzati, cominciano a comparire nei risultati di ricerca
3. KOL e media che coprono il lancio creano link verso il tuo sito (backlink)
4. I backlink aumentano l'autorità del sito, che fa salire tutti i contenuti
5. Il traffico da ricerca continua per mesi, anche quando il buzz del lancio si è spento

---

## Lista di controllo tecnica del sito (L-4 settimane)

Questi sono i prerequisiti tecnici. Richiedono al massimo 1–2 giorni di lavoro del developer.

### Basi tecniche

- [ ] **HTTPS attivo:** il sito deve avere il lucchetto verde. Senza HTTPS, Google penalizza il ranking.
- [ ] **Mobile-friendly:** apri il sito su un iPhone e su un Android e verifica che sia usabile. Usa il [test di Google](https://search.google.com/test/mobile-friendly) per una verifica rapida.
- [ ] **Core Web Vitals:**
  - LCP (Largest Contentful Paint) < 2,5 secondi — il contenuto principale deve caricarsi velocemente
  - CLS (Cumulative Layout Shift) < 0,1 — la pagina non deve "saltare" mentre carica
  - Misura con [PageSpeed Insights](https://pagespeed.web.dev/)

### Indicizzazione

- [ ] **Sitemap XML:** un file che dice ai motori di ricerca quali pagine del sito esistono. Il tuo CMS (WordPress, Webflow, ecc.) la genera automaticamente. Verifica che esista all'URL `tuosito.com/sitemap.xml`.
- [ ] **Google Search Console:** collega il tuo sito gratuitamente su [search.google.com/search-console](https://search.google.com/search-console). Carica la sitemap. Ti dice come Google vede il tuo sito.
- [ ] **Bing Webmaster Tools:** stesso concetto, ma per Bing. Importante perché Bing alimenta il motore di ricerca interno di molti AI tool (ChatGPT usa Bing per la ricerca web). Registrati su [bing.com/webmasters](https://www.bing.com/webmasters).

### Ottimizzazione delle pagine principali

**Titolo della homepage (tag `<title>`):**
- Struttura: `[Nome prodotto] — [Cosa fa in 5–7 parole] | [Brand]`
- Esempio: `Docuflow — Documentazione API automatica con AI | Docuflow`
- Limite: ≤70 caratteri (il resto viene tagliato da Google)

**Meta description:**
- Appare sotto il titolo nella pagina dei risultati di ricerca
- Deve includere le keyword principali e una CTA
- Limite: ≤160 caratteri
- Esempio: "Genera documentazione API professionale in 2 minuti. Collega il tuo repo, seleziona gli endpoint, esporta. Prova gratis."

**H1 (titolo principale della pagina):**
- Ogni pagina deve avere un solo H1
- Deve contenere la keyword principale (es. "AI documentation tool")
- Deve coincidere con o essere simile al tag `<title>`

---

## IndexNow — la cosa più importante da fare il giorno del lancio

**Cos'è IndexNow (spiegazione semplice):** normalmente i motori di ricerca scoprono i nuovi contenuti "girando" il web ogni qualche giorno o settimana. IndexNow è un protocollo che ti permette di dire a Bing "ho appena pubblicato questa pagina, vienici a guardare adesso". Bing indicizza entro minuti, non giorni. Questo è importante perché Bing alimenta ChatGPT, Copilot e altri AI tool.

**Come configurare IndexNow (una volta sola):**

**Passo 1:** genera la chiave su [Bing Webmaster Tools](https://www.bing.com/webmasters) → IndexNow → Genera chiave

**Passo 2:** crea un file di testo con solo la chiave e caricalo sul sito all'URL `tuosito.com/[chiave].txt`

**Passo 3:** verifica che Bing riesca a raggiungerlo

**Come inviare le URL il giorno del lancio:**

Ogni volta che pubblichi un nuovo contenuto importante (blog post, pagina feature, ecc.), invia questa richiesta POST:

```bash
curl -X POST https://api.indexnow.org/indexnow \
  -H "Content-Type: application/json" \
  -d '{
    "host": "tuosito.com",
    "key": "LA-TUA-CHIAVE-INDEXNOW",
    "urlList": [
      "https://tuosito.com/blog/post-di-lancio",
      "https://tuosito.com/features",
      "https://tuosito.com/pricing"
    ]
  }'
```

**Alternativa senza terminale:** usa il form diretto su Bing Webmaster Tools → IndexNow → Submit URLs. Non è automatico ma funziona per i lanci one-shot.

---

## Il post del blog di lancio — struttura SEO

Il blog post di lancio è il contenuto che resterà online più a lungo e che raccoglierà i backlink dai media e dai KOL.

**Struttura raccomandata:**

```
Titolo (H1): "Introducing [Nome prodotto]: [Cosa fa]"
Esempio: "Introducing Docuflow: API Documentation That Writes Itself"

Primo paragrafo (100–150 parole):
Spiega immediatamente: cos'è il prodotto, chi lo usa, e quale problema risolve.
Non iniziare con la storia dell'azienda — inizia con il valore per l'utente.

H2: Come funziona [Nome prodotto]
Spiega le 2–3 feature principali. Per ognuna: descrizione + uno screenshot o GIF.

H2: Per chi è [Nome prodotto]
Descrivi l'ICP: "È ideale per developer che..."

H2: [Nome prodotto] vs [alternativa principale]
Un confronto onesto e specifico. Non inventare punti di forza — sii preciso.

H2: Come iniziare
3–5 passi per fare la prima azione utile col prodotto.

H2: Prezzi
Sii trasparente. "Gratuito" se è gratuito. "Freemium con piano a $X/mese" se è così.

CTA finale: link al prodotto + (se applicabile) link alla pagina PH
```

**Schema JSON da aggiungere al post:**
```json
{
  "@context": "https://schema.org",
  "@type": "Article",
  "headline": "Introducing [Nome prodotto]: [sottotitolo]",
  "datePublished": "2026-MM-GG",
  "author": {
    "@type": "Organization",
    "name": "[Nome azienda]",
    "url": "https://tuosito.com"
  },
  "description": "[Meta description del post]"
}
```

---

## GEO — come farti citare dai motori di ricerca AI

**Cos'è GEO (Generative Engine Optimization):** quando qualcuno chiede a ChatGPT "qual è il miglior tool per documentazione API?", ChatGPT non naviga il web in tempo reale (a meno che non abbia browsing attivo). Cita invece fonti che ha indicizzato in precedenza. GEO è l'arte di diventare una di quelle fonti.

**Come i modelli AI scelgono cosa citare:**

I modelli tendono a citare contenuti che:
1. **Rispondono direttamente alla domanda** — se una pagina inizia con "Docuflow è uno strumento per automatizzare la documentazione API", è più facile da citare di una pagina che ci arriva dopo 3 paragrafi
2. **Usano struttura chiara** — tabelle, liste, titoli espliciti aiutano i modelli a estrarre informazioni
3. **Sono citati da fonti attendibili** — backlink da media tech riconosciuti aumentano la probabilità di essere usati come fonte

**Azioni concrete:**

**Aggiungi una sezione FAQ alla homepage o al blog post:**
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
        "text": "[Confronto diretto e specifico]"
      }
    }
  ]
}
```

**Configura robots.txt per permettere ai crawler AI:**
```
# AI search crawlers
User-agent: ChatGPT-User
Allow: /

User-agent: OAI-SearchBot
Allow: /

User-agent: Bingbot
Allow: /

User-agent: PerplexityBot
Allow: /
```

**Schema per il software:**
```json
{
  "@context": "https://schema.org",
  "@type": "SoftwareApplication",
  "name": "[Nome prodotto]",
  "applicationCategory": "[Categoria — es. DeveloperApplication]",
  "operatingSystem": "Web",
  "offers": {
    "@type": "Offer",
    "price": "0",
    "priceCurrency": "USD",
    "description": "Piano gratuito disponibile"
  },
  "description": "[Descrizione chiara e completa]"
}
```

---

## Dopo il lancio — raccolta dei backlink

I backlink (altri siti che linkano al tuo) sono il segnale più forte per il ranking. Il momento del lancio è l'occasione migliore per raccoglierli.

**Passo 1 — Monitora le menzioni senza link:**
Usa Google Alert (`tuosito.com site:google.com`) o il tool gratuito di Ahrefs Backlink Checker per trovare articoli o post che menzionano il tuo prodotto ma non linkano. Contatta l'autore e chiedi gentilmente di aggiungere il link.

**Passo 2 — Ringrazia chi ha linkato:**
Se un blogger o un creator ti ha linkato, mandagli un breve messaggio di ringraziamento. Questo costruisce una relazione e aumenta la probabilità che lo facciano di nuovo in futuro.

**Passo 3 — Crea contenuto che attrae link nel tempo:**
- Pagine di confronto: "[Nome prodotto] vs [Competitor]" — le persone le linkano spesso in discussioni
- Tutorial approfonditi: "[Use case complesso] con [Nome prodotto] — guida passo per passo"
- Dati originali: se hai metriche interessanti (es. "i nostri utenti risparmiano in media 4 ore/settimana"), pubblicale — i giornalisti linkano dati originali

---

## Calendario azioni SEO

| Quando | Azione |
|:---|:---|
| L-4 settimane | Verifica titoli, meta description, H1 di tutte le pagine principali |
| L-4 settimane | Installa Google Search Console e Bing Webmaster Tools |
| L-4 settimane | Configura IndexNow su Bing |
| L-1 settimane | Scrivi e ottimizza il blog post di lancio |
| **Launch Day** | Pubblica blog post + invia URL tramite IndexNow |
| L+3 giorni | Verifica che le nuove pagine siano indicizzate (GSC → Coverage) |
| L+1 settimana | Cerca menzioni senza link e contatta gli autori |
| L+2–4 settimane | Crea 1–2 pagine di confronto con competitor principali |
| Ogni mese | Aggiorna il blog post di lancio con nuove feature e milestones |
