# Ballspielturnier – Kurzanleitung (ENTWURF)

`ballturnier.html` ist eine einzelne Datei, die komplett offline läuft (Doppelklick → öffnet im Browser). Es gibt keinen Server, kein Login und keine Internetverbindung. Alle Daten bleiben auf dem Gerät. Empfohlen: aktueller Edge, Chrome oder Firefox, für die Turnierleitung am besten am Laptop.

## Ablauf (Reiter oben)

1. **Rahmendaten**: Turniername, Datum, Anzahl Hallen (1–12) mit Name und Sportart, Startzeit, spätestes Ende, Spieldauer je Sportart, Wechselzeit, Blockpausen. Der Überblick zeigt, ob die Vorrunde ins Zeitfenster passt.
2. **Klassen**: Mehrere auf einmal eingeben, z. B. `5a, 5b, 6a` (oder eine Spalte aus Excel einfügen), dann Enter.
3. **Gruppen**: 1 oder 2 Gruppen anlegen und „Automatisch verteilen“ (zufällig oder nach Reihenfolge). Anpassen geht per Ziehen mit der Maus (auf eine Klasse ziehen = tauschen) oder über das Auswahlfeld an der Klasse.
4. **Spielplan**: „Spielplan erzeugen“ berechnet die Vorrunde: jede gegen jede, in jeder Sportart genau einmal, ohne Doppelbelegung. Ziele sind möglichst wenige Runden, gleichmäßige Pausen und kein Wechsel zur gleichen Sportart direkt hintereinander.
   - Verschieben: Spiel antippen, dann ein freies Feld oder ein anderes Spiel (Tausch) antippen. Konflikte werden rot markiert.
   - Ansichten: Gesamtübersicht, je Halle, je Klasse.
   - PDF: Gesamtspielplan, Hallenpläne (eine PDF oder je Halle eine eigene) und Laufzettel je Klasse.
5. **Ergebnisse**: Zwei Zahlenfelder je Spiel, Enter springt ins nächste Feld, mit Filtern. Rechts steht die Tabelle live.
6. **Tabelle**: Wertung nach Punkteschema und Tie-Break. Bei echtem Gleichstand lässt sich die Reihenfolge manuell festlegen (Los). Auch als PDF.
7. **Playoffs** (optional): 1. A gegen 1. B, 2. A gegen 2. B usw. (bei 1 Gruppe: 1.–2., 3.–4.). Je Paarung ein Spiel, die Sportart ist frei wählbar. Bei Unentschieden werden Sieger und Vermerk festgelegt. Auch als PDF.
8. **Urkunden**: Vorlage hochladen (PNG, JPG oder PDF), Textfelder in der Vorschau verschieben und mit Platzhaltern wie `{klasse}` und `{platzText}` versehen. Danach eine PDF mit allen Urkunden, nur Platz 1 bis N oder einzeln. Ohne Vorlage entsteht eine schlichte Standard-Urkunde.

**⚙ Punkteschema & Daten**: Punkteschema je Sportart (Parameter oder eigene Formel), Reihenfolge der Tie-Break-Kriterien, Backup und „Neues Turnier“.

Zeiten (Start, Spieldauer, Pausen) lassen sich nach dem Erzeugen ändern, die Uhrzeiten verschieben sich dann einfach mit. Ändern sich Hallen oder Gruppen, warnt die App. Beim Neu-Erzeugen lässt sich wählen, ob passende Ergebnisse übernommen werden.

## Speichern und Backup – wichtig

- **Automatisch**: Nach jeder Änderung wird ein Zwischenstand im Browser gespeichert. Er bleibt nur in diesem Browser auf diesem Gerät.
- **Backup speichern** (oben rechts): Lädt den kompletten Stand als `Turnier_JJJJ-MM-TT_HHMM.json` herunter, einschließlich Urkundenvorlage. Oben steht, wie lange das letzte Backup her ist.
- **Backup laden**: Stellt einen Stand vollständig wieder her, nach einem Warnhinweis. So geht es auf einem anderen Gerät weiter.
- Wer Verlauf oder Websitedaten löscht oder in einem privaten Fenster arbeitet, verliert den Zwischenstand. Deshalb am Turniertag regelmäßig ein Backup speichern, z. B. auf einen USB-Stick oder nach OneDrive.
- **Neues Turnier**: Übernimmt auf Wunsch Hallen, Zeiten, Punkteschema und Urkundenvorlage als Vorbelegung.

## Hinweise zum Entwurf

- Das **Punkteschema** (Sieg 3 / Unentschieden 1 / Niederlage 0) und die **Tie-Break-Reihenfolge** sind Platzhalter. Sie lassen sich unter ⚙ ohne Programmänderung ersetzen.
- Alle Spiele einer Runde beginnen gleichzeitig. Der Takt ergibt sich aus der längsten Spieldauer plus Wechselzeit.
- Eingebettete Bibliotheken (unverändert, am Dateiende): jsPDF 2.5.2 und jsPDF-AutoTable 3.8.4 (MIT), pdf.js 3.11.174 (Apache-2.0).
