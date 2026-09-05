# APC Americano Tracker

Ein schlanker, selbst-gehosteter Punktetracker für Americano-Turniere des **Alsdorfer Padel Club (APC)**. Läuft komplett im Browser, keine Installation, keine Datenbank, keine Kosten.

## Was das Tool macht

- Erfasst Ergebnisse pro Match live während eines Americano-Turniers
- Rechnet automatisch die Einzelpunkte aller Spieler:innen zusammen (nicht Team-Punkte – beim Americano rotieren die Partner ja jede Runde)
- Verteilt Pausen bei ungerader Teilnehmerzahl automatisch fair, sodass niemand deutlich mehr aussetzt als andere
- Zeigt jederzeit eine Live-Tabelle mit dem aktuellen Punktestand
- Funktioniert für 1–6 Plätze gleichzeitig, bei beliebiger Spielerzahl (mind. 4)

## Funktionen

- ✅ Frei wählbare Anzahl Plätze (1–6)
- ✅ Beliebige Spielerzahl, automatische faire Rotation und Pausenverteilung
- ✅ 24-Punkte-Scoring pro Match (Standard-Americano) – zweite Zahl wird automatisch ergänzt
- ✅ Live-Leaderboard, sortiert nach Gesamtpunkten
- ✅ Eingebauter Rundentimer (Start/Pause/Reset, ±5-Minuten-Anpassung)
- ✅ Automatisches Speichern nach jeder Änderung (kein Datenverlust bei versehentlichem Neuladen)
- ✅ Manuelle Backup-Funktion: Turnierstand als Text kopieren und z. B. per WhatsApp sichern, jederzeit wiederherstellbar
- ✅ APC-Branding (Logo, Farben, Schrift) fest eingebaut
- ✅ Läuft als einzelne HTML-Datei – kein Build, keine Abhängigkeiten, kein Server nötig

## Nutzung

### 1. Turnier einrichten
1. Datei öffnen (lokal per Doppelklick oder über den gehosteten Link)
2. Anzahl der verfügbaren Plätze auswählen (1–6)
3. Namen aller Spieler:innen eintragen (ein Name pro Zeile)
4. Reicht die Spielerzahl nicht für die gewählte Platzanzahl, werden automatisch weniger Plätze genutzt – der Tracker zeigt das direkt an
5. „Turnier starten“

### 2. Während des Turniers
- Pro Platz wird das Ergebnis eingetragen (eine Zahl reicht, die Gegenseite wird automatisch auf 24 ergänzt)
- „Runde abschließen“ schreibt die Punkte gut und generiert direkt die nächste Runde mit neuer, fairer Team-/Pausenzuteilung
- Die Tabelle rechts zeigt jederzeit den Zwischenstand

### 3. Turnier beenden
„Turnier beenden“ zeigt die finale Rangliste mit Sieger:in. Mit „Neues Turnier starten“ geht’s zurück zum Setup.

### 4. Backup
Über den Button „💾 Sichern“ lässt sich der komplette Stand als Text kopieren (z. B. an sich selbst per WhatsApp schicken). Bei Bedarf lässt sich dieser Text jederzeit wieder einfügen – sowohl während eines laufenden Turniers als auch auf dem Start-Bildschirm, falls der Tracker neu geöffnet werden musste.

## Deployment

Diese Datei ist eine einzelne, in sich geschlossene `index.html` – sie kann direkt gehostet werden, z. B. kostenlos über [Netlify](https://netlify.com):

1. Repo mit Netlify verbinden (**Add new site → Import an existing project**)
2. Keine Build-Einstellungen nötig (kein Build-Command, kein Framework)
3. Deploy – fertig ist eine öffentliche URL

Alternativ: Datei direkt per Drag & Drop auf [app.netlify.com/drop](https://app.netlify.com/drop) ziehen für einen Sofort-Link ohne Repo.

## Technische Hinweise

- Reines HTML/CSS/JavaScript, keine Frameworks, keine externen Abhängigkeiten außer dem Google-Font „Montserrat“
- Speicherung erfolgt automatisch im Browser (`localStorage`) – der Stand bleibt auf dem genutzten Gerät/Browser erhalten, auch nach Neuladen der Seite
- Logo ist als Base64 direkt im Code eingebettet – die Datei bleibt dadurch ein einzelnes, portables File ohne separate Bilddatei

## Bekannte Grenzen

- **Kein Mehrgeräte-Sync**: Der Tracker ist für die Bedienung von *einem* Gerät während des Turniers gedacht (z. B. ein Tablet am Tisch). Öffnet jemand den Link auf einem zweiten Handy, sieht diese Person eine eigene, unabhängige, leere Kopie – kein Live-Abgleich zwischen Geräten.
- **Kein Zugriffsschutz**: Wer den Link hat, kann Ergebnisse eintragen bzw. verändern. Für den internen Gebrauch im Verein unkritisch, für öffentliche Verlinkung ggf. zusätzlich absichern.
- Gedacht für Americano im 24-Punkte-Format; andere Zählweisen sind aktuell nicht einstellbar.

---

**Alsdorfer Padel Club (APC) e.V.** · Sportforum Alsdorf · [apc-alsdorf.de](https://www.apc-alsdorf.de/)
