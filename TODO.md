# 🌑 TODO – BloodyEclipseAssistant

> Lebendes Dokument. Haken setzen mit `- [x]`.
> Die technischen Details zu jedem Punkt stehen in [docs/PLAN.md](docs/PLAN.md).

## 🌑 Phase 0 – Fundament (M0)
- [x] Repository anlegen
- [x] README mit Banner (blutroter Mond) einchecken
- [x] Programmiersprache & Projektstruktur festlegen → Python 3.12, siehe [Gesamtplan](docs/PLAN.md)
- [x] `.gitignore` (inkl. `.env`) und `.env.example`
- [ ] Lizenz hinzufügen (Empfehlung GPL-3.0, wegen Piper)
- [ ] `pyproject.toml` mit Abhängigkeiten, `ruff`, `pytest`
- [ ] `config.py`: `.env` laden und prüfen
- [ ] `python -m bea doctor`

## 🌒 Phase 1 – Untis lesen (M1) · [Plan 01](docs/01-untis-google-sync.md)
- [ ] Server und Schulkürzel aus der WebUntis-Adresse der Schule eintragen
- [ ] Login mit dem Schülerkonto testen – darf es den Stundenplan per Schnittstelle abrufen?
- [ ] Stundenplan für 14 Tage abrufen
- [ ] Ausfall, Vertretung, Raumwechsel und Prüfung auslesen; echte Feldnamen im Plan nachtragen
- [ ] In `Lesson` übersetzen, Doppelstunden bündeln, Schlüssel und Hash bilden
- [ ] `bea sync --dry-run` zeigt die Stunden als Tabelle

## 🌓 Phase 2 – Google schreiben (M2)
- [ ] Google-Cloud-Projekt, Calendar API aktivieren, OAuth-Client „Desktop-App"
- [ ] Zustimmungsbildschirm auf „In Produktion" stellen (sonst läuft das Login nach 7 Tagen ab)
- [ ] `bea login`: Token speichern und automatisch erneuern
- [ ] Eigenen Kalender „Untis 🌑" anlegen
- [ ] Termine anlegen / aktualisieren / löschen mit festen Event-IDs
- [ ] Zweiter Sync-Lauf verändert nichts

## 🌔 Phase 3 – Änderungen erkennen (M3)
- [ ] SQLite-Zustand (`lessons`, `changes`, `meta`)
- [ ] Vergleich alt/neu, `Change`-Einträge erzeugen
- [ ] Ausfälle im Kalender markieren
- [ ] Schutz vor Massenlöschung, erster Lauf ohne Changes
- [ ] Nächtlicher Voll-Abgleich gegen Google
- [ ] Fehlerbehandlung (Netz, Login, Limits)

## 🌕 Phase 4 – Stimme (M4) · [Plan 02](docs/02-sprachausgabe.md)
- [ ] Piper einbinden, Stimme `de_DE-thorsten-high` laden
- [ ] Satz-Bausteine: Uhrzeit, Stunde, Tag, Fach, Raum
- [ ] Sprechnamen für Fächer und Lehrkräfte in der Konfiguration
- [ ] Morgen-Ansage zusammenstellen
- [ ] `bea say heute | morgen | aenderungen`

## 🩸 Phase 5 – Assistenz (M5)
- [ ] Wiedergabe-Warteschlange mit Aufmerksamkeitston
- [ ] Ansage-Regeln: Ruhezeit, bündeln, nichts doppelt, Stumm-Schalter
- [ ] Zeitplan: Morgen-Ansage, Abend-Vorschau, „Gleich geht's weiter"
- [ ] Änderungen sofort ansagen
- [ ] `bea run` als Dauerbetrieb

## 🌘 Phase 6 – Konflikte & Dauerbetrieb (M6, M7)
- [ ] Private Termine lesen, Überschneidungen mit Unterricht erkennen
- [ ] Konflikte ansagen, freie Zeitfenster berechnen
- [ ] `systemd`-Dienst, Autostart
- [ ] Verhalten nach Neustart und Netzausfall testen

## ✨ Feinschliff & Release
- [ ] Tests für Vergleichslogik, Sätze und Ansage-Regeln
- [ ] Eclipse-Modus (Dark Theme in Blutrot)
- [ ] Screenshots und Hörprobe in die README
- [ ] Erstes Release 🎉

## 💡 Ideen-Speicher
- [ ] Zuhören: Aktivierungswort + Spracherkennung (Plan 02, Abschnitt 8)
- [ ] Freiere Formulierungen über ein Sprachmodell
- [ ] „Halb-intelligente" Vorschläge für freie Zeitfenster (Lernzeit, Pausen)
- [ ] Wochenübersicht als Bild / PDF
- [ ] Widget für den Homescreen
