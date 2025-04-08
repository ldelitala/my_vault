*tags*: [[BASI DI DATI]] [[DEFINIZIONI BD]]

## Definizione - Dominio

> [!Definizione] Dominio
> Insieme di valori validi di una [[Definizione - Proprietà|proprietà]]

Un dominio può avere le seguenti caratteristiche:

| **Criterio**   | **Tipo di proprietà** | **Descrizione**                           | **Esempio**                               |
| -------------- | --------------------- | ----------------------------------------- | ----------------------------------------- |
| *Struttura*    | Atomica               | Non scomponibile in sotto-valori          | "Età" = 22                                |
|                | Strutturata           | Scomponibile in sotto-valori              | "Indirizzo" = (Via, Numero, Città)        |
| *Unicità*      | Univoca               | Ha un valore unico per ogni entità        | "Matricola" per uno studente              |
|                | Multivalore           | Può avere più valori per la stessa entità | "Email" per una persona con più indirizzi |
| *Presenza*     | Totale                | Ogni entità ha sempre un valore           | "Nome" per una persona                    |
|                | Opzionale             | Alcune entità possono non avere il valore | "Numero di telefono secondario"           |
| *Variabilità*  | Costante              | Il valore non cambia nel tempo            | "Data di nascita"                         |
|                | Variabile             | Il valore può cambiare nel tempo          | "Indirizzo di residenza"                  |
| *Derivabilità* | Calcolata             | Ottenuta da altri dati                    | "Età" calcolata da "Data di nascita"      |
|                | Non calcolata         | Memorizzata direttamente nel database     | "Nome"                                    |

Questa tabella fornisce una visione chiara delle diverse classificazioni delle proprietà e dei loro utilizzi nei modelli di dati!

## Riferimenti utili

* 