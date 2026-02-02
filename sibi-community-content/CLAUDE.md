# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a content management and presentation system for the **Sibi Community** platform. It manages product updates (release notes) and knowledge items for healthcare software. The project:

1. Fetches community contributions from Jira via the Atlassian MCP
2. Stores data in CSV format in `community-data/`
3. Displays content through an interactive HTML web interface (`index.html`)

## Commands

### Run Local Web Server
```bash
python3 -m http.server 8000
# Navigate to http://localhost:8000/index.html
```

## Architecture

- **index.html** - Single-page application with sidebar navigation and content areas. Pure JavaScript (no dependencies)
- **community-data/*.csv** - CSV files with embedded ADF/JSON content for knowledge items and product updates

## Jira Integration

Use the Atlassian MCP tools to fetch Jira issues:
- `mcp__atlassian__searchJiraIssuesUsingJql` - Search issues with JQL
- `mcp__atlassian__getJiraIssue` - Get specific issue details

## Content Writing

Use the **sibi-community-content** skill for writing knowledge items and product updates. The skill contains:
- Complete writing guidelines and structure templates
- Terminology and cross-linking strategy
- Style examples

### Quick Reference

**Kennisitem structuur:**
1. Wat is [functionaliteit]?
2. Hoe werkt het? (genummerde stappen)
3. Goed om te weten
4. Vragen/Support (optioneel)

**Productupdate structuur:**
1. Openingszin (wat is er nieuw)
2. Wat is er nieuw? (bullet points met **vette labels**)
3. Waarom is dit handig? (bullet points met **vette labels**)
4. Goed om te weten

**Schrijfstijl:**
- Informeel, toegankelijk, actief (Dutch "je"/"jij")
- **Vet** voor productnamen (Sibi Hub, Bind) en UI-elementen
- Cross-link naar gerelateerde kennisitems

## Adding New Content

When adding new items to `index.html`:
1. Add menu item in sidebar with `data-target="yyyymmdd-identifier"` attribute (newest first, give `active` class)
2. Add corresponding `<div class="content-item" id="yyyymmdd-identifier">` with content
3. Remove `active` class and add `style="display: none;"` to previous first item
