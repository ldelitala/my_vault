*status*: #bozza 
*tags*: [[RO]] [[Grafi e Reti di Flusso]] [[ALGORITMI]] [[ALGORITMI RO]]

## 2 - Algoritmo - cammini minimi successivi

1. Si inizializza uno *pseudoflusso ottimale*  ( * )
2. Finché non diventa un *flusso ammissibile* (ovvero $g(x)\neq 0$ ) ( * * ) :
	1. Si trova un *albero dei cammini minimi* sul grafo del *flusso residuo* $G_{x}$ con radice in $O_{x}$ e destinazione in $D_{x}$ ( * * * )
	2. Si seleziona il primo nodo di $D_{x}$ raggiungibile
	3. Se il nodo non è raggiungibile ($d[t]=+ \infty$) -> non esiste flusso ammissibile
	4. aumentiamo lo pseudoflusso con il cammino minimo trovato
3. -> Abbiamo trovato un flusso ammissibile ottimo

1. x=pseudoflusso_ottimale
2. while ($g(x)!=0$):
	1. (p,d)=albero_dei_cammini_minimi( $G_{x},O_{x},D_{x}$ ) (p vettore albero, d vettore costi)
	2. t = argmin {$d[i]$ :  $i \in D_{x}$}
	3. if ($d[t]=+ \infty$) then {caso = "vuoto"; break}
	4. x = aumenta_flusso(x,p,t)
3. caso = "ottimo"; (x è il flusso ottimo obv)


( * ) lo *pseudoflusso ottimale* lo si trova impostando $x_{ij}=0$ se $c_{ij} > 0$ e $x_{ij}=u_{ij}$ se $c_{ij} \leq 0$. In questo modo il grafo del flusso residuo ha solo archi di costo positivo -> il che significa che non ci sono cammini aumentanti di costo negativo -> il che vuol dire che lo pseudoflusso è ottimo. (Ora c'è da renderlo *ammissibile*)

( * * ) $g(x)$ è scritta qui: [[1.4 - Definizione - Flusso ammissibile e Valore del flusso]]

( * * * ) Ciò si fa usando un algoritmo che crea alberi di cammini minimi (obv). Se $|O_{x}|=1$, si usa semplicemente $G_{x}$. Altrimenti si crea un albero dei cammini minimi con radici multiple modificando il grafo residuo aggiungendo un nodo radice "fasullo" che è collegato a tutti i nodi appartenenti a $O_{x}$ con archi di valore nullo. 
## Riferimenti utili

* [[1.4 - Definizione - Flusso ammissibile e Valore del flusso]]
* [[1.5 - Definizione - Pseudoflusso]]
* [[1.6 - Definizione - Sbilanciamento, eccesso di flusso e difetto di flusso, nodo bilanciato]]