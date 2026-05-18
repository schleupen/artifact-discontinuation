# artifact-discontinuation

In diesem Repository werden die von Schleupen abgekündigten ("obsolete") und entfernten Artefakte ("removed") der Schleupen.CS 3.0-Software aufgeführt.
Folgende Artefakt-Arten werden betrachtet:
 * Cmdlets (PowerShell)
 * Packages (NuGet)
 * Privileged Interfaces
 * Services
 * User Interfaces

In jedem dieser Verzeichnisse finden sich jeweils eine `obsolete.json`- und eine `removed.json`-Datei. Diese Dateien enthalten jeweils als relevante Informationen (hier anhand von Beispieldaten):
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
Beachte: Die Versionsangaben in den Dateien `obsolete.json` und `removed.json` (z.B. `discontinuation-version` in obigem Beispiel) beziehen sich auf den **Entwicklungsbeginn** (hier WV24). Dieser unterscheidet sich vom **Auslieferungszeitpunkt** der jeweiligen Version, der nach Abschluss der Entwicklungsperiode liegt. Die beiden Zeitpunkte haben damit typischerweise einen Abstand von ca. 3 Monaten. 
