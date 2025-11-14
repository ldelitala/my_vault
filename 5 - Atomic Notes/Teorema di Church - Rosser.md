*status*: #finito 
*tags*:  [[PDP]] [[LAMBDA CALCOLO]]

## Teorema di Church - Rosser (o Proprietà di Confluenza)

* Se \( e \) è una &lambda;-espressione 
* e se (&exist; e1,e2) :
$$
e \equiv_{\beta} e_1 \land e \equiv_{\beta} e_2 \land e_1 \not\equiv_{\alpha} e_2
$$

* allora \( \exists e' \) tale che 
$$
e_1 \equiv_{\beta} e' \land e_2 \equiv_{\beta} e'
$$


## Riferimenti utili

* 