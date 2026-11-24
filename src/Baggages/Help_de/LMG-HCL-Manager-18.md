### HCL-Manager-18

Jeder Lichtmanager 1..N besitzt identischen Aufbau. Die Kanalseite „LM x" ist in folgende Abschnitte gegliedert:

- **Kanaldefinition**: Beschreibung und Suspendiert.
- **HCL-Ausgang**: HCL-Achsen, HCL-Zeitfenster, Bereitstellung der Lichtmanager-Sollwerte und Status-KOs (siehe Status-KOs je Lichtmanager).
- **Profile**: Anzahl Profile (1–4). Jedes Profil hat eine eigene Unterseite mit Wochentagen, Saison und bis zu 10 Stützpunkten.
- **Externe Eingänge & Steuerobjekte**: Sperr-Verhalten mit Rückfallstrategie, adaptive Helligkeit, Tag/Nacht-Quelle sowie externe Farbtemperatur- und Helligkeitsquelle.
- **Saisonale Umschaltung**: Wechsel zwischen Sommer- und Winter-Profilen (siehe Saison-Profil).
- **Sende-Verhalten**: Aktualisierungsintervall.
- **Vorausschau & Fortschritt**: optionale KOs zum nächsten Stützpunkt und zum Tagesverlauf.

Im Baum liegen unter jedem Lichtmanager die Unterseiten **HCL-Kurve**, **Profil 1..n** und, wenn aktiviert, **Adaptive Helligkeit**.
