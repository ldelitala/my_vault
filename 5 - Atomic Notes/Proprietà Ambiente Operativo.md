*tags*: [[IntroAI]] [[DEFINIZIONI]]

## Proprietà ambiente operativo

### Tabella riassuntiva


| Categoria                    | Tipo 1           | Tipo 2                     | Tipo 3                     |
| ---------------------------- | ---------------- | -------------------------- | -------------------------- |
| **Osservabilità**            | *Completa*       | *Parziale*                 |                            |
| **Predicibilità**            | *Deterministico* | *Stocastico*               | *Non Deterministico*       |
| **Struttura Temporale**      | *Episodico*      | *Sequenziale*              |                            |
| **Evoluzione dell'ambiente** | *Statico*        | *Dinamico*                 | *Semidinamico*             |
| **Conoscenza delle Regole**  | *Note*           | *Ignote*                   |                            |
| **# agenti**                 | *Singolo*        | *Multi-agente competitivo* | *Multi-agente cooperativo* |
| **# stato**                  | *Discreto*       | *Continuo*                 |                            |
### Tabella con spiegazioni

| **Osservabilità**                    | *Completa*                                                                                                                                                            | *Parziale*                                                                         |
| ------------------------------------ | --------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- |
|                                      | i sensori danno accesso allo stato completo dell'ambiente e non serve salvare lo stato                                                                                | sono presenti limiti nell'apparato sensoriale                                      |
|                                      |                                                                                                                                                                       |                                                                                    |
| **# Agenti**                         | *Singolo*                                                                                                                                                             | *Multiplo competitivo*                                                             |
|                                      | *Multiplo cooperativo*                                                                                                                                                |                                                                                    |
|                                      |                                                                                                                                                                       |                                                                                    |
| **Predicibilità**                    | *Deterministico*                                                                                                                                                      | *Stocaistico*                                                                      |
|                                      | se lo stato successivo è completamente determinato dallo stato corrente e dall'azione                                                                                 | se esistono degli elementi di incertezza con associata probabilità                 |
|                                      | *Non - Deterministico*                                                                                                                                                |                                                                                    |
|                                      | esistono vari risultati possibili di un azione ma non in base ad una probabilità                                                                                      |                                                                                    |
|                                      |                                                                                                                                                                       |                                                                                    |
| **Struttura Temporale**              | *Episodico*                                                                                                                                                           | *Sequenziale*                                                                      |
|                                      | l'esperienza è divisa in episodi atomici in cui l'agente riceve una percezione ed esegue l'azione, indipendentemente dalle azioni intraprese negli episodi precedenti | Ogni decisione può influenzare quelle successive (es. schacchi)                    |
|                                      |                                                                                                                                                                       |                                                                                    |
| **Evoluzione dell'ambiente**         | *Statica*                                                                                                                                                             | *Dinamica*                                                                         |
|                                      | l'ambiente non cambia mentre agente decide                                                                                                                            | ambiente cambia mentre agente decide (non rispondere in tempo equivale a non gire) |
|                                      | *Semi dinamica*                                                                                                                                                       |                                                                                    |
|                                      | l'ambiente non cambia ma la valutazione della prestazione si (es. schacchi con timer)                                                                                 |                                                                                    |
|                                      |                                                                                                                                                                       |                                                                                    |
| **# Stato**                          | *Discreto*                                                                                                                                                            | *Continuo*                                                                         |
|                                      |                                                                                                                                                                       |                                                                                    |
| **Stato di Conoscenza delle Regole** | *Note*                                                                                                                                                                | *Ignote*                                                                           |
|                                      | es. gioco di carte (osservabilità parziale ma regole conosciute)                                                                                                      |                                                                                    |
|                                      |                                                                                                                                                                       |                                                                                    |




## Riferimenti utili

* [[Ambiente]]
* [[Ambiente Operativo]]