*status*: #finito #spicciolo
*tags*: [[PDP]] [[SISTEMA DEI TIPI]]

## Ambiente dei Tipi in Lambda Calcolo

### Sintassi
L’ambiente dei tipi è una funzione (di dominio finito) che associa nomi a tipi (in pratica è una tabella). Si scrive così:

$$
\Gamma = x_1: \tau_1, \ x_2: \tau_2, \ \dots, \ x_k: \tau_k
$$

e useremo la funzione

$$
\Gamma (x_i) = \tau_i
$$

che restituisce il tipo **𝜏𝑖** dato il valore **𝑥𝑖**.

La notazione

$$
\Gamma, \ x: \tau
$$

indica che stiamo aggiungendo l'associazione **𝑥: 𝜏** all'ambiente.

La notazione:

$$
\Gamma \vdash e: \tau
$$

è usata per indicare che l’espressione **𝑒** ha tipo **𝜏** nell’ambiente di tipo **Γ**. (Ovvero, se valuti l'espressione con le associazioni nome-valore dell'ambiente, trovi che ha tipo **𝜏**.)




## Riferimenti utili

* [[Principi di Correttezza in Lambda Calcolo]]