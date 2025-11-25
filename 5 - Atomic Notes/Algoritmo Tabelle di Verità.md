*tags*: [[AGENTI BASATI SULLA CONOSCENZA]] [[METODI DI RISOLUZIONE SAT]]

>[!question] A cosa serve?
> determinare se $\alpha$ è conseguenza logica della [[Base di conoscenza KB]]

> [!example] funzionamento 
> 1) enumera tutte le possibili interpretazioni della KB 
> 	* k simboli -> $2^k$ interpretazioni
> 	
> 2) Per ciascuna interpretazione:
> 	* Se non soddisfa KB -> OK
> 	* Se soddisfa KB -> si controlla che soddisfi anche $\alpha$
> 
> 3) Se anche solo una interpretazione che soddisfa KB non soddisfa anche $\alpha$ allora la risposta sarà NO

## Riferimenti utili

* [[Model Checking]]