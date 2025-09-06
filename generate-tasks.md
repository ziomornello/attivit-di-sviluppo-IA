Linee guida per la gestione delle liste di attività nei file Markdown per tracciare i progressi nel completamento di un PRD

## Implementazione delle attività

- **Una sottoattività alla volta:** NON iniziare la prossima sottoattività finché non chiedi il permesso all’utente e l’utente non dice "yes" o "y".
- **Protocollo di completamento:**  
  1. Quando completi una sottoattività, contrassegnala immediatamente come completata cambiando da `[ ]` a `[x]`.
  2. Se tutte le sottoattività sotto un’attività principale sono ora `[x]`, segui questa sequenza:
    - Prima: esegui l’intera suite di test (`pytest`, `npm test`, `bin/rails test`, ecc.)
    - Solo se tutti i test passano: esegui lo staging delle modifiche (`git add .`)
    - Pulizia: rimuovi eventuali file temporanei e codice temporaneo prima di eseguire il commit
    - Commit: usa un messaggio di commit descrittivo che:
      - Usa il formato conventional commit (`feat:`, `fix:`, `refactor:`, ecc.)
      - Riassume ciò che è stato realizzato nell’attività principale
      - Elenca le modifiche e aggiunte chiave
      - Fa riferimento al numero del task e al contesto del PRD
      - Formattta il messaggio come un comando su singola riga usando i flag `-m`, ad esempio:

        ```
        git commit -m "feat: add payment validation logic" -m "- Validates card type and expiry" -m "- Adds unit tests for edge cases" -m "Related to T123 in PRD"
        ```
  3. Una volta che tutte le sottoattività sono contrassegnate come completate e le modifiche sono state committate, contrassegna come completata anche l’attività principale.
- Fermati dopo ogni sottoattività e attendi il via libera dell’utente.

## Manutenzione della lista di attività

1. Aggiorna la lista di attività mentre lavori:
   - Contrassegna attività e sottoattività come completate (`[x]`) secondo il protocollo sopra.
   - Aggiungi nuove attività man mano che emergono.

2. Mantieni aggiornata la sezione "Relevant Files":
   - Elenca ogni file creato o modificato.
   - Fornisci per ogni file una descrizione in una riga del suo scopo.

## Istruzioni per l’AI

Quando lavora con le liste di attività, l’AI deve:

1. Aggiornare regolarmente il file della lista di attività dopo aver terminato qualsiasi lavoro significativo.
2. Seguire il protocollo di completamento:
   - Contrassegnare ciascuna sottoattività completata con `[x]`.
   - Contrassegnare l’attività principale con `[x]` una volta che tutte le sue sottoattività sono `[x]`.
3. Aggiungere le nuove attività individuate.
4. Mantenere "Relevant Files" accurato e aggiornato.
5. Prima di iniziare il lavoro, verificare quale sottoattività è la prossima.
6. Dopo aver implementato una sottoattività, aggiornare il file e poi fermarsi in attesa dell’approvazione dell’utente.
