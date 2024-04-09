# TBZ-Module-323

## Funktional Programmieren

### von Bianka Maria Zieba

### Inhaltsverzeichnis

- [TBZ-Module-323](#tbz-module-323)
  - [Funktional Programmieren](#funktional-programmieren)
    - [von Bianka Maria Zieba](#von-bianka-maria-zieba)
    - [Inhaltsverzeichnis](#inhaltsverzeichnis)
    - [Begriff Funktion](#begriff-funktion)
    - [Imperative vs. Deklarative](#imperative-vs-deklarative)
    - [Merkmale einer pure function](#merkmale-einer-pure-function)
    - [Rein funktionale Ansätze](#rein-funktionale-ansätze)
    - [Unveränderliche Datenstrukturen](#unveränderliche-datenstrukturen)
    - [Call by Value](#call-by-value)
    - [Call by Reference](#call-by-reference)

---

### Begriff Funktion

Wir haben Funktionen bereits im Modul 319 kennengelernt, als wir z.Bsp. einen einfachen Taschenrechner programmiert haben und dabei darauf geachtet haben, dass wir jede mathematische Funktion (+, - , *, /) in eigene Methoden oder Funktionen schreiben, also z.Bsp. so:

```javascript
public static int add(int a, int b) {
 return a + b;
}
```

Diese Funktion erhält zwei Zahlen als Parameter, addiert diese und retourniert die Summe beider Zahlen.
Eine andere Funktion wäre z.Bsp. diese:

```javascript
public static char getFirstCharacter(String s) {
 return s.charAt(0);
}
```

Diese Funktion erhält einen String als Parameter und retourniert das erste Zeichen aus dem String.

### Imperative vs. Deklarative

**Imperative Programmierung:**

- [Die imperative Programmierung](#imperative-programmierung) legt den Fokus auf die schrittweise Ausführung von Anweisungen.
- Sie betont den direkten Zustandswechsel eines Programms durch sequenzielle Anweisungen, die vom Entwickler explizit definiert werden.
- Bekannte imperative Sprachen sind C, C++, Java und Python.

**Deklarative Programmierung:**

- [Die deklarative Programmierung](#deklarative-programmierung) beschreibt, was das Programm erreichen soll, ohne explizit den Ausführungsweg anzugeben.
- Sie nutzt höhere Abstraktionsebenen und abstrahiert viele Implementierungsdetails, was zu prägnanterem und ausdrucksstärkerem Code führt.
- Beispiele für deklarative Paradigmen sind die funktionale Programmierung (z.B. Haskell) und die logische Programmierung (z.B. Prolog).

---

### Merkmale einer pure function

Wenn alle die folgenden Eigenschaften erfüllt sind, ist eine Funktion eine sogenannte "pure function":

- Gibt nur einen Wert zurück (Wenn die Funktion einen Array zurückgibt, gilt das dennoch als ein Wert - nämlich ein Array)
- Berechnet den Rückgabewert nur aufgrund der ihr übergebenen Parameter
- Verändert keine existierenden Werte (neue in der Funktion selber definierte Werte dürfen verändert werden)

Weil sich eine pure function an diese drei Regeln hält, ist sie referenziell Transparent - d. h. Sie könnte auch durch Ihren Return-Wert ersetzt werden, ohne dass sich die Funktionalität des Programmes ändert.

### Rein funktionale Ansätze

Rein funktionale Funktionen erfüllen drei Regeln (siehe PureFunctions Aufgabe 1):

1. [Ein Rückgabewert pro Funktion](#nur-ein-rückgabewert)
2. [Rückgabewert abhängig von den Parametern](#rückgabewert-nur-abhängig-von-den-aufrufparametern)
3. [Keine Veränderung von Werten außerhalb der Funktion](#verändert-keine-existierenden-werte-außerhalb-der-methode)

---

### Unveränderliche Datenstrukturen

Unveränderlichkeit kann auf zwei Arten erreicht werden:

- [Kopie der Daten](#kopie-der-daten): Die Originaldaten bleiben unverändert, während eine Kopie erstellt wird, die bearbeitet werden kann.
- [Rekursion](#rekursion): Durch rekursive Funktionsaufrufe werden neue Kopien von lokalen Variablen erzeugt.
Es ist wichtig, dass Funktionen immer per Wert übergeben werden, damit Kopien anstelle von Referenzen übertragen werden. Funktionale Sprachen verhindern oft die Referenzübertragung, um die Anwendung des funktionalen Paradigmas zu fördern.

---

### Call by Value

[Call by Value](#call-by-value) bedeutet, dass Funktionen Kopien der Originaldaten übergeben werden. Änderungen in der Funktion haben keine Auswirkungen auf externe Variablen.

---

### Call by Reference

[Call by Reference](#call-by-reference) bedeutet, dass Funktionen eine Referenz auf eine Variable übergeben wird. Änderungen an dieser Variable wirken sich nicht nur innerhalb der Funktion aus, sondern auch außerhalb.

---
