---
name: story-maken
description: Maak stories aan in Jira op het SIA-bord. Gebruik deze skill wanneer een gebruiker een nieuwe functionaliteit of verbetering wil vastleggen als story. De skill zorgt voor een consistente structuur met een functionele lens, acceptatiecriteria, technische opmerkingen en een feature flag-besluit.
---

# Stories maken

Deze skill helpt bij het aanmaken van stories in Jira op het SIA-bord. Elke story volgt een vaste structuur, afgeleid van de werkwijze die in het team gehanteerd wordt.

## Werkwijze

1. **Verzamel de benodigde informatie**: Wat wil de gebruiker bouwen? Vraag door als de functionele lens of acceptatiecriteria onduidelijk zijn.
2. **Maak het ticket aan** via de Jira MCP tool (`createJiraIssue`) met projectKey `SIA` en issueType `Story`.
3. **Geef de link terug** zodat het ticket direct te openen is.

## Beschrijvingsstructuur

Gebruik altijd deze vaste opbouw, in deze volgorde:

**Functionele lens** (optioneel maar vaak aanwezig)
Een korte inleiding die de context schetst vanuit de gebruiker of het product. Beschrijft waarom deze story er is. Geen kopje nodig als de acceptatiecriteria voor zichzelf spreken.

**Acceptatiecriteria**
Een genummerde lijst van concrete, toetsbare criteria. Subcriteria krijgen een inspringing en ook een genummerde of bullet-lijst. Schrijf vanuit het gedrag van het systeem of de gebruiker — concreet en zonder vaagheden.

**Technisch**
Technische opmerkingen, aanwijzingen of besluiten die zijn gemaakt tijdens refinement. Gebruik een punt (`…`) als er nog niets is ingevuld. Laat dit blok weg als er echt niets technisch te melden is.

**Feature flag**
Geef aan of er een feature flag gebruikt wordt: `Ja` of `Nee`. Voeg een korte toelichting toe als de keuze niet vanzelfsprekend is (bijv. "Ja, om gradueel aan te zetten per klant" of "Nee, direct beschikbaar voor iedereen").

## Opmaakregels

- Gebruik **geen headings** (geen `##` of `###`) in de Jira-beschrijving.
- Gebruik **vetgedrukte tekst** als kopjes: `**Acceptatiecriteria**`, `**Technisch**`, `**Feature flag**`.
- Schrijf acceptatiecriteria als genummerde lijst. Gebruik inspringing en sublists voor detaillering.
- Gebruik `contentFormat: markdown` bij het aanmaken van het ticket.
- Schrijf in het Nederlands, in de tweede of derde persoon (niet "ik").
- Het woordgebruik is direct en functioneel — geen marketingtaal.

## Patroon acceptatiecriteria

Acceptatiecriteria beschrijven wat waar en zichtbaar is, of wat een gebruiker kan doen. Veelvoorkomende patronen uit de praktijk:

- "Als [gebruiker] dan [gedrag]"
- "[Functionaliteit] is [eigenschap]."
- "[Gebruiker] kan [actie]."
- Subcriteria specificeren edge cases, uitzonderingen of UI-details.

## Voorbeeld beschrijving

**Acceptatiecriteria**

1. Leden van de oplosgroep kunnen de categorie van een melding aanpassen.

    1. Alleen naar actieve categorieën.
    2. Titel, beschrijving en reacties blijven ongewijzigd.

2. De wijziging wordt gelogd in de historie van de melding.

    1. Zichtbaar: wie heeft gewijzigd, van welke naar welke categorie, wanneer.

**Technisch**

* Gebruik de bestaande audit-log infrastructuur voor de logging.

**Feature flag**

* Nee.

## Tweede voorbeeld (met functionele lens)

De controleur moet bij het starten van de kwaliteitsroutine kunnen kiezen voor een snelproces. Als dat actief is, hoeft de auteur en eigenaar niets te doen en kan de controleur zelfstandig het kennisitem of groepsbestand door het proces halen.

**Acceptatiecriteria**

1. Controleur kan **Snelproces** starten vanuit het instelscherm.

    1. Snelproces slaat stappen 2 t/m 4 over en gaat direct naar de afrondingsstap.
    2. Normale notificaties worden niet verstuurd; er is één vervangende notificatie.

2. Instelbaar per organisatie of snelproces beschikbaar is.

    1. Default: aan voor nieuwe klanten, uit voor bestaande klanten.

**Technisch**

* …

**Feature flag**

* Nee.
