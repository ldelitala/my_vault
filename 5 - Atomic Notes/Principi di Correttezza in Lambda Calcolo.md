*status*: #finito
*tags*:  [[PDP]] [[SISTEMA DEI TIPI]]

## Principi di Correttezza
### Progresso (in Lambda)
$$
\text{Se } \emptyset \vdash e: \tau, \text{ allora } e \text{ è un valore oppure } e \rightarrow e' \text{ per una qualche espressione } e'.
$$

### Conservazione (in Lambda)
$$
\text{Se } \Gamma \vdash e: \tau \text{ e } e \rightarrow e', \text{ allora } \Gamma \vdash e': \tau.
$$

### Substitution Lemma
I tipi sono preservati dall’operazione di sostituzione.

$$
(\Gamma, \ x: \tau_1) \vdash e: \tau
$$
$$
\Gamma \vdash e_1 : \tau_1
$$
$$
\Gamma \vdash e \{ x = e_1 \} : \tau
$$

## Riferimenti utili

* [[Principi di Correttezza]]
* [[Ambiente dei Tipi in Lambda Calcolo]]