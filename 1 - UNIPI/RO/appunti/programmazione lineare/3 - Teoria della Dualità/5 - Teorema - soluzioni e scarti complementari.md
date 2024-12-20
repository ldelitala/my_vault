*status*: #bozza 
*tags*: [[RO]] [[PROGRAMMAZIONE LINEARE]] [[TEOREMI RO]] [[DUALITÀ]]

## Teorema: Soluzioni e Scarti Complementari

> Date due soluzioni $\bar{x}$ e $\bar{y}$, ammissibili rispettivamente per $P$ e per $D$, esse sono **ottime** *se e solo se* verificano le condizioni degli **scarti complementari**.

### Perché questo teorema è utile?

Se abbiamo una soluzione ottima di uno dei due problemi (primale o duale), questo teorema ci permette facilmente di trovare la soluzione ottima dell'altro. Questo perché potremo sfruttare la seguente deduzione:
$$
\bar{y}_{i} (b_{i} - A_{i} \bar{x}) = 0
$$
$$
\begin{align}
\bar{y}_{i} > 0 \quad  \to \quad A_{i} \bar{x} = b_{i} \\
A_{i} \bar{x} < b_{i} \quad \to \quad \quad \bar{y}_{i} = 0
\end{align}
$$

Scriverò in appunti futuri come sfruttare questa informazione, anche se a occhio è abbastanza intuibile.


## Riferimenti utili

* 