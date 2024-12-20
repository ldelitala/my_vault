
status: #finito 

tags:  [[PDP]] [[LAMBDA CALCOLO]]

## Esempio completo: calcolo del Fattoriale di 3 usando il Combinatore Y

Consideriamo la funzione fattoriale definita come:

### 1. Definizione della funzione fattoriale

La funzione ricorsiva \( G \) è:
$$
G = \lambda f. \lambda n. (\text{if } n = 0 \text{ then } 1 \text{ else } n \times (f \; (n - 1)))
$$

_PS: ovviamente questo non è puro lambda calcolo, ma almeno è leggibile_

### 2. Definizione della funzione fattoriale completa
   
Utilizzando il combinatore Y, definiamo:
$$
F = Y \; G 
$$

### 3. Calcolo di \( F \; 3 \)

$$
F \; 3 = (Y \; G) \; 3 = G \; (Y \; G) \; 3 = G \; F \; 3
$$

### 4. Sostituzione di \( G \)

Sostituendo \( G \):
$$
G \; F \; 3 = (\lambda f. \lambda n. \text{if } n = 0 \text{ then } 1 \text{ else } n \times (f \; (n - 1))) \; F \; 3
$$

### 5. Applicazione alla funzione

Qui, \( f \) è sostituito con \( F \) e \( n \) con \( 3 \):
$$
= \lambda n. \text{if } n = 0 \text{ then } 1 \text{ else } 3 \times (F \; (3 - 1))
$$

### 6. Continuando con \( F \; 2 \)

$$
= 3 \times (F \; 2)
$$

### 7. Ripetizione del processo

$$
F \; 2 = G \; F \; 2 = \lambda n.( \text{if } n = 0 \text{ then } 1 \text{ else } 2 \times (F \; (2 - 1)))
$$
$$
= 2 \times (F \; 1)
$$

### 8. Continuazione fino a 0

$$
F \; 1 = 1 \times (F \; 0)
$$
$$
F \; 0 = 1 \quad (\text{base case})
$$

### 9. Calcolo finale

Ora possiamo sostituire i risultati:
$$
F \; 1 = 1 \quad \Rightarrow \quad F \; 2 = 2 \times 1 = 2
$$
$$
F \; 3 = 3 \times 2 = 6
$$
$$
F \; 4 = 4 \times 6 = 24
$$
## Riferimenti

* [[il combinatore Y]]
* [[Come usare il combinatore Y]]