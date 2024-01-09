# Operatoren


_vv

Mit einem Java-Operator können Operationen in einem Satz von Werten ausgeführt werden. Es gibt dabei eine Vielzahl unterschiedlicher Java-Operatoren, die in unäre, binäre und ternäre Operatoren unterteilt werden. Unär bedeutet, dass der Java-Operator einstellig ist, binär beschreibt einen zweistelligen Operator und der ternäre Bedingungsoperator ist dreistellig.

Ein Beispiel für einen unären Java-Operator ist die Negation, die durch „!beispiel“ ausgedrückt wird. Die Subtraktion ist ein Beispiel für einen binären Java-Operator, weil hier zwei Operanden benötigt werden (a – b). Der einzige ternäre Java-Operator ist der Bedingungsoperator, der nach der if-then-else-Methode funktioniert:

( <boolescher ausdruck=""> ) ? AusgabewertTrue : AusgabewertFalse;
Im Folgenden stellen wir Ihnen die unterschiedlichen Java-Operatoren vor.

_>>
## Was sind Operatoren? 


- Kernteil der Programmiersprache Java
- Zusammen mit Operanden ausführbar
- Können Variablen manipulieren
- Unterteilung in unäre, binäre oder ternäre Operatoren ...
- ... oder in die Art der Operation möglich (Vergleich, Verknüpfung, arithmetischer Operator, ...)

_>>
## Unäre Operatoren

Operatoren, die auf genau **einen** Operanden bezogen sind  
Beispiele:
- !bool (Negation)
- zähler++ (Inkrementierung)
- -8 (neg. Vorzeichen)


_>>
## Binäre Operatoren

... benötigen **zwei** Operanden!
Beispiele:
- 2+2 (Addition)
- alter=19 (Zuweisung)
- geschlecht!=m (Vergleich)


_>>
## Ternäre Operatoren

... benötigen genau **drei** Operanden.
- nur einen ternären Operator in Java 
- auch als "ternärer" oder "ternary" Operator bekannt
- *bedingung* **?** *statement wenn erfüllt* **:** *statement wenn nicht erfüllt*
- beispiel: wahrheit = i < 10 **?** false **:** true;
> Was passiert hier, wenn i = 10 ist?  
> Wie könnte man die Bedingung viel geschickter implementieren?


_>>
## Arithmetische Operatoren

Hinter arithmetischen Operatoren verbergen sich die mathematischen "Standard"-operatoren **+**, **-**, __*__, **/**.
Dazu kommt der Modulo- oder auch Restwert-Operator **%**. Er gibt bei einer Division den ganzen Rest zurück.<br>
Beispiel:           
9 / 4 = 2 (Rest 1)  
9 % 4 = 1  
>9 % 8 = **?**


_>>
## Inkrementieren / Dekrementieren

- Möglichkeit, Zahlen-Variablen um Wert 1 zu manipulieren
- Operator **++** für Inkrement, **--** für Dekrement
- Pre- und Postinkrement bzw. -dekrement möglich
- >Was könnte der Unterschied sein?


_>>
## Vergleiche

- **==** : Gleichheit
- > Warum nicht "="?
- **!=** : Ungleichheit
- **<**, **<=** : kleiner, kleiner gleich
- **>**, **>=** : größer, größer gleich


_>>
## Boolsche Verknüpfungen
|          |                   |
|:--------:|:-----------------:|
|  **!**   |    Verneinung     |
|  **&&**  |  logisches "Und"  |
| **\|\|** | logisches "Oder"  |
|  **^**   | exklusives "Oder" |
> Was liefert folgender Term?  
> **!true || 2 == 2 && 10 < 9** 


_>>
## Zuweisungsoperatoren

|        |                         |
|:------:|:-----------------------:|
| **=**  |   einfache Zuweisung    |
| **+=** |  Addition + Zuweisung   |
| **-=** | Subtraktion + Zuweisung |
| __*=__ |  Multiplikation + Zuw.  |
| **/=** |  Division + Zuweisung   |
| **%=** |   Modulo + Zuweisung    | 

_>>

*a += b* → *a = a + b*

Beispiel: 
  ```java
        int i = 3;
        i += 4;     // i = i + 4; -> 7

        double d = 3.2;
        d /= 2;     // d = d / 2; -> 1.6
  ```


_>>
## Bitweise Operatoren

- können einzelne Bits von Zahlen manipulieren
- nur für wenige spezielle Anwendungsfälle wichtig
<br>

|                    |                                                     |
|:------------------:|:---------------------------------------------------:|
|       **&**        |                   bitweise "Und"                    |
|       **\|**       |                   bitweise "Oder"                   |
|       **^**        |                   bitweise  "XOR"                   |
|       **~**        |                invertiert alle Bits                 |
| **>>** <br> **<<** | Bitshift: verschiebt alle<br> Bits in eine Richtung |

_>>

Beispiel für bitweisen Operationen  
```java
    int i = 3;                  // binär 011
    int j = 6;                  // binär 110
    
    int bitweiseUnd = i & j;    // binär 010, dezimal 2
```
```java
    int i = 3;                  // binär 011
    i = i<<1;                   // binär 110, dez. 6
```

_>>

#### Beispiel Anwendungsfall: Wir möchten überprüfen, ob die Hälfte einer geraden Zahl ungerade ist.  

<br>

Lösung ohne bitweise Operation:  
```java
            (x / 2) % 2 == 1
```
Lösung mit bitweiser Operation:  
```java
            x>>1 & 1
```

_>>

x>>1 & 1 ???  
- **x>>1** verschiebt alle Bits um eine Stelle nach rechts 
- wenn Binär ganz rechts eine "1" steht, ist die Zahl ungerade da alle anderen Stellen Zweierpotenzen sind  
- daher bitweiser "Und"-Vergleich mit 1

Bitweise Operatoren können auch als Zuweisung kombiniert werden!  
a = a & 2  
a &= 2

Note: Das kann natürlich keiner lesen, ist aber für den Prozessor deutlich performanter.  
Kann in bestimmten Fällen Sinn machen, aber für uns erstmal egal :-)  
Bitshift nach rechts: Halbierung bei geraden Zahlen.