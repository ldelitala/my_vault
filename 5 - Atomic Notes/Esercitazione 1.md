*tags*: [[AGENTI BASATI SULLA RICERCA]]

## Esercitazione 1

![[es_1_teseo-testo.pdf]]

### Risoluzione

#### 1) scrivere PEAS, tipo di ambiente, tipo di agente, formulazione del problema in termini di RO

##### PEAS
* Performance measures: arrivare all'obiettivo, numero di mosse minimo
* Environment: grid 4x4
* Actuators: spostamento su, giù, destra, sinistra
* Sensors: posizione di se stesso, percezione muri e percezione dell'uscita

##### tipo di ambiente
* Osservabilità: totale
* Predicibilità: deterministica
* Struttura temporale: Sequenziale
* Evoluzione dell'ambiente: statico
* Conoscenza delle regole: note
* numero di agenti: singolo
* cardinalità dello stato: discreto

##### tipo di agente
* è un agente con stato (per ricordarsi dove è andato)
* è un agente con obiettivo

##### formulazione in termini di RO
* stato iniziale: (2,1)
* goal test: (2,4)
* azioni: la funzione azioni(r,c) darà come risultato l'insieme $\{\text{destra, sinistra, su, giù}\}$  meno l'insieme dei movimenti di costrizione dei muri
* costi: ogni azione costa 1

#### 2) scrivere lo spazio degli stati

(2,1) <-> (1,1), (2,2)
(1,1) <-> (1,2) <-> (1,3) <-> (1,4) <-> (2,4)
(2,2) <-> (2,3), (3,2) 
(2,3) <-> (3,3) <-> (4,3) <-> (4,2), (4,4)
(3,2) <-> (3,1) <-> (4,1) <-> (4,2)
(4,4) <-> (4,3) , (3,4)
(3,4) <-> (2,4)

#### 3) Provare gli algoritmi di ricerca noti
* troppo difficile da rappresentare in via testuale, c'è bisogno di disegnare il grafo
## Riferimenti utili

* [[PEAS]]
* [[Proprietà Ambiente Operativo]]
* [[es_1_teseo-testo_soluzioni.pdf]]