*status*: #finito 
*tags*:  [[PDP]] [[OOP]] [[JAVA]]

## Regola della Pre-Condizione

> Ogni volta che la _Pre-Condizione_ del metodo del _super-tipo_ è soddisfatta, deve essere soddisfatta anche la _Pre-Condizione_ del metodo del _sotto-tipo_. Formalmente:

$$ \text{Pre-Condizioni super-tipo} \Rightarrow \text{Pre-Condizioni sotto-tipo} $$

### Esempio:

* _Pre-Condizione_ del metodo _pippo_ del _super-tipo_: $X > 10$ 
* _Pre-Condizione_ del metodo _pippo_ del _sotto-tipo_ dopo _overriding_: $X > 5$

In questo esempio, ogni volta che la _Pre-Condizione_ del metodo del _super-tipo_ è soddisfatta, lo è anche quella del metodo del _sotto-tipo_:

$$ (X > 10) \Rightarrow (X > 5) $$

## Riferimenti utili

* [[Principio di Sostituzione di Liskov]]
* [[regole derivate da LSP]]
* [[Regola dei Metodi]]
* [[Regola della Post-Condizione]]
* [[Pre-condizioni e Post-condizioni]]