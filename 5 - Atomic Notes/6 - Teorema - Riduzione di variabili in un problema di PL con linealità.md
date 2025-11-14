*status*: #bozza 
*tags*: [[RO]] [[PROGRAMMAZIONE LINEARE]] [[TEOREMI]]

## Teorema - soluzioni nel caso di linealità

> Se $\text{lin}(P) \neq \{0\}$, ossia $\text{rank}(A) < n$, allora il problema di PL può essere risolto studiando in sua vece un diverso problema di PL la cui matrice dei coefficienti si ottiene *eliminando una colonna da A*.

> Formalmente:
$$
\text{max}\{ cx : Ax \leq b \} \quad \text{con } \text{rank}(A) < n 
\quad \rightarrow \quad 
\text{max}\{ c'x'_{new} : A'x'_{new} \leq b \}.
$$
> Dove:

- $A = [A', a^n] \in \mathbb{R}^{m \times n}$,  $A' \in \mathbb{R}^{m \times n-1}$, $a^n \in \mathbb{R}^m$
- $x \in \mathbb{R}^n$, $x'_{new}\in \mathbb{R}^{n-1}$
- $c = [c', c_n] \in \mathbb{R}^n$,  $c' \in \mathbb{R}^{n-1}$, $c_n \in \mathbb{R}$
- $b \in \mathbb{R}^m$

La relazione tra soluzione nuova e soluzione vecchia è:
$$
x'_{new} = x' + \beta x_{n} \quad 
\text{dove} \quad x =[x',x_{n}] \quad
\text{e} \quad
A'\beta = a^n $$
$$
x' \in \mathbb{R}^{n-1},\ x_{n} \in \mathbb{R},\ \beta \in \mathbb{R}^{(n-1)}
$$
quindi, di solito, trovato $x'_{new}$ si scrive: $x=[x'_{new},0]$ (infatti si vede subito che risolve il problema originale)

**nota**: in realtà la colonna non considerata da $A'$ potrebbe essere una qualsiasi, ma l'ho scritta non considerando l'ultima per semplicità di scrittura e lettura.

## Riferimenti utili

* [[1.1 - Modello Standard di PL]]
* [[1 - Definizione - Problema di Programmazione Lineare]]
* [[6.1 - Dimostrazione - Riduzione di variabili in un problema di PL con linealità]]
* [[6.3 - Corollario - Proprietà del problema ridotto]]
* [[6.2 - Esempio - Riduzione di variabili in un problema di PL con linealità]]