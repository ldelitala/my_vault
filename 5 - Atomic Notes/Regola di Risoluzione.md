*tags*: [[AGENTI BASATI SULLA CONOSCENZA]] [[METODI DI RISOLUZIONE SAT]]

>[!summary] Regola di Risoluzione
> La **regola di risoluzione** è un’unica regola di inferenza per la logica proposizionale, particolarmente usata su KB in **forma normale congiuntiva (CNF)**.  
> Permette di combinare due clausole contenenti **letterali complementari** per generare nuove clausole.

>[!tip] Concetto base
> - Si selezionano due clausole con un letterale e il suo complementare.  
> - Si eliminano i letterali complementari e si uniscono gli altri letterali per formare la nuova clausola.  
> - Caso speciale: {P} e {¬P} → **{}** (clausola vuota), che rappresenta una **contraddizione** e indica che la KB è **insoddisfacibile**.

>[!example] Esempio
> - Clausola 1: {P, Q}  
> - Clausola 2: {¬P, R}  
> - Risoluzione: {Q, R}  
>
> Caso chiave:  
> - Clausola 1: {P}  
> - Clausola 2: {¬P}  
> - Risultato: {} → contraddizione

>[!tip] Intuizione logica della risoluzione
> - Due clausole con un letterale e il suo complementare: {P, …}, {¬P, …}  
> - In ogni modello che le soddisfa, **almeno uno degli altri letterali deve valere**.  
> - Eliminando P e ¬P otteniamo una nuova clausola che è **sempre vera se le originali sono vere** → conseguenza logica.

>[!info] Note operative
> - La regola è **completa per l’insoddisfacibilità**: se l’insieme di clausole è insoddisfacibile, la clausola vuota verrà sempre generata applicando correttamente la regola.  
> - Viene usata principalmente per verificare se una clausola α è **conseguenza logica** della KB:  
>   - Si aggiunge ¬α alla KB e si applica la risoluzione.  
>   - Se si ottiene {}, α è deducibile dalla KB.


## Riferimenti utili

* [[Forma Normale Congiuntiva FNC o CNF]]  
* [[Conseguenza logica]]
