*tags*: [[AGENTI BASATI SULLA CONOSCENZA]]

![[es_3_2023_02_28_pdf.pdf]]

### Esercizion 1 - sportcity

#### 1) FOL
##### ✔ Predicati
Usiamo predicati unari per rappresentare le proprietà dei cittadini:

- $C(x)$ : "$x$ ama il Calcio"
- $B(x)$ : "$x$ ama il Basket"
- $T(x)$ : "$x$ ama il Tennis"
- $S(x)$ : "$x$ è un abitante di SportCity"

La costante `laura` rappresenta l’individuo Laura.  
Le variabili (come $x$) sono universalmente quantificate quando non indicato diversamente.

##### ✔ Conoscenze in FOL
Le informazioni date si esprimono in logica del primo ordine (FOL) come:

$$
1)\quad \forall x\; (C(x) \land S(x) \to B(x))
$$

$$
2)\quad \forall x\; (T(x) \land S(x) \to \lnot B(x))
$$

$$
3)\quad S(\text{laura})
$$


##### ✔ Eliminazione delle implicazioni
$$
1)\quad \forall x\; (\lnot(C(x) \land S(x)) \lor B(x))
    \equiv \forall x\; (\lnot C(x) \lor \lnot S(x) \lor B(x))
$$

$$
2)\quad \forall x\; (\lnot(T(x) \land S(x)) \lor \lnot B(x))
    \equiv \forall x\; (\lnot T(x) \lor \lnot S(x) \lor \lnot B(x))
$$

$$
3)\quad S(\text{laura})
$$

##### ✔ Forma Clausolare (CNF)
In CNF ogni formula è riscritta come un insieme di clausole (disgiunzioni di letterali).

$$
1)\quad \{\lnot C(x),\; \lnot S(x),\; B(x)\}
$$

$$
2)\quad \{\lnot T(x),\; \lnot S(x),\; \lnot B(x)\}
$$

$$
3)\quad \{S(\text{laura})\}
$$

#### 2) Dimostrazione

La clausola goal è:

$$
T(\text{laura}) \to \lnot C(\text{laura})
$$

che negata diventa:

$$
\lnot(T(\text{laura}) \to \lnot C(\text{laura})) 
\equiv \lnot(\lnot T(\text{laura}) \lor \lnot C(\text{laura})) 
\equiv T(\text{laura}) \land C(\text{laura})
$$
$$
\equiv \{T(\text{laura})\}, \{C(\text{laura})\}
$$
##### Dimostrazione per negazione (Risoluzione)

Le clausole di conoscenza istanziate per Laura sono:

$$
\begin{aligned}
1) &\quad \{\lnot C(\text{laura}),\; B(\text{laura})\} \\
2) &\quad \{\lnot T(\text{laura}),\; \lnot B(\text{laura})\} \\
3) &\quad \{S(\text{laura})\} 
\end{aligned}
$$

E la negazione del goal:

$$
4) \quad \{T(\text{laura})\},\quad 5) \quad \{C(\text{laura})\}
$$
---
##### Passo 1: Risoluzione tra clausole 2 e 4

$$
\{\lnot T(\text{laura}), \lnot B(\text{laura})\} \quad \text{e} \quad \{T(\text{laura})\} 
\quad \Rightarrow \quad \{\lnot B(\text{laura})\}
$$

---

##### Passo 2: Risoluzione tra clausole 1 e 5

$$
\{\lnot C(\text{laura}), B(\text{laura})\} \quad \text{e} \quad \{C(\text{laura})\} 
\quad \Rightarrow \quad \{B(\text{laura})\}
$$

---

##### Passo 3: Risoluzione finale

$$
\{B(\text{laura})\} \quad \text{e} \quad \{\lnot B(\text{laura})\} 
\quad \Rightarrow \quad \square
$$

---

### ✅ Conclusione

Abbiamo derivato una **contraddizione**, quindi la formula iniziale del goal è **conseguenza logica** della base di conoscenza.  
In simboli:

$$
KB \models T(\text{laura}) \to \lnot C(\text{laura})
$$
#### 3) Dimostrazione

##### KB in CNF (istanziata su `laura`)
Le clausole della knowledge base, istanziate per `laura`, sono:

$$
\begin{aligned}
1') &\quad \{\lnot C(\text{laura}),\; B(\text{laura})\} \\
2') &\quad \{\lnot T(\text{laura}),\; \lnot B(\text{laura})\} \\
3') &\quad \{S(\text{laura})\}
\end{aligned}
$$

---

##### (a) Controesempio per "$C(\text{laura}) \to T(\text{laura})$"

Vogliamo un'interpretazione che renda vere tutte le clausole della KB ma **falsifichi** $C(\text{laura}) \to T(\text{laura})$.
Per far fallire l'implicazione serve $C(\text{laura})$ vero e $T(\text{laura})$ falso.

Sia l'interpretazione $I_a$ definita su dominio $\{\text{laura}\}$ così:

- $S(\text{laura}) = \text{true}$ (richiesto dalla KB)  
- $C(\text{laura}) = \text{true}$ (per falsificare l'implicazione)  
- $T(\text{laura}) = \text{false}$  (sempre per falsificare l'implicazione)
- $B(\text{laura}) = \text{true}$ (imposto per soddisfare la clausola 1')

Verifichiamo le clausole:

$$
\begin{aligned}
1')\; \{\lnot C,\; B\}: &\quad \lnot C(\text{laura}) \lor B(\text{laura})
= \text{false} \lor \text{true} = \text{true} \\
2')\; \{\lnot T,\; \lnot B\}: &\quad \lnot T(\text{laura}) \lor \lnot B(\text{laura})
= \text{true} \lor \text{false} = \text{true} \\
3')\; \{S\}: &\quad S(\text{laura}) = \text{true}
\end{aligned}
$$

Quindi $I_a\models KB$. Però
$$C(\text{laura})=\text{true},\quad T(\text{laura})=\text{false} \implies
C(\text{laura})\to T(\text{laura}) \text{ è falsa in } I_a.$$

Conclusione: esiste un modello della KB che falsifica (a), quindi **(a) non è conseguenza logica** della KB.

---

##### (b) Controesempio per "$\lnot B(\text{laura}) \to T(\text{laura})$"

Vogliamo un'interpretazione che renda vere tutte le clausole della KB ma **falsifichi** $\lnot B(\text{laura}) \to T(\text{laura})$.
Per far fallire questa implicazione serve $\lnot B(\text{laura})$ vera (cioè $B$ falso) e $T(\text{laura})$ falso.

Sia l'interpretazione $I_b$:

- $S(\text{laura}) = \text{true}$  (dalla KB)
- $B(\text{laura}) = \text{false}$ (per avere $\lnot B$ vera)  
- $T(\text{laura}) = \text{false}$ (per falsificare l'implicazione)  
- $C(\text{laura}) = \text{false}$ (scelta libera compatibile)

Verifichiamo le clausole:

$$
\begin{aligned}
1')\; \{\lnot C,\; B\}: &\quad \lnot C(\text{laura}) \lor B(\text{laura})
= \text{true} \lor \text{false} = \text{true} \\
2')\; \{\lnot T,\; \lnot B\}: &\quad \lnot T(\text{laura}) \lor \lnot B(\text{laura})
= \text{true} \lor \text{true} = \text{true} \\
3')\; \{S\}: &\quad S(\text{laura}) = \text{true}
\end{aligned}
$$

Quindi $I_b\models KB$. Però
$$\lnot B(\text{laura})=\text{true},\quad T(\text{laura})=\text{false} \implies
\lnot B(\text{laura}) \to T(\text{laura}) \text{ è falsa in } I_b.$$

Conclusione: esiste un modello della KB che falsifica (b), quindi **(b) non è conseguenza logica** della KB.


## Riferimenti utili

* [[Esercitazione 3 parte 2]]