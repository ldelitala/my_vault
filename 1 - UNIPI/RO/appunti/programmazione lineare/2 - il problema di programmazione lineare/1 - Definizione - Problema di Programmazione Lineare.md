*status*: #finito
*tags*: [[RO]] [[PROGRAMMAZIONE LINEARE]] [[DEFINIZIONI RO]]

## Definizione: Problema di Programmazione Lineare

> Un problema di **Programmazione Lineare** è un _problema di ottimizzazione_ (di massimo o di minimo) caratterizzato dalle seguenti proprietà:

1. Un numero finitio $n$ di variabili reali, di solito rappresentato dal vettore $x \in R^n$.
2. la funzione obbiettivo $c(x) : R^n \rightarrow R$ è lineare ( * )
3. l'insieme ammissibile è definito da un insieme finito di vincoli lineari ( ** )

( * ) $c(x)$ è lineare solo se $\exists c \in \mathbb{R} : c(x) = cx$. Inoltre, è importante ricordare la seguente proprietà delle funzioni lineari:
$$ c\ (\alpha x\ +\ \beta y) = \alpha \cdot c\ (x)\ +\ \beta  \cdot c\ (y) \qquad \forall x,y \in R^n,\ \forall \alpha , \beta \in R $$

 ( ** ) ricordiamo che i vincoli lineari sono del tipo:
 $$
 \begin{align}
 ax=b \\ 
 ax \leq b \\
 ax \geq b \\
\end{align}
 $$

## Riferimenti utili

* [[1.1 - Modello Standard di PL]]
* [[1.1.1 - tecniche di standardizzazione dei problemi di PL]]