# JavaScript

------

* Vobereitung: siehe [Notwendige Installationen](#install) unter Appendix 
* <span style="color:green">**Tag 1**</span> → JavaScript-Grundlagen mit Fokus auf alles, was für React unerlässlich ist.
* <span style="color:grey">**Tag 2**</span> → Vertiefung moderner JavaScript-Features + Vorbereitung auf React-Komponenten-Denken.

___



## **0. Einführung – Ziel des Kurses** *(10 Min)*

- Wer bin ich / Wozu lernen wir das?

- JavaScript als Basis für React

- Kursüberblick: Tag 1 = Grundlagen, Tag 2 = modernes JS + React-Denken

- Überprüfung der Installationen

  

*Übung:* ...

## 1. Variablen & Datentypen (25 Min)

* `let`, `const` vs. `var` (historisch)
* Primitive Typen (string, number, boolean, null, undefined)
* Arrays & Objekte – erste Einführung

*Übung:*

```javascript
let name = "Anna";
let age = 17;
let hobbies = ["Lesen", "Gaming"];
let person = { name: "Anna", age: 17 };

console.log(name, age, hobbies[1], person.name);

TODO: Ergänze das Code-Snippet 
```



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
   2. Suche nach `'live server'` und wähle die von Ritwick Dey erstellte aus. Installiere diese.


6. **Starte den Live Server**: Kehre zum Explorer-Tab zurück, klicke mit der rechten Maustaste auf die Datei `index.html` und wähle `Open with Live Server` aus dem Kontextmenü. Dein Browser sollte sich automatisch öffnen und die HTML-Datei anzeigen.

7. **Erstelle eine JavaScript-Datei**: Erstelle im Explorer-Sidebar eine neue Datei mit dem Namen `script.js.

8. **Füge JavaScript-Code hinzu**: Schreibe den folgenden Code in die Datei `script.js`:

   ```javascript
   console.log('Learning JavaScript!');
   ```

   

9. Der `console.log()`-Befehl wird verwendet, um Ausgaben in die Browser-Konsole zu drucken.

10. **Öffne die Browser-Konsole**: In deinem Browser musst du die Konsole öffnen (z.B. mit `Command+Option+J` auf macOS oder `Strg+Umschalt+J` auf Windows/Linux).
    Du solltest die Meldung `'Learning JavaScript!'` in der Konsole sehen.
