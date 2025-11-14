parte di [[DEFINIZIONI]] [[RO]]

## Grafi e Reti di Flusso

### Domanda e Offerta
$$
D=\{i \in N : b_{i} > 0\} \qquad O=\{i \in N: b_{i} < 0\}
$$
#### Domanda globale e Offerta globale

$$
D_{G}=\sum_{i \in D}b_{i} \qquad O_{G}=\sum_{i \in O}b_{i}
$$
* [[4.2 - Definizione - Domanda Globale e Offerta Globale]]

### Vincoli di conservazione del flusso (!!!!)

$$
\sum_{(j,i) \in BS(i)}x_{ji} - \sum_{(i,j) \in FS(i)} x_{ij}=b_{i}, \quad \forall i \in N
$$
* [[4.3 - Definizione - Vincoli di Conservazione del Flusso e Vincoli di capacità sugli archi]]

#### Condizione necessaria alla conservazione del flusso derivata dai vincoli

$$
D_{G}=-O_{G} \qquad \to \qquad \sum_{i \in D}b_{i} = - \sum_{i \in O}b_{i} \qquad \to \qquad \sum_{i \in N}b_{i}=0
$$
* [[4.2 - Definizione - Domanda Globale e Offerta Globale]]
### Vincoli di capacità sugi archi (!!!!)

$$
 l_{ij} \leq x_{ij} \leq u_{ij} \qquad \forall (i,j) \in A
$$

* [[4.3 - Definizione - Vincoli di Conservazione del Flusso e Vincoli di capacità sugli archi]]

### Flusso ammissibile (!!!!)

* $0 \leq x_{ij} \leq u_{ij} \quad \forall (i,j) \in A$                           -> (*vincoli di capacità*)
* $\sum_{(j,i) \in BS(i)}x_{ji} - \sum_{(i,j) \in FS(i)} = b_{i} \qquad i \in N$ -> (*principio di conservazione*)

#### Definizione alternativa di flusso ammissibile usando lo pseudoflusso

$$
g(x)= \sum_{i \in O_{x}}e_{x}(i) = - \sum_{j \in D_{x}}e_{x}(i)
$$

* [[4.4 - Definizione - Flusso ammissibile e Valore del flusso]]

### Sbilanciamento (!)
$$
e_{x}(i)= \sum_{(j,i) \in BS(i)}x_{ji}- \sum_{(i,j) \in FS(i)} x_{ij}- b_{i}
$$
#### Eccesso di flusso
$$
O_{x}=\{i \in N: e_{x}(i) > 0\}
$$
#### Difetto di flusso

$$
D_{x}= \{i \in N: e_{x}(i) < 0\}
$$
#### Nodo Bilanciato

$$
i \in N : e_{x}(i)=0 \qquad  (i \not\in D_{x}, \ i \not\in O_{x})
$$

* [[4.6 - Definizione - Sbilanciamento, eccesso di flusso e difetto di flusso, nodo bilanciato]]

### Problema del flusso massimo (!!!!!)

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
* [[3 - Definizione - Problema del flusso massimo]]
### Problema del flusso di costo minimo (!!!!!)

$$
\text{min}\{cx : Ex=b,\ l \leq x \leq u \} 
$$
ps Ex=b rappresenta i vincoli di conservazione del flusso

* [[4 - Definizione - Problema del flusso di costo minimo]]


## Programmazione Lineare

### Modello Standard di PL (!!!!!)
$$max\{\ cx\ :\ Ax \leq b\ \}$$
* [[1.1 - Modello Standard di PL]]

#### Direzione ammissibile

$$
\text{Dato } \bar{x} \in P \text{, se vale :}
$$
$$
A_{i}(\bar{x}+\lambda \xi)= A_{i}\bar{x} + \lambda A_{i}\xi \leq b_{i} \ , \qquad \forall \lambda \in [0,\bar{\lambda}] \ , \qquad \bar{\lambda} >0 \ , \qquad i=1,\dots,m
$$
$$
\text{allora } \xi \text{ è detto direzione ammissibile per } \bar{x}
$$

### Problema Duale associato al Primale (!!!!)

$$
\text{Problema Primale} \to \text{Problema Duale}

$$
$$
\text{max}\{c^Tx : Ax \leq b,\ x \geq 0\}
 \ \to \ 
\text{min}\{y^Tb: y^TA^t \geq c,\ y \geq 0\} \\
$$
* [[1.1 - Definizione - il Problema Duale associato]]

### Condizione degli scarti complementari (!!!!)

$$
\bar{y}_{i}(b_{i}-A_{i} \bar{x})=0 \quad \forall i
$$

* [[5.1 - Definizione - Soluzioni complementari e Scarti Complemetari]]

### Insieme complementare della Base
$$
N = \{1,\dots,m\} / B
$$
* [[6.1 - Definizione - Insieme complementare alla Base]]


### Soluzione Duale associata ala base (!!!!!)

$$
\bar{y}=[ \ y_{B} \ , \ y_{N} \ ]=[ \ c \ (A^t_{B})^{-1} \ , \ 0 \ ]
$$

* [[6.2 -  Definizione - Soluzione Duale associata alla Base]]

### Insieme degli indici dei vincoli attivi

$$
I(\bar{x}) = \{i: A_{i}\bar{x}=b_{i} \}
$$
* [[7 - Definizione - insieme degli indici dei vincoli attivi]]

### Cono di recessione associato ad una base

$$
 \text{rec}(P_{B})=\{x:A_{B}x \leq 0\}
$$
* [[9.2 - Definizione - Cono di recessione associato ad una base]]


## Programmazione Lineare Intera

### Problema di Programmazione Lineare Intera
$$
\text{max }\{ \ cx: Ax \leq b , \ x \in \mathbb{Z}^n \ \}
$$
* [[1 - Definizione - Problema di Programmazione Lineare Intera (PLI)]]

## Elementi Grafici
### Iperpiano
$$ P_{i} = \{\ x\ :\ ax=0\ \} \qquad a,x \in R^{n} $$
### Semispazio

$$ S_{i} = \{\ x\ :\ ax \leq 0 \} \quad \text{or} \quad S_{i} = \{\ x\ :\ ax \geq 0 \}$$
### Poliedro
$$P = \{\ x\ :\ Ax \leq b \}$$
### Insieme Convesso

$$ ∀x,y∈S,  ∀λ∈[0,1],\ \text{si ha:}\ \ λx+(1−λ)y∈S. $$
### Cono

$$\forall x \in S, \; \forall \alpha \geq 0, \; \alpha x \in S$$
#### Cono Convesso Poliedrico
$$\{\ x\ :\ Ax \leq 0\ \}$$
### Direzione di Recessione di un Poliedro
$$x + \lambda d \in P \quad \forall x \in P, \; \forall \lambda \geq 0$$
### Inviluppo Conico
Sia $V$ un insieme finito di vettori $\{ v_1,v_2,...,v_t\} \subset \mathbb{R}^n$ 
$$\text{cono}(V) = \{\ v = \sum^t_{i=1} a_i v_i\ :\ a_i \geq 0 \quad i=1,\text{...},t \} $$
### Inviluppo Convesso
$$ \text{conv}(S) = \bigcap_{C \subseteq S, C \text{ convesso}}C$$
