# 🧪 Sub-Helper — Der Prüfer

Der Haupt-Loop macht die Arbeit, der Sub-Helper prüft sie, bevor sie zählt.

---

## Was der Sub-Helper tut

**Täglich: Live-App Testing** (Base44)
- Login funktioniert? (grasso.bank@gmx.de)
- Dashboard sichtbar?
- Affiliate-Ranking korrekt?
- Keine Console Errors (DevTools)?
- Payment-Flow funktioniert?
- Bugs protokollieren → in `⏳ BUG_REPORT.md` schreiben

**Code (nach Features):**
- Läuft es ohne Fehler?
- Tests grün?
- Syntax korrekt?
- Keine Hard-codeten Credentials?

**Inhalte (Text/Doku):**
- Deutsche Rechtschreibung?
- Brand-Stil konsistent?
- Struktur logisch?

**Design/Websites:**
- Responsive (Handy + Desktop)?
- Links funktionieren alle?
- Keine 404er?

---

## Wie der Sub-Helper läuft

Der Haupt-Loop lädt eine Worktree auf:

```bash
git -C "C:\Users\Cristian\Desktop\Kommandozentrale" worktree add ../Kommandozentrale-check --detach
```

Sub-Helper checkt aus, prüft, und kommentiert:

```
✅ Code läuft. Tests grün.
🟡 Ein Link (Zeile 45) ist tot: /galvany/video.mp4
→ Behoben? Ja/Nein
```

Wenn Fehler → Zurück an Haupt-Loop mit Fehlerbericht.  
Wenn OK → STATUS.md updaten mit ✅

---

## Manuell prüfen (wenn du unsicher bist)

Falls der Loop dir etwas zeigt, auf das du schauen willst:

1. Öffne `Kommandozentrale-check/` Worktree
2. Prüf die Datei
3. Kommentier in `LOOP_STATUS.md`:
   ```
   Sub-Helper-Feedback 2026-08-25:
   ❌ Der Galvany-Video ist nicht 9:16
   → Bitte neu schneiden im Hochformat
   ```
4. Loop sieht das, arbeitet nach und prüft nochmal

---

**Status:** Bereit | Sub-Helper starten = automatisch mit Loop
