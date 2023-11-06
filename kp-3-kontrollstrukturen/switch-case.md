# Einführung in Switch-Case in JavaScript

In diesem Abschnitt werden wir uns mit Switch-Case-Anweisungen in JavaScript vertraut machen. Switch-Case bietet eine praktische Möglichkeit, eine Variable gegen verschiedene Werte zu testen und basierend auf dem übereinstimmenden Wert verschiedene Anweisungen auszuführen.
<br><br>

## Grundstruktur einer Switch-Case-Anweisung

Die Grundstruktur einer Switch-Case-Anweisung sieht folgendermaßen aus:

```javascript
let ausdruck = 'Wert';

switch (ausdruck) {
  case 'Wert1':
    // Code, der ausgeführt wird, wenn der Ausdruck 'Wert1' entspricht
    break;
  case 'Wert2':
    // Code, der ausgeführt wird, wenn der Ausdruck 'Wert2' entspricht
    break;
  // Weitere case-Anweisungen können folgen
  default:
    // Code, der ausgeführt wird, wenn kein Case übereinstimmt
}

```

Die Switch-Anweisung vergleicht den Wert des Ausdrucks mit den Werten in den Case-Anweisungen. Wenn ein übereinstimmender Wert gefunden wird, wird der zugehörige Codeblock ausgeführt. Das break-Schlüsselwort wird verwendet, um die Anweisung zu beenden, sobald ein Übereinstimmungsfall gefunden wurde.
<br><br>

## Beispiel einer Switch-Case-Anweisung

Hier ist ein einfaches Beispiel:

```javascript
let tag = 'Mittwoch';

switch (tag) {
  case 'Montag':
    console.log('Heute ist Montag.');
    break;

  case 'Dienstag':
    console.log('Heute ist Dienstag.');
    break;

  case 'Mittwoch':
    console.log('Heute ist Mittwoch.');
    break;

  default:
    console.log('Heute ist ein anderer Tag.');
}

```
> **Output: Heute ist Mittwoch.**

In diesem Beispiel wird der Wert der Variable tag mit den verschiedenen Fällen in den Case-Anweisungen verglichen. Da der Wert 'Mittwoch' entspricht, wird der zugehörige Anweisungsblock ausgeführt.

[<kbd> <br> Austesten <br> </kbd>][LinkForLoop]

[LinkForLoop]: https://www.w3schools.com/js/tryit.asp?filename=tryjs_switch '(w3schools.com) Try out: Switch-Case'

### Default
Der Default gibt an, was ausgegeben werden soll, falls keiner der Spezialwerte zutrifft. Dieser kann weggelassen werden, ist jedoch nicht ratsam. Am Besten überlegt man sich als erstes, was der Default ist, bevor man die Spezialcases definiert. 

***Tipp:*** *Man kann einen Wert/Spezialcase durch den Default ersetzen. Z. B. anstatt für alle 7 Tage einen Case zu machen, kann man für Mo-Sa einen Case erstellen und standartmässig vermuten, es ist Sonntag. Dadurch spart man sich eine Case-Abfrage.*
<br><br>

## Vorteile von Switch-Case

* Switch-Case ist besonders nützlich, wenn Sie eine Variable gegen viele verschiedene Werte testen müssen.
* Die Switch-Case-Anweisung kann leichter zu lesen und zu pflegen sein als eine lange Kette von if-else-if-Anweisungen.

## Einschränkungen von Switch-Case

* In den Case-Anweisungen können nur konstante Werte verwendet werden, keine komplexen Bedingungen oder Ausdrücke.
* Verglichen mit if-else-if-Anweisungen bietet Switch-Case weniger Flexibilität, da es nicht so vielseitig ist.

