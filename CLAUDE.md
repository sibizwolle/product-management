# Product Management

Dit is een verzameling van product management taken en skills.

## Beschikbare taken

### 1. Community Content (`sibi-community-content/`)
Schrijven van kennisitems en productupdates voor de Sibi Community. Bevat een skill met schrijfrichtlijnen, voorbeelden en terminologie.

## Structuur

Elke taak heeft een eigen map met:
- Eigen `CLAUDE.md` met taak-specifieke instructies
- Skills in `.claude/skills/`
- Eventuele tooling en data

## Toevoegen van nieuwe taken

1. Maak een nieuwe map aan voor de taak
2. Voeg een `README.md` en `CLAUDE.md` toe
3. Maak eventuele skills in `.claude/skills/`
4. Update de tabel in de root `README.md`

## Jira-integratie

Bij het aanpassen van Jira-tickets via de MCP-tool:

- Gebruik **geen ADF-formaat** voor het `description`-veld of reacties — dat geeft vaak fouten.
- Geef reacties altijd mee als **plain Markdown string** via `addCommentToJiraIssue`.
- De titel (`summary`) kan gewoon als string worden meegegeven via `editJiraIssue`. Bij Sentry-errors begint de titel altijd met `[500]`, gevolgd door een functionele omschrijving in begrijpelijk Nederlands.
- Het `description`-veld kan worden bijgewerkt via `editJiraIssue` met een plain Markdown string. Lees altijd eerst de bestaande beschrijving en vul aan — verwijder nooit bestaande inhoud, tenzij de gebruiker daar expliciet toestemming voor geeft.
- Gebruik **geen Markdown-koppen** (# / ## / ###). Gebruik in plaats daarvan een **vetgedrukte zin** als kopje, gevolgd door een nieuwe paragraaf met de inhoud.

## Werkwijze commits

We werken trunk-based: elke wijziging die upstream moet gaat als een kleine, zelfstandige (atomic) commit direct op `main`. Geen feature branches, geen PRs.

## Werkwijze TODO-lijst

Elk onderdeel heeft een `TODO.md` in de bijbehorende map. Regels:

- Als er tickets zijn die nog community content nodig hebben, leg dat vast in de `TODO.md`.
- Als de todo-lijst wijzigt, commit dat direct naar GitHub:
  - Elke wijziging is een **losse commit** met daarin **tenminste het ticketnummer** dat de wijziging veroorzaakt, plus een duidelijke beschrijving.
  - Voorbeeld commit message: `feat(todo): voeg SIA-1899 toe aan TODO (productupdate nieuwsbijdragen)`
- Als een item van de todolijst is afgevinkt, verdwijnt het uit de open lijst en wordt het naar het "Afgevinkt" blok verplaatst — ook dit met een duidelijk commit message.
- Controleer bij elke aanpassing altijd de datum bovenaan het bestand opnieuw.
