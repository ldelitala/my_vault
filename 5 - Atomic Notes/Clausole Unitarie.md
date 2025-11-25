*tags*: [[AGENTI BASATI SULLA CONOSCENZA]] [[METODI DI RISOLUZIONE SAT]]

>[!Definizione] Clausola unitaria
>
> Una **clausola unitaria** è una clausola che contiene **un solo letterale non ancora assegnato**.  
>
> In particolare:
> * Ad esempio, $\{B\}$ è unitaria.  
> * Anche $\{B, \neg C\}$ diventa unitaria se $C = \text{True}$.

>[!todo] Per l'euristica di DPLL:
> * Conviene assegnare **prima valori ai letterali in clausole unitarie**.  
> * L'assegnamento è **obbligato**:
>    * **True** se il letterale è positivo.  
>    * **False** se il letterale è negativo.

>[!summary] In breve:
> Le clausole unitarie permettono di **ridurre rapidamente lo spazio di ricerca**, poiché determinano assegnamenti obbligatori.

>[!important] Implicazioni pratiche:
>
> * Garantisce una **propagazione immediata delle assegnazioni**, accelerando l'algoritmo DPLL.  
> * È una delle euristiche più efficaci per migliorare le prestazioni nella soddisfacibilità di formule in **FNC**.

## Riferimenti utili

* [[Algoritmo DPLL]]  
* [[Forma Normale Congiuntiva FNC o CNF]]
