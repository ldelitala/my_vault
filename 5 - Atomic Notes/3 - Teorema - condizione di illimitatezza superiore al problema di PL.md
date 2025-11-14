*status*: #bozza
*tags*:  [[RO]] [[PROGRAMMAZIONE LINEARE]] [[TEOREMI]]

## Teorema - condizione di illimitatezza superiore al problema di PL

> Se $c \cdot d \geq 0$ per un qualche $d \in \text{rec}(P)$ allora il problema di massimizzazione è *illimitato superiormente*.
### Dimostrazione
Per la definizione di *direzione di recessione*:
$$ d \in \text{rec}(P) \quad \leftrightarrow \quad x + \lambda d \in P \qquad \forall x \in P\quad \text{posto che}\ \ \forall \lambda \geq 0,\ $$
quindi la funzione obbiettivo lungo $d$ è:
$$ c\ (x + \lambda d) = c\ x + \lambda \ c\ d$$
Se $c \cdot d \geq 0$, poiché $\lambda \geq 0$, il termine $\lambda\ c\ d$ può diventare arbitrariamente grande aumentando $\lambda$. Questo implica che la funizone obiettivo può crescere indefinitamente lungo $d$. 

## Riferimenti utili

* [[8 - Direzione di Recessione di un Poliedro]]
* [[1.1 - Modello Standard di PL]]