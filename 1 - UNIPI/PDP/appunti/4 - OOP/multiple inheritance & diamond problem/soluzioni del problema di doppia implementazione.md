*status*: #finito 
*tags*:  [[PDP]] [[OOP]]

## Soluzioni nei linguaggi di programmazione

#### C++ (Disambiguazione)

In C++, si può disambiguare nelle chiamate di funzione:

```cpp
int main() {
    C c = C();
    c.A::foo(); // DISAMBIGUAZIONE con .A
}
```

- **Pro**: Supporto completo per l'ereditarietà multipla.
- **Contro**: Maggiore attenzione richiesta al programmatore.

#### Java (Interfacce)

In Java non esiste ereditarietà multipla tramite le classi. Tuttavia, è possibile simulare un’ereditarietà multipla tramite le **interfacce**, oppure usare le **interfacce con metodi di default** per una gestione limitata.

- **Pro**: Soluzione intuitiva e trasparente.
- **Contro**: Funzionalità limitate rispetto alla vera ereditarietà multipla.

#### Python (Method Resolution Order - MRO)

In Python, il **Method Resolution Order** utilizza l'**algoritmo C3**, che risale l’albero di ereditarietà in modo deterministico, evocando il primo metodo trovato (linearizzazione della gerarchia delle classi).

#### Dart (Mixin)

La soluzione **Mixin** in Dart evita il problema tramite *composizione* delle classi, piuttosto che ereditarietà. Un mixin è un componente che può essere "mescolato" a una classe esistente. In questo modo, si può estendere una singola classe (single inheritance) e aggiungere mixin, con possibilità di **overriding**.

- **Pro**: La single inheritance rende la gerarchia più lineare e prevedibile. L'overriding nei mixin evita conflitti.
- **Contro**: Non supportato in molti dei linguaggi di programmazione più diffusi.


## Riferimenti utili

* [[Problema della doppia implementazione]]
* [[Introduzione al problema di Multiple Inheritance]]