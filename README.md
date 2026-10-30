# Bootstank-Log

Benzinverbrauch eines Motorboots auf dem Bodensee, gemessen in Liter pro Motorstunde (L/h).

## Was die App kann

- **Verbrauch nach der Voll-zu-Voll-Methode:** Eine Periode (P1, P2 …) reicht von einer Vollbetankung zur nächsten. Teilbetankungen (T1, T2 …) werden der jeweils nächsten Vollbetankung zugerechnet.
- **Tank-Check:** Restmenge und Reichweite ab der letzten Vollbetankung, optimistisch (Durchschnitt aller Perioden) und konservativ (bisheriger Höchstwert), mit einem Drittel Reserve.
- **Kosten in Euro:** Tankungen in der Schweiz werden in CHF erfasst und mit dem Kurs vom Tanktag umgerechnet.
- **Verlauf:** Säulen je Periode (Breite = gefahrene Stunden), Durchschnitt als Linie.
- **Belegfotos**, sechs Farbschemata inklusive Rotlicht für die Nacht.

## Wo die App läuft

Die App läuft über GitHub Pages:
https://jan-ai75.github.io/bootstank-log/

Die Tankdaten liegen in `tankdaten.json` im privaten Repository `boot-daten`, Belegfotos dort unter `belege/`. Das [Boot-Cockpit](https://jan-ai75.github.io/boot-cockpit/) liest und schreibt dieselbe Datei, Betankungen und Motorstunden lassen sich also in beiden Apps erfassen. Dieses Repository enthält nur den Code, keine Tankdaten.

Für den Zugriff wird einmal pro Gerät ein GitHub-Schlüssel (Fine-grained Token, nur `boot-daten`, Contents: Read and write) eingetragen. Er bleibt im Browser des Geräts. Ohne Netz speichert die App Änderungen zunächst lokal und überträgt sie beim nächsten Abgleich.

Die frühere Fassung als Artifact auf claude.ai kann GitHub nicht erreichen und wird nicht mehr verwendet.

## Aufbau

Eine einzelne Datei, `index.html`, ohne Build-Schritt. Dazu kommen das Logo (`icon.svg` sowie `icon-192.png`, `icon-512.png` und `apple-touch-icon.png` für den Startbildschirm) und `manifest.webmanifest`. Externe Abhängigkeiten: Google Fonts und [fecha](https://github.com/taylorhakes/fecha) für Datumsformate.
