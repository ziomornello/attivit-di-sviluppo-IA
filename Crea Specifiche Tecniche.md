# Regola: Generare un elenco di attività da un PRD

## Obiettivo

Guidare un assistente IA nella creazione di un elenco di attività dettagliato e passo-passo in formato Markdown basato su un Documento dei Requisiti di Prodotto (PRD) esistente. L’elenco di attività deve guidare uno sviluppatore nell’implementazione.

## Output

- **Formato:** Markdown (`.md`)
- **Percorso:** `/tasks/`
- **Nome file:** `tasks-[nome-file-prd].md` (es.: `tasks-prd-user-profile-editing.md`)

## Processo

1. **Ricevere riferimento al PRD:** L’utente indica all’IA uno specifico file PRD.
2. **Analizzare il PRD:** L’IA legge e analizza i requisiti funzionali, le user story e le altre sezioni del PRD specificato.
3. **Valutare lo stato attuale:** Esaminare la codebase esistente per comprendere l’infrastruttura, i pattern architetturali e le convenzioni. Inoltre, identificare eventuali componenti o funzionalità già esistenti che potrebbero essere rilevanti per i requisiti del PRD. Poi, individuare i file, i componenti e le utility correlati già esistenti che possono essere sfruttati o che richiedono modifiche.
4. **Fase 1: Generare le attività principali:** In base all’analisi del PRD e alla valutazione dello stato attuale, creare il file e generare le attività principali, ad alto livello, necessarie per implementare la funzionalità. Usa il tuo giudizio su quante attività di alto livello utilizzare. Probabilmente saranno circa
5. **Informare l’utente:** Presentare queste attività all’utente nel formato specificato (senza sotto-attività per ora). Ad esempio: “Ho generato le attività di alto livello basate sul PRD. Pronto a generare le sotto-attività? Rispondi con ‘Go’ per procedere.”.
6. **Attendere la conferma:** Mettersi in pausa e attendere che l’utente risponda con “Go”.
7. **Fase 2: Generare le sotto-attività:** Una volta che l’utente conferma, suddividere ciascuna attività principale in sotto-attività più piccole e operative, necessarie per completare l’attività principale. Assicurarsi che le sotto-attività seguano logicamente dall’attività principale, coprano i dettagli di implementazione implicati dal PRD e considerino i pattern della codebase esistente quando rilevante, senza esserne vincolati.
8. **Identificare i file rilevanti:** In base alle attività e al PRD, identificare i file che dovranno essere creati o modificati. Elencarli nella sezione `File rilevanti`, includendo i file di test corrispondenti quando applicabile.
9. **Generare l’output finale:** Combinare attività principali, sotto-attività, file rilevanti e note nella struttura Markdown finale.
10. **Salvare l’elenco delle attività:** Salvare il documento generato nella directory `/tasks/` con il nome file `tasks-[nome-file-prd].md`, dove `[nome-file-prd]` corrisponde al nome base del file PRD di input (es.: se l’input è `prd-user-profile-editing.md`, l’output sarà `tasks-prd-user-profile-editing.md`).

## Formato di output

Il piano di attività generato deve seguire questa struttura:

```markdown
## File rilevanti

- `path/to/potential/file1.ts` - Breve descrizione del motivo per cui questo file è rilevante (es.: Contiene il componente principale per questa funzionalità).
- `path/to/file1.test.ts` - Test unitari per `file1.ts`.
- `path/to/another/file.tsx` - Breve descrizione (es.: Gestore della route API per l’invio dei dati).
- `path/to/another/file.test.tsx` - Test unitari per `another/file.tsx`.
- `lib/utils/helpers.ts` - Breve descrizione (es.: Funzioni di utilità necessarie per i calcoli).
- `lib/utils/helpers.test.ts` - Test unitari per `helpers.ts`.

### Note

- I test unitari dovrebbero in genere essere collocati accanto ai file di codice che stanno testando (es.: `MyComponent.tsx` e `MyComponent.test.tsx` nella stessa directory).
- Usa `npx jest [optional/path/to/test/file]` per eseguire i test. L’esecuzione senza un percorso esegue tutti i test trovati dalla configurazione di Jest.

## Attività

- [ ] 1.0 Titolo dell’attività principale
  - [ ] 1.1 [Descrizione sotto-attività 1.1]
  - [ ] 1.2 [Descrizione sotto-attività 1.2]
- [ ] 2.0 Titolo dell’attività principale
  - [ ] 2.1 [Descrizione sotto-attività 2.1]
- [ ] 3.0 Titolo dell’attività principale (potrebbe non richiedere sotto-attività se puramente strutturale o di configurazione)
```

## Modello di interazione

Il processo richiede esplicitamente una pausa dopo la generazione delle attività principali per ottenere la conferma dell’utente (“Go”) prima di procedere con la generazione delle sotto-attività dettagliate. Questo assicura che il piano di alto livello sia allineato con le aspettative dell’utente prima di entrare nei dettagli.

## Pubblico target

Supponi che il lettore principale dell’elenco di attività sia uno sviluppatore junior che implementerà la funzionalità, con consapevolezza del contesto della codebase esistente.