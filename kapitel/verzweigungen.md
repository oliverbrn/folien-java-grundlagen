# Verzweigungen / Kontrollstrukturen

_>>
- Möglichkeit anhand von Bedingungen unterschiedliche Anweisungen auszuführen
- Bedingungen sind Wahrheitswerte (boolean, true oder false)
- in Java: if-else und switch-case

_>>

## If-Statement

- keyword "if"
- Syntax: **if**(*bedingung*) { *code* }

```java
    int a = 5, b = 6;

    if ( a == b ) {
        System.out.println("a und b sind gleich!");
    }
```

_>>


## If-Else-Statement

- keyword "else"
- kann hinter einer "if"-Anweisung stehen
- wird ausgeführt, falls vorangehende Bedingung der if-Anweisung nicht erfüllt wurde
- Syntax: **if** (*bedingung*) { ... } **else** { ... }

```java
    if ( a == b ) {
        System.out.println("a und b sind gleich!");
    } else {
        System.out.println("a und b sind ungleich!");
    }
```

_>>

Was, wenn wir mehrere Fallunterscheidungen haben?
Beispiel:  
Wir möchten abhängig vom Alter angeben, ob eine Person als Kind (0-14), Jugendlicher(<18) oder Erwachsener(>=18) gilt.  

```java
    if ( /* bedingung */ ) {
        // anweisungsblock, wenn bedingung == true
    } else {
        // anweisungsblock, wenn bedingung == false
    }
```
Note: Das soll jemand am whiteboard versuchen (mit Hilfe der Gruppe). Hoffentlich kommt dabei irgendwie ein verschachteltes if raus. Dann Überleitung zu else if

_>>


## Else if

- Möglichkeit, verschiedene Bedingungen in einer Struktur unterzubringen
- funktioniert genau wie ein neues if-statement im Anweisungsblock vom else
  - WENN ...
  - SONST WENN ... (beliebig oft schachtelbar)
  - SONST
- Syntax: **else if**( *bedingung* ) { *code* }

_>>

Unser Beispiel könnte also so aussehen:

```java
    String str = "Unbekannter";

    if ( alter < 14 ) {
        str = "Kind";
    } else if( alter <= 18 ) {
        str = "Jugendlicher";
    } else {
        str = "Erwachsener";
    }
    
    System.out.println("Ich bin ein " + str + ".");    
```
