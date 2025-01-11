*status*: #bozza 
*tags*: [[RO]] [[Grafi e Reti di Flusso]] [[ALGORITMI]] [[ALGORITMI RO]]

## 2 - Algoritmo - Algoritmo algebrico del Simplesso Duale

#### Algoritmo a parole

0. scegli una base duale ammissibile
1. calcoli la soluzione primale e la soluzione duale
2. se la soluzione primale è ammissibile -> **la soluzione è ottima**
3. altrimenti, seleziona un indice per il quale la soluzione primale non è ammissibile come indice entrante.
	* per la regola anticiclo di Bland, se ci sono più opzioni seleziona l'indice di valore minore
4. calcola $\eta_{B} = A_{k}A_{B}^{-1}$ (non so se capirò mai il significato di questa cosa)
5. Se $\eta_{B} \leq 0$ -> **la soluzione duale è illimitata** e il **primale è vuoto**
6. Altrimenti, per ogni $\eta_{i} > 0$ calcola $\theta_{i}=\frac{\bar{y}_{i}}{\eta_{i}}$ e prendi il valore minore
7. A parità di valore, come al solito, prendi l'indice minore. Quello sarà l'indice uscente
8. Aggiorna la base con indice uscente e indice entrante
9. Torna al passo 1


#### Algoritmo algebrico

0. Scegli B Duale ammissibile
1. $\bar{x}=A_{B}^{-1}b_{B}$, $\bar{y}=[\bar{y}_{B},\bar{y}_{N}]=[cA_{B}^{-1},0]$
2. if ( $A_{N}\bar{x} \leq b_{B}$ ) -> **la soluzione è ottima**
3. $k=\text{min}\{i \in N : A_{i}\bar{x}>b_{i}\}$
4. $\eta_{B}=A_{k}A_{B}^{-1}$
5. if ( $\eta_{B} \leq 0$ ) -> **la soluzione è vuota**
6. $\bar{\theta}=\text{min}\left\{ \theta_{i}=\frac{\bar{y}_{i}}{\eta_{i}}: \eta_{i} > 0 , \ i \in B \right\}$
7. $h=\text{min}\{i \in B : \theta_{i} = \bar{\theta}\}$
8. $B= (B \ \cup \{k\})$ \ $\{h\}$
9. torna al passo 1



## Riferimenti utili

* 