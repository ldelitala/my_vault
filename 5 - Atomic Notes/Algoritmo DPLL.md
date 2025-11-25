*tags*: [[AGENTI BASATI SULLA CONOSCENZA]] [[METODI DI RISOLUZIONE SAT]]

>[!question] A cosa serve?
> partendo da una $KB$ in [[Forma Normale Congiuntiva FNC o CNF]] risolve il problema di soddisfacibilità di una formula, migliornado [[Algoritmo Tabelle di Verità]] usando l'euristica.

>[!note] Euristiche:
> 1) [[Terminazione anticipata]]
> 2) [[Letterali Puri]]
> 3) [[Clausole Unitarie]]

>[!example] Funzionamento dell'algoritmo DPLL
>
> 1) Si parte da una **formula in CNF** e da una lista di tutti i simboli proposizionali.
>
> 2) Si verifica lo **stato delle clausole** rispetto al modello parziale corrente:
>    * Se **tutte le clausole** sono vere, l'algoritmo restituisce **True** (la formula è soddisfacibile).
>    * Se **almeno una clausola** è falsa, l'algoritmo restituisce **False** (la formula non è soddisfacibile).
>
> 3) Si applicano le **euristiche per ridurre lo spazio di ricerca**:
>    * Si cerca un **simbolo puro** tra i simboli rimanenti:
>        * Se ne esiste uno, lo si assegna al valore appropriato (**True** se positivo, **False** se negativo) e si richiama ricorsivamente l'algoritmo con il simbolo rimosso dalla lista.
>    * Altrimenti, si cerca una **clausola unitaria**:
>        * Se ne esiste una, il suo letterale non assegnato viene obbligatoriamente assegnato (**True** se positivo, **False** se negativo) e si richiama ricorsivamente l'algoritmo.
>
> 4) Se non ci sono simboli puri né clausole unitarie, si prende il **primo simbolo** della lista e si esplorano entrambe le assegnazioni possibili:
>    * **True** per il simbolo e si richiama ricorsivamente l'algoritmo sul resto dei simboli.
>    * **False** per il simbolo e si richiama ricorsivamente l'algoritmo sul resto dei simboli.
>
> 5) L'algoritmo termina quando tutte le clausole sono state valutate o quando si trova una clausola falsa, restituendo il risultato finale.

>[!info] Caratteristiche
> * è **completo** e *termina sempre*
> * ci sono tecniche per migliorare ulteriormente l'algoritmo

>[!question] Curiosità
> Il nome deriva dai creatori
>  DPLL: Davis, Putman, e poi Lovemann, Loveland

## Riferimenti utili

* [[Base di conoscenza KB]]