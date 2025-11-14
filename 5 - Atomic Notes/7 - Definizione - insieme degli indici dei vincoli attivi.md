*status*: #bozza 
*tags*: [[RO]] [[PROGRAMMAZIONE LINEARE]] [[DEFINIZIONI]] [[DEFINIZIONI PURE RO]]

## Definizione: *insieme degli indici dei vincoli attivi*

> Dato un punto $\bar{x} \in P$, i vincoli che vengono soddisfatti da $\bar{x}$ come uguaglianze vengono detti vincoli attivi in $\bar{x}$. Indichiamo con $I(\bar{x})$ l'insieme degli indici dei vincoli attivi.

> Formalmente:

$$
I(\bar{x}) = \{i: A_{i}\bar{x}=b_{i} \}
$$
#### Osservazioni
Osserviamo che $P_{I(\bar{x})}$ è una faccia del poliedro che contiene $\bar{x}$. In generale, qualsiasi $I \subseteq I(\bar{x})$ definisce una faccia $P_{I}$ che contiene $\bar{x}$. Chiaramente, $I(\bar{x})$ definisce la faccia minimale tra tutte queste.

## Riferimenti utili

* [[10 - Faccia di un Poliedro]]
* [[4 - Poliedro]]