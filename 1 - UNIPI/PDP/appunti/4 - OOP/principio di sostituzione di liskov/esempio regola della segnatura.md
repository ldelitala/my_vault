*status*: #finito
*tags*:  [[PDP]] [[OOP]] [[JAVA]]

## Esempio

```java
// Super-tipo
class ProcessatoreGenerico {
    // Metodo generico con parametro Object e ritorno Object
    public Object processa(Object input) {
        return input;
    }
}

// Sotto-tipo
class ProcessatoreDiStringhe extends ProcessatoreGenerico {
    // Tipo del parametro più generico (CharSequence) e tipo del risultato più specifico (String)
    @Override
    public String processa(CharSequence input) {
        // Converte il parametro in String e lo elabora, restituendo una String
        return input.toString().toUpperCase();
    }
}

// Classe principale per dimostrare la sostituzione
public class Main {
    public static void main(String[] args) {
        // Istanza del super-tipo
        ProcessatoreGenerico processatore1 = new ProcessatoreGenerico();
        System.out.println("ProcessatoreGenerico: " + processatore1.processa("ciao")); // Output: ciao

        // Istanza del sotto-tipo assegnata a una variabile di tipo super-tipo
        ProcessatoreGenerico processatore2 = new ProcessatoreDiStringhe();
        System.out.println("ProcessatoreDiStringhe come ProcessatoreGenerico: " + processatore2.processa("ciao")); // Output: CIAO
    }
}
```

Come si vede, a livello di tipi, due programmi identici che usano rispettivamente il super-tipo e il sotto-tipo risultano sempre corretti.

## Riferimenti utili

* [[Regola della Segnatura (Tipatura)]]
* [[regole derivate da LSP]]
* [[Principio di Sostituzione di Liskov]]