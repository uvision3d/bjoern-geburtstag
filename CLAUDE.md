# Hinweise für Claude Code

Projekt: Geburtstags-Webapp für Björn (57). Alles steckt in `index.html` (HTML, CSS, ein `<script>`-Block in `{ … }`). Siehe README.md für die Funktionen.

## Arbeitsweise des Nutzers

- Auf Deutsch antworten, kurz und direkt.
- Wenn etwas entfernt oder gelöscht werden soll: wirklich aus dem Code löschen, nicht nur ausblenden. Wenn echtes Löschen nicht geht, Alternativen vorschlagen.
- Änderungen nach jedem Schritt am Handy (360–420 px) und am Desktop prüfen. Zeilenumbrüche dürfen nicht unschön wirken (`text-wrap: balance/pretty`, keine einzelnen Wörter allein in einer Zeile, kein seitliches Scrollen).

## Bewusst entfernte oder abgelehnte Dinge (nicht wieder einbauen, außer auf Wunsch)

- Zahlenkerzen „5“ und „7“ (ersetzt durch 57 einzelne Kerzen).
- Sprachausgabe/Stimme mit Glückwünschen.
- Oberste Zeile „27. November · Alles Gute zum Geburtstag“.
- Titel „Björn hat heut Geburtstag (wird 57)“ und Countdown zum 60. (zurückgenommen, es gilt „Björn – wird heute 57!“ und der Renten-Countdown).

## Technik

- Torte: SVG (Kuchen) + Canvas `#candles` (Kerzen, Flammenphysik, Rauch), gleiches Koordinatensystem 400×370.
- Spiel: Canvas `#game`, logische Höhe 300, Breite folgt dem Seitenverhältnis. Pausiert außerhalb des Sichtfelds.
- Konfetti: Canvas `#fx` fixed über der Seite.
- `prefers-reduced-motion` schaltet Konfetti ab.
- `localStorage` nur in try/catch (Spiel-Rekord).
- Ständchen startet beim Laden (auf Wunsch); blockiert der Browser den Ton, beim ersten Tippen.
- Jubel nach dem Auspusten ist die Aufnahme `jubel.mp3` (vom Nutzer); den früheren synthetischen Jubel nicht wieder einbauen.
- Auspusten auch per Mikrofon (auf Wunsch), mit kleinem Hinweis unter den Knöpfen. Schwellen `MIC_LOW`/`MIC_RMS`.
