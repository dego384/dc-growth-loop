# 📤 Report Format für Base44

Wenn der Loop einen Bug findet, schreibt er den Report so auf, dass du ihn direkt zu Base44 kopieren kannst.

---

## Das Format (Copy-Paste Ready)

```
[TITLE] Bug: Rank-System steigt nicht

[DESCRIPTION]
Das Affiliate Ranking-System springt nicht auf das nächste Level, nachdem ein Paket gekauft wird.

[REPRODUCTION STEPS]
1. Login mit grasso.bank@gmx.de
2. Generiere einen Invite-Link
3. Registriere einen neuen Test-User über diesen Link
4. Lass den Test-User das Paket "Premium 5k" kaufen
5. Kehre zu grasso.bank Dashboard zurück

[EXPECTED]
- Rank: 1 → 2
- Dashboard zeigt: "1/10 Affiliate Bonus: 5%"
- Transaktion ist in der Affiliate-History sichtbar

[ACTUAL]
- Rank bleibt auf 1
- Kein Bonus-Info sichtbar
- Transaktion wird NICHT in der Affiliate-History angezeigt
- Browser Console Error: TypeError: Cannot read property 'rankUp' of undefined

[SEVERITY]
🔴 CRITICAL (blockiert die gesamte Affiliate-Funktion)

[AFFECTED FEATURES]
- Affiliate Ranking
- Bonus Calculation
- Einladungs-System

[BROWSER & OS]
Chrome, Windows 11

[REPRODUCIBLE]
Immer

[ADDITIONAL INFO]
Das korrekte Verhalten sollte sein:
- Rank 1-9: Bonus % vom Monat
- Rank 10+: Bonus % lebenslang
- Bonus wird täglich aktualisiert, Auszahlung monatlich

[SUGGESTED FIX]
Die rankUp() Funktion wird wahrscheinlich nicht nach Payment Success aufgerufen.
Check: affiliate-service.js Zeile 234 - Hook für onPaymentComplete
```

---

## So nutzt du das

1. Loop findet Bug → schreibt Report in dieser Form
2. Du öffnest die Report-Datei im Kommandozentrale-Ordner
3. Du gehst zu Base44 → Bugs/Issues-Sektion
4. Du kopierst den TEXT (alles zwischen den ``` Linien)
5. Du pasteest ihn rein → fertig

---

## Abkürzungen, die der Loop nutzt

| Code | Bedeutung |
|------|-----------|
| 🔴 CRITICAL | App ist unbenutzbar, Business-Impact hoch |
| 🟡 HIGH | Feature funktioniert nicht richtig, aber Workaround gibt es |
| 🟢 LOW | Cosmetic, Typo, Edge-Case |
| Immer | Bug tritt bei jedem Versuch auf |
| Manchmal | Nur unter bestimmten Bedingungen |
| Einmalig | Schwer zu reproduzieren |

---

## Beispiel: Vorerst diesen Bug

```
[TITLE] Bug: Affiliate Bonus-Regeln nicht korrekt implementiert

[DESCRIPTION]
Das Affiliate-Ranking-System folgt nicht den dokumentierten Regeln:
- Ranks 1-9 sollten einen monatlich variablen Bonus geben (wenn Leute über den Einladungs-Link kaufen)
- Rank 10+ sollten einen LEBENSLANGEN Bonus geben
- Aktuell werden Ranks überhaupt nicht erhöht

[REPRODUCTION STEPS]
1. Login mit grasso.bank@gmx.de
2. Generiere einen Invite-Link
3. Registriere Test-User über diesen Link
4. Lass Test-User "Premium 5k" kaufen
5. Kehre zu grasso.bank Dashboard zurück

[EXPECTED]
- grasso.bank Rank: 1 → 2
- Dashboard zeigt: Affiliate Bonus 5% (monatlich)
- Nach 10 Käufen: Rank 10, Bonus wird lebenslang

[ACTUAL]
- Rank bleibt auf 1, keine Steigerung
- Keine Affiliate-Bonus Info sichtbar
- Neue Käufe werden nicht registriert

[SEVERITY]
🔴 CRITICAL

[AFFECTED FEATURES]
- Affiliate Ranking
- Affiliate Bonus Calculation
- User Retention (wichtig für Launch)

[BROWSER & OS]
Chrome, Windows 11

[REPRODUCIBLE]
Immer

[BUSINESS IMPACT]
Das Affiliate-System ist eine Kernfunktion für Q1 2026 Launch.
Ohne funktionierende Ranks können wir Partner nicht erfolgreich rekrutieren.

[SUGGESTED FIX]
1. Check: Payment Success Hook ruft updateAffiliateRank() auf?
2. Check: Database speichert neuen Rank?
3. Check: Frontend liest Update nach Refresh?
```

---

**Der Loop schreibt jeden Tag einen Report. Deine Aufgabe: Zu Base44 kopieren + fixen lassen.**
