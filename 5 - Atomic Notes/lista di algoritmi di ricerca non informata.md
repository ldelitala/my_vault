*tags*: [[AGENTI BASATI SULLA RICERCA]]

| **Algoritmo**                                     | **Descrizione**                                                       | **Completezza**      | **Ottimalità**        | **Tempo**                              | **Memoria**                         | **Condizioni / Osservazioni importanti**                                                                                |
| ------------------------------------------------- | --------------------------------------------------------------------- | -------------------- | --------------------- | -------------------------------------- | ----------------------------------- | ----------------------------------------------------------------------------------------------------------------------- |
| **Ricerca in ampiezza (BFS)**                     | Esplora i nodi in ordine di profondità crescente                      | ✅                    | ✅ (se costi uniformi) | $O(b^{d})$                             | $O(b^{d})$                          | Trova sempre la soluzione più breve se ogni passo ha costo uguale. Può diventare molto costosa in memoria.              |
| **Ricerca in profondità (DFS)**                   | Esplora un cammino fino in fondo prima di tornare indietro            | ✅ (se spazio finito) | ❌                     | $O(b^{m})$                             | $O(bm)$                             | Può restare bloccata in cicli infiniti. Bassa memoria ma può trovare soluzioni non minime.                              |
| **Ricerca a profondità limitata**                 | Come DFS ma con un limite di profondità $l$                           | ❌ (se $l < d$)       | ❌                     | $O(b^{l})$                             | $O(bl)$                             | Evita cicli infiniti, ma può fallire se la soluzione è più profonda del limite.                                         |
| **Ricerca con approfondimento iterativo (IDDFS)** | Combina BFS e DFS aumentando progressivamente il limite di profondità | ✅                    | ✅ (se costi uniformi) | $O(b^{d})$                             | $O(bd)$                             | Ripete più volte la ricerca in profondità, ma con un costo totale simile alla BFS e consumo di memoria molto inferiore. |
| **Ricerca del costo uniforme (UCS)**              | Espande il nodo con il **costo cumulativo** minimo $g(n)$             | ✅ (se i costi > 0)   | ✅                     | $O(b^{\lceil C^*/\varepsilon \rceil})$ | Dipende dal numero di nodi generati | Estende BFS a costi variabili; garantisce la soluzione a costo minimo. Usa una coda di priorità (fronte).               |
| **Ricerca bidirezionale** | Esegue due ricerche BFS contemporanee, una dallo stato iniziale e una dallo stato obiettivo, fino all’incontro | ✅ | ✅ (se costi uniformi) | $O(b^{d/2})$ | $O(b^{d/2})$ | Molto efficiente in teoria, ma richiede di conoscere esplicitamente lo stato obiettivo e di poter invertire le azioni. |

---

**Legenda**  
- $b$: fattore di diramazione (numero medio di successori per nodo)  
- $d$: profondità della soluzione ottimale  
- $m$: profondità massima dello spazio di ricerca  
- $C^*$: costo della soluzione ottimale  
- $\varepsilon$: costo minimo di un’azione  


## Riferimenti utili

* [[Algoritmi di ricerca informata]]