<p align="center">
  <img src="blood-moon.svg" alt="Blutroter Mond – BloodyEclipseAssistant" width="100%">
</p>

<p align="center">
  <b>Your perfect <i>half</i> intelligent assistant 🌑🩸</b><br>
  <sub>Stundenplan trifft Kalender – wenn der Mond rot wird, ist dein Tag geplant.</sub>
</p>

<p align="center">
  <img alt="Status" src="https://img.shields.io/badge/status-in%20development-b30d12?style=for-the-badge">
  <img alt="Untis" src="https://img.shields.io/badge/Untis-compatible-ff6a4d?style=for-the-badge">
  <img alt="Google Calendar" src="https://img.shields.io/badge/Google%20Calendar-compatible-8b0a10?style=for-the-badge">
  <img alt="Intelligence" src="https://img.shields.io/badge/intelligence-50%25-5a0508?style=for-the-badge">
</p>

---

## 🌒 Was ist das?

Der **BloodyEclipseAssistant** ist ein persönlicher Assistent, der zwei Welten verbindet:

- 📚 **Untis** – dein Stundenplan, Vertretungen und Ausfälle
- 📅 **Google Calendar** – Termine, Erinnerungen, Freizeit

Er gleicht beides ab, erkennt Konflikte und hilft dir, den Überblick zu behalten. Und ja: Er ist nur **halb** intelligent – dafür mit voller Überzeugung. 😉

## ✨ Features

| | Feature | Status |
|---|---|---|
| 📚 | Stundenplan aus Untis abrufen | 🔜 geplant |
| 📅 | Termine mit Google Calendar synchronisieren | 🔜 geplant |
| ⚠️ | Konflikte zwischen Unterricht und Terminen erkennen | 🔜 geplant |
| 🔔 | Erinnerungen bei Vertretung und Ausfall | 🔜 geplant |
| 🗣️ | Sprachausgabe: sagt Tagesplan und Änderungen von selbst an | 🔜 geplant |
| 🧠 | „Halb-intelligente" Vorschläge für freie Zeitfenster | 💡 Idee |
| 🌑 | Eclipse-Modus (Dark Theme, natürlich blutrot) | 💡 Idee |

> Den genauen Fortschritt findest du in der [**TODO.md**](TODO.md).

## 🧭 Technische Pläne

| Dokument | Inhalt |
|---|---|
| [**Gesamtplan**](docs/PLAN.md) | Technik-Entscheidungen, Architektur, Projektstruktur, Meilensteine |
| [**Plan 01 – Untis ↔ Google Calendar**](docs/01-untis-google-sync.md) | Zugriff, Berechtigungen, Sync-Ablauf, Änderungs-Erkennung, Konflikte |
| [**Plan 02 – Sprachausgabe**](docs/02-sprachausgabe.md) | Wann und wie der Assistent spricht, Stimme, Satzbau, Ansage-Regeln |

## 🗺️ So funktioniert's

```mermaid
flowchart LR
    U[📚 Untis] --> A{{🌑 BloodyEclipse<br/>Assistant}}
    G[📅 Google Calendar] --> A
    A --> K[⚠️ Konflikt-Check]
    A --> V[💡 Vorschläge]
    A --> N[🔔 Benachrichtigungen]
    A --> S[🗣️ Sprachausgabe]
    style A fill:#b30d12,stroke:#5a0508,color:#fff
```

## 🌗 Mondphasen der Entwicklung

```
🌑  Idee & Repository          ✅
🌒  Untis-Anbindung            ⬜
🌓  Google-Calendar-Anbindung  ⬜
🌔  Abgleich & Konflikt-Logik  ⬜
🩸  Sprachausgabe & Assistenz  ⬜
🌕  Release                    ⬜  ← Vollmond, aber blutrot
```

## 🚀 Loslegen

> ⚠️ Das Projekt befindet sich noch am Anfang – die Schritte unten sind der Plan.

```bash
# Repository klonen
git clone https://github.com/Duo-FrozenPIXEL/BloodyEclipseAssistant.git
cd BloodyEclipseAssistant
```

<details>
<summary>🔐 Zugangsdaten (Platzhalter)</summary>

Zugangsdaten gehören **nie** ins Repository. Kopiere [`.env.example`](.env.example) nach `.env` (steht in der `.gitignore`) und fülle sie aus:

```env
UNTIS_SERVER=
UNTIS_SCHOOL=
UNTIS_USER=
UNTIS_PASSWORD=
GOOGLE_CREDENTIALS_FILE=secrets/credentials.json
GOOGLE_TOKEN_FILE=secrets/token.json
```

Alle weiteren Einstellungen (Sync-Takt, Stimme, Ansagezeiten) stehen in der `.env.example`.

</details>

## 🧩 Fun Facts

- 🌑 Eine **Blutmond**-Färbung entsteht bei einer totalen Mondfinsternis: Der Mond liegt im Erdschatten und wird nur noch von rotem Licht bestrahlt, das durch die Erdatmosphäre gebrochen wird.
- 🤖 „Halb intelligent" heißt: kluge Vorschläge – aber du hast immer das letzte Wort.

## 🤝 Mitmachen

Ideen, Bugs oder Wünsche? Erstelle gerne ein [Issue](https://github.com/Duo-FrozenPIXEL/BloodyEclipseAssistant/issues) oder einen Pull Request.

---

<p align="center">
  Made with 🩸 by <a href="https://github.com/Duo-FrozenPIXEL"><b>Duo-FrozenPIXEL</b></a>
</p>
