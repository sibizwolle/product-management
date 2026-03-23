---
name: idea-maken
description: Maak een idee aan op het Sibi Ideeënbord (SIO). Gebruik deze skill wanneer een gebruiker een idee, wens of feature request wil vastleggen op het ideeënbord, of wanneer een bestaand of nieuw SIA-ontwikkelticket als delivery ticket gekoppeld moet worden aan een idee.
---

# Idee aanmaken op het Sibi Ideeënbord

Deze skill helpt bij het aanmaken van ideeën in Jira op het SIO-bord (Sibi Ideeënbord), en optioneel het koppelen van een SIA-ontwikkelticket als delivery ticket.

## Werkwijze

1. **Verzamel de benodigde informatie**: Wat is het idee? Vraag door als de samenvatting onduidelijk is. Een beschrijving en aanleiding (bijv. een SUP- of SIA-ticket) zijn optioneel maar welkom.
2. **Maak het idee aan** via `mcp__atlassian__createJiraIssue`:
   - `cloudId`: `fe5866fa-e890-4ded-893b-ac8efdc85710`
   - `projectKey`: `SIO`
   - `issueTypeName`: `Idea`
   - `contentFormat`: `markdown`
   - Verwerk de aanleiding in de beschrijving als die er is.
3. **Koppel een delivery ticket** (vraag de gebruiker):
   - **Bestaand SIA-ticket koppelen**: gebruik `mcp__atlassian__createIssueLink` met `type: "Polaris work item link"`, `inwardIssue: <SIA-ticket>`, `outwardIssue: <nieuw SIO-idee>`
   - **Nieuw SIA-ticket aanmaken**: maak eerst een Story aan via `mcp__atlassian__createJiraIssue` met `projectKey: SIA` (volg de skill `story-maken` voor de juiste structuur), koppel daarna zoals hierboven
   - **Geen delivery ticket**: sla deze stap over
4. **Geef de links terug** van alle aangemaakte en gekoppelde tickets.
