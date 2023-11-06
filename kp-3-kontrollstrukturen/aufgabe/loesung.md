# Lösung FizzBuzz 


Ziel der Aufgabe war es eine Zahlenreihenfolge von 1 bis 100 zu haben, durch drei teilbare Zahlen durch Fizz, durch 7 teilbare Zahlen durch Buzz und durch beide Zahlen Teilbare durch Fizzbuzz ersetz werden sollen.

Es gibt hier nicht *die* richtige Lösung. Man kann dieses Spiel auf viele verschiedene Arten machen. Folgende Art ist eine davon. 

``` js
// Variablen initialisieren
let i = 1;
let zahl;

// Schleife bis 100
while (i <= 100) {
    zahl = i;

    if (zahl % 3 == 0 && zahl % 7 == 0) { // Test ob durch beide Zahlen teilbar
        zahl = "FizzBuzz";
    } else if (zahl % 3 == 0) { // Test ob durch 3 teilbar
        zahl = "Fizz";
    } else if (zahl % 7 == 0) { // Test ob durch 7 teilbar
        zahl = "Buzz";
    }

    // Ausgabe des Wertes
    document.write(zahl + " <br>");

    // Inkrementierung des Zählers
    i++;
}
```
Ein gutes Video zu dieser Aufgabe ist von Tom Scott: [FizzBuzz: One Simple Interview Question](https://www.youtube.com/watch?v=QPZ0pIK_wsc)
<br>

## Bonusaufgabe
Wenn man den Code erweitert, kann man nun auch die Zahlen-Werte Variablen zuweisen, welche auch automatisch den Text auf der Website verändern. 

``` js
// Variablen initialisieren
let i = 1;
let zahl1 = 3;
let zahl2 = 7;
let zahl;

// Einfügen der Werte in den Text
document.getElementById("zahl1").innerHTML = zahl1;
document.getElementById("zahl2").innerHTML = zahl2;

// Schleife bis 100
while (i <= 100) {
    zahl = i;

    if (zahl % zahl1 == 0 && zahl % zahl2 == 0) { // Test ob durch beide Zahlen teilbar
        zahl = "FizzBuzz";
    } else if (zahl % zahl1 == 0) { // Test ob durch 3 teilbar
        zahl = "Fizz";
    } else if (zahl % zahl2 == 0) { // Test ob durch 7 teilbar
        zahl = "Buzz";
    }

    // Ausgabe des Wertes
    document.write(zahl + " <br>");

    // Inkrementierung des Zählers
    i++;
}
```