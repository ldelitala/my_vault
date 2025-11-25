*tags*: [[DEFINIZIONI]] [[METODI DI RISOLUZIONE SAT]] [[AGENTI BASATI SULLA CONOSCENZA]]

>[!Definizione] Algoritmi SAT-Solver
>
> I **SAT-Solver** sono algoritmi di **ricerca euristica e ottimizzata** progettati per risolvere il [[PROBLEMA SAT]], cioè determinare in modo efficiente se una formula in [[Forma Normale Congiuntiva FNC o CNF]] è soddisfacibile.

>[!hint] Obiettivo Primario
>
> Il loro scopo principale è **trovare rapidamente un modello (un'assegnazione di verità)** che soddisfi la formula di input o, in caso negativo, dimostrare che la formula è insoddisfacibile (UNSAT).

>[!help] Meccanismo e Risultato
>
> A differenza del [[Model Checking]] (che è esaustivo) e dei [[Metodo di inferenza (Risoluzione)]] (che sono metodi di prova), i SAT-Solvers usano strategie intelligenti di ricerca:
> 1.  **Approccio:** Sono algoritmi basati sulla **ricerca di modelli** nello spazio degli stati (assegnazioni di verità).
> 2.  **Efficienza:** Nonostante il problema SAT sia **NP-completo**, questi algoritmi sono estremamente efficienti su molti problemi reali grazie all'uso di **euristiche** (come l'eliminazione dei [[letterali puri]] e la propagazione delle [[Clausole Unitarie]]).
> 3.  **Output:** Se la formula è soddisfacibile, il SAT-Solver restituisce **un modello** (l'assegnazione che la rende vera), che funge da certificato di soddisfacibilità.

>[!summary] In breve:
> I SAT-Solvers sono strumenti ingegnerizzati che scambiano la completezza della prova (tipica della Risoluzione) con l'**efficienza operativa** nella ricerca di un modello, fornendo la soluzione pratica al [[PROBLEMA SAT]].

## Riferimenti utili

* [[PROBLEMA SAT]]
* [[Algoritmo DPLL]] (Esempio di ricerca sistematica)
* [[Algoritmo WALK-SAT]] (Esempio di ricerca locale)