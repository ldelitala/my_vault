*status*: #bozza 
*tags*: [[RO]] [[PROGRAMMAZIONE LINEARE]] [[DUALITÀ]]

## Introduzione: Teoria della Dualità

Siccome ho trovato un video che lo spiega molto bene, non mi dillungherò a spiegarlo ma lascio il link al video:

https://youtu.be/E72DWgKP_1Y?si=C8W46wU7MALPe70n

In sintesi, per ogni problema di PL
$$
 \text{max}\{cx : Ax \leq b,\ x \geq 0\}
$$
si può scrivere il corrispettivo problema:
$$
 \text{min}\{yb: yA \geq c,\ y \geq 0\}
$$
e le cose fighe da sapere rispetto a questi due problemi sono:
* Il primo è detto **Primale**, mentre il secondo **Duale**
* Le soluzioni del primo sono sempre minori uguali del secondo (teorema della dualità debole)
$$
 \text{max}\{cx : Ax \leq b,\ x \geq 0\} \leq  \text{min}\{yb: yA \geq c,\ y \geq 0\}
$$
* In casi particolari, la relazione è di uguaglianza (teorema della dualità forte)
$$
 \text{max}\{cx : Ax \leq b,\ x \geq 0\} =  \text{min}\{yb: yA \geq c,\ y \geq 0\}
$$
* Se si prova a trovare il *problema duale* del **Duale**, si ottiene di nuovo il **Primale**.

In poche parole il **Duale** ci permette di affrontare il problema da un altro punto di vista nei momenti di crisi e ci da una marea di strumenti utili per sviluppare algoritmi che risolvano i problemi di PL!

## Riferimenti utili

* 