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
\text{Se} \quad P = \{x : Ax \leq 0 \} = \text{conv}(X) + \text{cono}(V) \quad \text{ allora:}
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
