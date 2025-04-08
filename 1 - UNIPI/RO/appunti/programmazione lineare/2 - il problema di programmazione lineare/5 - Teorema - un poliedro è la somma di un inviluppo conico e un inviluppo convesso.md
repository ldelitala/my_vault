*status*: #bozza 
*tags*: [[RO]] [[PROGRAMMAZIONE LINEARE]] [[TEOREMI RO]]

## Teorema - un poliedro è la somma di un inviluppo conico e un inviluppo convesso

> L'insieme $P \in \mathbb{R}^n$ è un **poliedro** *se e solo se* esistono un insieme di punti $X$ e un insieme di vettori $V$ tali per cui è possibile descrivere $P$ come la somma dell'*inviluppo convesso* di $X$ e dell'*inviluppo conico* di $V$.

> Formalmente:

$$ P \subseteq \mathbb{R}^n \text{ è un poliedro} \quad \leftrightarrow \quad \exists X = \{x_1,...,x_t\},\ \exists V = \{v_1,...,v_s\} : P = \text{conv}(X) + \text{cono}(V)$$
**Proprietà del Teorema**:
1. $\text{cono}(V) = \text{rec}(P)$.
2. $X$ è l'insieme dei vertici di $P$
3. $conv(X)$ è il più piccolo poliedro che contiene i vertici di $X$
4. se $\text{rec}(P) = 0$ allora il Poliedro è [[6 - Insieme Compatto|compatto]].


## Riferimenti utili

* [[6 - Insieme Compatto]]
* [[5 - Insieme Convesso]]
* [[9.1 - Inviluppo Conico]]
* [[9.2 - Inviluppo Convesso]]
* [[7 - Cono]]