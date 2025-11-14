*tags*: [[introAI]] [[DEFINIZIONI]]

## Problemi di ricerca subottima

### Ricerca Beam
* si migliora il costo della frontiera mantenendo solo i k nodi migliori

### IDA*: Approfondimento iterativo applicato ad A*
* combina una ricerca in profondità con A*: 
	1. ricerca in profondità finché $f(n)$ è minore di un certo valore $f*$. Se un nodo ha valore $f(n) \geq f*$ allora non lo espande. 
	2. Se alla fine della ricerca in profondità ha trovato il goal ---> abbiamo fatto
	3. Altrimenti, aggiorna il valore $f*$ ad un valore maggiore
	4. Ripeti la ricerca in profondità partendo da tutti i nodi che non sono ancora stati espansi aka torna al passo 1

### RBFS: Ricerca Best-First Ricorsiva
* in poche parole è una ricerca best-first dove però cerchi di ricordarti sempre quale siala "seconda strada migliore". Quando seguendo la normale strada best-first trovi solo nodi con euristica maggiore della seconda strada migliore allora vuol dire che probabilmente nella "seconda strada migliore" c'è in realtà un percorso più efficente. L'algoritmo best first quindi si interrompe e ricomincia da lì.

### SMA*: Memory Bounded A*
* occupa tutta la memoria poi quando la memoria è finita dimentica via via i nodi peggiori


## Riferimenti utili

* 