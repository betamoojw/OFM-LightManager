### Saison-Quelle (F7-Hybrid)

Parameter **Saisonale Umschaltung** (`SeasonSource`) je Lichtmanager:

- **Aus**: Profile mit der Saison `Sommer` oder `Winter` werden nicht gewählt (saison-neutral).
- **Automatisch (Astro + Offset)**: automatische Bestimmung; **Saison-Offset** (`SeasonOffsetDays`, −90…+90 Tage) verschiebt den Wechsel.
- **Festes Datum**: **Sommer-Beginn** / **Sommer-Ende** als (Monat, Tag); unterstützt Jahreswechsel-Übergang (Südhalbkugel).
- **Kommunikationsobjekt**: K04 `LM x: Eingang, Sommer=1` (DPT 1.001) schaltet zur Laufzeit.

**Vorbelegung** (`SummerActiveInit`, unter Lichtmanager → Allgemein): `Nichts (undefiniert)` / `Wert vom Bus lesen` / `Winter (0)` / `Sommer (1)`.

**Persistenz** (`SummerActiveSavePower=Ja`): letzter K04-Wert in `OpenKNX::Flash` (Per-Master Slot `{magic:0x03, summerActive:bool}`); überschreibt Init beim Reboot. Bei `Nein` wird der Slot mit `0x00`-Bytes überschrieben. Magic 0x03 ⇒ Layout-Mismatch (z. B. alter 0x02-Block) wird erkannt und ignoriert.

