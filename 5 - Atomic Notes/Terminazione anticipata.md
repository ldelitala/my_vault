*tags*: [[AGENTI BASATI SULLA CONOSCENZA]] [[METODI DI RISOLUZIONE SAT]]

>[!question] Cosa è?
>
> La **terminazione anticipata** è una tecnica dell'algoritmo **DPLL** che permette di decidere la verità di una clausola anche con **interpretazioni parziali**.  
> 
> In particolare:
> 1. Se un **letterale** di una clausola è vero, allora l'intera clausola è vera indipendentemente dagli altri letterali.
> 2. Se **anche una sola clausola** risulta falsa, allora l'interpretazione non può essere un modello dell'insieme di clausole.

>[!summary] In breve:
> La terminazione anticipata permette di **evitare di valutare tutte le interpretazioni complete**, fermandosi appena si può decidere la verità di una clausola o si trova una clausola falsa.

>[!example]
>Ad esempio, se $A$ è vero, allora le clausole $\{A, B\}$ e $\{A, C\}$ sono automaticamente vere, indipendentemente dai valori di $B$ e $C$.

>[!important] Implicazioni pratiche:
>
> * Riduce drasticamente il numero di interpretazioni da verificare nell'algoritmo DPLL.
> * È una forma di **ottimizzazione basata su euristiche**, utile per la soddisfacibilità di formule in **FNC**.

## Riferimenti utili

* [[Algoritmo DPLL]]
* [[Forma Normale Congiuntiva FNC o CNF]]
