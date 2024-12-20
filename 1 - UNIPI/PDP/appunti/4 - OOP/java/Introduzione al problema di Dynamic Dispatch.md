*status*: #finito
*tags*:  [[PDP]] [[JAVA]] [[OOP]]

## Introduzione al problema

In caso di overriding, se il _riferimento_ all'oggetto è di tipo diverso all'oggetto stesso (vedi esempio), c'è bisogno di un algortmo per decidere quale sia il metodo giusto. Questo metodo è il __Dynamic Dispatch__. Infatti :

> Il _Dynamic Dispatch_ è un processo che permette di decidere quale metodo invocare a runtime basandosi sul _tipo specifico dell'oggetto_ su cui si sta chiamando il metodo, piuttosto che sul _tipo della variabile_ a cui fa riferimento l'oggetto. 

Questo significa che anche se una variabile è di un tipo generico (come una classe base), può comunque riferirsi a un oggetto di una classe derivata.

## Riferimenti utili

* [[tabella dei metodi e sharing strutturale in java]]
* [[esempio di dynamic dispatch in java]]