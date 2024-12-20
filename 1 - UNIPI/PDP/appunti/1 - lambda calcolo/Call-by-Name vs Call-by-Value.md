*status*: #finito
*tags*:  [[PDP]] [[LAMBDA CALCOLO]]

## Call-by-Name vs Call-by-Value

In sintesi:

- **Call-by-Name**: Si applica sempre l’operazione più esterna possibile, ritardando l'operazione interna finché non è necessaria.
  
- **Call-by-Value**: Si procede sempre con l’operazione più interna, valutando i parametri prima di applicarli.

### Esempio in Lambda Calcolo

Consideriamo la seguente funzione:
$$ (λx.x)(λx.(λy.y)k)$$

$$ \text{call by name: } $$
$$ \underline{(λx.x)(λx.(λy.y)k)} \equiv_{\beta} (λx.(λy.y)k) \equiv_{\beta} λx.k $$
$$ \text{call by value: } $$
$$ (λx.x)(λx.\underline{(λy.y)k}) \equiv_{\beta} (λx.x)(λx.k) \equiv_{\beta} λx.k $$

_Nota bene_: in questo esempio banale il risultato è lo stesso, ma potrebbero esistere casi in cui varia. In particolare, il prof mette spesso nel compito esercizi in cui, con uno dei due metodi, la lambda espressione entra in un loop mentre con l'altro no.



## Riferimenti utili

* 