# Einführung in Bedingungen in JavaScript

Hier möchten wir anschauen, was Bedingungen sind in JavaScript, wozu man sie einsetzen kann und was für verschiedene Arten es gibt. 

## Bedingungen

Bedingungen in JavaScript ermöglichen es, Code auszuführen, basierend auf bestimmten Kriterien oder Ausdrücken. Das heisst also, man kann einen Anweisungsblock nur dann ausführen, wenn es eine Bestimmte Bedingung erfüllt. 

### Einfache if-Bedingung

Eine einfache if-Bedingung führt Code aus, wenn eine Bedingung wahr ist.

```javascript
let zahl = 5;

if (zahl > 2) {
  console.log("Die Zahl ist grösser als 2.");
}
```
> **Output: Die Zahl ist grösser als 2.**

Was man hier jetzt gesagt hat, ist: Die Zahl ist **5**. Wenn die Zahl **grösser ist als zwei**, dann führe die Answeisungen aus. 5 ist grösser als 2 => Anweisung ausführen. 

Eine solche Bedingung ist auch als Wenn->Dann... Bedingung bekannt. 

### Bedingungsparameter
Die Bedingung, welche ein Element/Statement erfüllen muss befindet sich in den **Klammern ()** nach dem if. Darin kann man mit allem arbeiten, was ein **true/false Ergebnis** ausgibt, sprich man kann mit Vergleichsoperatoren oder logischen Operatoren oder anderen Funktionen mit einem booleschen Output arbeiten. 

Mit && oder || kann man auch Bedingungen durch "und/oder" verknüpfen.

## if-else-Bedingung
Man kann das nun weiter führen und eine if-esle-Bediungung machen. Das heisst, man Code aus, wenn eine Bedingung nicht zutrifft. 

```javascript
let zahl = 1;

if (zahl > 2) {
  console.log("Die Zahl ist grösser als 2.");
  
} else {
  console.log("Die Zahl ist maximal 2.");
}
```
> **Output: Die Zahl ist maximal 2.**

Hier sagt man folgendes: Die Zahl ist 1. Wenn die Zahl **grösser ist als zwei**, dann führe den ersten Anweisungsblock aus. Wenn die Zahl ***nicht* grösser ist als zwei**, führe den alternativen Anweisungsblock aus. 

## Verschachtelte Bedingungen
Man kann Bedingungen innerhalb von anderen Bedingungen festlegen. Diese Bedingungen müssen jedoch auch beide erfüllt sein, damit die Anweisungen der zweiten Bedingung ausgeführt werden. 

![Nested condition flow](https://media.geeksforgeeks.org/wp-content/uploads/Nested_if.jpg)

Obenstehende Grafik stellt dar, wie eine solche verschachtlung visuell aussehen könnte. Mit Code und simplen Inhalt kann man das folgendermassen darstellen. 

```javascript
let zahl = 6;

if (zahl % 2 == 0) {
    if (zahl > 10) {
        console.log("Case 1: Die Zahl ist gerade und grösser als 10.");

    } else {
        console.log("Case 2: Die Zahl ist gerade und nicht grösser als 10.");

    }

} else {
  console.log("Case 3: Die Zahl ist ungerade.");
}
```
> **Output: Case 1: Die Zahl ist gerade und grösser als 10.**

*Quizfrage: Welcher Output kommt, wenn man 15 als Zahl vorgibt?*
<details>
    <summary>Antwort</summary>
    <i>Case 3: Die Zahl ist ungerade.</i><br>
    Dies ist, weil nur geprüft wird, ob die Zahl grösser als 10 ist, wenn sie gerade ist. Ansonsten müsste man im else-Statement ebenfalls noch eine Bedingung einfügen. 
</details>

## Mehrstufige if-else-Bedingungen
Es ist auch möglich, mehrere Bedingungen abzufragen. Dies kann man erzielen durch ein "else if"-Statement. 

```javascript
let zahl = 5;

if (zahl > 5) {
  console.log("Case 1: Die Zahl ist grösser als 5.");
  
} else if ( zahl < 5) {
  console.log("Case 2: Die Zahl ist kleiner als 5.");

} else {
    console.log("Case 3: Die Zahl ist genau 5.");
}
```
> **Output: Die Zahl ist genau 5.**

Hier geht folgendes von statten: Die Zahl ist 5. **Wenn** die Zahl grösser ist als 5, **dann** Case 1. **Wenn nicht, aber** die Zahl kleiner als 5 ist, **dann** Case 2. **Wenn auch nicht**, **dann** Case 3.

Else-if-Statements kann man beliebig of hintereinander ketten. Zu beachten ist dabei nur, dass eine Bedingung nicht mehr geprüft wird, sobald eine obere sich als wahr herausgestellt hat, auch wenn sie wahr sein könnte. 

Man kann auch mehrere einfach if-Bedingungen aneinanderreihen. Hier werden jedoch alle Anweisungen, für welche Statements die Bedingungen erfüllen, ausgeführt. Ausserdem reagiert das else nur auf das letzte if. Alleinstehende else darf es nicht mehr als eines geben. 

```javascript
let zahl = 6;

if (zahl % 2 == 0) {
    console.log("Case 1: Die Zahl ist gerade");
} 
if (zahl > 10) {
    console.log("Case 1: Die Zahl ist grösser als 10.");

} else {
    console.log("Case 2: Die Zahl ist nicht grösser als 10.");
}
```
> **Output 1: Case 1: Die Zahl ist gerade**
>
> **Output 2: Case 2: Die Zahl ist nicht grösser als 10.**

Es gibt noch eine weitere Art von Mehrstufigen Bedingungen, nähmlich Switch-Case-Anweisungen. Dazu mehr unter **switch-case**.