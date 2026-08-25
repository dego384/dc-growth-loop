# Kommandozentrale Loop — DC Growth SaaS

**Projektinhaber:** Cristian (comcaveai@gmail.com)  
**Fokus:** DC Growth SaaS (automatische Meta Ads Plattform für PV-Installateure)  
**Status-Datei:** `LOOP_STATUS.md`

## Das Projekt

🚀 **DC Growth SaaS**
- Automatische Meta Ads Plattform für PV-Installateure
- Preismodell: Premium 5k€/3.5k€
- Affiliate-System: 10 Levels
- Launch: Q1 2026

---

## Loop-Regeln

**Jeden Morgen um 06:30 Uhr:**
1. Lese STATUS.md → wo stehen wir mit DC Growth?
2. Scanne den `⏳ PENDING`-Ordner → was ist neu?
3. Nimm die nächste offene Aufgabe
4. Arbeite sie ab (Code/Feature/Dokumentation)
5. Ein Sub-Helper prüft das Ergebnis
6. Schreib es zurück in STATUS.md
7. Stopp wenn nichts mehr offen

**Jeden Tag um 06:45 Uhr (nach Feature-Work):**
1. Lade CREDENTIALS.local (Base44 Login-Daten)
2. Teste Live-App: https://dc-growth-suite.base44.app/login
3. Folge QA_TEST_CHECKLIST.md (6 Abschnitte)
4. Wenn Bug gefunden:
   - Schreib Bug-Report mit Template
   - Schreib Report-Text für Cristian (wie man es bei Base44 einfügt)
   - Stopp = warte auf Cristian-Fix
5. Wenn alles OK: Schreib ✅ in STATUS.md

**Abbruchbedingung:** STATUS.md zeigt `✅ ALLES FERTIG` — dann schlafen

**Wer kann was ändern:**
- Neue Aufgaben: in `⏳ PENDING/*.md` schreiben
- Alle anderen Dateien: nur der Loop darf sie ändern

**Verbote:**
- Keine Dateien löschen ohne Bestätigung
- Keine Git-Operationen ohne Überblick
- Keine Meta/Facebook APIs ohne Token (Cristian stellt sie zur Verfügung)

---

## Sub-Helper-Regeln

Ein separater Claude-Agent prüft, bevor etwas gilt:

✅ **Code:** Läuft es? Tests grün? Keine Syntax-Fehler?  
✅ **Features:** Tut die Funktion, was sie soll?  
✅ **Doku:** Klar dokumentiert für nächste Dev?  
✅ **Links:** Alle URLs funktional?

Wenn Fehler → zurück an Worker mit Fehlerbericht.

---

## Quick-Kommando (für dich)

- `Kommandozentrale APP STATUS` → Zeig den DC Growth Stand
- `Kommandozentrale APP STOP` → Loop pausieren bis Befehl
