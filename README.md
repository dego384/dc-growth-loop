# 🚀 DC Growth SaaS Loop

Automatische Entwicklung für DC Growth — dein Meta Ads Plattform für PV-Installateure. Jeden Morgen um 06:30 Uhr startet der Loop, liest den Status und arbeitet die nächste Feature ab.

---

## 5 Säulen

| # | Name | Datei | Was es tut |
|---|------|-------|-----------|
| 1️⃣ | **Automation** | `LOOP_STARTEN.md` | Startet täglich um 06:30 |
| 2️⃣ | **Gedächtnis** | `LOOP_STATUS.md` | Offene Aufgaben + erledigte Features |
| 3️⃣ | **Anleitung** | `CLAUDE.md` | Regeln für den Loop |
| 4️⃣ | **Prüfer** | `SUB_HELPER.md` | Checkt Code vor Fertigstellung |
| 5️⃣ | **Aufgaben** | `⏳ PENDING/` | Deine neuen Feature-Requests |

---

## Schnelleinstieg

### 1. Loop starten (einmalig)
```bash
/schedule create daily 6:30 "Kommandozentrale APP"
```

Dann läuft es automatisch:
- **06:30 Uhr:** Feature-Development + Testing
- **06:45 Uhr:** Daily QA auf Live-App (Base44)

### 2. Feature hinzufügen
Neue Datei in `⏳ PENDING/`:

```
⏳ PENDING - 2026-08-25 Meta Ads Integration.md
```

Inhalt:
```
**Aufgabe:** Meta Ads API Integration testen
**Frist:** 2026-08-27
**Details:** Test-Account aufsetzen, Basic Sync bauen
**Priorität:** 🔴 URGENT
```

Loop findet die Datei morgen früh → nimmt sie an.

### 3. Status checken
```
Kommandozentrale APP STATUS
```

---

## Das Projekt

🚀 **DC Growth SaaS**
- Automatische Meta Ads Plattform für PV-Installateure
- Preise: 5k€ (Premium), 3.5k€ (Standard)
- Affiliate: 10 Levels
- Launch: Q1 2026

---

## Offene Features (heute)

1. 🔴 **Affiliate 10-Level-Struktur** — warte auf Preismodell
2. 🟡 **Meta Ads API Test** — nächste im Queue
3. 🟡 **Dashboard Design** — dann
4. 🟡 **Landing Page** — dann
5. 🟡 **Pricing-Seite** — zuletzt

---

## Befehle (für dich)

| Befehl | Was |
|--------|-----|
| `Kommandozentrale APP STATUS` | Zeig Fortschritt |
| `Kommandozentrale APP STOP` | Pausieren |

---

## Nicht anfassen

Diese Dateien verwaltet der Loop selbst:
- ✋ `LOOP_STATUS.md` (täglich aktualisiert)
- ✋ `Kommandozentrale-check/` (Prüf-Kopie)

Änderungen → schreib in `⏳ PENDING/`.

---

**Status:** 🟢 Bereit  
**Erstellt:** 2026-08-25  
**Start:** Nach `/schedule`-Befehl
