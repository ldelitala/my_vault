*status*: #bozza 
*tags*: [[RO]] [[DEFINIZIONI RO]] [[DEFINIZIONI MATEMATICHE PURE RO]] [[Grafi e Reti di Flusso]]

## 4 - Definizione - Problema del flusso massimo

Dato un grafo orientato pesato $G=(N,A)$, di cui conosciamo la capacità di ogni arco e di cui abbiamo un nodo sorgente $s$ e un nodo pozzo $t$, il problema del flusso di valore massimo consiste nel trovare la quantità di flusso massima che può essere inviata da $s$ a $t$. 

In termini matematici:
$$
\text{funzione obiettivo:} \qquad \text{max} \  v
$$
$$
\text{ vincoli capacità:} \qquad 0 \leq x_{ij} \leq u_{ij} \quad \forall (i,j) \in A
$$
$$
\text{vincolo di conservazione del flusso: } \sum_{(j,i) \in BS(i)}x_{ji} - \sum_{(i,j) \in FS(i)} =
\begin{cases}
 \ -v \quad i = s \\
 \quad v \qquad i = t \\
 \quad 0 \quad \text{altrimenti}
\end{cases}

\qquad i \in N
$$

Ovvero cerchiamo di trovare un flusso ammissibile con lo sbilanciamento $b_{s}$ maggiore (usiamo v come variabile di supporto per scriverlo in termini matematici).


## Riferimenti utili

* [[4.4 - Definizione - Flusso ammissibile e Valore del flusso]]
* [[3.2 - Algoritmo - Cammini Aumentanti]]
* [[3.1 - Teorema - Taglio minimo uguale a Flusso Massimo]]