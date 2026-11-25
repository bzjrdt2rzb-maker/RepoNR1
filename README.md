# Länder-Kilometer

Kleine Web-App (GitHub Pages): Kilometer vom Startland zu Zielländern speichern und nachschlagen.
Die Daten liegen in `data.json` in diesem Repo – dadurch sind sie auf allen Geräten gleich.

## Befehle

| Befehl | Wirkung |
|---|---|
| `+1234 Frankreich` / `+1234,Frankreich` | Land mit 1234 km speichern; existiert es schon, wird die km-Zahl aktualisiert |
| `-1234` | alle Länder mit genau 1234 km |
| `~1234` / `~1234 50` | Länder im Bereich ±20 km (bzw. ±50) |
| `?fra` | Länder suchen, deren Name „fra“ enthält |
| `von Japan` | alle Entfernungen von Japan zu den anderen Ländern, gleiche zusammengefasst, nach Anzahl absteigend (Modus „Von Land“) |
| `liste` / `#` | alle Einträge |
| `löschen Frankreich` | Eintrag entfernen (mit Rückfrage) |
| `neu` | Daten neu von GitHub laden |
| `hilfe` | Befehlsliste aufklappen |

## Einrichtung (einmalig)

1. **GitHub Pages aktivieren:** Repo → *Settings* → *Pages* → *Source: Deploy from a branch* →
   Branch auswählen (der Branch, auf dem `index.html` liegt) → *Save*.
   Danach ist die Seite unter `https://<benutzername>.github.io/RepoNR1/` erreichbar.
2. **Token erstellen:** GitHub → *Settings* → *Developer settings* → *Personal access tokens* →
   *Fine-grained tokens* → *Generate new token*.
   - Repository access: *Only select repositories* → `RepoNR1`
   - Permissions → Repository permissions → **Contents: Read and write**
3. Auf jedem Gerät die Seite öffnen, unter **Einstellungen** das Token eintragen → *Speichern & laden*.
   Bei *Branch* den Branch eintragen, auf dem die Daten liegen sollen (leer = Standard-Branch des Repos).

## Entfernungsmatrix

`distances.json` enthält die Entfernung zwischen allen 197 Ländern (Methode wie Globle; Matrixwerte in 0,1 km, also `Wert / 10` = km, ungerundet. Die App rundet beim Anzeigen und Suchen auf 5 km). Die Suche („− Suchen“) gilt vom gewählten Startland (Standard China).
