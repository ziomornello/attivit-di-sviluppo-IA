# Regola: Generazione di un Documento dei Requisiti del Prodotto (PRD)

## Obiettivo

Guidare un assistente AI nella creazione di un Documento dei Requisiti del Prodotto (PRD) dettagliato in formato Markdown, a partire da un prompt iniziale dell’utente. Il PRD deve essere chiaro, attuabile e adatto a un junior developer per comprendere e implementare la funzionalità.

## Processo

1. Ricevere il prompt iniziale: l’utente fornisce una breve descrizione o richiesta per una nuova funzionalità.
2. Porre domande di chiarimento: prima di scrivere il PRD, l’AI deve porre domande di chiarimento per raccogliere dettagli sufficienti. L’obiettivo è comprendere il “cosa” e il “perché” della funzionalità, non necessariamente il “come” (che sarà definito dallo sviluppatore). Assicurati di fornire opzioni in elenchi alfabetici/numerati così che io possa rispondere facilmente con le mie selezioni.
3. Generare il PRD: in base al prompt iniziale e alle risposte dell’utente alle domande di chiarimento, generare un PRD usando la struttura indicata di seguito.
4. Salvare il PRD: salvare il documento generato come `prd-[feature-name].md` all’interno della directory `/tasks`.

## Domande di chiarimento (Esempi)

L’AI dovrebbe adattare le domande in base al prompt, ma ecco alcune aree comuni da esplorare:

- Problema/Obiettivo: "Quale problema risolve questa funzionalità per l’utente?" oppure "Qual è l’obiettivo principale che vogliamo raggiungere con questa funzionalità?"
- Utente target: "Chi è l’utente principale di questa funzionalità?"
- Funzionalità principali: "Puoi descrivere le azioni chiave che l’utente dovrebbe poter eseguire con questa funzionalità?"
- Storie utente: "Potresti fornire alcune storie utente? (es. Come [tipo di utente], voglio [eseguire un’azione] così da [beneficio].)"
- Criteri di accettazione: "Come sapremo quando questa funzionalità è implementata con successo? Quali sono i criteri di successo chiave?"
- Ambito/Limitazioni: "Ci sono cose specifiche che questa funzionalità non dovrebbe fare (non-obiettivi)?"
- Requisiti dei dati: "Quali dati deve mostrare o manipolare questa funzionalità?"
- Design/UI: "Ci sono mockup esistenti o linee guida UI da seguire?" oppure "Puoi descrivere l’aspetto e la sensazione desiderati?"
- Casi limite: "Ci sono potenziali casi limite o condizioni di errore che dovremmo considerare?"

## Struttura del PRD

1. Introduzione/Panoramica: descrivi brevemente la funzionalità e il problema che risolve. Indica l’obiettivo.
2. Obiettivi: elenca gli obiettivi specifici e misurabili per questa funzionalità.
3. Storie utente: dettaglia le narrazioni utente che descrivono l’uso della funzionalità e i benefici.
4. Requisiti funzionali: elenca le funzionalità specifiche che la soluzione deve avere. Usa un linguaggio chiaro e conciso (es. "Il sistema deve consentire agli utenti di caricare una foto profilo."). Numera questi requisiti.
5. Non obiettivi (Fuori ambito): indica chiaramente cosa questa funzionalità non includerà per gestire l’ambito.
6. Considerazioni di design (Opzionale): link ai mockup, descrivi requisiti UI/UX, o menziona componenti/stili rilevanti, se applicabile.
7. Considerazioni tecniche (Opzionale): menziona eventuali vincoli tecnici, dipendenze o suggerimenti noti (es. "Dovrebbe integrarsi con il modulo Auth esistente").
8. Metriche di successo: come verrà misurato il successo di questa funzionalità? (es. "Aumentare l’engagement del 10%", "Ridurre i ticket di supporto relativi a X").
9. Questioni aperte: elenca eventuali domande rimanenti o aree che necessitano di ulteriore chiarimento.

## Pubblico di riferimento

Presumi che il lettore principale del PRD sia un junior developer. Pertanto, i requisiti dovrebbero essere espliciti, non ambigui e, dove possibile, evitare gergo. Fornisci dettagli sufficienti affinché comprenda lo scopo della funzionalità e la logica di base.

## Output

- Formato: Markdown (.md)
- Posizione: `/tasks/`
- Nome file: `prd-[feature-name].md`

## Istruzioni finali

1. NON iniziare a implementare il PRD
2. Assicurati di porre all’utente domande di chiarimento
3. Utilizza le risposte dell’utente alle domande di chiarimento per migliorare il PRD

