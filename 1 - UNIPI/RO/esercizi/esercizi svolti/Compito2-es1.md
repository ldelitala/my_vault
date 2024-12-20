*status*: #bozza 
*tags*: [[ESERCIZI RO]] [[RO]]

## Compito2-es1

### Legenda
* MC: Magazzini Centrali
* MP: Magazzini Periferici
* CO: Concessionarie
* P: insieme dei posti dove può essere costruito un MC
* $f_{h}$: costo costruzione MC in $h \in P$
* Q: insieme dove può essere costruito un MP
* $g_{j}$: costo construzione MP in $j \in Q$
* C: insieme di CO
* $c_{hji}$: costo di i-esimo CO di venire rifornito da j-esimo MP che è a sua volta fornito da h-esimo MC

### Obbiettivo
-> minimizzare il costo di costruzione e distribuzione

### Variabili di supporto
$$
x_{hji}=
\begin{cases}
1 \quad \text{se il CO i è servito dal MP j che è rifornito dal MC h} \\
0 \quad altrimenti
\end{cases}
 \qquad \{i,j,h\} \in C \times Q \in P
$$


### Vincoli descritti a parole
* Ogni CO deve essere servito da un solo MP ed ogni MP da un solo MC

### Modello

* $\sum_{h \in P} \sum_{j \in Q}x_{hji}=1\ , \quad i \in C$ (E) (Condizione di Partizione CO)
* $y_{hj} \geq x_{hji} \ , \quad h \in P, \quad j \in Q, \quad i \in C$ (I) (Relazione tra x e y)
* $\sum_{h \in P} y_{hj} \leq 1 \ , \quad j \in Q$ (G) (Condizione di unicità copertura MP)
* $z_{h} \geq y_{hj} \ , \quad h \in P \ , \quad j \in Q$ (O) (Condizione necessaria alla costruzione di un MC)
* $\sum_{h \in P} z_{h}f_{h}+ \sum_{j \in Q}g_{j}\sum_{h \in P}y_{hj}+ \sum_{h \in P}\sum_{j \in Q}\sum_{i \in C}c_{hji}x_{hji}$ (P) (funzione obbiettivo)
* $z_{h} \in \{0,1\} \ , \quad h \in P$ (A) (Variabile Decisionale per quale MC costruire)
* $y_{hj} \in \{0,1\} \ , \quad h \in P \ , \quad j \in Q$ (B) (Variabile di supporto per tenere traccia di quale MC serve quale MP)

## Riferimenti utili

* 