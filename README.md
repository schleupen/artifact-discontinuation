# artifact-discontinuation

In diesem Repository werden die von Schleupen abgekündigten ("obsolet") und entfernten Artefakte der Schleupen.CS 3.0-Software aufgeführt.
Folgende Artefakt-Arten werden betrachtet:
 * Cmdlets
 * Packages
 * Privileged Interfaces
 * Services
 * User Interfaces

In jedem dieser Verzeichnisse finden sich jeweils eine `obsolet.json`- und eine `removed.json`-Datei. Diese Dateien enthalten (hier an Hand von Beispieldaten):
```
  {
      "command": "Set-CSFeature",          // Identifikator des Artefaktes
      "successor": "Enable-CSFeature",     // optional: eine Information über einen Nachfolger
      "discontinuation-version": "WV24",   // erste Hauptversion, in der das Artefakt nicht mehr vorhanden sein wird
      "discontinuation-date": null,        // Datum, ab der das Artefakt nicht mehr vorhanden sein wird (-version und -date sind wechselseitig gesetzt)
      "obsolete-since": "2024-06-20",      // Zeitpunkt, seit dem das Artefakt abgekündigt ist
      "is-disruptive": false               // Angabe, ob es einen überlappenden Zeitraum (is-disruptive=false) mit der Verfügbarkeit des Nachfolgers oder nicht gibt (is-disruptive=true)
    },
```
