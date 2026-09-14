# README pflegen

`README.md.src` enthält die Projektbeschreibung und die Projekt-Badges.
`README.md` ist die eingecheckte Ausgabe. Sebastian-Theme ergänzt das
Unternehmens-Badge in derselben Zeile und einen zurückhaltenden Footer.

## Werkzeug einrichten

Installiere [mise](https://mise.jdx.dev/getting-started.html) und Git.
Führe im vertrauenswürdigen Checkout aus:

```sh
mise trust
mise install --locked
mise run readme:write
mise run readme:check
```

`mise.toml` legt die CLI-Version für dieses Projekt fest. `mise.lock` enthält
Prüfsummen für Linux, macOS und Windows. Die README-Tasks verwenden genau diese
installierte Version. Sie installieren nichts automatisch und weichen nicht
auf eine systemweit verfügbare CLI aus. Nutzer des Projekts brauchen mdtheme
nicht; das Werkzeug dient der Pflege dieser README.

Bearbeite `README.md.src`, behalte genau ein Paar `mdtheme:badges`-Marker und
kopiere Unternehmens-Badge und Footer nicht in die Quelldatei. Prüfe den Diff
und committe Quelle und Ausgabe zusammen. CI prüft die Ausgabe ohne Dateien
zu verändern, bei jedem PR und Push auf den Hauptbranch.

## Vor dem Push

```sh
mise run readme:pre-push
git push
```

Das erste Kommando erzeugt die README erneut und schlägt bei einem unsauberen
Worktree fehl, auch bei ungetrackten Dateien. Prüfe und committe Änderungen
selbst und starte das Kommando erneut. Es führt weder Staging noch Commit oder
Push aus. Bestehende Hooks bleiben erhalten; es wird kein Hook installiert.

## CLI und Theme aktualisieren

Ändere die CLI-Version in `mise.toml` und führe aus:

```sh
mise lock --platform linux-arm64,linux-x64,macos-arm64,macos-x64,windows-x64
mise install --locked
mise run readme:write
mise run readme:check
```

Prüfe Lockfile und Ausgabe zusammen. Das Theme ist unabhängig davon über `ref`
in `mdtheme.yaml` gepinnt. Verwende einen geprüften Commit für ein Branding-Update.
Branches und Tags funktionieren ebenfalls; `main` übernimmt Änderungen bei jedem
Aufruf. Auch mit installierter CLI benötigen Generierung und Prüfung Git-Zugriff
auf das Theme-Repository. Theme-Dateien sind Daten und werden nicht ausgeführt.

Die [Entscheidung zur README-Erzeugung](adr/0001-compose-readme-with-mdtheme.md) hält den Vertrag fest.
