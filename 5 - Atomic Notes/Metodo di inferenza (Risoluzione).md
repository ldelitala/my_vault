*tags*: [[AGENTI BASATI SULLA CONOSCENZA]] [[METODI DI RISOLUZIONE SAT]]

>[!question] A cosa serve?
> Il **metodo di inferenza** o **Risoluzione** è una procedura di inferenza per la logica proposizionale che opera su una KB in **forma normale congiuntiva (CNF)**.  
> 
> Il suo uso pratico più comune è **verificare se una clausola è una conseguenza logica della KB**: si controlla se **aggiungerla alla KB** la mantiene soddisfacibile. 
> 
> In generale, per quanto non dia un modello di soluzione come gli [[Algoritmi SAT-Solvers]], è un ottimo modo per dimostrarre la soddisfacibilità di una formula.


>[!note] Idee chiave
> * L'algoritmo combina clausole per produrre nuove clausole che derivano logicamente dalle precedenti usando la cosiddetta [[Regola di Risoluzione]]. Se nel farlo incappa in una clausola contraddittoria allora vorrà dire che la formula non è soddisfacibile perché contiene, appunto, una contraddizione.
> * Le clausole vuote sono insoddisfacibili per definizione, quindi se si deriva una clausola vuota abbiamo fatto.
> * L’obiettivo operativo è capire se una nuova clausola è **accettabile** dalla KB:
>     - Se la sua aggiunta negata **genera** la clausola vuota → per il [[Teorema di refutazione]] allora la clausola è *conseguenza logica* della KB.  
>     - Se la sua aggiunta negata **non genera** la clausola vuota → la clausa non è *conseguenza logica* della KB

>[!example] Funzionamento dell’algoritmo (visione operativa)
>
> 1.  **Si nega la conclusione** che si vuole dimostrare ($\neg \alpha$).
> 2.  Si aggiunge $\neg \alpha$ alla Base di Conoscenza ($KB$).
> 3.  Si applica iterativamente la **[[Regola di Risoluzione]]** (inferenza) al set di clausole.
> 4.  Se si arriva alla **[[Clausola Vuota** ($\square$), l'insieme è insoddisfacibile, e quindi $\text{KB} \models \alpha$ è dimostrata vera.

>[!info] Caratteristiche
> * Basato su una sola regola, semplice e meccanica.  
> * Usato come **test di conseguenza logica**: una clausola è deducibile ↔ la sua negazione porta a contraddizione.  
> * La generazione delle clausole può esplodere → complessità alta nel caso peggiore.  
> * Fondamento teorico dei moderni SAT solver, che introducono ottimizzazioni drastiche.

>[!summary] In breve:
> La Risoluzione è un metodo **sintattico** (basato sulla manipolazione delle regole) che usa l'inferenza per trovare una contraddizione, stabilendo così la **validità** di una proposizione.

## Riferimenti utili
* [[Forma Normale Congiuntiva FNC o CNF]]
* [[Teorema di refutazione]]
* [[Conseguenza logica]]
* [[Regola di Risoluzione]]
