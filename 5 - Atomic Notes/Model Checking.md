*tags*: [[DEFINIZIONI]] [[METODI DI RISOLUZIONE SAT]] [[AGENTI BASATI SULLA CONOSCENZA]]

>[!Definizione] Model checking
>
> Il **model checking** è una forma di inferenza per verificare se $KB \models \alpha$:

>[!hint] nota:
> Formalmente, la condizione da verificare è:
> $$
> M(KB) \subseteq M(\alpha)
> $$
> dove $M(\varphi)$ indica l’insieme dei modelli che soddisfano la formula $\varphi$.

> [!help] come funziona?
 si basa direttamente sulla definizione di conseguenza logica:
> 1. Si enumerano **tutti i modelli** che soddisfano la base di conoscenza $KB$.
> 2. Si verifica che in **ognuno** di questi modelli la formula $\alpha$ sia vera.

>[!summary] In breve:
> il model checking consiste nel controllare che **tutti i modelli di KB** rendano vera anche **α**.

## Riferimenti utili

* [[Conseguenza logica]]
* [[Modello di una formula]]