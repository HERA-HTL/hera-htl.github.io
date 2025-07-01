# JavaScript Grundlagen

Für diesen JavaScript-Crashkurs in einer Kleingruppe konzentrieren wir uns darauf, die Grundlagen von JavaScript und Schlüsselkonzepte durch ein aufbauendes, fortlaufendes Projekt zu erarbeiten. 

Unser Ziel ist es, ein solides Fundament im Frontend-Bereich mit JavaScript zu erreichen. 

Die zwei Tage (2 x 200 Minuten) werden wir optimal nutzen, um von den absoluten Basics bis hin zu interaktiven Webanwendungen zu gelangen.

## Projektidee: "Mein Interaktives Dashboard"

Wir werden ein einfaches Dashboard erstellen, das im Laufe des Kurses immer interaktiver wird. Es beginnt statisch, dann werden wir es mit JavaScript dynamisch machen, Benutzereingaben verarbeiten und schließlich Daten von einer externen Quelle abrufen.

## Tag 1: Die Grundlagen von JavaScript & Erste DOM-Interaktionen (4 h)

**Ziel:** Verstehen, was JavaScript ist, wie man es ausführt, und die grundlegenden Bausteine (Variablen, Datentypen, Operatoren, Funktionen) sowie die ersten Schritte der DOM-Manipulation lernen.



### 1.1 Einführung in JavaScript & Setup (ca. 25 min)

* **Was ist JavaScript?** 
  Eine Programmiersprache, die Webseiten dynamisch macht
  TODO: Erklären Sie, dass HTML für die Struktur, CSS für das Styling und JavaScript für die Interaktion und Logik zuständig ist. Es ist die einzige Sprache, die direkt im Browser funktioniert.

* **Warum JavaScript lernen?** 
  Es ist essentiell für Webanwendungen und eröffnet viele Karrieremöglichkeiten

* **Computer-Setup (Überblick):** 
  Sie benötigen einen Webbrowser (Chrome empfohlen) und einen Code-Editor (Visual Studio Code, kurz VSCode, empfohlen)



Unsere erste JavaScript-Anwendung:

**Übung 1.1.1: Projektordner und Dateien erstellen**

Erstelle einen Ordner (z.B. mein_dashboard). Darin erstelle eine `index.html` und eine `script.js` Datei.

**Übung 1.1.2: Basale HTML-Struktur** 

Füge den grundlegenden HTML-Code in `index.html` ein, einschliesslich des `<script src="script.js" defer></script>` Tags im `<head>`.

Der `defer`-Parameter stellt sicher, dass das Skript nach dem Laden des HTML-Dokuments verarbeitet wird.

Grundlegender HTML-Code:

```html
<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Document</title>
    </head>
    <body>
        <h1>Hello World!</h1>
    </body>
</html>
```

**Übung 1.1.3: Erste JavaScript-Ausgabe** 

Schreibe in `script.js`: `console.log('Hallo Dashboard!');`.

**Übung 1.1.4: Ausführen mit Live Server** 

Installiere die VSCode-Erweiterung "Live Server". Öffne `index.html` mit Live Server. Öffne die Browser-Konsole (`Cmd+Opt+J` oder `Ctrl+Shift+J`). 

> Zeige, dass die Meldung erscheint!

**Diskussion:** 

`console.log()` ist ein Objekt (`console`) mit einer Methode (`log()`) zum Ausgeben von Nachrichten.

**Kommentare:** 

Einzeilige Kommentare mit `//`.

### 1.2 JavaScript Variablen & Datentypen (ca. 45 min)

* Variablenkonzept: Ein Name, den Sie einem Wert geben, um ihn später zu verwenden. Variablen sind wie Labels für Werte.

* let und const Keywords:

  * let: Eine Variable, deren Wert geändert werden kann.

  * const: Eine Konstante, deren Wert nach der Zuweisung nicht mehr geändert werden kann, sonst führt es zu einem Fehler. Benennungskonvention: Grossbuchstaben (z.B. FILE_SIZE_LIMIT).

Übung 1.2.1: Variablen deklarieren und neu zuweisen:

* Variablen-Benennungsregeln: Nur Buchstaben, Zahlen, Unterstriche. Nicht mit einer Zahl beginnen. Keine reservierten Schlüsselwörter (z.B. console, if, for). Case-sensitive (Message ist anders als message).
* Benennungskonventionen: camelCase (für Variablen, Funktionen) und snake_case (eher selten in JS, aber existiert). Wir werden camelCase verwenden.
* Grundlegende Datentypen: Definitionen für verschiedene Datentypen. JavaScript erkennt diese Typen, um Operationen korrekt auszuführen.
  * Strings: Zeichenfolgen, in Anführungszeichen ("" oder '' oder   für Template Strings). Template Strings (``): Ermöglichen das Einbetten von Variablen mit ${variable}.
  * Numbers: Ganze Zahlen (Integers) und Dezimalzahlen (Floats). Arithmetische Operationen möglich.
  * Booleans: true oder false Werte. Wichtig für Entscheidungen im Programm.
  * Undefined: Standardwert für Variablen, denen noch kein Wert zugewiesen wurde.
  * Null: Repräsentiert einen absichtlich leeren oder unbekannten Wert.

Diskussion: Unterschied zwischen undefined und null (undefined = default, null = intentional).

Übung 1.2.2: Datentypen und Template Strings:

* (Kurze Erläuterung zu typeof null als 'object' ist ein bekannter JavaScript-Fehler, aber kein Hindernis für Anfänger).

### 1.3 Operatoren (ca. 30 min)

◦

Arithmetische Operatoren: +, -, *, /, ** (Exponentiation), % (Rest)



.

◦

Zuweisungsoperatoren: = (Standardzuweisung)

. Kombinierte Zuweisungen: +=, -=, *=

.

◦

Vergleichsoperatoren: == (gleich, mit Typumwandlung), != (nicht gleich), === (strikt gleich, ohne Typumwandlung), !== (strikt nicht gleich)

. >, <, >=, <=. Empfehlung: Immer strikte Vergleiche (===, !==) verwenden, um unerwartete Typumwandlungen zu vermeiden

.

◦

Logische Operatoren: && (AND), || (OR), ! (NOT)

. Geben Booleans zurück

.

◦

typeof Operator: Prüft den Datentyp eines Werts und gibt ihn als String zurück



.

◦

Übung 1.7: Operatoren anwenden:

### 1.4 Funktionen (ca. 50 min)

◦

Konzept: Ein Block von Code, der eine spezifische Aufgabe ausführt und wiederverwendbar ist



.

◦

Eigene Funktionen erstellen: Mit dem function-Keyword, einem Namen, runden Klammern für Parameter und geschweiften Klammern für den Körper

. Aufruf mit ()

.

◦

Parameter und Argumente: Variablen in der Funktionsdefinition, die Eingaben annehmen

. Argumente sind die Werte, die beim Aufruf übergeben werden

.

◦

return Statement: Gibt einen Wert an den Aufrufer zurück

. Beendet die Funktion sofort

.

◦

Variablen-Gültigkeitsbereich (Scope): local scope (Variablen innerhalb einer Funktion) vs. global scope (Variablen ausserhalb jeder Funktion)

. Lokale Variablen sind nur innerhalb der Funktion zugänglich. Globale Variablen sind überall zugänglich

.

◦

Pfeilfunktionen (Arrow Functions): Eine kürzere, prägnantere Syntax für Funktionen



. Wichtig für React!

▪

Syntax: const funktionName = (parameter) => { /* Funktion body */ }

.

▪

Einzelzeilige Funktionen können {} und return weglassen: const add = (a, b) => a + b;

.

▪

Ein Parameter: Klammern können weggelassen werden: const square = num => num * num;

.

▪

Keine Parameter: Leere Klammern sind erforderlich: const hallo = () => console.log('Hallo!');

.

◦

Übung 1.8: Funktionen erstellen und verwenden:

### 1.5 Einführung ins Document Object Model (DOM) & Erste Manipulation (ca. 50 min)

◦

Was ist das DOM? Eine hierarchische Baumstruktur von Objekten, die eine Webseite bilden

. Der Browser macht das DOM zugänglich, damit wir Seite, Stil und Inhalt mit JavaScript ändern können

.

◦

document Objekt: Der Eintrittspunkt zu allen HTML-Elementen

.

◦

Auswahl von HTML-Elementen:

▪

document.querySelector(): Wählt das erste Element, das einem CSS-Selektor entspricht (z.B. #id, .klasse, tag)



.

▪

document.querySelectorAll(): Wählt alle Elemente, die einem CSS-Selektor entsprechen. Gibt eine NodeList zurück (ähnlich einem Array)



.

◦

Elemente manipulieren:

▪

Inhalt ändern: element.textContent (Textinhalt) oder element.innerHTML (HTML-Inhalt)

.

▪

Klassen hinzufügen/entfernen: element.classList.add(), element.classList.remove(). Nützlich für CSS-Styling

.

◦

Projekt Schritt 1: Dashboard-Header aktualisieren:

▪

Fügen Sie in index.html ein <h1> und ein <p> mit IDs hinzu (z.B. dashboard-titel, status-nachricht).

▪

Übung 1.9: DOM-Elemente auswählen und Text ändern:

▪

Übung 1.10: Dynamisches Styling mit Klassen:

•

Fügen Sie in style.css (die wir später einbinden, oder temporär im <head>) Regeln hinzu:

•

Fügen Sie in script.js hinzu:

◦

Zusammenfassung Tag 1: Wir haben JavaScript kennengelernt, grundlegende Bausteine verstanden und erste Interaktionen mit dem DOM vorgenommen.