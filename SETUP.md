# FlowKit — Zero-Budget Setup

## Status: Landing Page ✅ Fertig | Rest ⏳ Wartet auf Accounts

---

## Was bereits fertig ist

| Komponente | Status | Details |
|------------|--------|---------|
| **Landing Page** | ✅ **FERTIG** | `index.html` — professionelle Dark-Mode Landing Page, mobile-responsive, deutsche Sprache |
| **Design** | ✅ **FERTIG** | CSS-Only, keine externen Bilder nötig, Gradient-Effects, Animationen |
| **Bild-Prompts** | ✅ **FERTIG** | Siehe `bild-prompts.md` — sofort nutzbar für Leonardo.ai / Bing |

---

## Was als NÄCHSTES passieren muss

### 1. Accounts erstellen (Marcel als Mensch — ~10 Minuten)

| Account | Link | Dauer | Kosten |
|---------|------|-------|--------|
| **GitHub** | github.com/signup | 2 Min | 0 EUR |
| **Vercel** | vercel.com (GitHub-Login) | 1 Min | 0 EUR |
| **Leonardo.ai** | leonardo.ai | 2 Min | 0 EUR (150 Tokens/Tag) |
| **n8n Cloud** | app.n8n.cloud | 2 Min | 0 EUR (100 Executions) |
| **Airtable** | airtable.com | 2 Min | 0 EUR (1.200 Records) |
| **Tally** | tally.so | 1 Min | 0 EUR (unbegrenzt) |

**Gesamtdauer: ~10 Minuten**

---

### 2. Deploy der Landing Page (ich — Cloudi — 2 Minuten)

Sobald du Vercel verbunden hast:
1. Ich lade `index.html` in ein GitHub-Repo
2. Vercel deployt automatisch
3. Live unter `flowkit.vercel.app` (oder Custom-Domain)

---

### 3. Integration n8n + Airtable + Tally (Kimi-Subagent)

Was Kimi baut, sobald Accounts da sind:

**n8n Workflow:**
- Tally-Formular → Airtable (Lead-Erfassung)
- E-Mail-Benachrichtigung bei neuem Lead
- Slack/Discord-Benachrichtigung (optional)

**Airtable Base:**
- Tabelle: `Leads` (Name, E-Mail, Firma, Nachricht, Status, Datum)
- Tabelle: `Protokolle` (Gesprächsnotizen)
- Tabelle: `Angebote` (Status-Tracking)

**Tally Formular:**
- Felder: Name, E-Mail, Firma, Telefon, Nachricht
- Danke-Seite mit Kalender-Link (später)

---

## Kostenübersicht

| Phase | Monatlich | Einmalig |
|-------|-----------|----------|
| **Phase 1 (JETZT)** | **0 EUR** | 0 EUR |
| **Phase 2 (nach Umsatz)** | ~5 EUR | Domain |
| **Phase 3 (Scale)** | ~15-20 EUR | Hosting |

---

## Nächste Schritte

1. **DU:** Erstelle Accounts (10 Minuten)
2. **MIR:** Schicke die Zugangsdaten / API-Keys
3. **ICH:** Deploy Landing Page + starte Kimi für Integration
4. **KIMI:** Baut n8n + Airtable + Tally (2-3 Stunden)
5. **ERGEBNIS:** Komplettes System live

---

## Screenshot der Landing Page

Lokale Preview:
```bash
# Auf dem Server:
cd /root/.openclaw/workspace/KI-Holding/03_COMPANIES/FlowKit/landing-page
python3 -m http.server 8080
# Dann im Browser: http://localhost:8080
```

Oder einfach die `index.html` doppelklicken (lokal).

---

## Notizen

- Impressum und Datenschutz sind Platzhalter — müssen vor Go-Live gefüllt werden
- E-Mail-Adresse `hello@flowkit.de` ist Platzhalter — braucht tatsächliche Domain
- Analytics (Plausible) kommt später auf Oracle Cloud
- Bilder für Social Media kommen von Leonardo.ai (täglich 150 Tokens)
