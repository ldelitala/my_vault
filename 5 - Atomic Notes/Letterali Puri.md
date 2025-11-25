*tags*: [[AGENTI BASATI SULLA CONOSCENZA]] [[METODI DI RISOLUZIONE SAT]]

>[!Definizione] Letterale puro
> Un **simbolo puro** è un simbolo che appare con lo **stesso segno** in tutte le clausole di una formula.  

>[!example]
> Ad esempio, nelle clausole $\{A, \neg B\}, \{\neg B, \neg C\}, \{C, A\}$:
> * $A$ è puro,  
> * $B$ è puro,  
> * $C$ non è puro perché compare sia positivamente che negativamente.

>[!todo] Per l'euristica di DPLL:
> 1. Nel determinare se un simbolo è puro si possono trascurare le occorrenze in clausole già rese vere.
> 2. I **simboli puri** possono essere assegnati a:
>    * **True**, se il letterale è positivo.
>    * **False**, se il letterale è negativo.
>
>*Nota*: Questo **non elimina modelli utili**. Se le clausole hanno un modello, continueranno ad averlo anche dopo questo assegnamento, poiché non renderà mai falsa una clausola in cui compare il simbolo puro.

>[!summary] In breve:
> I simboli puri permettono di **assegnare valori senza rischio di falsificare clausole**, ottimizzando l'algoritmo DPLL.

>[!important] Implicazioni pratiche:
>
> * Riduce il numero di assegnamenti da verificare.
> * È un’**euristica semplice ma potente** per accelerare la soddisfacibilità di formule in **FNC**.

## Riferimenti utili

* [[Algoritmo DPLL]]  
* [[Forma Normale Congiuntiva FNC o CNF]]
