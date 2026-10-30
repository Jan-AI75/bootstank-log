# Bootstank-Log

Benzinverbrauch eines Motorboots auf dem Bodensee, gemessen in Liter pro Motorstunde (L/h).

## Was die App kann

- **Verbrauch nach der Voll-zu-Voll-Methode:** Eine Periode (P1, P2 …) reicht von einer Vollbetankung zur nächsten. Teilbetankungen (T1, T2 …) werden der jeweils nächsten Vollbetankung zugerechnet.
- **Tank-Check:** Restmenge und Reichweite ab der letzten Vollbetankung, optimistisch (Durchschnitt aller Perioden) und konservativ (bisheriger Höchstwert), mit einem Drittel Reserve.
- **Kosten in Euro:** Tankungen in der Schweiz werden in CHF erfasst und mit dem Kurs vom Tanktag umgerechnet.
- **Verlauf:** Säulen je Periode (Breite = gefahrene Stunden), Durchschnitt als Linie.
- **Belegfotos**, sechs Farbschemata inklusive Rotlicht für die Nacht.

## Wo die App läuft

Die App läuft als Artifact auf claude.ai:
https://claude.ai/artifact/RCF8B7Gnyz9WfL1Qws7x3m

Die Tankdaten liegen im Datenspeicher dieses Artifacts und sind auf allen angemeldeten Geräten gleich. Dieses Repository enthält nur den Code, keine Tankdaten.

Wird `index.html` außerhalb von claude.ai geöffnet (lokal oder über GitHub Pages), arbeitet die App im Modus „Nur lokal“: Die Daten liegen dann nur im jeweiligen Browser.

## Aufbau

Eine einzelne Datei, `index.html`, ohne Build-Schritt. Externe Abhängigkeiten: Google Fonts und [fecha](https://github.com/taylorhakes/fecha) für Datumsformate.
