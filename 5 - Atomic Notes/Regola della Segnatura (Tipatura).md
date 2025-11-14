*status*: #finito
*tags*:  [[PDP]] [[OOP]] [[JAVA]]

## Regola della Segnatura (Tipatura)

> Gli oggetti del _sotto-tipo_ devono implementare tutti i metodi del _super-tipo_. Inoltre, le **segnature** dei metodi del _sotto-tipo_ devono essere compatibili con quelle dei corrispondenti metodi del _super-tipo_.

**Nota**: Con _segnature compatibili_ si intende che il metodo del _sotto-tipo_ può avere parametri di tipo più generico e un tipo di ritorno più specifico. Questo garantisce che, se si sostituisce un _super-tipo_ con un _sotto-tipo_, i tipi dei risultati rimangano coerenti.


## Riferimenti utili

* [[esempio regola della segnatura]]
* [[Principio di Sostituzione di Liskov]]
* [[regole derivate da LSP]]