# 🔍 Daily QA Test Checklist für Base44

**Läuft täglich automatisch um 06:45 Uhr (nach Feature-Work)**

---

## 1️⃣ Login + Session

- [ ] Login-Seite erreichbar (https://dc-growth-suite.base44.app/login)
- [ ] Email `grasso.bank@gmx.de` akzeptiert
- [ ] Password funktioniert
- [ ] Nach Login: Dashboard-Seite lädt
- [ ] Session bleibt erhalten (Refresh)
- [ ] Logout funktioniert

---

## 2️⃣ Dashboard Basics

- [ ] Dashboard lädt ohne Fehler
- [ ] Alle Widgets sichtbar
- [ ] Keine roten Fehler-Meldungen
- [ ] Responsive (Handy + Desktop)
- [ ] Browser Console: keine Fehler (F12 → Console Tab)

---

## 3️⃣ Affiliate System Testen

**Scenario A: Einladung + Kauf (Rank 1-9)**
- [ ] "Invite Link" generieren klappt
- [ ] Link ist korrekt formatiert
- [ ] Test-Link in Incognito öffnen → neuer User kann sich registrieren
- [ ] Nach Kauf: Rank steigt auf nächstes Level
- [ ] Bonus-Prozentsatz wird korrekt angezeigt
- [ ] Bonus wird am Ende des Monats berechnet

**Scenario B: Rank 10 (Lifetime Bonus)**
- [ ] User erreicht Rank 10
- [ ] UI zeigt: "🏆 Lifetime Bonus aktiv"
- [ ] Bonus ist jetzt 0% vom Monat, 100% lebenslang
- [ ] Auch alte Transaktionen werden neu berechnet

**Scenario C: Kein Bonus ohne Kauf**
- [ ] User lädt Leute ein, diese kaufen NICHT
- [ ] Rank bleibt bei 1
- [ ] Kein Bonus-Button sichtbar

---

## 4️⃣ Payment Flow

- [ ] Pricing-Seite zeigt beide Modelle (5k€ Premium, 3.5k€ Standard)
- [ ] Kauf-Button funktioniert
- [ ] Payment Gateway (Stripe?) lädt
- [ ] Nach erfolgreicher Zahlung: Bestätigungs-Email geht raus
- [ ] Dashboard aktualisiert sich mit neuem Status

---

## 5️⃣ Datenintegrität

- [ ] Alle User-Daten bleiben nach Logout erhalten
- [ ] Affiliate-History ist korrekt (welche User hast du eingeladen?)
- [ ] Bonus-Berechnung stimmt mit Regeln überein

---

## 6️⃣ Error Handling

- [ ] Bei Network-Error: Sinnvolle Fehlermeldung (nicht nur Weiß)
- [ ] Bei Invalid Login: "Email/Password falsch" (nicht Server Error)
- [ ] Bei zu vielen Logins: Nicht gesperrt werden

---

## 🚨 Bugs / Probleme

Wenn etwas nicht stimmt: Schreib in `⏳ BUG_REPORT.md`:

```
## Bug: [Titel]
- **Datum:** 2026-08-25 06:45
- **Szenario:** [Was hast du gemacht?]
- **Erwartet:** [Was sollte passieren?]
- **Actual:** [Was passiert stattdessen?]
- **Severity:** 🔴 CRITICAL / 🟡 HIGH / 🟢 LOW
- **Screenshot/Log:** [wenn möglich]
- **Reproducible:** [immer / manchmal / einmalig]
```

---

**Status:** Bereit zum Testen  
**Frequency:** Täglich 06:45 Uhr
