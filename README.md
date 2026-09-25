# INHELDER Website

Responsive Website mit sechs Seiten, erstellt mit HTML, CSS und JavaScript. Kein kostenpflichtiger Website-Baukasten und keine externen JavaScript-Abhängigkeiten.

## Dateien bearbeiten

- `build.py`: Texte, Seitenstruktur, Navigation und gemeinsame Seitenelemente. Erzeugt die sechs HTML-Seiten.
- `dist/style.css`: Schrift, Farben, Abstände und responsive Gestaltung.
- `dist/script.js`: Wohnungsnavigator, mobile Navigation und E-Mail-Formular.
- `dist/assets/`: Bilder.
- `netlify.toml`: Konfiguration für Netlify.

Die HTML-Dateien unter `dist/` werden erzeugt. Inhaltliche Änderungen deshalb in `build.py` vornehmen.

## Lokal aktualisieren

Voraussetzung: Python 3. Es sind keine zusätzlichen Python-Pakete nötig.

```sh
python3 build.py
python3 -m http.server 8000 --directory dist
```

Anschliessend im Browser `http://localhost:8000` öffnen.

## GitHub und Netlify

1. Das Projekt als privates Repository im eigenen GitHub-Konto ablegen, z. B. `inhelder-website`.
2. In Netlify ein Projekt aus diesem GitHub-Repository importieren.
3. Produktionsbranch: `main`. Netlify liest die übrigen Einstellungen aus `netlify.toml`.
4. Die erzeugte Netlify-Adresse prüfen, einschliesslich Unterseiten und Wohnungsnavigator.
5. Die eigene Domain erst nach der inhaltlichen Freigabe verbinden.

Netlify führt bei einem neuen Stand des verbundenen Branches `python3 build.py` aus und veröffentlicht `dist`.

## Aktueller Stand

- Bilder sind gekennzeichnete KI-generierte Platzhalter.
- Wohnungsnummern, Flächen, Preise und Status im Navigator sind Beispieldaten.
- Grundrisse und die Lagekarte sind Platzhalter.
- Das Kontaktformular öffnet einen vorbereiteten Entwurf im E-Mail-Programm. Es gibt keinen serverseitigen Formularversand.
- `.openai/hosting.json` gehört zur bestehenden Sites-Vorschau und wird von Netlify nicht benötigt oder als Website-Datei veröffentlicht.

Vor dem offiziellen Start die Platzhalter durch bestätigte Angaben ersetzen und Impressum sowie Datenschutzhinweise an den endgültigen Betrieb anpassen.
