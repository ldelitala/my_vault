*status*: #finito 
*tags*:  [[PDP]] [[JAVA]] [[OOP]]

## Esempio

```java
// OVERVIEW: un IntSet è un insieme di interi

public class IntSet {

	public IntSet(int capacity) {
	// REQUIRES: capacity non negativo
	// EFFECTS: crea un insieme vuoto che può ospitare capacity elementi
	}
	
	
	/**
	* Aggiunge un elemento all'insieme
	* @param elem valore intero
	* @return true se l'inserimento viene aggiunto, false se già presente
	* @throws FullSetException se l'insieme è pieno
	*/
	public boolean add(int elem) throws FullSetException {
	// REQUIRES: numero di elementi contenuti nell'insieme minore di capienza
	// EFFECTS: se elem non è presente nell'insieme lo aggiunge e 
	// restituisce true, restituisce false altrimenti
	}
	
	
	public boolean contains(int elem) {
	// REQUIRES:
	// EFFECTS: restituisce true se elem p presente nell'insieme,
	// false altrimenti
	}
}

```


## Riferimenti utili

* [[Fasi della progettazione e dello sviluppo di java]]