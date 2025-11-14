*tags*: [[DEFINIZIONI]] [[AGENTI BASATI SULLA RICERCA]]

## A* pesato

> [!Definizione] A* pesato  
> Variante dell’algoritmo A* che utilizza la funzione:
>  $$f(n)=g(n)+W⋅h(n)$$  
>  con $W>1$ per dare maggiore peso all’euristica.

In questo modo non abbiamo più garantita la soluzione ottima ma possiamo comunque trovare una buona soluzione ad un costo computazionale a volte anche molto ridotto.

Se la soluzione ottima ha costo $C*$ possiamo trovare una soluizone che stia tra $C*$ e $WC*$.

>[!example]
>![[Pasted image 20251111174453.png]]

>[!note]
> $g(n)$ è il costo per arrivare al nodo e $h(n)$ è l'euristica della soluzione ottimale


## Riferimenti utili

* [[A*]]
* [[Problemi di ricerca]]