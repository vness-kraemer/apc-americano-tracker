# 🎾 APC Americano Tracker

Der Punktetracker, der schneller rechnet als ihr nach dem dritten Match noch im Kopf könnt.

Gebaut für Americano-Turniere des **Alsdorfer Padel Club (APC)** – läuft komplett im Browser, merkt sich alles, verzeiht Fehler, und macht am Ende sogar noch ein Bild für Instagram. Läuft auf jedem Gerät mit Browser. Kostet nix. Muss nicht installiert werden. Kein Konto, kein Login, kein Kleingedrucktes.

### 🔗 [Jetzt live ausprobieren → apc-americano-tracker.netlify.app](https://apc-americano-tracker.netlify.app/)

---

## Was das Ding kann

Beim Americano rotieren die Partner jede Runde – und spätestens ab Runde 4 weiß niemand mehr, wer wie oft schon pausiert hat oder wie viele Punkte Karina eigentlich hat. Genau dafür ist dieser Tracker da.

- 🏟️ **1–6 Plätze frei wählbar**, beliebig viele Spieler:innen (mind. 4) – reicht die Anzahl nicht für alle gewählten Plätze, wird automatisch angepasst, ganz ohne Kopfrechnen
- ⚖️ **Faire Pausen-Rotation** – wer am wenigsten pausiert hat, ist automatisch als Nächstes dran. Niemand kann sich mehr "aus Versehen" öfter eine Pause gönnen
- 🔢 **24-Punkte-Scoring** – eine Zahl eintragen, die Gegenseite ergänzt sich von selbst
- 🏆 **Live-Tabelle** – der Zwischenstand ist immer sichtbar, auch für alle, die schon anfangen wollen zu diskutieren, wer eigentlich vorne liegt
- 🔀 **Tauschen** – für den Fall, dass jemand verletzt ausfällt, zu spät kommt, oder partout nicht gegen die eigene Partnerin spielen möchte. Zwei Namen antippen, fertig
- ↩️ **Runde zurücknehmen** – falls sich beim Eintragen jemand vertippt (kommt vor, besonders nach dem dritten Aufschlag-Ass)
- 💾 **Sichern & Wiederherstellen** – Turnierstand als Text kopieren, sich selbst schicken, jederzeit wieder einspielen. Kein Turnier geht verloren, nur weil das Handy kurz spinnt
- 🔒 **Bildschirm bleibt an** – schläft nicht mitten in Runde 5 einfach ein
- 📸 **Ergebnis-Bild für Instagram** – am Ende ein Klick, fertig ist die Grafik im APC-Design. Recap-Content, ohne dass irgendwer nachträglich in Canva rumfummeln muss

## So läuft's ab

1. **Plätze wählen**, Namen eintippen (ein Name pro Zeile), Turnier starten
2. **Ergebnisse eintragen**, Runde abschließen – die nächste Zuteilung kommt automatisch
3. Bei Bedarf **tauschen**, **zurücknehmen** oder zwischendurch **sichern**
4. **Turnier beenden** → Sieger:in steht fest, Bild für Insta ist einen Klick entfernt

## Selbst hosten

Ist bereits live unter dem Link oben. Wer sich eine eigene Kopie bauen will (z. B. für einen anderen Verein, andere Farben, wer weiß):

1. Repo forken/klonen
2. `index.html` liegt im Root – kein Build nötig, keine Abhängigkeiten außer dem Google Font "Montserrat"
3. Bei [Netlify](https://netlify.com) einbinden: **Add new site → Import an existing project**, alle Build-Felder leer lassen, Deploy klicken
4. Fertig ist die eigene URL

## Technisches Kleingedruckte

- Reines HTML/CSS/JavaScript, keine Frameworks
- Speicherung läuft automatisch über `localStorage` – der Stand bleibt auf dem genutzten Gerät/Browser erhalten
- Logo ist als Base64 direkt im Code eingebettet, damit alles eine einzige, portable Datei bleibt

## Ehrlich gesagt: die Grenzen

- **Ein Gerät, ein Turnier** – der Tracker ist für die Bedienung von *einem* Gerät gedacht (Tablet am Tisch). Öffnet jemand den Link auf einem zweiten Handy, sieht diese Person eine eigene, leere Kopie – kein Live-Sync zwischen Geräten (noch nicht, siehe unten).
- **Kein Zugriffsschutz** – wer den Link hat, kann Ergebnisse eintragen. Für den Vereinsgebrauch unter Freund:innen völlig okay, für die große weite Öffentlichkeit vielleicht nicht.
- **Nur 24-Punkte-Americano** – andere Zählweisen gibt's aktuell nicht.
- Eine "echte" Mehrgeräte-Version mit gemeinsamer Datenbank (jedes Handy sieht live denselben Stand) ist technisch möglich, aber (noch) nicht eingebaut.

---

**Alsdorfer Padel Club (APC) e.V.** · Sportforum Alsdorf · [apc-alsdorf.de](https://www.apc-alsdorf.de/)

*Nur noch ein Turnier, versprochen.* 😅
