*tags*: [[DEFINIZIONI]] [[AGENTE]]

## Classificazione di Agenti (elemento esecutivo)

> [!Definizione] Agente con tabella  
> Utilizza una **tabella di ricerca** che associa direttamente ogni percezione (o stato percepito) a un’azione predefinita.  
> La decisione è effettuata mediante un lookup nella tabella: dato l’input percepito, si restituisce l’azione corrispondente. È semplice ed efficiente in ambienti con spazio di percezioni limitato, ma poco scalabile e difficile da adattare se le situazioni aumentano o cambiano.

> [!Definizione] Agente reattivo semplice  
> Seleziona le azioni esclusivamente in base alla percezione corrente, senza tenere conto delle esperienze passate.  
> È strutturato tramite regole del tipo _condizione → azione_, che stabiliscono il comportamento in ogni situazione.

> [!Definizione] Agente basato su modello (con stato)  
> Mantiene una rappresentazione interna dello stato del mondo, aggiornata in base alla storia delle percezioni e delle azioni eseguite.  
> Questo stato consente di inferire informazioni non immediatamente percepibili e di scegliere azioni più appropriate.

> [!Definizione] Agente con obiettivo  
> Agisce con l’intento di raggiungere uno o più obiettivi specifici.  
> Seleziona le azioni che massimizzano la probabilità di conseguire tali obiettivi, valutando le conseguenze delle proprie scelte.

> [!Definizione] Agente con valutazione di utilità  
> Gestisce situazioni in cui gli obiettivi sono molteplici o conflittuali, utilizzando una _funzione di utilità_ per assegnare un valore numerico al grado di soddisfazione di ciascun esito.  
> Sceglie le azioni che massimizzano l’utilità complessiva, ottimizzando le decisioni in modo razionale.

## Riferimenti utili

* 