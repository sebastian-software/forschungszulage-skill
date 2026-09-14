# ADR-0001: README mit mdtheme erzeugen

Status: akzeptiert

## Entscheidung

Aktualisiert: 2026-09-14

Dieses Repository erzeugt die eingecheckte `README.md` mit der nativen mdtheme-CLI
aus `README.md.src` und Sebastian-Theme. Projektbeschreibung und Einstieg stehen
im Vordergrund. Das Unternehmens-Badge ergänzt die Projekt-Badges; das Logo steht
im Footer. Die vorhandenen Projekt-Badges bleiben Teil der Quelldatei.

CLI und Theme werden unabhängig voneinander im Projekt gepinnt. CI prüft die
Ausgabe ohne Schreibzugriff. Mitwirkende erzeugen und committen Änderungen selbst;
der Pre-Push-Check führt weder Staging noch Commits aus. Gemeinsames Branding
muss dadurch nicht kopiert werden. Dafür benötigen Mitwirkende eine zusätzliche
Werkzeuginstallation und Git-Zugriff für die Prüfung.

Dies ist ein lebendes Dokument. Änderungen am Vertrag werden hier festgehalten;
konkrete Versionen gehören in die Konfiguration.
Siehe [README pflegen](../readme-theme.md).
