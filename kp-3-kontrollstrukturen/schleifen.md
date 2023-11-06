# Einführung in JavaScript-Schleifen

JavaScript ist eine Programmiersprache, die es uns ermöglicht, wiederholte Aufgaben zu automatisieren. Schleifen sind ein wichtiger Teil der Programmierung und ermöglichen es, dass bestimmte Anweisungen wiederholt ausgeführt werden. Es gibt zwei Hauptarten von Schleifen in JavaScript: die `for`-Schleife und die `while`-Schleife.

## Die for-Schleife

Die `for`-Schleife ist eine häufig verwendete Schleife, wenn wir wissen, wie oft eine bestimmte Aufgabe wiederholt werden soll. Sie besteht aus drei Hauptteilen:

``` JavaScript
for (initialisierung; bedingung; veränderung) {
  // Code, der wiederholt werden soll
}
```

* **Initialisierung:** Hier wird eine Variable erstellt und initialisiert, die als Zähler für die Schleife dient. Das ist die Variable, welche bei jeder Wiederholung angepasst wird.

* **Bedingung:** Hier wird überprüft, ob die Schleife weiterhin ausgeführt werden soll. Solange die Bedingung wahr ist, wird die Schleife fortgesetzt.

* **Veränderung:** Hier definiert man, wie der Zähler jede Runde angepasst werden soll (z. B. um 1 erhöht). Es ist wichtig, darauf zu achten, dass die Bedingung mit dieser Anpassung erreichbar ist. 

``` JavaScript
for (let i = 0; i < 5; i++) {
  console.log("Dies ist die " + (i + 1) + ". Wiederholung.");
}
```
> **Output:**
> - Dies ist die 1. Wiederholung.
> - Dies ist die 2. Wiederholung.
> - Dies ist die 3. Wiederholung.
> - Dies ist die 4. Wiederholung.
> - Dies ist die 5. Wiederholung.


Dieser Code wird 5-mal ausgeführt und es wird "Dies ist die 1. Wiederholung." bis "Dies ist die 5. Wiederholung." in der Konsole ausgeben.

*Tipp: Grundsätzlich startet man beim zählen bei 0. Dies erleichtert das weitere Berechnen der Variablen.*

[<kbd> <br> Austesten <br> </kbd>][LinkForLoop]

[LinkForLoop]: https://www.w3schools.com/js/tryit.asp?filename=tryjs_loop_for_ex '(w3schools.com) Try out: For-Loop'
<br>

## Die while-Schleife
Die `while`-Schleife wird verwendet, wenn wir nicht im Voraus wissen, wie oft die Schleife wiederholt werden soll. Sie besteht aus einer Bedingung, und solange diese wahr ist, wird der Schleifenblock ausgeführt.

``` JavaScript
while (bedingung) {
  // Code, der wiederholt werden soll
}
```
Ein einfaches Beispiel:

``` JavaScript
let i = 0;

while (i < 5) {
  console.log("Dies ist die " + (i + 1) + ". Wiederholung.");
  i++;
}

```

Dieser Code erzielt das gleiche Ergebnis wie das vorherige for-Schleifenbeispiel. Unterschied hier ist eigentlich vor allem, wir definieren unsere drei Hauptelemente an anderer Stelle. 
* **Initialisierung:** Die Zähler-Variable wird vor dem Beginn der Schleife definiert `let i = 0;`

* **Bedingung:** Die Bedingung wird im Kopf der Schleife definiert `while (i < 5)`

* **Veränderung:** Die Anpassung der Variable wird innerhalb der Schleife vorgenommen `i++;`

[<kbd> <br> Austesten <br> </kbd>][LinkWhileLoop]

[LinkWhileLoop]: https://www.w3schools.com/js/tryit.asp?filename=tryjs_while '(w3schools.com) Try out: While-Loop'
<br>

## Die do-while-Scheife
Die `do-while`-Schleife ist eine Unterart der `while`-Schleife in JavaScript. Im Gegensatz zur `for`- und `while`-Schleife wird der Schleifenblock bei der `do-while`-Schleife immer mindestens einmal ausgeführt, bevor die Bedingung überprüft wird. Das bedeutet, dass selbst wenn die Bedingung von Anfang an falsch ist, der Schleifenblock einmal ausgeführt wird.

Hier ist die grundlegende Struktur der `do-while`-Schleife: 

``` JavaScript
do {
  // Code, der mindestens einmal ausgeführt wird
} while (bedingung);
```

* Der Code innerhalb des `do`-Blocks wird mindestens einmal ausgeführt, unabhängig von der Bedingung.
* Nach der Ausführung des `do`-Blocks wird die Bedingung überprüft. Wenn die Bedingung wahr ist, wird der Schleifenblock erneut ausgeführt. Andernfalls wird die Schleife beendet.

``` JavaScript
let i = 0;
do {
  console.log("Dies ist die " + (i + 1) + ". Wiederholung.");
  i++;
} while (i < 5);
```

In diesem Beispiel wird der Code "Dies ist die 1. Wiederholung." bis "Dies ist die 5. Wiederholung." in der Konsole ausgeben, genau wie bei den vorherigen Beispielen. Auch wenn `i` am Anfang bereits größer oder gleich 5 wäre, würde der Schleifenblock mindestens einmal ausgeführt.

[<kbd> <br> Austesten <br> </kbd>][LinkDoWhileLoop]

[LinkDoWhileLoop]: https://www.w3schools.com/js/tryit.asp?filename=tryjs_while '(w3schools.com) Try out: do-while-Loop'
<br>

## Schleifen mit Arrays

In JavaScript können Schleifen verwendet werden, um durch Listen von Begriffen oder Werten zu gehen. Dies ist hilfreich, wenn Sie eine Liste von Wörtern, Namen oder anderen Daten haben und diese nacheinander anzeigen oder verarbeiten möchten.

Hier ist ein einfaches Beispiel mit einem Array:
``` JavaScript
let begriffe = ["Apfel", "Banane", "Kirsche", "Dattel"];

// Eine while-Schleife, um die Begriffe auszugeben
let i = 0;
while (begriffe[i]) {
  console.log("Begriff: " + begriffe[i]);
  i++;
}
```
> **Output:**
> - Begriff: Apfel
> - Begriff: Banane
> -  Begriff: Kirsche
> - Begriff: Dattel

<br>
In diesem Beispiel haben wir ein Array namens `begriffe`, das Früchten entspricht. Wir verwenden eine `while`-Schleife, um durch die Liste der Begriffe zu iterieren und sie nacheinander auszugeben. Diese Mechanik kann man auf diverse Arten einsetzen, um Werte abzuarbeiten oder gespeicherte Inhalte anzuzeigen. 
<br><br>

[<kbd> <br> Austesten <br> </kbd>][LinkArrayLoop]

[LinkArrayLoop]: https://www.w3schools.com/js/tryit.asp?filename=tryjs_loop_while_cars '(w3schools.com) Try out: Loop with Array'