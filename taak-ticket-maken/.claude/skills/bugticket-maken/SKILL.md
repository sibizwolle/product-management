---
name: bugticket-maken
description: Maak bugtickets aan in Jira op het SIA-bord. Gebruik deze skill wanneer een gebruiker een bug wil rapporteren of een bugticket wil aanmaken. De skill zorgt voor een consistente structuur met situatie, reproductiestappen en gewenste situatie.
---

# Bugtickets maken

Deze skill helpt bij het aanmaken van bugtickets in Jira op het SIA-bord. Elk ticket volgt een vaste structuur zodat bugs eenduidig worden beschreven en makkelijk reproduceerbaar zijn voor het ontwikkelteam.

## Werkwijze

1. **Verzamel de benodigde informatie**: Vraag door als de situatie, reproductiestappen of gewenste situatie onduidelijk of onvolledig zijn.
2. **Maak het ticket aan** via de Jira MCP tool (`createJiraIssue`) met projectKey `SIA` en issueType `Bug`.
3. **Geef de link terug** zodat het ticket direct te openen is.

## Beschrijvingsstructuur

Gebruik altijd deze drie onderdelen in de beschrijving, in deze volgorde:

**Situatie**
Beschrijf de huidige situatie: wat doet de software, wat gaat er fout en in welke context treedt het op.

**Reproductiestappen**
Beschrijf stap voor stap hoe de bug te reproduceren is. Wees concreet en volledig, zodat een ontwikkelaar de bug zelf kan nabootsen.

**Gewenste situatie**
Beschrijf wat het verwachte, correcte gedrag zou moeten zijn.

## Opmaakregels

- Gebruik **geen headings** (geen `##` of `###`) in de Jira-beschrijving.
- Gebruik **vetgedrukte tekst** als kopjes: `**Situatie**`, `**Reproductiestappen**`, `**Gewenste situatie**`.
- Gebruik genummerde lijsten voor de reproductiestappen.
- Gebruik `contentFormat: markdown` bij het aanmaken van het ticket.
- Schrijf in het Nederlands, beknopt en feitelijk.

## Voorbeeld beschrijving

**Situatie**
Bij het bewerken van een kennisitem wordt een geplakte afbeelding altijd onderaan de content geplaatst, ongeacht waar de cursor staat.

**Reproductiestappen**
1. Open een bestaand kennisitem en klik op **Bewerken**.
2. Klik ergens midden in de tekst om de cursor daar te plaatsen.
3. Plak een afbeelding via Ctrl+V.
4. De afbeelding verschijnt onderaan de content, niet op de cursorpositie.

**Gewenste situatie**
De afbeelding wordt ingevoegd op de plek waar de cursor staat.
