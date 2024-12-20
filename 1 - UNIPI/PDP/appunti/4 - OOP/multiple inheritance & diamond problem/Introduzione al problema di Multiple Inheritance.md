*status*: #finito
*tags*:  [[PDP]] [[OOP]]

## Introduzione al problema

In alcuni casi, un'astrazione può derivare da due astrazioni diverse. Ad esempio:
![[ereditarietà_multipla.png]]

In questo esempio, sia l'aeroplano che l'automobile possono essere considerati come **Veicoli** _Rifornibili_:

![[ereditarietà_multipla2.png]]

Anche se questa possibilità offre al programmatore maggiore astrazione e modularità del codice, l’ereditarietà multipla _comporta rischi_, in particolare:
- **Implementazioni diverse dello stesso metodo**
- **[[#Diamond Problem]]**

## Riferimenti utili

* 