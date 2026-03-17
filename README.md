# Forschungszulage Skill

Ein Claude-Skill, der Unternehmen durch den gesamten Antragsprozess der deutschen Forschungszulage (FZulG) begleitet - von der BSFZ-Bescheinigung bis zum Finanzamt-Antrag.

## Was kann dieser Skill?

- **Prozessbegleitung**: Schritt-fuer-Schritt durch den zweistufigen Antragsprozess (BSFZ + Finanzamt)
- **Projektbeschreibungen formulieren**: Ueberzeugende Texte fuer die vier kritischen BSFZ-Textfelder mit Zeichenlimit-Optimierung
- **Sprachpruefung**: Texte auf Klarheit, Ton und Ueberzeugungskraft pruefen - kein Behoerdendeutsch, kein Marketing-Sprech
- **Plausibilitaetspruefung**: Bestehende Antraege systematisch auf Schwachstellen und haeufige Ablehnungsgruende pruefen
- **Foerderberechnung**: Voraussichtliche Foerderhoehe berechnen (inkl. KMU-Bonus, Gemeinkostenpauschale, Auftragsforschung)

## Installation

Den Ordner als Skill in Claude Code einbinden:

```bash
claude skills add /pfad/zu/forschungszulage-skill
```

## Struktur

```
forschungszulage-skill/
├── SKILL.md                              # Haupt-Skill
└── references/
    ├── ablehnungsgruende.md              # Detaillierte Ablehnungsgruende + Gegenstrategien
    ├── antragssprache.md                 # Sprachleitfaden: Ton, Stil, Vorher/Nachher-Beispiele
    ├── berechnungsbeispiele.md           # 6 konkrete Rechenbeispiele
    └── checkliste.md                     # Vollstaendige Pruefcheckliste vor Einreichung
```

## Beispiel-Anwendungen

- "Ich moechte die Forschungszulage fuer unser KI-Projekt beantragen"
- "Kannst du meine BSFZ-Projektbeschreibung pruefen?"
- "Wie hoch waere unsere Forschungszulage bei 3 FuE-Mitarbeitern?"
- "Unser Antrag wurde abgelehnt - was koennen wir verbessern?"

## Aktualitaet

Der Skill enthaelt die Regelungen Stand 2026 (Bemessungsgrundlage 12 Mio. EUR, Gemeinkostenpauschale 20%, Stundensatz 100 EUR, KMU-Foerdersatz 35%).

## Lizenz

[MIT](LICENSE) - Copyright (c) 2026 [Sebastian Software GmbH](https://oss.sebastian-software.com/), Mainz, Germany
