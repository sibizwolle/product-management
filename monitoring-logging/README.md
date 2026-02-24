# Taak: Monitoring & Logging

Errors en waarschuwingen uit Sentry triëren, analyseren en omzetten naar bruikbare Jira-tickets die klaar zijn om opgepakt te worden door het ontwikkelteam.

## Doel

Sentry-meldingen zijn rauw en technisch. Deze taak zorgt dat ze worden vertaald naar begrijpelijke, goed gedocumenteerde bug-tickets met voldoende context voor een ontwikkelaar om direct aan de slag te gaan.

## Skills

- **process-sentry-to-jira** — Verwerkt een Sentry-issue naar een compleet Jira-ticket: functionele titel, gestructureerde beschrijving, parent-koppeling en statuswijziging naar Sprintready.

## Werkwijze

1. Nieuwe Sentry-errors worden als Jira-ticket aangemaakt via de Sentry-integratie.
2. Gebruik de `process-sentry-to-jira` skill om het ticket aan te vullen en klaar te maken.
3. Het ticket is klaar als het een functionele titel heeft, een volledige beschrijving, een parent en de status Sprintready.
