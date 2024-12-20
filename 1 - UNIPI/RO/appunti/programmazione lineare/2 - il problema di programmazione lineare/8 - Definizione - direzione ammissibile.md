*status*: #bozza 
*tags*: [[RO]] [[PROGRAMMAZIONE LINEARE]] [[DEFINIZIONI RO]] [[DEFINIZIONI MATEMATICHE PURE RO]]

## Definizione: *direzione ammissibile*

> Dato $\bar{x} \in P$, un vettore $\xi \in \mathbb{R}$ è detto una *direzione ammissibile* per $\bar{x}$ se esiste $\bar{\lambda} >0$ per cui $\bar{x}+ \lambda \xi$ è ammissibile per $P$ per ogni $\lambda \in [0,\bar{\lambda}]$, cioé per ogni $i=1,\dots,m$ vale: 
$$
A_{i}(\bar{x}+\lambda \xi)= A_{i}\bar{x} + \lambda A_{i}\xi \leq b_{i}
$$

#### Osservazioni
Chiaramente se $\xi \in \text{rec}(P)$ allora $\xi$ è una *direzione ammissibile* per qualsiasi punto di P.

Inoltre, se consideriamo solo i [[7 - Definizione - insieme degli indici dei vincoli attivi|vincoli attivi]], ovvero $i \in I(\bar{x})$, la *direzione ammissibile* è verificata da $A_{i}\xi \leq 0$.

Se, invece, consideriamo $i \notin I(\bar{x})$ si ha che la condizione è verificata da ogni direzione, purché $\lambda$ si prenda sufficientemente piccolo.

## Riferimenti utili

* [[8.1 - Teorema - una direzione è ammissibile se appartiene al cono degli indici attivi]]