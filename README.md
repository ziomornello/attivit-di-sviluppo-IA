# 🚀 Task di Sviluppo AI 🤖

Benvenuti in **AI Dev Tasks**! Questo repository fornisce una raccolta di file markdown progettati per potenziare il tuo flusso di lavoro di sviluppo di funzionalità con IDE e CLI basati su AI. Originariamente creati per [Cursor](https://cursor.sh/), questi strumenti funzionano con qualsiasi assistente di codifica AI, inclusi Claude Code, Windsurf e altri. Sfruttando questi prompt strutturati, puoi approcciare sistematicamente la creazione di funzionalità, dall'ideazione all'implementazione, con checkpoint integrati per la verifica.

Smetti di lottare con richieste AI monolitiche e inizia a guidare il tuo collaboratore AI passo dopo passo!

## ✨ L'Idea di Base

Costruire funzionalità complesse con l'AI a volte può sembrare una scatola nera. Questo flusso di lavoro mira a portare struttura, chiarezza e controllo al processo:

1.  **Definizione dell'Ambito:** Delineare chiaramente cosa deve essere costruito con un Documento dei Requisiti di Prodotto (PRD).
2.  **Pianificazione Dettagliata:** Suddividere il PRD in un elenco di attività granulare e attuabile.
3.  **Implementazione Iterativa:** Guidare l'AI ad affrontare un'attività alla volta, permettendoti di rivedere e approvare ogni modifica.

Questo approccio strutturato aiuta a garantire che l'AI rimanga in carreggiata, rende più facile il debug dei problemi e ti dà fiducia nel codice generato.

## Flusso di Lavoro: Dall'Idea alla Funzionalità Implementata 💡➡️💻

Ecco il processo passo dopo passo utilizzando i file `.md` in questo repository:

### 1️⃣ Creare un Documento dei Requisiti di Prodotto (PRD)

Per prima cosa, stendi il progetto per la tua funzionalità. Un PRD chiarisce cosa stai costruendo, per chi e perché.

Puoi creare un PRD leggero direttamente nel tuo strumento AI preferito:

1.  Assicurati di avere il file `create-prd.md` da questo repository accessibile.
2.  Nel tuo strumento AI, avvia la creazione del PRD:

    ```text
    Usa @create-prd.md
    Ecco la funzionalità che voglio costruire: [Descrivi la tua funzionalità in dettaglio]
    Fai riferimento a questi file per aiutarti: [Opzionale: @file1.py @file2.ts]
    ```
    *(Suggerimento Pro: Per gli utenti di Cursor, la modalità MAX è consigliata per PRD complessi se il tuo budget consente una generazione più completa.)*

    ![Esempio di avvio della creazione di un PRD](https://pbs.twimg.com/media/Go6DDlyX0AAS7JE?format=jpg&name=large)

### 2️⃣ Genera la Tua Lista di Attività dal PRD

Con il tuo PRD redatto (es. `MyFeature-PRD.md`), il passo successivo è generare un piano di implementazione dettagliato e passo dopo passo per il tuo Sviluppatore AI.

1.  Assicurati di avere `generate-tasks.md` accessibile.
2.  Nel tuo strumento AI, usa il PRD per creare le attività:

    ```text
    Ora prendi @MyFeature-PRD.md e crea le attività usando @generate-tasks.md
    ```
    *(Nota: Sostituisci `@MyFeature-PRD.md` con il nome file effettivo del PRD che hai generato nel passaggio 1.)*

    ![Esempio di generazione di attività da un PRD](https://pbs.twimg.com/media/Go6FITbWkAA-RCT?format=jpg&name=medium)

### 3️⃣ Esamina la Tua Lista di Attività

Ora avrai una lista di attività ben strutturata, spesso con attività e sotto-attività, pronta per essere elaborata dall'AI. Questo fornisce una chiara roadmap per l'implementazione.

![Esempio di una lista di attività generata](https://pbs.twimg.com/media/Go6GNuOWsAEcSDm?format=jpg&name=medium)

### 4️⃣ Istruisci l'AI a Lavorare sulle Attività (e a Segnare il Completamento)

Per garantire un progresso metodico e consentire la verifica, useremo `process-task-list.md`. Questo comando istruisce l'AI a concentrarsi su un'attività alla volta e ad attendere il tuo via libera prima di passare alla successiva.

1.  Crea o assicurati di avere il file `process-task-list.md` accessibile.
2.  Nel tuo strumento AI, di' all'AI di iniziare con la prima attività (es. `1.1`):

    ```text
    Per favore, inizia con l'attività 1.1 e usa @process-task-list.md
    ```
    *(Importante: Devi fare riferimento a `@process-task-list.md` solo per la *prima* attività. Le istruzioni al suo interno guidano l'AI per le attività successive.)*

    L'AI tenterà di eseguire l'attività e poi ti chiederà di revisionarla.

    ![Esempio di avvio di un'attività con process-task-list.md](https://pbs.twimg.com/media/Go6I41KWcAAAlHc?format=jpg&name=medium)

### 5️⃣ Rivedi, Approva e Avanza ✅

Man mano che l'AI completa ogni attività, tu rivedi le modifiche.

*   Se le modifiche vanno bene, rispondi semplicemente con "sì" (o un'affermazione simile) per istruire l'AI a segnare l'attività come completata e passare alla successiva.
*   Se sono necessarie modifiche, fornisci un feedback all'AI per correggere l'attività corrente prima di andare avanti.

Vedrai crescere una soddisfacente lista di elementi completati, fornendo una chiara visualizzazione della tua funzionalità che prende vita!

![Esempio di una lista di attività in progressione con elementi completati](https://pbs.twimg.com/media/Go6KrXZWkAA_UuX?format=jpg&name=medium)

Anche se non è sempre perfetto, questo metodo si è dimostrato un modo molto affidabile per sviluppare funzionalità più grandi con l'assistenza dell'AI.

### Dimostrazione Video 🎥

Se vuoi vederlo in azione, l'ho dimostrato nel podcast di [Claire Vo "How I AI"](https://www.youtube.com/watch?v=fD4ktSkNCw4).

![Dimostrazione di AI Dev Tasks sul podcast How I AI](https://img.youtube.com/vi/fD4ktSkNCw4/maxresdefault.jpg)

## 🗂️ File in questo Repository

*   **`create-prd.md`**: Guida l'AI nella generazione di un Documento dei Requisiti di Prodotto per la tua funzionalità.
*   **`generate-tasks.md`**: Prende in input un file markdown PRD e aiuta l'AI a suddividerlo in una lista di attività di implementazione dettagliata e passo dopo passo.
*   **`process-task-list.md`**: Istruisce l'AI su come elaborare la lista di attività generata, affrontando un'attività alla volta e attendendo la tua approvazione prima di procedere. (Questo file contiene anche la logica per l'AI per segnare le attività come completate).

## 🌟 Vantaggi

*   **Sviluppo Strutturato:** Impone un processo chiaro dall'idea al codice.
*   **Verifica Passo-Passo:** Ti permette di rivedere e approvare il codice generato dall'AI ad ogni piccolo passo, garantendo qualità e controllo.
*   **Gestione della Complessità:** Suddivide le grandi funzionalità in compiti più piccoli e digeribili per l'AI, riducendo la possibilità che si perda o generi codice eccessivamente complesso e scorretto.
*   **Affidabilità Migliorata:** Offre un approccio più affidabile per sfruttare l'AI per lavori di sviluppo significativi rispetto a singoli e grandi prompt.
*   **Tracciamento Chiaro dei Progressi:** Fornisce una rappresentazione visiva delle attività completate, rendendo facile vedere quanto è stato fatto e cosa viene dopo.

## 🛠️ Come Usare

1.  **Clona o Scarica:** Ottieni questi file `.md` nel tuo progetto o in una posizione centrale dove il tuo strumento AI può accedervi.
    ```bash
    git clone https://github.com/snarktank/ai-dev-tasks.git
    ```
2.  **Segui il Flusso di Lavoro:** Usa sistematicamente i file `.md` nel tuo assistente AI come descritto nel flusso di lavoro sopra.
3.  **Adatta e Itera:**
    *   Sentiti libero di modificare i prompt all'interno dei file `.md` per adattarli meglio alle tue esigenze specifiche o al tuo stile di codifica.
    *   Se l'AI ha difficoltà con un'attività, prova a riformulare la descrizione iniziale della tua funzionalità o a suddividere ulteriormente le attività.

## Istruzioni Specifiche per Strumento

### Cursor

Gli utenti di Cursor possono seguire il flusso di lavoro descritto sopra, utilizzando i file `.md` direttamente nella chat dell'Agente:

1.  Assicurati di avere i file di questo repository accessibili
2.  Nella chat dell'Agente di Cursor, fai riferimento ai file con `@` (es. `@create-prd.md`)
3.  Segui il flusso di lavoro in 5 passaggi come descritto sopra
4.  **Modalità MAX per i PRD:** L'uso della modalità MAX in Cursor per la creazione di PRD può produrre risultati più approfonditi se il tuo budget lo consente

### Claude Code

Per usare questi strumenti con Claude Code:

1.  **Copia i file nel tuo repo**: Copia i tre file `.md` in una sottodirectory del tuo progetto (es. `/ai-dev-tasks`)

2.  **Fai riferimento in CLAUDE.md**: Aggiungi queste righe al file `./CLAUDE.md
