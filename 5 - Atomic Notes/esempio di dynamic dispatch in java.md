*status*: #finito
*tags*: [[PDP]] [[OOP]] [[JAVA]]

## Esempio di Dynamic Dispatch

```java

class Animale {
    void verso() {
        System.out.println("Verso generico");
    }
}

class Cane extends Animale {
    @Override
    void verso() {
        System.out.println("Bau!");
    }
}

class Gatto extends Animale {
    @Override
    void verso() {
        System.out.println("Miao!");
    }
}

public class Test {
    public static void main(String[] args) {
    
        // Riferimento di tipo Animale che punta a un oggetto Cane
        Animale mioAnimale = new Cane();  
        
        // Stampa "Bau!" grazie al dynamic dispatch
        mioAnimale.verso();                
    }
}

```


## Riferimenti utili

* [[Introduzione al problema di Dynamic Dispatch]]
* [[tabella dei metodi e sharing strutturale in java]]