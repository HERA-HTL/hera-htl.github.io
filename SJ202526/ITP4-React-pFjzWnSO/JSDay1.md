# JavaScript

------

* Vorbereitung: siehe [Notwendige Installationen](#install) unter Appendix 
* <span style="color:green">**Tag 1**</span> → JavaScript-Grundlagen mit Fokus auf alles, was für React unerlässlich ist.
* <span style="color:grey">**Tag 2**</span> → Vertiefung moderner JavaScript-Features + Vorbereitung auf React-Komponenten-Denken.

___



## **0. Einführung – Ziel des Kurses** (10 Min)

- Wozu lernen wir das?

- JavaScript als Basis für React

- Kursüberblick: Tag 1 = Grundlagen, Tag 2 = modernes JS + React-Denken

- Überprüfung der Installationen (siehe [Notwendige Installationen](#install))


## 1. Variablen & Datentypen (25 Min)

* `let`, `const` vs. `var` (historisch)
* Primitive Typen (string, number, boolean, null, undefined)
* Arrays & Objekte – erste Einführung

<u>Beispiele</u>:

```javascript
let name = "Anna";
let age = 17;
let hobbies = ["Lesen", "Gaming"];
let person = { name: "Anna", age: 17 };

console.log(name, age, hobbies[1], person.name);
```

<u>Aufgabe 1.1:</u> Ergänze das Beispiel mit weiteren Anwendungen zu den Primitiven Typen inkl. null und undefined.

<u>Aufgabe 1.2:</u> Neues Objekt `auto` anlegen mit Marke, Baujahr, Farbe → Ausgabe in Konsole.

## 2. Operatoren & Kontrollstrukturen (20 Min)

- Vergleich: `==` vs. `===`
- Logische Operatoren (`&&`, `||`, `!`)
- `if`/`else`, `switch`
- Ternärer Operator: `Bedingung ? Wert1 : Wert2`

<u>Beispiele</u>:

```javascript
let score = 85;
if (score >= 90) console.log("Sehr gut");
else if (score >= 75) console.log("Gut");
else console.log("Nachsitzen...");

let score = 85;let result = score >= 75 ? "Bestanden" : "Nicht bestanden";console.log(result);
```

<u>Aufgabe 2.1:</u> Temperatur-Check (über/unter 0 Grad → Ausgabe).

## 3. Funktionen (30 Min)

- Function Declaration
- Arrow Functions
- Parameter, Default-Werte

<u>Beispiele:</u>

```javascript
function greet(name = "Gast") {
  return `Hallo, ${name}!`;
}
console.log(greet("Mia"));
console.log(greet());
```

<u>Aufgabe 3.1:</u> Funktion schreiben, die alle Zahlen in einem Array verdoppelt.

## 4. Arrays & Objekte – Arbeiten mit Daten (35 Min)

- `map`, `filter`, `forEach`, `find`
- Zugriff auf Objektwerte

<u>Beispiele</u>:

```javascript
let zahlen = [1, 2, 3, 4];
let verdoppelt = zahlen.map(n => n * 2);
console.log(verdoppelt);
```

<u>Aufgabe 4.1:</u> Liste mit Namen → nur die mit mehr als 4 Buchstaben filtern.

## 5. DOM & Events (kurz) (30 Min)

- `getElementById()` bzw. `querySelector()`
- `addEventListener()`
- Eventobjekt

<u>Beispiele:</u>

```html
<button id="btn">Klick mich</button>
<script>
  document.getElementById("btn").addEventListener("click", () => {
    alert("Hallo!");
  });
</script>
```

<u>Aufgabe 5.1:</u> Button → bei Klick Hintergrundfarbe ändern.

## 6. Miniprojekt – ToDo Liste in JS (50 Min)

- Eingabefeld + Button
- Neue Aufgaben ins Array pushen
- Aufgaben in Liste anzeigen
- Löschen möglich machen

**Ergebnis:** Anwenden und  kombinieren von Variablen, Arrays, Funktionen und DOM-Events.

## Appendix

### Notwendige Installationen {#install}

Für die Programmierung mit JavaScript benötigen Sie lediglich zwei Dinge:

* Einen **Webbrowser**: **Chrome** oder **Firefox**
* Einen **Code-Editor**: **Visual Studio Code (VSCode)** ist der bevorzugte Code-Editor, da er schnell und einfach zu bedienen ist

**Code-Editor**: 

VSCode ist kostenlos und auf allen wichtigen Betriebssystemen verfügbar. Du kannst ihn von [https://code.visualstudio.com](https://code.visualstudio.com) herunterladen und installieren.

Für die Entwicklung von React-Anwendungen (JavaScript im Backend oder für komplexe Frontends) ist **Node.js** zusätzlich erforderlich.
Node.js ist eine JavaScript-Laufzeitumgebung, die es ermöglicht, JavaScript außerhalb des Browsers auszuführen. 
Lade die letzte LTS-Version von  [https://nodejs.org](https://nodejs.org) herunter und überprüfe die Installation mit `node -v` in der Befehlszeile.


Erste Schritte zur Ausführung eines JavaScript Codes

Um Ihre erste JavaScript-Anwendung auszuführen, führe diese Schritte durch

1. **Erstelle einen Projektordner**: Lege einen Ordner auf deinem Computer an, z.B. `beginning_javascript`, der alle deine Dateien enthält.

2. **Öffne den Ordner in VSCode**: Öffne Visual Studio Code und wähle `File > Open Folder…` aus der Menüleiste, um den gerade erstellten Ordner zu öffnen..

3. **Erstelle eine HTML-Datei**: Erstelle eine neue Datei und speichere diese als `index.html`.
  Füge den folgenden Standard-HTML-Code ein:

  ```html
  <!DOCTYPE html>
  <html lang="en">
    <head>
      <meta charset="UTF-8">
      <meta name="viewport" content="width=device-width, initial-scale=1.0">
      <title>Document</title>
      <script src="script.js" defer></script>
    </head>
    <body>
      <h1>Hello World!</h1>
    </body>
  </html>
  ```
4. Das `<script>`-Tag mit dem `defer`-Attribut stellt sicher, dass das JavaScript erst verarbeitet wird, nachdem das HTML-Dokument vom Browser geladen wurde.

5. **Installiere die Live Server Extension**: Dies ist eine nützliche VSCode-Erweiterung, die dir ermöglicht, einen lokalen Server zum Testen deines Codes zu starten.
   1. Klicke auf das Erweiterungssymbol (ein Puzzle-Block) in der Aktivitätsleiste oder drücke `Strg+Umschalt+X` (oder `Command+Umschalt+X` auf macOS).
   2. Suche nach `'live server'` und wähle die von Ritwick Dey erstellte aus (siehe https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer). Installiere diese. 


6. **Starte den Live Server**: Kehre zum Explorer-Tab zurück, klicke mit der rechten Maustaste auf die Datei `index.html` und wähle `Open with Live Server` aus dem Kontextmenü. Dein Browser sollte sich automatisch öffnen und die HTML-Datei anzeigen.

7. **Erstelle eine JavaScript-Datei**: Erstelle im Explorer-Sidebar eine neue Datei mit dem Namen `script.js.

8. **Füge JavaScript-Code hinzu**: Schreibe den folgenden Code in die Datei `script.js`:

   ```javascript
   console.log('Learning JavaScript!');
   ```

9. Der `console.log()`-Befehl wird verwendet, um Ausgaben in die Browser-Konsole zu drucken.

10. **Öffne die Browser-Konsole**: In deinem Browser musst du die Konsole öffnen (z.B. mit `Command+Option+J` auf macOS oder `Strg+Umschalt+J` auf Windows/Linux).
    Du solltest die Meldung `'Learning JavaScript!'` in der Konsole sehen.

## Musterlösungen der Aufgaben

### 1. Variablen & Datentypen

In JavaScript gibt es verschiedene Datentypen, die unterschiedliche Arten von Werten darstellen. Hier sind die wichtigsten: String, Number, Boolean, null, undefined und ~~Symbol~~.

**String:** Ein String ist eine Folge von Zeichen und wird verwendet, um Text darzustellen. Er wird in einfachen oder doppelten Anführungszeichen eingeschlossen.

```javascript
let meineZeichenkette = "Hallo Welt!";
let meinName = 'Max Mustermann';
```

**Number:** Der Datentyp Number repräsentiert sowohl ganze Zahlen als auch Gleitkommazahlen (Dezimalzahlen).

```javascript
let meineZahl = 10;
let pi = 3.1415;
let negativeZahl = -5;
```

**Boolean:** Ein Boolean-Wert kann entweder `true` (wahr) oder `false` (falsch) sein. 

Er wird oft in Kontrollstrukturen verwendet, um Bedingungen zu überprüfen.

```javascript
let istWahr = true;
let istFalsch = false;
```

**Null:** `null` stellt einen absichtlich nicht vorhandenen Wert dar. Es ist ein eigenständiger Datentyp und kein Objekt.

```javascript
let meinWert = null;
```

Undefined: `undefined` wird verwendet, wenn einer Variablen noch kein Wert zugewiesen wurde. Es ist der Standardwert für Variablen, die deklariert, aber nicht initialisiert wurden.

```javascript
let meineVariable; // meineVariable ist undefined
console.log(meineVariable); // Ausgabe: undefined
```

### 2. Operatoren & Kontrollstrukturen

TODO

## Beispiel-Quiz

**Frage 1 (1 Punkt)**
Welche der folgenden Variablendeklarationen ist **blockscope** und wird in React bevorzugt?
 a) `var`
 b) `let`
 c) `const`
 *(1 richtige Antwort)*

**Frage 2 (1 Punkt)**
Welche Ausgabe erzeugt folgender Code?

```javascript
let x = "5";
let y = 5;
console.log(x == y, x === y);
```

a) `true false`
b) `false true`
c) `true true`

**Frage 3 (2 Punkte)**
Schreibe eine **Arrow Function** `square`, die eine Zahl quadriert und zurückgibt.
Beispiel: `square(4)` → `16`

**Frage 4 (2 Punkte)**
Gegeben:

```javascript
let numbers = [1, 2, 3, 4, 5];
```

a) Nutze `filter`, um alle geraden Zahlen zu erhalten. *(1 Punkt)*

b) Nutze `map`, um jede Zahl zu verdoppeln. *(1 Punkt)*

**Frage 5 (2 Punkte)**

Welcher Code fügt einen Klick-Eventlistener zu einem Button mit der ID `saveBtn` hinzu, sodass `"Gespeichert!"` in der Konsole ausgegeben wird?
 *(Schreibe nur die relevanten 2–3 Zeilen)*

**Frage 6 (2 Punkte)**
Kurze Erklärung: Was ist der Unterschied zwischen **primitive** und **referenzbasierten** Datentypen in JavaScript?
 *(max. 2 Sätze)*
