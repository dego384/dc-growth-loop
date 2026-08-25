# 🚀 DC Growth Loop starten

Kopiere diesen Befehl in Claude Code Terminal:

```bash
/schedule create daily 6:30 "Kommandozentrale APP"
```

**Dann:**
- Jeden Morgen um 06:30 Uhr startet ein Agent
- Liest `LOOP_STATUS.md` → wo stehen wir?
- Nimmt die nächste 🟡 PENDING Feature
- Arbeitet sie ab (Code/Testing)
- Sub-Helper prüft (Tests grün? Keine Bugs?)
- STATUS.md wird aktualisiert
- Schläft bis morgen 06:30

---

## Neue Feature hinzufügen

Datei erstellen: `⏳ PENDING - TITEL.md`

```
**Aufgabe:** [Was soll gebaut werden?]
**Frist:** [YYYY-MM-DD]
**Priorität:** 🔴 URGENT / 🟡 NORMAL
**Details:** [Kontext, API-Doku Link, etc.]
```

Loop findet die Datei morgen → nimmt sie an.

---

## Wenn blockiert

Schreib in `LOOP_STATUS.md`:
```
🔴 BLOCKED: Preismodell-Freigabe
Warte auf: Cristian-Entscheidung bis 2026-08-26
```

Loop liest das, stoppt, wartet.

---

**Status:** Bereit  
**Erstellt:** 2026-08-25
