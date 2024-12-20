*status*: #finito
*tags*:  [[PDP]] [[OOP]]

## Diamond Problem

> Il **diamond problem** è un problema di ambiguità nell’ereditarietà multipla. Si verifica quando una classe deriva da due classi che condividono un antenato comune, causando potenziali conflitti se le classi intermedie sovrascrivono metodi o proprietà dell’antenato.

![[diamond_problem.png]]

### Soluzioni

#### C++ 
-> **Virtual Inheritance**: Quando una classe viene estesa usando *virtual*, il compilatore di C++ sa che, in caso di **diamond problem**, deve creare una sola copia della classe antenata.

![[diamond_problem_c.png]]
![[diamond_problem_c2.png]]

#### Java, Python e Dart
-> La soluzione adottata per la [[soluzioni del problema di doppia implementazione|doppia implementazione]] risolve anche il **diamond problem**. 


## Riferimenti utili

* [[Introduzione al problema di Multiple Inheritance]]
* [[soluzioni del problema di doppia implementazione]]