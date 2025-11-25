*tags*: [[DEFINIZIONI]] [[AGENTI BASATI SULLA CONOSCENZA]] [[LOGICA PROPOSIZIONALE]]


>[!Definizione] Forma Normale Congiuntiva (FNC)
>
> La **Forma Normale Congiuntiva (FNC)** è una rappresentazione di una formula logica in cui:
>
> 1. La formula è una **congiunzione** (AND, ∧) di una o più **clausole**.
> 2. Ogni clausola è una **disgiunzione** (OR, ∨) di **letterali**.
> 3. Un **letterale** è una variabile booleana o la sua negazione.
>
> In simboli:
>
> $$
> F = (l_{1,1} \lor l_{1,2} \lor \dots) \land (l_{2,1} \lor l_{2,2} \lor \dots) \land \dots
> $$
>
> Dove ogni $l_{i,j}$ è un letterale.

>[!summary] In breve:
> La FNC è una congiunzione di clausole (insiemi di letterali) che permette ragionamenti e algoritmi di soddisfacibilità efficaci.

> [!important] **Rappresentazione come insiemi:**  
> Ogni clausola può essere vista come un **insieme di letterali**, e la formula come un **insieme di clausole**, utile nelle implementazioni di algoritmi di SAT:
>
> $$
> F = \{ \{l_{1,1}, l_{1,2}, \dots\}, \{l_{2,1}, l_{2,2}, \dots\}, \dots \}
> $$
>

## Riferimenti utili

* 