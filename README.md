# SuperAwesome Guides

Dette repository indeholder alle guides og nyheder til SuperAwesome, serveret fra CDN'et på `https://guidecdn.superawesome.dk`.

## Hurtig start

### Tilføj et nyt indlæg

1. Opret en ny `.mdx`-fil i den relevante mappe (`guides/` eller `nyheder/`)
2. Tilføj frontmatter med de nødvendige metadata
3. Skriv dit indhold med Markdown/MDX
4. Commit og push til `main`-branchen
5. GitHub Action genererer automatisk `manifest.json`

## Mappestruktur

```
guides/
├── guides/          # Guides og hjælpeartikler
├── nyheder/            # Nyheder og annonceringer
├── manifest.json    # Auto-genereret (REDIGER IKKE)
└── README.md
```

## Frontmatter-format

Alle filer skal have frontmatter øverst:

```yaml
---
title: "Titlen på dit indlæg"
description: "En kort beskrivelse."
username: "DitBrugernavn"
uuid: "din-uuid-her"
released: "DD/MM/YYYY"
tags: ["tag1", "tag2"]
---
```

## GitHub Actions

Hvert push til `main` der ændrer `.mdx`- eller `.md`-filer udløser automatisk en genopbygning af `manifest.json`. Du kan også køre den manuelt fra Actions-fanen på GitHub.

For at generere manifestet lokalt:

```bash
npm install
npm run generate-manifest
```
