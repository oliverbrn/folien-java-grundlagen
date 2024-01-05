## Datentypen


-.-

### Was sind Datentypen?

- legen fest, was für Daten zur Laufzeit gespeichert und verarbeitet werden
- können zum Beispiel Zahlen, Buchstaben oder Wahrheitswerte reräsentieren
- Unterscheidung in **primitive Datentypen** und **Referenzdatentypen**


-.-

### Primitive Datentypen

- 8 verschiedene primitive Datentypen in Java
- können in Integrale Daten (Ganzzahlen), Gleitkomma-Daten, Logische Daten und Zeichen-Daten unterschieden werden
- syntaktisches Mittel von Java und können "einfach" genutzt werden

._.
In Java gibt es 8 verschiedene primitive Datentypen. Diese können weiter unterschieden werden:
- Integraler Datentyp (Ganzzahl): **byte**, **short**, **int**, **long**
- Gleitkomma Datentyp: **float**, **double**
- Logischer Datentyp: **boolean**
- Zeichen Datentyp: **char**<br>

._.
Die primitiven Datentypen sind Kern der Programmiersprache Java und können ohne Einbinden einer Fremdbibliothek genutzt werden. Beispiel:
  ```java 
  class PrimitiveDatentypen {
    
      public static void main(String...args) {
        
          int alter = 20;
          double groesse;         // noch nicht initialisiert
          char geschlecht = 'w';
          boolean raucher = false;
      }
  
  }
  ```
  
._.
Da Java eine plattformunabhängige Programmiersprache ist, sind die Datentypen überall gleich groß! 


-.-

### Integraler Datentyp

| Bezeichnung | keyword in Java | Speichergröße in Byte |             Wertebereich             |
|-------------|:---------------:|:---------------------:|:------------------------------------:|
| Byte        |      byte       |          1B           |             -128 ... 127             |
| Short       |      short      |          2B           | -2<sup>15</sup> ... 2<sup>15</sup>-1 |
| Integer     |       int       |          4B           | -2<sup>31</sup> ... 2<sup>31</sup>-1 |
| Long        |      long       |          8B           | -2<sup>63</sup> ... 2<sup>63</sup>-1 |


-.-

### Gleitkomma-Datentyp

| Bezeichnung | keyword in Java | Speichergröße in Byte |
|-------------|:---------------:|:---------------------:|
| Float       |      float      |          4B           |
| Double      |     double      |          8B           |

-.-

- Wertebereich nicht eindeutig festgelegt, da Präzision (Nachkommastellen) mit gespeichert werden muss
- wird in einer späteren Schulung genau behandelt
- bis dahin stellen wir uns das anhand folgenden Beispiels vor:
    - 4 Bit Speichergröße
    - 2<sup>4</sup> Möglichkeiten
    - bei ganzen Zahlen ergibt sich ein Wertebereich von **-2<sup>3</sup>** ... **2<sup>3</sup>-1** -> **-8** ... **7**
    - bei 1 Nachkommastelle kann man die 1 bzw. -1 schon nicht mehr speichern... (**-0.8** ... **0.7**)
    - **WICHTIG**: so funktioniert das zum Glück nicht, dient nur um zu verstehen, warum kein festgelegter Wertebereich existiert :-)
    - Wen es interessiert: IEEE 754 (Standarddarstellung für Binäre Gleitkommazahlen in Computersystemen)


-.-

### Logischer Datentyp

- Hier gibt es nur den Boolean (keyword **boolean**)
- Speichert die Wahrheitswerte **true** und **false**
- Standardwert: false
- Frage: Wie groß könnte der Boolean in Java sein?


### Zeichen-Datentyp
- Auch hier gibt es nur Einen, den Character (keyword **char**)
- 2 Byte groß
- repräsentiert einzelne Zeichen aus Wertetabellen
- ASCII- bzw. Unicode
- Standardwert '\u0000'
- "\u" ist eine sog. Escapesequenz, macht dem Compiler klar, dass ein 4-Stelliger, hexadezimaler Unicode folgt. Es gibt verschiede Escapesequenzen, später mehr...