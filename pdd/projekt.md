# Organisation 'Bausteine Computergestützter Datenanalyse'

## User Stories / Anwendungsfälle

### Potentielle Erstnutzer:in

Potentielle Erstnutzer:innen können sich auf einer Webseite einen schnellen Überblick zu vorhandenen Materialien zu verschaffen und diese detailliert sichten.

### Erstnutzer:innen

Erstnutzer:innen haben die Möglichkeit Bausteine auszuwählen und in einer für sie sinnvollen Art und Weise zusammenzufügen und falls notwendig zu ergänzen.

### Mathematik B (Master) HS Bochum

Der Kurs Mathematik B in den Masterstudiengängen Bauingenieurwesen und Umweltingenieurwesen behandelt Grundlagen der Statistik und die Anwendung von R zur Aufbereitung und Analyse von Datensätzen. Das Modul wird mit einer Studienarbeit abgeschlossen, die Aufgabenstellungen kommen dabei aus den Bereichen Verkehrswesen, Wasserwesen und dem konstruktiven Ingenieurbau.

Für den Kurs sind folgende Unterlagen notwendig:

- Mathematische Grundlagen

  - Skript als PDF und ggf. online als HTML-Dokument

  - Erklärvideos

  - Übungsaufgaben

  - Musterlösungen zu Übungsaufgaben

- Arbeiten mit R (dplyr und ggplot2)

  - Skript und Tutorials online und ggf. als PDF - Dokument

  - Erklärvideos

  - Übungsaufgaben

  - Musterlösungen zu Übungsauzfgaben

- Studienarbeiten

  - Aufgabenstellungen

  - Ergänzende Informationen zu Aufgaben

Zu Beginn des Semesters

- Auswahl der Inhalte für die Veranstaltung (falls Anpassung notwendig)

- Verlinkung der Dokumente von Moodle (wie oben)

Idealerweise werden alle Dokumente auf Github automatisch aktualisiert und es ist keinerlei Handarbeit notwendig, falls Unterlagen angepasst werden müssen (was immer wieder vorkommt, auch im laufenden Semester).

## Bausteine

### Liste

Methodenbausteine

TODO

Werkzeugbausteine

TODO

Anwendungsbausteine

TODO

### Inhalte

- Voraussetzungen

- Lernziele

- Unterlagen (Skript, Tutorial, Erklärvideos)

- Aufgaben mit Musterlösungen und Angaben zum geschätzten Zeitbedarf

Fragen

- Brauchen alle Arten von Bausteinen alle Inhalte? Ein Anwendungsbaustein kommt zum Beispiel ggf. ohne Unterlagen aus

## Technische Umsetzung

### Verzeichnisstruktur

#### Erste Möglichkeit: Gliederung nach Inhalten

```
BCD
├── pdd
│   ├── projekt.md
│   └── _quarto.yml
├── styleguide
│   ├── styleguide.md
│   └── _quarto.yml
├── voraussetzungen
│   ├── baustein-1
│   ├── baustein-2
│   ├── ...
├── lernziele
│   ├── baustein-1
│   ├── baustein-2
│   ├── ...
├── unterlagen
│   ├── baustein-1
│   ├── baustein-2
│   ├── ...
│   ├── _quarto.yaml
├── aufgaben
│   ├── baustein-1
│   ├── baustein-2
│   ├── ...
└── .gitignore
```

Funktioniert gut, wenn es nur Skript und Übungsaufgaben gibt, für BCD wahrscheinlich zu unhandlich.

#### Zweite Möglichkeit: Gliederung nach Bausteinen

```
BCD
├── pdd
│   ├── projekt.md
│   └── _quarto.yml
├── styleguide
│   ├── styleguide.md
│   └── _quarto.yml
├── bausteine
│   ├── baustein-1
│   │   ├── 01-voraussetzungen.qmd
│   │   ├── 02-lernziele.qmd
│   │   ├── 03-unterlagen
│   │   │   ├── 00-bilder
│   │   │   │   └── ...
│   │   │   └── skript.qmd
│   │   ├── 04-aufgaben
│   │   │   ├── 00-bilder
│   │   │   │   └── ...
│   │   │   ├── aaa.qmd
│   │   │   ├── bbb.qmd
│   │   │   └── ...
│   ├── baustein-2
│   │   ├── ...
│   └── _quarto.yml
└── .gitignore
```

Fragen

- Wie kann man die konkreten Aufgaben aus einem Katalog von Aufgaben auswählen?

- Wie entsteht aus den Teilaufgaben ein Aufgabenblatt

- Namenskonventionen

  - Groß und Kleinschreibung oder alles klein?

  - Leerzeichen erlaubt oder nicht?

  - Vorangestellte Ziffern für Sortierung?

  - Minus oder Unterstrich zur Abtrennung?

#### Eigener GitHub-Account, mehrere Repositories, Gliederung nach Bausteinen

Beide Varianten oben gehen von einem Repository für BCD aus. Eine Alternative wäre ein `bausteine-computergestuetzter-datenanalyse` - Account auf GitHub mit mehreren Repositories.

Beispiel: Corona-Warn-App (https://github.com/corona-warn-app).

```
bausteine-computergestuetzter-datenanalyse
├── bcd-dokumentation
│   ├── .github
│   │   └── workflows
    │       └── ...
│   ├── projekt.md
│   └── _quarto.yml
├── bcd-styleguide
│   ├── .github
│   │   └── workflows
    │       └── ...
│   ├── styleguide.md
│   └── _quarto.yml
└── bcd-bausteine
    ├── .github
    │   └── workflows
    │       └── ...
    ├── baustein-1
    │   ├── 01-voraussetzungen.qmd
    │   ├── 02-lernziele.qmd
    │   ├── 03-unterlagen
    │   │   ├── 00-bilder
    │   │   │   └── ...
    │   │   └── skript.qmd
    │   ├── 04-aufgaben
    │   │   ├── 00-bilder
    │   │   │   └── ...
    │   │   ├── aaa.qmd
    │   │   ├── bbb.qmd
    │   │   └── ...
    ├── baustein-2
    │   └── ...
    └── _quarto.yml
```

### Zusammenstellung von Materialien für einen bestimmten Kurs

Möglichkeiten

- Für jeden Kurs wird unter GIT ein eigener Branch angelegt
  - Zwischen den Branches wird hin- und her gemergt (Cherrypick)

- TODO

Anmerkungen

- Hin- und her mergen ist fehleranfällig
