*tags*: [[AGENTI BASATI SULLA CONOSCENZA]] [[LOGICA DEL PRIMO ORDINE FOL]]

> [!example] Passaggi
> 1. Elimina le implicazioni ($\to$ e $\leftrightarrow$)
> 2. Porta le negazioni all'interno
> 3. *Standardizzazione* delle variabili: si fa in modo che ogni quantificatore usi una variabile diversa (questo aiuta con la Skolemizzazione)
> 4. *Skolemizzazione* dei quantificatori esistenziali
> 5. *Eliminizzazione* quantificatori universali
> 	1. Prima li portiamo davanti ![[portare davanti qualificatori universali.png]]
> 	2. poi li eliminiamo usanod la *convenzione* che le variabili libere sono quantificate universalmente ![[variabili libere quantificate universalmente.png]]
> 6. Si porta a **FNC**
> 7. Si scrive a clausole
> 8. *Separazione* delle variabili: clausole diverse, variabili diverse. (È anche questa una convenzione che aiuta gli algoritmi senza cambiare la logica) ![[clausole div nomi div.png]]

>[!warning] NOTA:
> Tutti i passi meno la **Skolemizzazione** preservano l’*equivalenza* delle formule. 
> 
> Con la **Skolemizzazione** è comunque preservata la *soddisfacibilità*, OVVERO una formula skolemizzata è soddisfacibile esattamente quando lo è la formula originale.


## Riferimenti utili

* [[Leggi equivalenze logiche]]
* [[Regole di inferenza e Skolemizzazione]]
* [[Forma Normale Congiuntiva FNC o CNF]]