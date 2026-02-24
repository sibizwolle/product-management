# Product Management

Verzameling van taken, skills en tools voor product management.

## Taken

| Taak | Beschrijving | Map |
|------|--------------|-----|
| Community Content | Kennisitems en productupdates schrijven voor Sibi Community | [taak-writing-community-content](./taak-writing-community-content/) |
| Monitoring & Logging | Sentry-errors triëren en omzetten naar bruikbare Jira-tickets | [taak-monitoring-logging](./taak-monitoring-logging/) |

## Structuur

```
product-management/
├── README.md              # Dit bestand
├── CLAUDE.md              # Algemene instructies voor Claude
├── taak-writing-community-content/    # Taak: Community content schrijven
│   ├── README.md
│   ├── CLAUDE.md
│   └── .claude/skills/    # Skills voor deze taak
├── taak-monitoring-logging/           # Taak: Sentry-errors triëren
│   ├── README.md
│   ├── CLAUDE.md
│   └── .claude/skills/    # Skills voor deze taak
└── [toekomstige-taken]/   # Andere PM-taken
```

## Gebruik

Elke taak heeft een eigen map met:
- **README.md** - Documentatie
- **CLAUDE.md** - Instructies voor AI-assistenten
- **.claude/skills/** - Specifieke skills voor de taak
