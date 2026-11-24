### Kommunikationsobjekte

### Globale Kommunikationsobjekte

#### Sperre (global) / Status Sperre
Globale Sperre inkl. Statusrückmeldung.

#### Entsperren Trigger
1-Bit Triggerobjekt zum gleichzeitigen Aufheben aller globalen, manager-spezifischen und kanal-spezifischen Sperren.

#### Sperre Lichtmanager 1..N / Status
Lichtmanager-spezifische Sperrobjekte inkl. Statusrückmeldung.
Sichtbar nur für Lichtmanager, die in der **Kanalauswahl** aktiviert sind.

#### Lichtmanager Status Helligkeit Soll / Farbtemperatur Soll
Je Lichtmanager zwei Sollwert-KOs; Sichtbarkeit abhängig von Option **Status-KOs je Lichtmanager**.

### Pro-Lichtmanager Kommunikationsobjekte

#### LM x: Eingang, Sommer=1 (K04)
1-Bit Eingang (DPT 1.001). Nur sichtbar bei **Saisonale Umschaltung** = `Kommunikationsobjekt`. Der Zustand wird gespeichert, wenn unter Lichtmanager → Allgemein „Saisonalen Zustand speichern…" auf **Ja** steht.

#### Helligkeitssensor (Lux)
2-Byte Eingang (DPT 9.004). Eingang für die adaptive Helligkeitsregelung.

#### Tag/Nacht (K06)
1-Bit Eingang (DPT 1.001). Nur sichtbar bei `DayNightSource = KO` (Adaptive Helligkeit oder Slew Tag/Nacht).

#### Adaptive Helligkeit aktiv
1-Bit Ausgang (DPT 1.011). Status der adaptiven Regelung.

### Pro-Kanal Kommunikationsobjekte (0.3.0)

| KO | Nr. | DPT | Funktion | Bedingung |
|---|---|---|---|---|
| Sperre | K02 | DPST-1-3 | Vollsperre Ein/Aus | `UseLock ≠ Nein` |
| Status Sperre | K03 | DPST-1-11 | Status der Kanalsperre | `UseLock ≠ Nein` |
| Status Tunable White kombiniert | K08 | DPST-249-600 | Helligkeit + CT + Überblendzeit | `StatusKoOutput` inkl. Kombiniert |
| LockColor | K09 | DPST-1-3 | Farbtemperatur-Achse sperren | `UseLock = Getrennt` |
| LockBrightness | K10 | DPST-1-3 | Helligkeits-Achse sperren | `UseLock = Getrennt` |
| Minuten bis nächstem SP | K11 | DPT 7.006 | Vorausschau: Minuten | `PreviewEnable = Ja` |
| Nächste Farbtemperatur | K12 | DPT 7.600 | Vorausschau: CT des nächsten SP | `PreviewEnable = Ja` |
| Nächste Helligkeit | K13 | DPT 5.001 | Vorausschau: Helligkeit des nächsten SP | `PreviewEnable = Ja` |
| Tagesfortschritt | K14 | DPT 5.001 | 0–100 % des Tagesverlaufs | `ProgressEnable = Ja` |
| Tagesphase | K15 | DPT 5.010 | 0=vor Aufgang … 5=Nacht | `ProgressEnable = Ja` |
| Externe Helligkeit (%) | K16 | DPT 5.001 | Externe Helligkeitsquelle | `ExtBrightnessDpt = Prozent` |
| Externe Helligkeit (lx) | K17 | DPT 9.004 | Externe Helligkeit, Lux-skaliert | `ExtBrightnessDpt = Lux` |
| Externe Farbtemperatur (K) | K18 | DPT 7.600 | Externe CT-Quelle | `ExtColorTempDpt = Kelvin` |
| Externe Farbtemperatur (Skalar) | K19 | DPT 5.001 | Externe CT, skaliert | `ExtColorTempDpt = Skalar` |

