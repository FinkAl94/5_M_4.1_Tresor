# Ballturnier – Kurzanleitung (ENTWURF)

`ballturnier.html` ist eine einzelne Datei, die komplett offline läuft (Doppelklick → öffnet im Browser). Es gibt keinen Server, kein Login und keine Internetverbindung. Alle Daten bleiben auf dem Gerät. Empfohlen: aktueller Edge, Chrome oder Firefox, für die Turnierleitung am besten am Laptop.

**Voreinstellungen wie beim Turnier 2025:**
- Felder T1–T2 Fußball, T3–T4 Handball, T5–T6 Basketball, Halle 7 Ballparcours.
- Beginn 8:40, 10 Min. Spiel und 10 Min. Wechsel.
- 3 Gruppen, a-Klassen in Gruppe C; jede Klasse spielt jede Ballsportart 2× und geht einmal in den Ballparcours (2 Klassen je Runde).
- 1 Punkt pro Tor bzw. Korb; Ballparcours-Punkte werden direkt eingetragen und zählen mit.
- Platzierungsspiele nach „Treffen in Halle 3“, danach Siegerehrung.

Alles lässt sich je Turnier ändern.

## Ablauf (Reiter oben)

1. **Rahmendaten**: Turniername und Datum. **Sportarten** hinzufügen, umbenennen oder entfernen: „Spiel“ (zwei Klassen gegeneinander, z. B. Volleyball) oder „Station“ (jede Klasse einmal, Punkte eintragen, z. B. Ballparcours, Torwandschießen; je Station ein/aus und Klassen je Runde). Eine neue Sportart braucht mindestens eine Halle; Sportarten mit eingetragenen Ergebnissen lassen sich nicht entfernen. Turniermodus: „feste Anzahl Spiele je Sportart“ (wie 2025) oder „jeder gegen jeden in jeder Sportart“.  Dazu Hallen/Felder mit Sportart, Zeiten und Blockpausen sowie der Schalter **„Platzierungsrunde durchführen“** – ohne Platzierungsrunde ergibt sich die Endplatzierung direkt aus der Vorrunde, die Siegerehrung folgt direkt danach. Der Überblick zeigt, ob alles ins Zeitfenster passt.
2. **Klassen**: Mehrere auf einmal eingeben, z. B. `8Ga 8Gb 8Ra` (oder eine Spalte aus Excel einfügen), dann Enter.
3. **Gruppen**: 1 bis 8 Gruppen anlegen (−/+ oder Zahl eingeben) und „Automatisch verteilen“. Voreingestellt wie 2025: Alle Klassen, die auf **a** enden (8Ga, 8Ra, 8Ma …), kommen in **Gruppe C**, die übrigen zufällig und möglichst gleich groß in A und B. Buchstabe und Zielgruppe sind einstellbar. Anpassen geht per Ziehen mit der Maus oder über das Auswahlfeld an der Klasse.
4. **Spielplan**: „Spielplan erzeugen“ berechnet die Vorrunde automatisch. Gegner kommen aus der eigenen Gruppe; bei ungerader Gruppengröße spielt je Runde eine Klasse gegen eine andere Gruppe, wie 2025 bei B und C. Ziele: keine Doppelbelegung, möglichst wenige Runden, wechselnde Sportarten und Gegner.
   - Verschieben: Spiel antippen, dann ein freies Feld oder ein anderes Spiel (Tausch) antippen.
   - Der Ballparcours ist eine eigene Station (Halle 7): Jede Klasse kommt genau einmal dran und hat in dieser Runde kein Spiel. Mit 12 Klassen und 2 Klassen je Runde sind es 7 Runden (8:40–10:50).
   - PDF: Gesamtplan, **Gesamtablauf** (Vorrunde, Treffen, Platzierungsspiele, Siegerehrung auf einer Seite), Pläne je Feld (für Halle 7 mit Spalten für Zeit und Punkte) und Laufzettel je Klasse.
5. **Ergebnisse**: Tore bzw. Körbe je Spiel eintragen; beim Ballparcours die Punkte (Zeit optional). Enter springt ins nächste Feld. Rechts steht die Tabelle live.
6. **Tabelle**: Rangliste je Gruppe nach Punkten. Gruppenübergreifende Spiele zählen für die eigene Klasse. Bei Gleichstand lässt sich die Reihenfolge manuell festlegen (Los).
7. **Platzierungsspiele**: Gruppenpaare frei einstellbar (z. B. A–B und C–D); je Paar 1. gegen 1., 2. gegen 2. usw.
   - Weitere Runden (bei 2, 4 oder 8 Gruppenpaaren) je Rang wählbar: Sieger gegen Sieger, Verlierer gegen Verlierer – bei A–B und C–D z. B. Finale (Sieger 1.A–1.B gegen Sieger 1.C–1.D) und Spiel um Platz 3. Voreingestellt nur für die Gruppenersten; ohne weitere Runde entscheiden die Vorrundenpunkte.
   - Gruppe C bekommt ein Sonderspiel mit frei wählbaren Namen (voreingestellt „Allstars Gruppe C – Allstars“). Ihre Platzierung ergibt sich aus den Vorrundenpunkten.
   - Klassen ohne Gegenplatz (z. B. 5. Gruppe B) bekommen ein Zusatzspiel mit frei wählbarem Gegner, ohne Einfluss auf die Platzierung.
   - Sportart und Halle sind je Spiel frei und unabhängig voneinander wählbar; die Vorrunden-Sportart einer Halle steht nur als Hinweis dabei. Bei Unentschieden wird der Sieger mit Vermerk festgelegt.
   - Spiele aussetzen: Über „Gespielt werden“ (z. B. nur 1. gegen 1. oder bis 3. gegen 3.) oder je Spiel über das Häkchen „spielen“. Ausgesetzte Paarungen erhalten ihren Platz nach Vorrundenpunkten (wahlweise geteilter Platz). Spiele mit Ergebnis lassen sich nicht aussetzen.
8. **Urkunden**: Vorlage hochladen (PNG, JPG oder PDF), Textfelder verschieben, Platzhalter wie `{klasse}` und `{platzText}` verwenden. Danach eine PDF mit allen, nur den besten oder einzelnen Urkunden.

**⚙ Punkteschema & Daten**: Punkteschema je Sportart (Parameter oder eigene Formel), Reihenfolge bei Gleichstand, Backup und „Neues Turnier“.

## Speichern und Backup – wichtig

- **Automatisch**: Nach jeder Änderung wird ein Zwischenstand im Browser gespeichert. Er bleibt nur in diesem Browser auf diesem Gerät.
- **Backup speichern** (oben rechts): Lädt den kompletten Stand als `Turnier_JJJJ-MM-TT_HHMM.json` herunter, einschließlich Urkundenvorlage.
- **Backup laden**: Stellt einen Stand vollständig wieder her, nach einem Warnhinweis. So geht es auf einem anderen Gerät weiter.
- Wer Browserdaten löscht oder in einem privaten Fenster arbeitet, verliert den Zwischenstand. Deshalb am Turniertag regelmäßig ein Backup speichern.
- **Neues Turnier**: Übernimmt auf Wunsch Hallen, Zeiten, Punkteschema und Urkundenvorlage als Vorbelegung.

Eingebettete Bibliotheken (unverändert, am Dateiende): jsPDF 2.5.2 und jsPDF-AutoTable 3.8.4 (MIT), pdf.js 3.11.174 (Apache-2.0).
