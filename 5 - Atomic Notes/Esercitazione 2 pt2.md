*tags*: [[AGENTI BASATI SULLA RICERCA]]

![[es_2_testo.pdf]]
### Confronto di euristiche ammissibili

>[!question] 1) Confronto di euristiche ammissibili basato su proprietà matematiche
>Siano date due euristiche ammissibili: h1 e h2. Quali delle seguenti euristiche sono ammissibili? Motivare le risposte.

h ammissibile <-> $h(n) \leq h^*(n) \quad \forall n$

##### a. $h(s) = h1(s) + h2(s)$ 
$$
\begin{align}
h_{1}(n) \leq h^*(n) \quad \forall n \\
h_{2}(n) \leq h^*(n) \quad \forall n
\end{align}
$$
Non garantisce che
$$
h_{1}(n) + h_{2}(n) \leq h^*(n) \quad \forall n
$$
**Conclusione:** Non sempre ammissibile, perché la somma può superare il costo reale.

##### b. $h(s) = |h1(s) − h2(s)|$, dove $| . |$ indica il valore assoluto 
$$
h_1(n) \leq h^*(n), \quad h_2(n) \leq h^*(n)
$$
Allora:
$$
-|h^*(n)| \leq h_1(n) - h_2(n) \leq h^*(n)
$$
Prendendo il valore assoluto:
$$
0 \leq |h_1(n) - h_2(n)| \leq h^*(n)
$$
**Conclusione:** Sempre ammissibile.


##### c. $h(s) = \max(h1(s), h2(s)) - 2$ 
$$
h_1(n) \leq h^*(n), \quad h_2(n) \leq h^*(n)
$$
Allora:
$$
\max(h_1(n), h_2(n)) \leq h^*(n) \implies \max(h_1(n), h_2(n)) - 2 \leq h^*(n) - 2
$$
**Conclusione:** Ammissibile?  
- Dipende dal contesto: se $h^*(n) \ge 2$ allora sì, altrimenti può diventare negativa, **ma resta ammissibile** perché ammissibilità richiede solo $h(n) \le h^*(n)$, non che sia positiva.  


##### d. $h(s) = 2h1(s) + h2(s)/2$
$$
h_1(n) \leq h^*(n), \quad h_2(n) \leq h^*(n)
$$
Allora:
$$
h(n) = 2 h_1(n) + \frac{h_2(n)}{2} \le 2 h^*(n) + \frac{h^*(n)}{2} = \frac{5}{2} h^*(n)
$$
**Conclusione:** Non sempre ammissibile, perché può superare $h^*(n)$.


##### e. $h(s) = (h1(s) + h2(s))/2$
$$
h_1(n) \le h^*(n), \quad h_2(n) \le h^*(n)
$$
Allora:
$$
h(n) = \frac{h_1(n) + h_2(n)}{2} \le \frac{h^*(n) + h^*(n)}{2} = h^*(n)
$$
**Conclusione:** Sempre ammissibile.


> [!question] Combinazione lineare di euristiche ammissibili
> Questo caso merita un discorso a parte. 
> Sia h1 l’euristica della somma delle distanze Manhattan di ogni numero dalla sua destinazione per il gioco dell’otto. Si consideri l’euristica $h2=2*h1+3$ 
> 
> a. h2 è una euristica ammissibile? 
> b. Possiamo garantire che troverà una soluzione ottimale se usata con un algoritmo Best First? 
> c. Se si è risposto SI alle prime due domande, la ricerca sarà più efficiente che con h1? 
> 
> Motivare le risposte.

#### a)

* non possiamo dire se h2 è ammissibile. 

#### b) 
* no
## Riferimenti utili

* [[Esercitazione 2]]
* [[Euristica ammissibile]]