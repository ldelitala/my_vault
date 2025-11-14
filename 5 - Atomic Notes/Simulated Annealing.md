*tags*: [[introAI]] [[DEFINIZIONI]] [[AGENTI BASATI SULLA RICERCA]]

## Simulated Annealing (Tempra)

La tempra è una tecninca metallurgica in cui si scalda molto velocemente un metallo e dopo si fa scendere di temperatura molto lentamente. Questo permette agli atomi di avere più tempo per cristallizzarsi, e quindi hanno spazio per trovare una configurazione ad energia più bassa.

Questo algoritmo sfrutta lo stesso principio usando un concetto "astratto" di temperatura unito al normale algoritmo di hill climbing.
Si parte con una temperatura alta. Questo significa che si accetta con probabilità alta che l'algoritmo scelga per il passo successivo un valore che si allontana dall'obbiettivo, invece di uno che si avvicina. Mano a mano che l'algoritmo procede si "cala la temperatura", ovvero si diminuisce la quantità di salti che si allontanano dall' obbiettivo. Così facendo si andrà mano a mano a scendere verso il minimo globale (o massimo) senza rimanere incastrati in quelli locali. 

>[!definizione] Formula della Temperatura 
>Sia $\nabla E$ la differenza del salto negativo e $T$ la temperatura (in costante decrescita), allora la probabilità di accettare il salto è:
> $$p=e^{\nabla E/T} $$

**I valori per T determinati sperimentalmente:**
  - il valore *iniziale* di **T** è tale che, per valori medi di **ΔE**,  $p = e^{\frac{\Delta E}{T}}$ sia all’incirca **0.5**.

## Riferimenti utili

* [[Hill Climbing]]