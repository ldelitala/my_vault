*status*: #finito 
*tags*:  [[PDP]] [[JAVA]] [[OOP]]

## Regola della Post-Condizione

> Se il metodo del _sotto-tipo_ viene chiamato con un valore valido (_Pre-Condizione_) anche per il _super-tipo_, il risultato deve essere valido per entrambi i tipi (anche se può essere diverso). Formalmente:

$$ (\text{Pre-Condizioni super-tipo } \land \text{Post-Condizioni sotto-tipo}) \Rightarrow \text{Post-Condizioni super-tipo} $$

### Esempio:

* _Post-Condizione_ del metodo _pippo_ del _super-tipo_: $Y > 20$
* _Post-Condizione_ del metodo _pippo_ del _sotto-tipo_ dopo _overriding_: $Y > 30$

Se le _Pre-Condizioni_ del super-tipo sono rispettate, si vede che quando la _Post-Condizione_ del _sotto-tipo_ è vera, lo è anche quella del _super-tipo_:

$$ \text{true} \land (Y > 30) \Rightarrow (Y > 20) $$
## Riferimenti utili

* [[Principio di Sostituzione di Liskov]]
* [[regole derivate da LSP]]
* [[Regola dei Metodi]]
* [[Regola della Pre-Condizione]]
* [[Pre-condizioni e Post-condizioni]]