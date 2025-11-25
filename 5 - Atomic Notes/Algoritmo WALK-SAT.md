*tags*: [[METODI DI RISOLUZIONE SAT]] [[AGENTI BASATI SULLA CONOSCENZA]]

>[!question] A cosa serve?
> **WalkSAT** è un algoritmo stocastico per determinare la soddisfacibilità di formule in **CNF**, basato su un processo iterativo di assegnamento e modifica dei simboli.

>[!example] Funzionamento passo-passo
>
> 1) Ad ogni passo, l'algoritmo **sceglie a caso una clausola non ancora soddisfatta**.
>
> 2) Tra i simboli della clausola, sceglie quale modificare (**flip**) secondo una probabilità $p$ (di solito $0.5$):
>    * **Passo casuale (random walk)**: si sceglie un simbolo a caso.
>    * **Passo di ottimizzazione**: si sceglie il simbolo che **massimizza il numero di clausole soddisfatte** dopo il flip.
>
> 3) L'algoritmo continua fino a raggiungere un numero predefinito di flip, **dopo il quale si arrende** se non è stata trovata una soluzione soddisfacibile.

>[!summary] In breve:
> WalkSAT combina **random walk** e **ottimizzazione locale** per esplorare lo spazio delle assegnazioni e trovare rapidamente modelli di formule CNF.

>[!important] Importante
> * se l'insieme di clausole è insoddisfacibile allora non terminerà mai e l'algoritmo è quindi **incompleto**
> 	* infatti si setta un numero massimo di *flip*

>[!important] Implicazioni pratiche:
>
> * È **completamente stocastico**, quindi può trovare soluzioni diverse in esecuzioni separate.
> * Funziona bene su formule grandi dove gli algoritmi deterministici come DPLL diventano troppo lenti.
*Può non terminare con successo se il numero massimo di flip è troppo basso.*

>[!important] Altri accorgimenti
> * Va bene per cercare un modello se sappiamo che esiste la soddisfacibilità
> 	* più un modello è vincolato, più difficile sarà da soddisfarre
> 	* se $m$ è il numero di clausole e $n$ il numero di simboli allora è importante il rapporto $\frac{m}{n}$
> 		* in generale, se il rapporto è maggiore di 4 la probabilità inizia a tendere a zero molto velocemente

![[Probabilità di soddisfacibilità.png]]

## Riferimenti utili

* [[Forma Normale Congiuntiva FNC o CNF]]