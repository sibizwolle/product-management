# Skill: Process Sentry intel to Jira ticket

Lees het opgegeven Sentry issue en vul het opgegeven Jira ticket aan met bruikbare informatie voor het ontwikkelteam.

## Input

De gebruiker geeft op:
- Sentry issue ID (bijv. `SIBI-2B4`)
- Jira ticketnummer (bijv. `SIA-1950`)

## Werkwijze

1. Haal het Sentry issue op via `get_issue_details` (organizationSlug: `sibi-zwolle`, regionUrl: `https://us.sentry.io`).
2. Haal het Jira ticket op via `getJiraIssue` (cloudId: `fe5866fa-e890-4ded-893b-ac8efdc85710`).
3. Analyseer de Sentry-data: wat is de fout, waar treedt hij op, hoe vaak, hoeveel gebruikers, welke tenant(s)?
4. Pas het Jira ticket aan:
   - **Titel (`summary`)**: schrijf een functionele foutmelding in begrijpelijk Nederlands — geen technische exception-tekst, maar wat de gebruiker ervaart of wat er functioneel misgaat.
   - **Beschrijving (`description`)**: schrijf in plain Markdown (geen ADF, geen Markdown-koppen). Gebruik vetgedrukte tekst als kopje gevolgd door een nieuwe paragraaf. Dek in ieder geval af:
     - Wat gaat er mis (functioneel én technisch)?
     - Waar in de code treedt het op?
     - Hoe vaak en hoeveel gebruikers zijn geraakt?
     - Wat moet er gebeuren om het op te lossen?
     - Vermelding van het Sentry issue ID met link.

## Opmaakregels voor Jira

- Gebruik plain Markdown voor zowel `description` als reacties — geen ADF-objecten.
- Geen Markdown-koppen (# / ## / ###). Gebruik **vetgedrukte tekst** als kopje, dan een witregel, dan de inhoud als nieuwe paragraaf.
- Houd de toon zakelijk en bondig.
