*tags*: [[METODI DI RISOLUZIONE SAT]]

>[!question] A cosa servono?
> Sfruttano la casualità degli algoritmi locali per trovare modelli più velocemente (in alcuni casi).

> [!example] funzionamento 
> * Gli ‘stati’ sono *interpretazioni*, assegnamenti completi 
> * L’obiettivo è un assegnamento che soddisfa tutte le clausole (un *modello*) 
> * Si parte da un assegnamento *casuale* 
> * Ad ogni passo si cambia il valore di un simbolo proposizionale (*flip*) a caso 
> * Gli stati sono valutati contando il numero di clausole soddisfatte (più sono meglio è)  

>[!summary] Algoritmi
> [[Algoritmo WALK-SAT]]

## Riferimenti utili

* [[Modello di una formula]]
* [[Interpretazione di una formula]]
* [[Algoritmo WALK-SAT]]