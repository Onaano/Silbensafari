# 🦒 Silben-Safari — Wörter hören, zerlegen & zusammensetzen

Interaktives Deutsch-Lernspiel für den **Anfangsunterricht** (Klasse 1, Schuleingangsphase, Förderunterricht, ggf. Anfang Klasse 2).
Kinder müssen noch nicht sicher lesen können: Bilder und Sprachausgabe tragen die leichten Stufen.

## 🎮 Die sechs Modi
1. **Wie viele Silben?** — Bild + Sprachausgabe, Antwort 1–4
2. **Silben hören** — wahlweise **Klatschen** oder **Schwingen** (Methode vor der Runde wählbar, in der Runde wechselbar); pro Silbe tippen, ● bzw. ∪ erscheint, „Rückgängig“, „Fertig“
3. **Baue das Wort!** — Silben ordnen per Ziehen (Maus + Touch) **oder** Antippen
4. **Welche Silbe fehlt?** — Lücke füllen (ab Stufe Mittel)
5. **Finde die gleiche Silbe!** — Zielsilbe in genau einem von vier Bildwörtern (ab Stufe Mittel)
6. **Silben-Safari gemischt** — Rundenplan aus den passenden Aufgabenarten

Eine Runde = **8 richtig gelöste** Aufgaben (8 Pfoten). Kein Zeitlimit, kein Punktabzug, kein Game Over. Hinweise sind freundlich und
verraten die Lösung nicht („Hör noch einmal genau hin.“). Keine Datenspeicherung.

## 📖 Lesen: wann wird es nötig?
- **Leicht:** nie. Modi 1, 2 und 3 (bei „Baue das Wort“ liegt die Silbenfolge als blasse Schablone in den Feldern).
- **Mittel / Schwer:** Silben lesen (Modi 3–5). „Welche Silbe fehlt?“ und „Gleiche Silbe“ gibt es deshalb erst ab Mittel.

## 🔤 Wortmaterial
**56 kuratierte Wörter** (1 Silbe: 8 · 2 Silben: 28 · 3 Silben: 15 · 4 Silben: 5), jedes mit eigener SVG-Illustration. Nur eindeutige Sprechsilben
(z. B. HA–SE, KAT–ZE, BA–NA–NE); bewusst **nicht** aufgenommen: Wörter mit strittiger Silbentrennung (z. B. „Fenster“, „Apfel“), schwer
bebilderbare oder mehrdeutige Wörter (z. B. „Nase“, „Mama“, „Dose“). Die Anzeige erfolgt in Großbuchstaben (klare Druckschrift).
Die Sprachausgabe bekommt immer das **vollständige Wort** („Banane“), nie getrennte Silben; einzelne Zielsilben werden nicht gesprochen.

Prüfübersicht aller Wörter: `pruefung/wortliste.html` (mit Bildern), `.pdf`, `.csv`.

### Eindeutige Lösungen
- *Welche Silbe fehlt?*: genau eine Option ergibt das Wort. Alle falschen Optionen ergeben **kein echtes deutsches Wort** — automatisch gegen ein
  deutsches Wörterbuch (≈340.000 Einträge) geprüft; 354 mögliche Treffer sind fest gesperrt (`FORMED_REAL`).
  Neue Wörter prüfen: `pruefung/woerter-pruefen.js` + `pruefung/woerterbuch-check.py`.
- *Gleiche Silbe*: Die Zielsilbe kommt in genau einem der vier Wörter vor (auch nicht als Buchstabenfolge in den anderen);
  ähnlich aussehende Bilder (z. B. Katze/Tiger/Löwe) erscheinen nie gemeinsam.

## 🔀 Abwechslung
Rundenplan zu Rundenbeginn; Aufgabenarten gleichmäßig verteilt, nie direkt dieselbe Art hintereinander; innerhalb einer Runde kein Wort doppelt;
Antwortpositionen zufällig (auch die Zahlenreihenfolge in „Wie viele Silben?“).

## 📱 Geräte & Bedienung
Smartboard, PC, Laptop, Tablet, Smartphone; Touch und Maus; Hoch- und Querformat. **Alle Aufgaben passen ohne Scrollen** auf Laptops ab ca. 600 px
Höhe und auf Handys im Hochformat; im Querformat steht das Bild links, die Bedienung rechts. Tastaturbedienung, sichtbare Fokusrahmen,
Kontraste ≥ 4,5:1 (Text) bzw. ≥ 3:1 (Bedienelemente), mindestens 44 px große Knöpfe, `prefers-reduced-motion`.
Ohne SpeechSynthesis funktioniert alles weiter (Hinweis auf der Startseite, bei „Silben hören“ wird das Wort dann angezeigt).

## 🛠️ Technik
Eine einzige `index.html` (HTML, CSS, Vanilla JavaScript). Keine Abhängigkeiten, keine externen Bilder/Schriften/APIs, keine Cookies, kein Tracking.
Netlify: Ordner per Drag & Drop (Build command leer, Publish directory `.`). GitHub: `index.html`, `README.md`, `.gitignore` (+ optional `arbeitsblaetter/`, `pruefung/`).

## 🖨️ Arbeitsmaterialien (`arbeitsblaetter/`, HTML + PDF)
- `teilnehmeruebersicht` — A4 quer, 30 Kinder × 10 Runden
- `arbeitsblatt-silben-entdecken` — Silbenzahl bestimmen, Silbenbögen, nach Silben sortieren, in Silben gliedern (**methodisch neutral**: kein Klatschen vorgeschrieben)
- `arbeitsblatt-silben-zusammensetzen` — Silben verbinden, fehlende Silbe, Reihenfolge, gleiche Silbe
Bilder und Aufgaben stammen aus demselben Wortdatensatz wie das Spiel und wurden aus dem fertigen HTML nachgeprüft.

## ✅ Qualitätssicherung
Sprach-/Didaktik-Check (Silbenzahl, Silben = Wort, eindeutige Lösungen, kein Wort doppelt pro Runde, Lesebedarf in „Leicht“) · Wörterbuch-Kontrolle aller
erzeugten falschen Wörter · alle Modi und Stufen als volle Runden über die Oberfläche · falsche Antworten ohne Fortschritt · Klatschen/Schwingen/Wechsel/Korrektur ·
Ziehen mit Maus **und** Touch + Tap-Alternative · Sprachausgabe (nur vollständige Wörter) und Betrieb ohne Sprachausgabe · Tastatur · 9 Bildschirmgrößen ·
Kontrastprüfung aus den berechneten Farben · Erzeugungszeit (max. wenige ms, keine Endlosschleifen) · Konsole ohne Fehler.

## 📄 Lizenz
© Förderfreude Games. Alle Rechte vorbehalten.
