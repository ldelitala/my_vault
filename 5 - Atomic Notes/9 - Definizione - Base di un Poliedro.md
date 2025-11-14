*status*: #bozza 
*tags*: [[RO]] [[PROGRAMMAZIONE LINEARE]] [[DEFINIZIONI]]

## Definizione: base di un Poliedro

##### Base
> Un insieme di indici $B$, di cardinalità $n$, tale che la sottomatrice quadrata $A_{B}$ sia invertibile viene detto una *base*.

##### Matrice di Base
> $A_{B}$ viene detta *matrice di base*.

##### Soluzione di Base
> $\bar{x}$ tale che $\bar{x}=A_{B}^{-1}b_{B}$ è detta *soluzione di base*

##### Soluzione di Base ammissibile e non ammissible
> Se $\bar{x} \in P$ allora è una *soluzione ammissibile* per $P$, altrimenti (se $\bar{x} \not\in P$) si dice *soluzione non ammissibile*.

##### Soluzione di Base degenere o non degenere
> Se la soluzione di base è definita solo dai vincoli di base, allora è detta *non degenere*, altrimenti è detta *degenere*.

>  In termini algebrici se $A_{i}x = b_{i}$ per un qualche $i \not\in B$, allora la soluzione si dice *degenere*, altrimenti ($A_{i}x<b_{i}, \forall i \not\in B$) è detto *non degenere*.

Il punto di definire degenere o non degenere è che ci permette di capire se una soluzione è trovata da una sola base o se esistono più basi che danno la stessa soluzione.

#### Note
Il concetto di base è potentissimo perché, siccome per il [[9.1 - Corollario - punto estremo di un Poliedro]] sappiamo che se $\bar{x}$ è una soluzione ammissibile allora è un estremo del Poliedro e la soluzione di un problema di PL si trova quasi sempre in un estremo (tranne quando il problema è [[3 - Teorema - condizione di illimitatezza superiore al problema di PL|superiormente illimitato]] o quando ci sono più soluzioni ottime)

## Riferimenti utili

* [[9.1 - Corollario - punto estremo di un Poliedro]]
* [[3 - Teorema - condizione di illimitatezza superiore al problema di PL]]