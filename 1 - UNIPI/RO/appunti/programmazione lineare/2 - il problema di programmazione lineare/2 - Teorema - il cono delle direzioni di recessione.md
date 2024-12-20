*status*: #bozza
*tags*: [[RO]] [[ALGEBRA LINEARE]] [[PROGRAMMAZIONE LINEARE]] [[TEOREMI RO]]

## Teorema - il cono delle direzioni di recessione

>Sia P un *poliedro*. Allora l'insieme delle direzioni di recessione è definito da:

$$ \text{rec}(P)=\{\ d\ \in\ \mathbb{R}^n\ :\ Ad \leq 0 \}$$
Notare come questa forma descriva un cono poliedrico convesso.
### Dimostrazione
Se $d$ è una *direzione recessiva*, aggiungendo $\lambda d$ a qualsiasi punto $x \in P$ (con $\lambda \geq 0$) il nuovo punto $x + \lambda d$ deve rispettare $A(x + \lambda d) \leq b$.

Sviluppando:
$$ Ax + \lambda Ad \leq b \quad \rightarrow \quad \lambda Ad \leq 0, \qquad \text{posto che}\ \ \forall \lambda \geq 0$$
Questo perché sappiamo che $Ax \leq b$. 
Dato che $\forall \lambda \geq 0$ , questa condizione implica che $Ad \leq 0$.

## Riferimenti utili

* [[7 - Cono]]
* [[4 - Poliedro]]
* [[8 - Direzione di Recessione di un Poliedro]]
* [[2.1 - Corollario - Linealità di P]]
* 