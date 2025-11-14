*status*: #bozza 
*tags*: [[RO]] [[PROGRAMMAZIONE LINEARE]] [[ALGEBRA LINEARE]] [[DEFINIZIONI]] [[DEFINIZIONI PURE RO]]

## Definizione: Faccia di un poliedro

> Sia $P=\{x \in \mathbb{R}^n : Ax \leq b \}$ un poliedro definito a un sistema di disuguagliaanze lineari, dove $A \in \mathbb{R}^{m \times n}$ e $b \in \mathbb{R}^m$. Sia $I \subseteq \{1,\dots,m\}$ un sottoinsieme degli indici delle righe. Una faccia di $P$ è definita come l'insieme

$$
P_{I}=\{x \in \mathbb{R}^n : A_{I}x = b_{I},\ A_{\bar{I}}x \leq b_{\bar{I}} \}
$$

>dove:
>* $A_{I}$ e $b_{I}$ sono la sottomatrice e il sottovettore ottenuti selezionando le righe di $A$ e $b$ corrispondenti agli indici $I$
>* $A_{\bar{I}}$ e $b_{\bar{I}}$ rappresentano le righe e i valori non selezionati (complemento di $I$).

In pratica, fissando alcuni vincoli al loro punto di eguaglianza con b, ovvero *al punto estremo di quelle sotto disequazioni*, stai consideranndo il sottoinsieme dei punti del Poliedro in cui quei punti estremi no cambiano. 
#### Esempio 
Se hai il quadrato definito come:
$$
\begin{cases}
\begin{align}
x_{1} \qquad \leq 1 \\
-x_{1} \qquad \leq 0 \\
x_{2} \leq 1 \\
-x_{2} \leq 0
\end{align}
\end{cases}
$$
Fissando $x_{2}  =1$ e risolvendo il sistema troveremo tutte le soluzioni in cui $x_{2}=1$, ovvero il lato superiore del quadrato. Fissando $x_{2}=1$ e $x_{1}=1$ troveremo invece il vertice $[1,1]$ del quadrato. 

#### Osservazioni
Notiamo che se il numero di punti fissati è uguale al numero di variabili (ovvero $n$) allora troviamo un vertice del poliedro.

**È importante** sapere le [[10.1 - Proprietà delle facce di un Poliedro|proprietà delle facce]].

## Riferimenti utili

* [[10.1 - Proprietà delle facce di un Poliedro]]