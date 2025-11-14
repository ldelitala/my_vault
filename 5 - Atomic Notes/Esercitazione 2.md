*tags*: [[AGENTI BASATI SULLA RICERCA]]

![[es_2_testo.pdf]]


## Risolvo

### Navigazione di un robot
#### a) formulazione del problema
* **spazio degli stati**: definisco lo spazio degli stati come tutti gli spigoli dei rettangoli + i punti A e P (ovvero impongo che l'agente si muova solo da spigolo a spigolo in linea retta)
* **stato iniziale**: punto P
* **stato obiettivo**: punto A
2. _Azioni_: muoversi in linea retta da un punto ad un altro (visibile)
3. _Modello di transizione_: 
4. _Funzione di costo_: c(a,b)=distanza in linea d'aria dove a e b sono due stati connessi nel modello di transizione

#### b) euristica di A*
* $h(s)$= distanza in linea d'aria con P
	* è chiaramente una sottostima di $h^*(s)$
	* è un'Euristica ammissibile, infatti ogni percorso possibile è più lungo del percorso in linea d'aria
	* siccome l'euristica è ammissibile, A* è ottimale


### Scala di parole

#### a) formulazione del problema
* **spazio degli stati**: definisco lo spazio degli stati come tutte le parole di dimensione k
* **stato iniziale**: parola iniziale
* **stato obiettivo**: punto di arrivo
2. **Azioni**: cambiare una lettera
3. **Modello di transizione**: ogni stato (parola) può transitare negli stati che rappresentano parole con solo una lettera di differenza
4. **Funzione di costo**: c(parola1, parola2) = 1 per ogni parola connessa nel modello

#### b) dimensione spazio di ricerca e fattore di diramazione
* **spazio di ricerca**: lo spazio di ricerca sarà formato da tutte le parole di dimensione k
* **fattore di diramazione**: l'insieme di stati in cui una parola può transitare è un sottoinsieme di tutte le stringhe che cambiano di una sola lettera per ciascuna lettera della parola di partenza, quindi $b \leq k*25$.

#### c) Quale algoritmo di ricerca non informata usereste per ricercare una soluzione nello spazio degli stati? Discutere completezza, ottimalità, complessità delle possibili soluzioni. Inoltre, la ricerca bidirezionale sarebbe appropriata per questo problema?

##### BFS
* Completo e Ottimale
* memoria: $O(b^d)$
* tempo: $O(b^d)$
* b: abbiamo detto essere $n *k$ con $n \ll 25$
* d: circa k

##### DFS (con limite)
* è applicabile se riusciamo a spezzare i cicli
	* per farlo possiamo per esempio imporre il limite di profondità di ricerca con limite= numero di parole di lunghezza k
* siccome così l'algoritmo è sistematico allora è completo
* ottimalità: non garantità
* tempo: $O(b^m)$
* spazio: $O(b*m)$
	* dove m=numero di parole di lunghezza k

##### IDFS
* completo perché spazio degli stati finito
* ottimo rispetto al costo: sì perché costo uniforme
* tempo: $O(b^d)$
* memoria: $O(b * d)$

#### d) Si proponga un’euristica da usare con un algoritmo di ricerca informata. Si dica se l’euristica è ammissibile e se ne discuta la completezza e l’ottimalità (con ricerca “ad albero”)

* possiamo prendere come euristica:
	* h(parola)= il numero di lettere che sono diverse con la parola obbiettivo
	* in quanto se il passaggio da uno stato all'altro richiede cambiare minimo una lettera allora il percorso soluzione avrà minimo quel numero di passaggi
* ammissibile: sì
	* se non ci fosse il limite che le stringhe debbano essere parole allora $h$ sarebbe uguale a $h^*$
* con $A^*$ si ottiene una ricerca completa e ottimale

#### e) Considerare il caso della ricerca locale.

* assumiamo h uguale a prima
	* in alcuni casi bisogna allontanarsi dalla parola obiettivo per trovare la catena


continua in [[Esercitazione 2 pt2]]

## Riferimenti utili

* [[Problemi di ricerca]]
* [[Euristica ammissibile]]
* [[Algoritmi di ricerca non informata]]
* [[Algoritmi di ricerca informata]]
* [[lista di algoritmi di ricerca non informata]]