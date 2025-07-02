# ConCorto
### Lorenzo Delitala (616506), Marco Lombardi (623184), Niccolò Fulgaro (621710)

#### Data di Consegna: 14 maggio 2025
#### Corso di laurea in Informatica - Dipartimento di Informatica - Università di Pisa
#### Progetto di IS e BD – appello maggio 2025

## 1 - Descrizione del Dominio

Il sistema ConCorto gestisce concorsi di cortometraggi, coinvolgendo diverse persone con ruoli differenti.

Ogni **concorso** ha una _durata_, una lista di _generi ammessi_, _lingue accettate_, la _massima durata_ per ciascun cortometraggio, il _numero massimo_ di cortometraggi per regista, il _numero di premi_ previsti e una _data di inizio_ per ogni fase. Le fasi sono: (1) Selezione del Comitato, (2) Sottomissione, (3) Recensione, (4) Valutazione, (5) Proclamazione.

Ogni **persona** è identificata da _nome_, _cognome_ ed _email_, e può assumere più ruoli.

Gli **organizzatori** pianificano e realizzano i concorsi, potendo collaborare a più eventi. Non possono partecipare come registi ai concorsi che organizzano.

I **registi** possono iscrivere i propri cortometraggi a più concorsi, rispettando il limite massimo previsto per ciascun concorso.

Il sistema mantiene una lista aggiornata di **esperti del settore**, da cui vengono selezionati i membri del Comitato per ciascun concorso.

I **membri del Comitato** sono esperti del settore selezionati dagli organizzatori prima della fine della fase 1 (Selezione del Comitato), redigono recensioni e selezionano i vincitori. Un membro del Comitato non può né recensire più di un cortometraggio dello stesso regista, né alcun cortometraggio da lui stesso prodotto, e, se è anche regista, non può leggere le recensioni dei propri cortometraggi.

I **giudici esterni**, se delegati da membri del Comitato, possono analizzare i cortometraggi (senza scrivere recensioni), ma non possono far parte contemporaneamente dello stesso Comitato.

I **cortometraggi**, prodotti dai registi, possono partecipare a uno o più concorsi e possono essere sottomessi solo durante la fase 2 (Sottomissione).

Ogni **recensione** è relativa a un solo cortometraggio, è scritta da un gruppo di esattamente tre membri del Comitato, contiene un _punteggio_ (da 0 a 5), un _commento generale_ e una _nota privata_ (accessibile solo ai membri del Comitato). La recensione è visibile agli altri membri del Comitato dalla fase 4 (Valutazione) e ai registi solo dalla fase 5 (Proclamazione). Le recensioni devono essere completate entro l'inizio della fase 4.

I vincitori sono selezionati tra i cortometraggi partecipanti durante la valutazione finale, compatibilmente con il numero di premi previsti dal concorso.

## 2 - Schema concettuale


![](schema_concettuale.png)

### Vincoli dello schema concettuale
#### Vincoli intrarelazionali
##### Recensione
- I punteggi delle recensioni devono essere compresi tra 0 e 5


#### Vincoli interrelazionali
##### Partecipa
- Il genere di un cortometraggio deve essere tra i generi ammessi dal concorso
- La lingua di un cortometraggio deve essere tra le lingue ammesse dal concorso
- La durata di un cortometraggio deve essere minore uguale della durata massima ammessa dal concorso
- Non possono partecipare più di un certo numero di cortometraggi dello stesso regista ad un concorso (il numero è specificato dagli organizzatori per ogni concorso)
- un cortometraggio che partecipa al concorso non può avere come regista un organizzatore dello stesso concorso
- i cortometraggi possono essere sottomessi solo dopo la data di inizio della fase 2 (Sottomissione dei cortometraggi) fino alla data di inizio della fase 3 (Recensione)

##### Fa
- Ogni cortometraggio deve essere recensito da esattamente tre membri del Comitato
- Un membro del Comitato non può recensire più di un cortometraggio dello stesso regista
- Un membro del comitato non può recensire un cortometraggio del quale lui stesso regista
- I membri del Comitato possono recensire i cortometraggi solo dalla data di inizio della fase 3 (Recensione) alla data di inizio della fase 4 (Valutazione Finale)


##### Delega
- i giudici esterni che vengono delegati non possono essere altri membri di quello stesso Comitato


##### Vince
- I cortometraggi vincitori sono esattamente la quantità specificata nell'attributo “numero premi” di concorso


##### Assegnato
- i membri del comitato devono essere assegnati dopo la data di inizio della fase 1 (Selezione dei Membri del Comitato) entro la data di inizio della fase 2 (Sottomissione dei Cortometraggi)

## 3 - Schema Logico-Relazionale

![Schema Logico-Relazionale](schema_logico.png)

### Testuale

- Persona ( _**uuid**_* , nome , cognome , email )
- Cortometraggio ( _**idCorto**_* , durata , titolo , genere , lingua , uuid* )
- Concorso ( _**idConcorso**_* , durata , fase1 , fase2 , fase3 , fase4 , fase5 , maxDurata , maxCorti , numeroPremi )
- Organizza ( _**uuid**_* , _**idConcorso**_* )
- Partecipa ( _**idCorto**_* , _**idConcorso**_* )
- Lingue ( _**lingua**_ )
- Generi ( _**genere**_ )
- LingueAccettate ( _**lingua**_* , _**idConcorso**_* )
- GeneriAmmessi ( _**genere**_* , _**idConcorso**_* )
- Vince ( _**idCorto**_* , _**idConcorso**_* )
- EspertoSettore ( _**uuid**_* )
- MembroComitato ( _**uuid**_* , _**idConcorso**_* )
- Delega ( _**uuid**_* , _**uuid**_* )
- Recensione ( _**idConcorso**_* , _**idCorto**_* , punteggio , commento , nota )
- RecensioneComitato ( _**idCorto**_* , _**uuid**_* )

### Dipendenze Funzionali

**Persona**  
- ***uuid**** → nome , cognome , email

**Cortometraggio**  
- ***idCorto**** → durata , titolo , genere , lingua , uuid*

**Concorso**  
- ***idConcorso**** → durata , fase1 , fase2 , fase3 , fase4 , fase5 , maxDurata , maxCorti , numeroPremi

**Recensione**  
- (***idConcorso**** , ***idCorto**** ) → punteggio , commento , nota

> Tutte le dipendenze rispettano la forma normale di Boyce-Codd (BCNF).

## 4 - Interrogazioni in SQL

### a)
**Caratteristiche richieste**: uso di proiezione, join e restrizione  
**Descrizione operazione**: Seleziona il nome dei registi che hanno fatto cortometraggi in lingua italiana.

```sql
SELECT DISTINCT p.nome
FROM Persona p
JOIN Cortometraggio c ON c.uuid = p.uuid
WHERE c.lingua = 'italiano';
```

### b)
**Caratteristiche richieste**: uso di `GROUP BY` con `HAVING`, `WHERE` e Sort. La lista degli attributi dopo `SELECT` deve contenere almeno tre elementi, due dei quali della tabella.

**Descrizione operazione**: Mostrare la distribuzione dei punteggi assegnati per ciascun concorso considerando solo quelli superiori a 2, grazie a una condizione WHERE. I risultati sono raggruppati per concorso e punteggio tramite GROUP BY, e filtrati ulteriormente con HAVING per mostrare solo i gruppi con almeno due recensioni. L'ordinamento finale è fatto con ORDER BY in base al punteggio.

```sql
SELECT 
    idConcorso, 
    punteggio, 
    COUNT(*) AS numeroRecensioni
FROM 
    Recensione
WHERE 
    punteggio > 2
GROUP BY 
    idConcorso, punteggio
HAVING 
    COUNT(*) >= 2
ORDER BY 
    punteggio;
```


### c)
**Caratteristiche richieste**: uso di `JOIN`, `GROUP BY` con `HAVING` e `WHERE`

**Descrizione operazione**: Mostra i concorsi che hanno ricevuto più di 5 recensioni in totale, considerando solo le recensioni con punteggio almeno 3.

```sql
SELECT 
    c.idConcorso, 
    COUNT(r.punteggio) AS NumeroRecensioni
FROM Concorso c
JOIN Recensione r ON c.idConcorso = r.idConcorso
WHERE r.punteggio >= 3
GROUP BY c.idConcorso
HAVING COUNT(r.punteggio) > 5;
```

### d)
**Caratteristiche richieste**: uso di `SELECT` annidata con quantificazione esistenziale (`EXISTS`)
**Descrizione operazione**: Seleziona i dati delle persone che hanno almeno un cortometraggio (cioè sono registi).

```sql
SELECT 
    p.uuid, 
    p.nome, 
    p.cognome
FROM Persona p
WHERE EXISTS (
    SELECT 1
    FROM Cortometraggio c
    WHERE c.uuid = p.uuid
);
```

### e)
**Caratteristiche richieste**: uso di `SELECT` annidata con quantificazione universale (`NOT EXISTS`)
**Descrizione operazione**: Seleziona gli identificativi dei concorsi in cui tutti i cortometraggi partecipanti sono nella stessa lingua.

```sql
SELECT idConcorso
FROM Concorso c
WHERE NOT EXISTS (
    SELECT 1
    FROM Partecipa p
    JOIN Cortometraggio co ON p.idCorto = co.idCorto
    WHERE p.idConcorso = c.idConcorso
      AND co.lingua <> (
          SELECT co2.lingua
          FROM Partecipa p2
          JOIN Cortometraggio co2 ON p2.idCorto = co2.idCorto
          WHERE p2.idConcorso = c.idConcorso
          LIMIT 1
      )
);
```

### f)
**Caratteristiche richieste**: uso di subquery di confronto quantificato (`ALL`)

**Descrizione operazione**: Seleziona gli identificativi dei concorsi in cui tutti i cortometraggi partecipanti hanno un punteggio superiore a 3.

```sql
SELECT idConcorso
FROM Concorso c
WHERE 3 < ALL (
    SELECT r.punteggio
    FROM Recensione r
    WHERE r.idConcorso = c.idConcorso
);
```

## 5 - Piani di accesso

### a)
#### Logico
$$
\begin{array}{c}
\pi_{\text{p.nome}} \\
| \\
\Join_{\text{c.uuid = p.uuid}} \\
/ \hspace{4em} \backslash \\
\text{Persona (p)} \hspace{2em} \sigma_{\text{c.lingua = "italiano"}} \\
\hspace{8em} | \\
\hspace{8em} \text{Cortometraggio (c)}
\end{array}
$$

#### Fisico senza indici


\begin{array}{c}
\boxed{\text{Distinct (O)}} \\
\vert \\
\boxed{\text{Sort (O, \{P.Nome\})}} \\
\vert \\
\boxed{\text{Project (O, \{P.Nome\})}} \\
\vert \\
\boxed{\text{PageNestedLoop (O\_I, O\_E, P.uid = C.uid)}} \\
/ \hspace{10em} \backslash \\
\hspace{4em} \boxed{\text{TableScan (Persone P)}} 
\hspace{2em} 
\boxed{\text{Filter (O, C.Lingua = "italiano")}} \\
\hspace{10em} \vert \\
\hspace{10em} \boxed{\text{TableScan (Cortometraggio C)}}
\end{array}


#### Fisico con indici

\begin{array}{c}
\boxed{\text{Distinct (O)}} \\
\vert \\
\boxed{\text{Sort (O, \{P.Nome\})}} \\
\vert \\
\boxed{\text{Project (O, \{P.Nome\})}} \\
\vert \\
\boxed{\text{PageNestedLoop (O\_I, O\_E, P.uuid = C.uuid)}} \\
/ \hspace{10em} \backslash \\
\hspace{4em} \boxed{IndexFilter(Persone\ P,\ P.uuid = C.uuid \ )} 
\hspace{2em} 
\boxed{IndexFilter (\ \text{Cortometraggi }\ C, \text{C.lingua="italiano"}\ )} \\
\end{array}

### b)

#### Logico

\begin{array}{c}

T_{\text{r.punteggio}} \\
| \\
{\large\sigma}_{\text{COUNT(*)}\geq2} \\
| \\
_{R.idConcorso, R.punteggio}{\large\gamma}_{\text{COUNT(*)}\rightarrow \text{NumeroRecensioni}} \\
| \\
{\large\sigma}_{R.punteggio\geq2} \\
| \\
\text{Recensioni } R

\end{array}


#### Fisico senza indici
$$
\begin{array}{c}

\boxed{Sort(O, \text{COUNT(*)})} \\
| \\
\boxed{Filter(O, \text{COUNT(*)}\geq2)} \\
| \\
\boxed{GroupBy(O, \{r.idConcorso, r.punteggio\}, \{\text{COUNT(*)} \}\ ) }\\
|\\
\boxed{Filter (O,\ r.punteggio \geq 2 )} \\
| \\
\boxed{TableScan(Recenione\ r)}
\end{array}
$$

#### Fisico con indici
$$
\begin{array}{c}
\boxed{Sort(O, \text{COUNT(*)})} \\
| \\
\boxed{Filter(O, \text{COUNT(*)}\geq2)} \\
| \\
\boxed{GroupBy(O, \{idConcorso, punteggio\}, \{\text{COUNT(*)}\}) }\\
| \\
\boxed{IndexFilter(Recensioni, Idx_{punteggio}, punteggio\geq2)}
\end{array}
$$

### C)
#### Schema logico
$$
\begin{array}{c}

{\large\sigma}_{\text{AVG}(R.punteggio)\geq3.5} \\
| \\
_{p.uuid, p.Nome, p.Cognome}{\large\gamma}_{\text{AVG}(r.punteggio)} \\
| \\
{\large\Join}_{c.uuid=p.uuid} \\
\begin{array}{cl}
/ && \backslash \\
{\large\Join}_{r.idCorto=c.idCorto}
&&
Persona\:\:P \\
\begin{array}{ccc}
/ && \backslash \\
{\large\sigma}_{r.punteggio\geq2} && Cortometraggio\:\:C \\
|&&\\
Recensione\:\:R&&
\end{array}
\end{array}


\end{array}
$$

#### Fisico senza indici

$$
\begin{array}{c}
\boxed{\text{FISICO SENZA INDICI}}\\\\

Filter(O, \text{AVG}(r.punteggio)\geq3.5)\\
| \\
GroupBy(O, \{p.uuid, p.Nome, p.Cognome\}, \{\text{AVG}(r.punteggio)\}) \\
| \\
Sort(O, p.uuid, p.Nome, p.Cognome) \\
| \\
PageNestedLoop(O_E, O_I, c.uuid=p.uuid) \\
\begin{array}{ccc}
/ && \backslash \\
PageNestedLoop(O_E, O_I, r.idCorto=c.idCorto) 
&&
TableScan(Persona\:\:p) \\
\begin{array}{ccc}
/&&\backslash\\
Filter(O, r.punteggio\geq2) 
&&
TableScan(Cortometraggio\:\:c) \\
| \\
TableScan(Recensione\:\:r)
\end{array}
\end{array}

\end{array}
$$

#### Schema fisico con indici

$$
\begin{array}{c}
\boxed{\text{FISICO SENZA INDICI}}\\\\

Filter(O, \text{AVG}(r.punteggio)\geq3.5)\\
| \\
GroupBy(O, \{p.uuid, p.Nome, p.Cognome\}, \{\text{AVG}(r.punteggio)\}) \\
| \\
Sort(O, p.uuid, p.Nome, p.Cognome) \\
| \\
IndexNestedLoop(O_E, O_I, c.uuid=p.uuid) \\
\begin{array}{rcl}
/ && \backslash &&&&&&&&&&&&&&&&&&\\
IndexNestedLoop(O_E, O_I, r.idCorto=c.idCorto) 
&&
IndexFilter(Persona\:\:p, Idx_{p.uuid}, c.uuid=p.uuid) \\
\begin{array}{rcl}
/&&\backslash\\
IndexFilter(Recensione\:\:r,Idx_{r.punteggio}, r.punteggio\geq2) 
&&
TableScan(Cortometraggio\:\:c) \\
\end{array}
\end{array}

\end{array}
$$
