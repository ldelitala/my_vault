*tags*: [[BASI DI DATI]] [[DEFINIZIONI BD]]

## Definizione - Omogeneità

> [!Definizione] Omogeneità
> Nel contesto del **modello relazionale**, un insieme di record è detto **omogeneo** quando tutti i record (o tuple) all'interno di una relazione hanno la **stessa struttura**.

Ciò significa che:

- Ogni record della relazione ha lo stesso numero di attributi (campi).
- Ogni attributo ha un tipo di dato predefinito e coerente tra tutti i record.

Ad esempio, consideriamo una relazione **Studenti**:

|Matricola|Nome|Età|Corso di Laurea|
|---|---|---|---|
|12345|Alice|22|Informatica|
|67890|Bob|21|Matematica|
|54321|Carlo|23|Fisica|

In questa relazione:

- Ogni riga (record) ha esattamente 4 attributi.
- Il tipo di dato di ogni colonna è lo stesso per tutti i record (es. "Matricola" è un numero intero, "Nome" è una stringa, ecc.).

Questa **uniformità strutturale** è ciò che rende gli insiemi di record **omogenei**.

## Riferimenti utili

* 