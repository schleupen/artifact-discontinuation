# artifact-discontinuation

In diesem Repository werden die von Schleupen abgekündigten ("obsolet") und entfernten Artefakte ("removed") der Schleupen.CS 3.0-Software aufgeführt.
Folgende Artefakt-Arten werden betrachtet:
 * Cmdlets (Powershell)
 * Packages
 * Privileged Interfaces
 * Services
 * User Interfaces

In jedem dieser Verzeichnisse finden sich jeweils eine `obsolet.json`- und eine `removed.json`-Datei. Diese Dateien enthalten jeweils als relevante Informationen (hier an Hand von Beispieldaten):
```
  {
      "command": "Set-CSFeature",          // Identifikator des Artefaktes
      "successor": "Enable-CSFeature",     // optional: eine Information über einen Nachfolger
      "discontinuation-version": "WV24",   // Zeitpunkt, ab dem das Artefakt nicht mehr vorhanden sein wird (siehe releases.json)
      "discontinuation-date": null,        // Datum, ab der das Artefakt nicht mehr vorhanden sein wird
                                           // Beachte: discontinuation-version und -date sind wechselseitig gesetzt
      "obsolete-since": "2024-06-20",      // Zeitpunkt, seit dem das Artefakt abgekündigt ist
      "disruption": "24hLFW"               // Angabe, ob es eine Disruption gibt, an der der Service umgestellt werden muss
    },
```
