# Sibi Community Content

Skill en tooling voor het schrijven van **kennisitems** en **productupdates** voor de Sibi Community - een kennisplatform voor zorgorganisaties die werken met Sibi-producten.

## Wat zit erin?

- **CLAUDE.md** - Instructies voor Claude Code
- **gemini.md** - Instructies voor Gemini
- **index.html** - Preview-tool voor content
- **.claude/skills/sibi-community-content/** - De skill met schrijfrichtlijnen

## Gebruik

### Content schrijven met Claude Code

1. Open deze map in Claude Code
2. De skill `sibi-community-content` is automatisch beschikbaar
3. Vraag om een kennisitem of productupdate te schrijven

### Content previewen

```bash
python3 -m http.server 8000
```

Open http://localhost:8000 in je browser.

## Content types

### Kennisitems
Educatieve artikelen die functionaliteit uitleggen. Structuur:
1. Wat is [functionaliteit]?
2. Hoe gebruik je [functionaliteit]?
3. Goed om te weten
4. Vragen/Support (optioneel)

### Productupdates
Release notes over nieuwe features. Structuur:
1. Opening (1-2 zinnen)
2. Wat is er nieuw?
3. Waarom is dit handig?
4. Goed om te weten

## Schrijfstijl

- Informeel Nederlands (je/jij, geen u)
- **Vet** voor productnamen en UI-elementen
- Actief cross-linken naar gerelateerde kennisitems
- Positieve, behulpzame toon

## Sibi-producten

- Sociaal Intranet
- Sibi Hub
- Bind
- Onboarding
- Flows
- Kwaliteitsroutine
