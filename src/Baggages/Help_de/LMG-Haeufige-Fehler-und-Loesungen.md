### Häufige Fehler und Lösungen

### Lichtmanager-Parameter oder HCL-KOs fehlen
- Lichtmanager global aktiviert?
- Lichtmanager in der **Kanalauswahl** aktiviert?
- Erst nach Aktivierung des globalen Lichtmanagers werden Zuordnung und Sperrparameter sichtbar.

### Lichtmanager wirkt nicht
- Lichtmanager global aktiviert?
- Manager im Konsumenten-Modul zugewiesen?
- Manager in der **Kanalauswahl** aktiviert und nicht **Suspendiert**?
- Gilt heute ein Profil? Mindestens ein Profil muss aktiv sein und unter **Gilt für** den aktuellen Wochentag (bzw. Urlaub/Feiertag) enthalten.
- Hat das Profil Stützpunkte mit sinnvollen Uhrzeiten bzw. Astro-Typen?
- Bei Astro-Stützpunkten: Standort und Zeitzone in den OpenKNX-Basisparametern gesetzt bzw. bei **Astro-Quelle** `Manuell` Sonnenauf- und -untergang eingetragen?
- Globale/spezifische Sperre aktiv?

### Saison-Profil schaltet nicht um
- **Saisonale Umschaltung** steht auf `Aus`? → Dann werden Profile mit der Saison `Sommer` oder `Winter` nicht gewählt.
- Ist bei den Profilen die **Saison** passend gesetzt (`Sommer`, `Winter`, `Sommer + Winter` oder `Fallback`)?
- Bei `Festes Datum`: Sommer-Beginn und Sommer-Ende korrekt eingetragen? Liegt das Datum im Bereich?
- Bei `Automatisch (Astro + Offset)`: Systemzeit und Datum korrekt?
- Bei `Kommunikationsobjekt`: KO `LM x: Eingang, Sommer=1` mit einer GA verbunden und Wert `1` gesendet?

