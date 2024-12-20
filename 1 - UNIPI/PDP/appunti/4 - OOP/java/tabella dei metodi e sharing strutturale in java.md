*status*: #finito
*tags*: [[PDP]] [[OOP]] [[JAVA]]

## Tabelle dei metodi e sharing strutturale

Siccome visitare l'albero della gerarchia delle classi è un metodo inefficiente, la JVM si basa su delle **tabelle dei metodi** per fare prima. 

> Ogni classe ha una _tabella_ e le tabelle delle _sottoclassi_ riprendono la struttura della tabella della _superclasse_, aggiungendo righe per i nuovi metodi o sovrascrivendo i puntatori ai metodi vecchi.


![[dispatch_vector.png]]



## Riferimenti utili

* [[Introduzione al problema di Dynamic Dispatch]]