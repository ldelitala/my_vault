
status: #finito

tags:  [[PDP]] [[LAMBDA CALCOLO]]

## Come usarlo?

1. **Definisci la funzione ricorsiva**:

   Scrivi la funzione ricorsiva $\text{G}$, dove $\text{e}$ contiene la $\lambda$-espressione con la chiamata ricorsiva. Ad esempio:
   $$ G = \lambda f. e $$$$ e = \lambda y. (fy)y  $$
   Qui, la funzione viene applicata a \( y \) e poi il risultato viene applicato di nuovo a \( y \). In pratica, \( e \) è il corpo della funzione ricorsiva e \( G \) è la lambda-espressione in cui la funzione ricorsiva stessa diventa variabile legata per permettere il giochino della ricorsione.
   

2. **Definisci la funzione ricorsiva completa**:

   Ora utilizzi il combinatore Y per definire la funzione ricorsiva completa:
   $$
   F = Y \; G 
   $$

3. **Applica un valore alla funzione ricorsiva**:

   Infine, applica un valore \( k \) alla funzione ricorsiva e calcola il risultato:
   $$
   F \; k 
   $$


## Riferimenti

* [[il combinatore Y]]
* [[Esempio d'uso del combinatore Y]]
