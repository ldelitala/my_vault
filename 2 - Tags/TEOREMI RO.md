
# Indice

### Algebra lineare
* [ ] [[2 - Teorema - il cono delle direzioni di recessione]]
* [ ] [[5 - Teorema - un poliedro è la somma di un inviluppo conico e un inviluppo convesso]] (!)
* [ ] [[4 - Teorema - qualsiasi cono finitamente generato è un cono poliedrico, e viceversa]]
* [ ] [[2.1 - Corollario - Linealità di P]]

### Grafi e Reti di flusso

#### Albero dei cammini minimi
##### Proprietà di SPT.S
* [ ] [[1.3.2 - Teorema - Proprietà di SPT.S con cicli non negativi]]

#### Flusso massimo
##### min cut - max flow
* [ ] [[3.1 - Teorema - Taglio minimo uguale a Flusso Massimo]] (!!!!)

#### Flusso di costo minimo
* [[4.7.1 - Corollario - Pseudoflusso minimale se non esistono cicli aumentanti]] !!!!

### Programmazione Lieare

#### Gli elementi grafici del problema

##### Recessione del poliedro
* [[2 - Teorema - il cono delle direzioni di recessione|il cono delle direzioni di recessione]] !!
* [[2.1 - Corollario - Linealità di P]] !
* [[3 - Teorema - condizione di illimitatezza superiore al problema di PL]]
* [[6 - Teorema - Riduzione di variabili in un problema di PL con linealità]]
	* [[6.3 - Corollario - Proprietà del problema ridotto]]

##### Vario genere
* [[4 - Teorema - qualsiasi cono finitamente generato è un cono poliedrico, e viceversa]]
* [[4.1 - Lemma - relazione bidirezionale tra vettori del cono e i suoi generatori]]
* [[5.1 - Corollario - condizione necessaria e sufficiente della soluzione ottima del problema di PL]]

##### Poliedro
* [[5 - Teorema - un poliedro è la somma di un inviluppo conico e un inviluppo convesso]]


#### Primale e Duale
##### Dualità
* [ ] [[3 - Teorema - dualità debole|Dualità debole]] (!!!)
	* [ ] [[4 - Teorema - dualità forte|Dualità forte]] (!!!)

* [ ] [[2 - Teorema - il Duale del Duale è il Primale|il Duale del Duale è il Primale]] (!!)

##### Scarti complementari
* [ ] [[5 - Teorema - soluzioni e scarti complementari|Il teorema degli scarti complementari]] (!!!!!!)
* [ ] [[5.4 - Corollario - Estensione del teorema sulla relazione tra soluzioni e scarti complementari|Estensione del teorema sulla relazione tra soluzioni e scarti complementari]] (!!)

##### Teoremi per la risoluzione degli algoritmi
* [ ] [[4.1 - Teorema - relazione tra soluzioni del primale e duale|relazione tra soluzioni del primale e del duale]] (!!!!)
* [ ] [[6 - Teorema - condizione necessaria e sufficiente per la ottimalità della soluzione|condizione necessaria e sufficiente per la ottimalità della soluzione]] (!!!!)
* [ ] [[3.2 - Corollario - certificato di ottimalità]] (!!!!!)


##### Altri teoremi sulla PL
* [ ] [[3 - Teorema - condizione di illimitatezza superiore al problema di PL]]
* [ ] [[6 - Teorema - Riduzione di variabili in un problema di PL con linealità]]
* [ ] [[8.1 - Proprietà - una direzione è ammissibile se appartiene al cono degli indici attivi]]
* [ ] [[9.1 - Corollario - punto estremo di un Poliedro]]
* [ ] [[6.3 - Corollario - Proprietà del problema ridotto]]
* [ ] [[3.1 - Corollario - Se il primale è illimitato il Duale è vuoto]]
* [ ] [[5.1 - Corollario - condizione necessaria e sufficiente della soluzione ottima del problema di PL]]

## Grafi e Reti di flusso



## Programmazione Lineare

### Teorema - il cono delle direzioni di recessione
$$ \text{rec}(P)=\{\ d\ \in\ \mathbb{R}^n\ :\ Ad \leq 0 \}$$
#### Corollario - Linealità di P
$$
 \text{lin}(P) = \{\ d \in \mathbb{R}^n\ :\ Ad=0 \} 
$$
### Teorema - condizione di illimitatezza superiore al problema di PL

> Se $c \cdot d \geq 0$ per un qualche $d \in \text{rec}(P)$ allora il problema di massimizzazione è *illimitato superiormente*.

### Teorema - qualsiasi cono finitamente generato è un cono poliedrico, e viceversa
**dai generatori al cono poliedrico**: $\qquad C = \text {cono}(V) \quad \rightarrow \quad \exists A : C = \{ x : Ax \leq 0 \}$ 
**dal cono poliedrico ai generatori**: $\qquad C = \{x : Ax \leq 0\} \quad \rightarrow \quad \exists V = \{v_1,..., v_n\} : C = \text{cono}(V)$

#### Lemma - relazione bidirezionale tra vettori del cono e i suoi generatori
$$
 \exists d \in \text{cono}(V) : c \cdot d >0 \quad \leftrightarrow \quad \exists v_i \in V : c \cdot v_i > 0
$$
### Teorema - un poliedro è la somma di un inviluppo conico e un inviluppo convesso
$$
 P \in \mathbb{R}^n \text{ è un poliedro} \quad \leftrightarrow \quad \exists X = \{x_1,...,x_t\},\ \exists V = \{v_1,...,v_s\} : P = \text{conv}(X) + \text{cono}(V)
$$
#### Corollario - condizione necessaria e sufficiente della soluzione ottima del problema di PL
$$
\text{Se} \quad P = \{x : Ax \leq b \} = \text{conv}(X) + \text{cono}(V) \quad \text{ allora:}
$$

$$
c \cdot v \leq 0,\ \forall v \in V \quad \leftrightarrow \quad \exists h : x_{h} \in X \ \ \text{è soluzione ottima}
$$

### Teorema - Riduzione di variabili in un problema di PL con linealità
$$
\text{max}\{ cx : Ax \leq b \} \quad \text{con } \text{rank}(A) < n 
\quad \rightarrow \quad 
\text{max}\{ c'x'_{new} : A'x'_{new} \leq b \}.
$$
 Dove:

- $A = [A', a^n] \in \mathbb{R}^{m \times n}$,  $A' \in \mathbb{R}^{m \times n-1}$, $a^n \in \mathbb{R}^m$
- $x \in \mathbb{R}^n$, $x'_{new}\in \mathbb{R}^{n-1}$
- $c = [c', c_n] \in \mathbb{R}^n$,  $c' \in \mathbb{R}^{n-1}$, $c_n \in \mathbb{R}$
- $b \in \mathbb{R}^m$

#### Corollario - Proprietà del problema ridotto

Il problema ridotto ha le seguenti proprietà:
  
1. Se il problema ridotto *non ha soluzioni ammissibili*, allora anche il problema originale non ne ha.  
2. Se il problema ridotto *è superiormente illimitato*, allora anche il problema originale è superiormente illimitato.  
3. Se il problema ridotto *ha una soluzione ottima* $x'_{new}$, allora:  
   - Se $cd \neq 0$, con $d = [\beta, -1]$, il problema originale è superiormente illimitato.  
   - Se $cd = 0$, il problema originale ha la stessa soluzione ottima, che è data da $x = [x'_{new}, 0]$.
