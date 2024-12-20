*status*: #bozza 
*tags*: [[RO]] [[Grafi e Reti di Flusso]] [[Cammini minimi]] [[ESERCIZI RO]]

## Compito1-es2

![[compito1_es2.png]]

A) II
B) II
C) I
D) II    -> $d= [4, 1, 4, 1, 1, 0, 3]$ che ha costo 14

**E)** Modificare il costo del minor numero possibile di archi fuori dall’albero dato affinché quello dato sia l’unico albero dei cammini minimi. È possibile modificare il costo di due soli archi dell’albero, mantenendo i costi non negativi, affinché quello dato sia un albero dei cammini minimi? Giustificare la risposta.
##### Svolgimento  

**Vettore dei costi dell’albero**:  $d = [5, 7, 4, 1, 1, 0, 4]$  
**Costo totale**: $22$  

#### Verifica delle condizioni di Bellman-Ford per gli archi non appartenenti all'albero:  

1. $d_{2} \leq d_{6} + c_{6,2}$  
   $7 \nleq 0 + 1$ → **falso**

2. $d_{5} \leq d_{2} + c_{2,5}$  
   $1 \leq 7 + 3$ → **vero**

3. $d_{4} \leq d_{6} + c_{6,4}$  
   $1 \leq 0 + 1$ → **vero**

4. $d_{7} \leq d_{4} + c_{4,7}$  
   $4 \nleq 1 + 2$ → **falso**

5. $d_{1} \leq d_{7} + c_{7,1}$  
   $5 \leq 4 + 1$ → **vero** (ma attenzione durante l'aggiornamento di $d_{7}$)
###### Caso 1: Modifica degli archi **fuori dall'albero**  
Affinché quello dato sia l’unico albero dei cammini minimi, è necessario che i valori degli archi fuori dall’albero rispettino fortemente le condizioni di Bellman.  
Le modifiche richieste sono:  
- $c_{6,2} > 7$  
- $c_{6,4} > 1$  
- $c_{4,7} > 3$  
- $c_{7,1} > 1$

###### Caso 2: Modifica degli archi **dell'albero**  
Per modificare gli archi dell’albero affinché quello dato sia un albero dei cammini minimi, occorre rendere **vere** le condizioni attualmente false:  
$$
\begin{cases}
d_{2} = c_{6,5} + c_{5,3} + c_{3,2} \leq d_{6} + c_{6,2} \\
d_{7} = c_{6,7} \leq d_{4} + c_{4,7} = c_{6,5}+c_{5,4}+c_{4,7}
\end{cases}
 \quad \to \quad 
 \begin{cases}
c_{6,5} + c_{5,3} + c_{3,2} \leq 1 \to 1+3+3 \leq 1\\
c_{6,7} \leq c_{6,5}+c_{5,4}+2 \to 4 \leq 1 + 0 +2
\end{cases}
$$
notiamo che per la prima condizione, $c_{6,5}$ non può essere aumentata, quindi nella seconda condizione dobbiamo modificare $c_{5,4}=1$. Notiamo però che per rendere la prima condizione vera serve per forza portare $c_{5,3},c_{3,2}=0$. È quindi impossibile modificare solo due archi per rendere entrambe le condizioni vere.

## Riferimenti utili

* 