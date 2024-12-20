parte di [[DEFINIZIONI RO]]

## Programmazione Lineare

### Modello Standard di PL
$$max\{\ cx\ :\ Ax \leq b\ \}$$

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