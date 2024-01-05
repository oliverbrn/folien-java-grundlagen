# Variabeln und Konstanten


## Was sind Variabeln?

- speichern Werte
- können beliebige primitive oder komplexe Datentypen haben
- findet man ausschließlich in Methoden und Konstruktoren
- werden klein und in camel-case angegeben
- müssen definiert werden bevor wir sie benutzen können -> stark typisierte Programmiersprache
- Unterscheidung zwischen Definition, Initialisierung und Deklaration


## Definition von Variabeln

- Definition gibt nur Datentyp und Bezeichner bekannt
- noch kein Wert zugewiesen
- Syntax: ***datentyp*** **bezeichner**;
- Beispiele:
```java
    int anzahlAutos;
    char zeichen;
    double entfernung;
```

## Initialisierung von Variabeln

- sollten initialisiert werden
- für jeden Datentyp gibt es einen default
- Syntax: **name** = *wert*; (Wobei der Wert zum Datentyp passen muss!)
- Beispiele:
```java
    anzahlAutos = 4;
    zeichen = 'h';
    entfernung = 29.12;
```

_>>

Hier die Definition einer Variable und folgende Initialisierung:
```java
    int anzahlAutos;
    anzahlAutos = 4;
    
    char zeichen;
    zeichen = 'h';
```


## Deklaration

- beschreibt die Definition und Initialisierung in einem Schritt
- immer sinnvoll, wenn Initialwert schon beim Anlegen bekannt ist
- Beispiele:
```java
    int zahl = 4;
    char zeichen = 'h';
    boolean istNatuerlichePerson = false;
```


## Konstanten

- feste Werte
- dienen der Übersicht oder Wiederverwendbarkeit
- **müssen** deklariert werden!
- bezeichner werden in Großbuchstaben angegeben und mit "_" verbunden
- Syntax: **final** *datentyp* *bezeichner* = *wert*;
- Beispiele:
```java
    final int GEBURTS_JAHR = 2000;
    final char GESCHLECHT = 'm';
```