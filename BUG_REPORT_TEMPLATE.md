# 🐛 Bug Report für Base44

**Kopiere dieses Template in eine neue Datei, wenn der Loop einen Bug findet:**

```
⏳ BUG - [DATUM] [KURZTITEL].md
```

---

## Template

```markdown
# Bug: [Präziser Titel]

**Gefunden:** [Datum + Uhrzeit, z.B. 2026-08-25 06:50]  
**Version:** [z.B. v0.1.0 oder "aktueller Branch"]  
**Severity:** 🔴 CRITICAL | 🟡 HIGH | 🟢 LOW

---

## Szenario (Wie es reproduzieren?)

1. [Schritt 1]
2. [Schritt 2]
3. [Schritt 3]

---

## Erwartet

[Was sollte passieren?]

---

## Actual (Tatsächlich)

[Was passiert stattdessen? Screenshot? Error-Message?]

---

## Details

- **Browser:** [Chrome / Firefox / Safari]
- **OS:** Windows 11
- **Reproducible:** Immer / Manchmal / Einmalig
- **Test-User:** grasso.bank@gmx.de
- **Login erforderlich?** Ja / Nein

---

## Logs / Screenshots

[Paste hier Browser Console Errors (F12 → Console)]

```
Error: [copy/paste hier]
```

---

## Fix-Vorschlag (optional)

[Wenn du eine Idee hast, was das Problem ist]

---

## Status

- [ ] Bestätigt (Loop hat es reproduziert)
- [ ] Assigned to: [Team-Mitglied]
- [ ] Fixed in: [Branch/Commit]
- [ ] Deployed: [Ja/Nein]
```

---

## Beispiel (Affiliate-Bug)

```markdown
# Bug: Rank-System steigt nicht nach Kauf

**Gefunden:** 2026-08-25 06:50  
**Severity:** 🔴 CRITICAL

## Szenario

1. Login mit grasso.bank@gmx.de
2. Invite-Link generieren
3. Mit Test-User registrieren (incognito)
4. Mit Test-User Paket "Premium 5k" kaufen
5. Zurück zu grasso.bank → Dashboard checken

## Erwartet

Rank sollte von 1 → 2 gehen + "1/10 Affiliate Bonus: 5%" anzeigen

## Actual

Rank bleibt auf 1. Keine Bonus-Info sichtbar.
Test-User wurde aber berechnet (Dashboard zeigt Transaktion)

## Details

- Browser: Chrome
- OS: Windows 11
- Reproducible: Immer
- Console Error:
  ```
  TypeError: Cannot read property 'rankUp' of undefined
  at line 234 of affiliate-service.js
  ```

## Fix-Vorschlag

Wahrscheinlich wird die Funktion `rankUp()` nicht aufgerufen nach Payment Success.
```

---

**Diese Datei wird täglich vom QA-Loop gefüllt.**
