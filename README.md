 CodeWe1302JavaScript
====================

Coding Weekend Project 2013-02 JavaScript Framework Evaluation

## Projektmotivation 

### Grundidee

* Evaluierung diverser JavaScript Frameworks durch Realisierung einer äquivalenten Testapplikation
* Ähnliches Projekt mit ToDo-App als Referenz: http://addyosmani.github.com/todomvc/

### Verzeichnis der Projekte mit umgesetzten Testapplikationen

* Backbone.js mit Underscore.js und Docco
  - https://github.com/sebastianfuss/backbone-test
* JavaScriptMVC mit StealJS, DocumentJS, jQuery und FuncUnit (QUnit, Selenium, Jasmine)
  - https://github.com/realthargor/javascriptMVCCodingWe
* AngularJS & AngularUI  mit Bootstrap und jQueryUI 
  - https://github.com/dataduke/CodeWe1302AngularJs

## Grundlagen zum JavaScript-Stack

### Aufbau des Frontends (Layers und Dependencies)

Top-Down-Architektur:

1. Eigene Applikation (Testapplikation)
2. JS Framework (Framework zur Evaluierung)
3. jQuery und andere JS Framework Dependencies (on Top von Protoype/Utilities)
4. PrototypeJS und/oder andere Utility-Frameworks (Low-Level-Funktionen und Patterns für Objekte)
5. JavaScript

### Funktionalitäten von JS-Frameworks

Gemeinsamkeiten (Häufige Standards):

- Templating
- Model-Binding
- Pageflow, Routing
- Messages, REST
- JS Dokumentation

Unterschiede:

- Patterns: MVC (Model-View-Controller) vs. MVVM (Model-View-ViewModel)

## Testumfeld

### Geschäftsprozess

Kundenerfassung mit Personendaten, Adressdaten und Bestätigung der gemachten Angaben.

### Felder der Testapplikation (Referenzimplementierung)

Personendaten (Page):

- Name und Vorname: Text-Fields (required)
- Geburtstag: Date-Field mit DatePicker (required)
- Kreditkarten Nummer: Number-Field (required, genau 10-stellig)

Adressdaten (Page):

- Land: Drop-Down-Box (required, mit Default-Wert)
- Strasse und Hausnummer: Text-Field und Number-Field (required)
- PLZ und Ort: Number-Field (Validierung mit automatischer Befüllung des Ortes)
- Wohnhaft seit: Date-Field mit DatePicker (required)
- if (Wohnhaft seit) < 2 Jahre: Neue Adressegruppe mit vorheriger Adresse (Toogle show/hide)

Zusammenfassung (Page):

- Datenwiedergabe (Labels, Output Fields)
- Datenbestätigung (Checkbox)
- Submit (Gemockter REST-Call zum Backend)

Ende (Page):

- Danke (Text)
- Neubestellung (Link zu Personendaten, Loop)

### Features der Testapplikation

siehe Beschreibung bei https://github.com/sebastianfuss/backbone-test

## JavaScript-Frameworks

### Ausgewählte Testkandidaten 

* AngularJS (http://angularjs.org/,  http://www.youtube.com/user/angularjs) & AngularUI (http://angular-ui.github.com/) 
  - __[DONE]__ TestApp Build mit Bootstrap, jQueryUI
* Backbone.js (http://backbonejs.org/) 
  - __[DONE]__ TestApp Build mit Underscore.js, Docco
* Ember.js (http://emberjs.com/)
* Knockout (http://knockoutjs.com/)
* JavaScriptMVC (http://javascriptmvc.com/) 
  - __[DONE]__ TestApp Build mit  StealJS, DocumentJS, jQuery, FuncUnit (QUnit, Selenium, Jasmine)

### Kurzvorstellung und Beschreibungen

siehe Dokumentation in einzelnen Projekt-Repos

## Evaluierung

### Evaluierungskriterien

- Pageflow, Routing
- Model, Data-Binding
- Felderdeklaration, Validierung
- REST-Anbindung
- Dokumentation
- Unit-Tests für Validierung, Pageflow

### Evaluierungsergebnisse

siehe Dokumentation in einzelnen Projekt-Repos

## Zusammenfassung und Fazit

TBD

## Referenzen

### Unterstützende Frameworks

- jQuery (http://jquery.com/), jQueryUI (http://jqueryui.com/), QUnit (http://qunitjs.com/) : Einige JS Frameworks bauen darauf auf (Dependencies)
- PrototypeJS (http://prototypejs.org/) : Sammlung von JavaScript-Basisfunktionalitäten; wird in  Kombination mit jQuery und Backbone.js häufig verwendet
- Bootstrap (http://twitter.github.com/bootstrap/) : Utility-Framework für Layout, HTML, CSS etc. 
- Underscore.js (http://underscorejs.org/) : Utility-Framework, welches grundlegende Hilfsfunktionen liefert, Vgl. Java Commons API
- Docco (http://jashkenas.github.com/docco/) : Codedokumentation
- Node.js (http://nodejs.org/) : Event-driven I/O server-side JavaScript environment
- RequireJS (http://requirejs.org/) : Module and File Loader for JS, verwendet bei einigen JS Frameworks (Dependencies)
- DocumentJS (http://javascriptmvc.com/docs.html#!/search/DocumentJS) : Codedokumentation
- StealJS (http://javascriptmvc.com/docs.html#!steal) : Collection of command line and JS client utilities that make building, packaging, and sharing JS applications
- FuncUnit (http://javascriptmvc.com/docs.html#!FuncUnit) : Testing of web applications with a simple jQuery-like syntax via integration with Jasmin (behavior-driven development framework), Selenium (capture and replay tool) and PhantomJS (headless WebKit with JavaScript API with support for  DOM handling, CSS selector, JSON, Canvas, and SVG) and automated QUnit tests (unit testing).

### Tools und Literatur

- JS Editoren/IDEs: 
    - WebStorm (http://www.jetbrains.com/webstorm/) : Kommerzielle IDE
    - NetBeans (http://netbeans.org/) : Open Source IDE
    - Cloud9IDE (https://c9.io/) : Online Editor mit Konsole und Repo-Anbing nach GitHub, BitBucket etc.
- JS Web Tools:
    - JSFiddle (http://jsfiddle.net/) : Online Editor with Code Sharing
    - cdnjs (http://cdnjs.com/) : Online hosted JS libraries/frameworks
    - Google CDN (https://developers.google.com/speed/libraries/devguide) : Online hosted libraries
    - Microsoft CDN (http://www.asp.net/ajaxlibrary/cdn.ashx) : Online hosted libraries
- Books: 
    - JavaScript Patterns (Stoyan Stefanov)

