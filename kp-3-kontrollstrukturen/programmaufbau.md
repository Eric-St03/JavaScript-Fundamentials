# Aufbau von JavaScript-Programmcode

Hier möchten wir den Aufbau von JavaScript-Code anschauen. Wir schauen uns an, wie dieser gegliedert ist und aus was er besteht.

## Aufbau

Programmcode in JavaScript wird grundsätzlich von oben nach unten bearbeitet. 

```javascript
let zahl = 5;

console.log(zahl);

let zahl = 17;
```

> **Output: 5**

Wenn die Variable unterhalb der Ausgabe verändert wird, wird diese Veränderung nicht in der Ausgabe aktualisiert. 


## Anweisung

JavaScript besteht aus einzelnen Anweisungen. Sie sind die kleinste ausführbare Einheit im Code. Eine Anweisung ist eine Zeile code, die mit einem Semicolon " ; " abgeschlossen wird. 

```javascript
console.log("Das ist eine einzelne Anweisung");
```

> **Output: Das ist eine einzelne Anweisung**

## Anweisungsblock

Ein Anweisungsblock ist eine Gruppierung mehrer einzelner Anweisungen. Dies ist vor allem praktisch, da man somit mehrere Anweisungen auf einmal kontrolieren kann. So kann man einen ganzen Anweisungsblock zum Beispiel nur ausführen, wenn dieser bestimmte Bedingungen erfüllt. Dazu mehr unter "**Bedingungen**".

``` JavaScript 
// einzelne Anweisung
let zahl = 15;

// Bedingter Anweisungsblock
if (zahl > 10) {
  console.log("Die Zahl ist grösser als 10.");

  let produkt = zahl * 3;

  console.log(produkt);
}
```

> **Output 1: Die Zahl ist grösser als 10.**
>
> **Output 2: 45**

Ein Anweisungsblock erkennt man an den geschweiften Klammern { }. Diese müssen geöffnet und wieder geschlossen werden, um Anweisungen zu gruppieren. Man kann auch Anweisungsblöcken (Gruppierungen) innerhalb anderer Anweisungsblöcken machen (Stichwort: ***Verschachteln***).