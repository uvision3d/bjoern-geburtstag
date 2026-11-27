# Björn wird 57 – Geburtstags-Webapp

Eine einzelne, eigenständige Webseite (`index.html`) zu Björns 57. Geburtstag (geboren am Donnerstag, 27.11.1969). Kein Build-Schritt, keine Abhängigkeiten außer Google Fonts (Shrikhand, DM Sans).

## Starten

Einfach `index.html` im Browser öffnen. Für die Neigungssensoren am Handy muss die Seite über `https://` laufen, z. B. per GitHub Pages oder Netlify Drop.

## Funktionen

- **Startbildschirm** „Tippen zum Feiern 🎉“ mit der Karikatur: Das eine Tippen gibt am Handy den Ton frei, damit das Ständchen sofort startet.
- **Torte mit 57 Kerzen** (Canvas): Flammen sind gedämpfte Federn, biegen sich im „Wind“ und gehen nach und nach aus. Jede Kerze hat ihre eigene Widerstandskraft.
- **Auspusten**: Den Knopf „Halten zum Auspusten“ 3 Sekunden gedrückt halten (Maus, Finger oder Leertaste) oder nach Tippen auf „Mikrofon einschalten“ 1 Sekunde echt ins Mikrofon pusten. Wer zu früh loslässt, sieht die erloschenen Kerzen wieder angehen (Trickkerzen).
- **Neigung**: Flammen zeigen immer nach oben (`deviceorientation`) und wackeln beim Schütteln (`devicemotion`). Auf iOS wird beim ersten Drücken um Erlaubnis gefragt. In der Claude-Artefakt-Ansicht ist das gesperrt.
- **Ständchen**: „Happy Birthday“ (gemeinfreie Melodie) per Web Audio als Spieluhr mit Bass und deutschem Mitsingtext. Startet über den Startbildschirm (bzw. beim ersten Tippen) und über den Knopf „Ständchen spielen“.
- **Sticker** mit Björn als Karikatur (`bjoern-karikatur.webp`, von Gemini erzeugt, freigestellt) oben rechts an der Torte; der Kopf ragt oben über den Kreis hinaus.
- **Jubel und Konfetti** nach dem Auspusten: Aufnahme `jubel.mp3` („Cheering Crowd“ von Universfield), per `fetch` geladen, braucht daher einen Webserver; kein zweites Ständchen.
- **Lebenszähler** (live): Tage, Stunden, Vollmonde und Herzschläge (geschätzt).
- **Countdown zur Rente**: Regelaltersrente mit 67, Beginn am 1.12.2036, mit Balken vom 18. Geburtstag bis zur Rente.
- **Mini-Game „Lauf, Björn, lauf!“** (Canvas): Björn rennt vor einer riesigen „60“ davon, springt über Geschenke und Kerzen, Kaffee bringt Vorsprung. Start nur über den Knopf, Rekord in `localStorage`.
- **1969-Zeitleiste** und **Glückwunschkarte** mit Zufallssprüchen und Kopieren-Knopf.

## Gestaltung

Pastell: Pfirsich `#ffe5d9`, Mint `#cdeedd`, Flieder `#f3e8ff`, Himmelblau `#d6ecff`, Gelb `#fff6cc`. Tinte `#3e3150`, Akzent `#b9548a`. Überschriften zentriert in Shrikhand, Fließtext in DM Sans. Die Seite ist auf Breiten von 360 bis 1440 px geprüft.
