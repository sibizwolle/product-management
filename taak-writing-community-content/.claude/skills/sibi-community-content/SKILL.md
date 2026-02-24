---
name: sibi-community-content
description: Schrijf kennisitems en productupdates voor de Sibi Community platform. Gebruik deze skill wanneer gebruikers vragen om (1) Nieuwe kennisitems te schrijven over Sibi producten en functionaliteiten, (2) Productupdates/releasenotes te maken voor nieuwe features, (3) Bestaande community content te herzien of aan te passen, (4) Content voor de Sibi Community kennisbank te creëren met de juiste schrijfstijl, structuur en tone-of-voice voor zorgorganisaties.
---

# Sibi Community Content

Deze skill helpt bij het schrijven van kennisitems en productupdates voor de Sibi Community - een platform waar zorgorganisaties kennis delen over Sibi producten zoals Sociaal Intranet, Bind, Onboarding, Sibi Hub en andere healthcare software oplossingen.

## Workflow Overzicht

Bij elke nieuwe schrijfopdracht:

1. **Bepaal het type content**: Kennisitem of productupdate?
2. **Verzamel relevante data**: Haal bestaande community data op indien nodig
3. **Kies de juiste structuur**: Volg de templates voor kennisitems of productupdates
4. **Schrijf met de juiste stijl**: Informeel, toegankelijk, gebruikersgericht
5. **Voeg cross-links toe**: Verwijs naar gerelateerde kennisitems
6. **Suggereer groep en categorie**: Bepaal waar de content thuishoort

## Kennisitems Schrijven

### Wanneer gebruik je dit?

Kennisitems leg je uit **wat** een functionaliteit is en **hoe** je deze gebruikt. Ze zijn educatief en beschrijvend.

### Structuur

Gebruik altijd deze vaste opbouw:

1. **Wat is [functionaliteit]?**
   - Neutrale, beschrijvende introductie
   - Leg uit wat het is en waarom het waardevol is (impliciet - geen expliciete "Wat is de waarde" kop)
   - Houd het beknopt (1-3 alinea's)

2. **Hoe gebruik je [functionaliteit]?** of **Gebruiksinstructies**
   - Gebruik genummerde stappen (1, 2, 3...)
   - Maak instructies concreet en actiegerecht
   - Gebruik **vet** voor UI-elementen en knoppen
   - Voeg waar relevant links toe naar gerelateerde kennisitems

3. **Goed om te weten**
   - Aanvullende tips, beperkingen of belangrijke details
   - Verwijzingen naar gerelateerde kennisitems
   - Gebruik bullet points

4. **Vragen/Support** (optioneel)
   - Waar kunnen gebruikers terecht met vragen
   - Contact informatie indien relevant

### Belangrijke Richtlijnen

- Schrijf op een **neutrale, beschrijvende** wijze
- Geen verzinsels - alleen informatie die expliciet beschikbaar is
- Suggereer altijd een groep en kenniscategorie waar het item thuishoort
- Link actief naar gerelateerde kennisitems (zie `references/terminologie-linking.md`)
- Gebruik consistent de terminologie uit `references/terminologie-linking.md`

## Productupdates Schrijven

### Wanneer gebruik je dit?

Productupdates zijn release notes die nieuwe features en verbeteringen aankondigen. Ze zijn enthousiasmerend en praktisch.

### Structuur

Gebruik deze vaste opbouw:

1. **Openingszin**
   - Korte, pakkende introductie (1-2 zinnen)
   - Vertel direct wat er nieuw is

2. **Wat is er nieuw?**
   - Beschrijf de nieuwe functionaliteit of verbetering
   - Gebruik bullet points met **vette labels**
   - Wees specifiek en concreet

3. **Waarom is dit handig?**
   - Concrete voordelen voor gebruikers
   - Gebruik bullet points met **vette labels**
   - Focus op praktische impact

4. **Goed om te weten**
   - Belangrijke details, tips of beperkingen
   - Link naar relevante kennisitems indien beschikbaar
   - Vermeld gerelateerde ideeën van het ideeënbord (met links)

### Belangrijke Richtlijnen

- Verzin **geen** functionaliteiten die niet expliciet genoemd zijn
- Suggereer relevante kennisitems die bij de update passen
- Gebruik een positieve, enthousiasmerende toon
- Wees specifiek over wat gebruikers kunnen doen

## Schrijfstijl

**Lees altijd** `references/schrijfstijl-voorbeelden.md` voor concrete voorbeelden en stijlrichtlijnen.

### Kernprincipes

- **Toon**: Informeel, toegankelijk, actief, positief, behulpzaam
- **Aanspreken**: Gebruik "je" en "jij" (nooit "u")
- **Structuur**: Duidelijke koppen (H2, H3), korte alinea's, lijsten
- **Opmaak**: 
  - **Vet** voor productnamen (Sibi Hub, Bind, etc.)
  - **Vet** voor UI-elementen en knoppen
  - *Cursief* voor nadruk waar nodig
- **Links**: Verwijs actief naar gerelateerde kennisitems
- **Vragen**: Stel directe vragen aan de lezer ("Wil je weten hoe...?")

### Voorbeelden Goede Toon

✓ "Zo hoef je niet meer in te loggen"
✓ "Zie direct in je e-mail"  
✓ "Klik op **Nieuwe categorie**"
✓ "Wil je weten hoe dit werkt?"

✗ "U hoeft niet meer in te loggen" (te formeel)
✗ "Selecteer de optie 'Nieuwe categorie'" (te technisch)

## Cross-linking Strategie

Verwijs altijd naar relevante kennisitems om een kennisnetwerk te bouwen:

- Bij eerste vermelding van belangrijke functionaliteit
- In "Goed om te weten" secties
- Bij gerelateerde concepten
- In productupdates naar uitgebreidere kennisitems

**Veelvoorkomende links**:
- Flows → "Wat is een flow"
- Sibi Hub → "Wat is Sibi Hub"  
- Groepen → "Wat zijn systeemgroepen", "Wat zijn gebruikersgroepen"
- Kennis → "Kennis aanmaken", "Openbare of besloten kennis"

Zie `references/terminologie-linking.md` voor complete overzicht.

## Groep en Categorie Bepalen

Stel altijd voor in welke groep en kenniscategorie het item thuishoort:

**Veelvoorkomende groepen**:
- Algemeen (voor algemene community informatie)
- Sociaal Intranet (voor intranet features)
- Bind (voor Bind functionaliteit)
- Onboarding (voor onboarding features)
- Kennis in groepen (voor kennisbeheer features)

**Veelvoorkomende categorieën**:
- Wat is... (introductie kennisitems)
- Hoe werkt... (instructies)
- Tips & Tricks
- Veelgestelde vragen

## Content Toevoegen aan index.html

Wanneer nieuwe content wordt geschreven, moet deze toegevoegd worden aan `index.html`:

1. **Menu-item toevoegen** in sidebar
   - Format: `data-target="yyyymmdd-identifier"`
   - Nieuwste items altijd bovenaan
   - Geef nieuwe item de `active` class

2. **Content-div toevoegen** 
   - Format: `<div class="content-item" id="yyyymmdd-identifier">`
   - ID moet exact overeenkomen met data-target
   - Voeg volledige HTML content toe

## Referenties

- `references/schrijfstijl-voorbeelden.md` - Concrete voorbeelden van schrijfstijl en structuren
- `references/terminologie-linking.md` - Productnamen en cross-linking strategie

**Lees deze referenties altijd voordat je content schrijft!**
