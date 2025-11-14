*status*: #bozza 
*tags*: [[RO]] [[PROGRAMMAZIONE LINEARE INTERA]]

## 2 - Introduzione - Algoritmo Branch & Bound (B&B)

L'algoritmo Branch & Bound è un approccio **divide et impera** che suddivide progressivamente un problema di Programmazione Lineare Intera (PLI) in sotto-problemi sempre più piccoli, al fine di trovare la soluzione ottimale. Ogni sotto-problema viene analizzato utilizzando due strumenti principali: **rilassamento continuo** ed **euristica**.

L'obiettivo è individuare una soluzione ottimale o, quando ciò non è possibile, stimare i limiti superiori e inferiori del problema per ottenere informazioni utili. Durante l'esplorazione dei sotto-problemi, l'algoritmo utilizza le informazioni raccolte per decidere se conviene continuare ad approfondire un ramo dell'albero dei sotto-problemi o passare a un altro ramo. Se un sotto-problema merita ulteriori approfondimenti, viene suddiviso in sotto-problemi più piccoli da analizzare in seguito.
### Rilassamento Continuo per la valutazione superiore

Il **rilassamento continuo** viene utilizzato per calcolare una valutazione superiore di un sotto-problema. Se il limite superiore dimostra che non è possibile trovare soluzioni migliori di quella attuale, l'algoritmo interrompe l'esplorazione di quel ramo, che si dice **potato dalla valutazione superiore**.

Il rilassamento continuo può anche produrre una soluzione valida. In tal caso, se la soluzione trovata è migliore di quella corrente, viene aggiornata. Poiché il rilassamento continuo garantisce la soluzione ottima del sotto-problema, l'esplorazione di quel ramo termina e si dice che è stato **chiuso per ottimalità**.


### Euristica per la valutazione inferiore

L'**euristica** genera, per ogni sotto-problema analizzato, una soluzione ammissibile. Siccome il rilassamento continuo può produrre soluzioni ammissibili, l'euristica non è indispensabile per garantire una soluzione; tuttavia, può migliorare significativamente l'efficienza dell'algoritmo.

Ad esempio:

1. Se l'euristica produce una soluzione migliore di quella attuale, questa viene aggiornata.
2. Se dopo il rilassamento continuo indica che non è possibile trovare una soluzione migliore di quella appena trovata, si può **chiudere il ramo per ottimalità**.

#### Definizione di Euristica
###### (dal greco _heurískein_, «scoprire, trovare»)

Aspetto del metodo scientifico che comprende un insieme di strategie, tecniche e procedimenti inventivi per ricercare un argomento, un concetto o una teoria adeguati a risolvere un problema dato. Benché l’uso del termine risalga a [I. Kant](https://www.treccani.it/enciclopedia/immanuel-kant/), la nozione cui rimanda è presente fin dall’antichità.


## Riferimenti utili

*  [[2.1 - Algoritmo - Branch & Bound (B&B)]]