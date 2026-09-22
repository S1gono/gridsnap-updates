# GridSnap

Fenster per Mausgeste ins Raster legen, ein Zwischenablage-Verlauf wie unter
Windows, und eine Ablage am Bildschirmrand für Dateien unterwegs. Für macOS 13
und neuer, Apple Silicon.

## Herunterladen

**[GridSnap.zip — aktuelle Testfassung](https://github.com/S1gono/gridsnap-updates/releases/download/latest/GridSnap.zip)**

Diese Adresse bleibt gleich und zeigt immer auf die neueste Fassung.

## Installation

Einmalig nötig. Danach hält sich GridSnap selbst aktuell.

1. Archiv entpacken und `GridSnap.app` nach **Programme** ziehen.
2. Die App ist noch nicht bei Apple notarisiert, deshalb blockiert macOS den
   ersten Start. Das einmal aufheben:

```bash
xattr -dr com.apple.quarantine /Applications/GridSnap.app
```

3. GridSnap starten. Beim ersten Start fragt macOS nach der Berechtigung für
   **Bedienungshilfen** — ohne sie kann das Programm keine Fenster bewegen.
   Systemeinstellungen ▸ Datenschutz & Sicherheit ▸ Bedienungshilfen.

## Updates

GridSnap prüft von selbst auf neue Fassungen und bietet sie an. Von Hand geht
es über **Einstellungen ▸ Nach Updates suchen**.

Spätere Updates lösen die Sperre aus Schritt 2 **nicht** erneut aus, und die
erteilte Berechtigung aus Schritt 3 bleibt ebenfalls erhalten. Der Schritt oben
ist also wirklich nur einmal nötig.

## Was in diesem Repository liegt

Nur die Update-Beschreibung (`appcast.xml`), die Versionshinweise und die
fertigen Programmdateien. **Kein Quellcode.**

Jede Datei ist mit einem privaten EdDSA-Schlüssel signiert, der ausschließlich
auf dem Rechner des Entwicklers liegt. GridSnap installiert nur, was zu dem
eingebauten öffentlichen Schlüssel passt; eine ausgetauschte Datei wird
abgelehnt.

Der Bereich [Releases](../../releases) enthält zwei Einträge: **latest** ist der
Download für Menschen, **builds** der Vorrat für die Update-Funktion mit allen
Fassungen und den Differenz-Paketen.

## Fehler melden

Kurz beschreiben, was du getan hast und was passiert ist. Hilfreich ist das
Protokoll:

```bash
tail -50 ~/Library/Logs/GridSnap/gridsnap.log
```
