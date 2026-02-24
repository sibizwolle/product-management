# Skill: Process Sentry intel to Jira ticket

Lees het opgegeven Sentry issue en vul het opgegeven Jira ticket aan met bruikbare informatie voor het ontwikkelteam.

## Input

De gebruiker geeft op:
- Sentry issue ID (bijv. `SIBI-2B4`)
- Jira ticketnummer (bijv. `SIA-1950`)

## Werkwijze

1. Haal het Sentry issue en het Jira ticket **tegelijk** op (parallel):
   - Sentry: `get_issue_details` (organizationSlug: `sibi-zwolle`, regionUrl: `https://us.sentry.io`)
   - Jira: `getJiraIssue` (cloudId: `fe5866fa-e890-4ded-893b-ac8efdc85710`)
2. Analyseer de Sentry-data: wat is de fout, waar treedt hij op, hoe vaak, hoeveel gebruikers, welke tenant(s)?
3. Pas het Jira ticket aan:
   - **Titel (`summary`)**: begin altijd met `[500]`, gevolgd door een functionele foutmelding in begrijpelijk Nederlands — geen technische exception-tekst, maar wat de gebruiker ervaart of wat er functioneel misgaat. Voorbeeld: `[500] Bijdrage niet gevonden bij hoveren in de tijdlijn`.
   - **Beschrijving (`description`)**: vul de bestaande beschrijving aan — verwijder nooit bestaande inhoud, tenzij de gebruiker daar expliciet toestemming voor geeft. Plaats de aanvulling **bóven** de bestaande Sentry-melding. Stuur de volledige nieuwe tekst (aanvulling + bestaande inhoud) via `editJiraIssue` als plain Markdown string, met `description` als sleutel in het `fields`-object. Dek in de aanvulling in ieder geval af:
     - **Situatie**: wat is de context, hoe vaak is het opgetreden, hoeveel gebruikers geraakt, welke tenant(s)?
     - **Wat gaat er mis?**: functionele én technische omschrijving, inclusief bestandslocatie en regelnummer.
     - **Reproductie**: stappen om de fout te reproduceren.
     - **Gewenst gedrag**: wat moet er gebeuren om het op te lossen?
     - Sluit af met een horizontale lijn (`---`) gevolgd door de originele Sentry-melding.

4. Zoek naar de best passende parent voor het ticket:
   - Gebruik `searchJiraIssuesUsingJql` om epics of stories te vinden die inhoudelijk aansluiten bij het component of de feature waar de bug in zit (bijv. op basis van trefwoorden uit de fout of het bestandspad).
   - Stel maximaal 3 kandidaten voor aan de gebruiker met een korte toelichting waarom ze passen.
   - Laat de gebruiker kiezen welke parent het wordt, of dat er geen parent gekoppeld wordt.
   - Koppel de gekozen parent via `editJiraIssue` met het veld `parent: { key: "SIA-XXXX" }`.

5. Vraag de gebruiker of de status van het ticket gewijzigd mag worden naar **Sprintready**:
   - Zo ja: haal de beschikbare transities op via `getTransitionsForJiraIssue` en voer de juiste transitie uit via `transitionJiraIssue`.
   - Zo nee: laat de status ongewijzigd.

## Opmaakregels voor Jira

- Gebruik altijd **plain Markdown strings** — geen ADF-objecten. Dit geldt voor zowel `description` (via `editJiraIssue`) als reacties (via `addCommentToJiraIssue`).
- Geen Markdown-koppen (# / ## / ###). Gebruik **vetgedrukte tekst** als kopje, dan een witregel, dan de inhoud als nieuwe paragraaf.
- Houd de toon zakelijk en bondig.
