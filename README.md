# PUG Delhi Presentation (2022-05-01)

- YouTube Playlist: <https://goto.pbi.tools/youtube>
- Presentation Slides: <https://goto.pbi.tools/pptx-2022-05-01-delhi-ug>

## Create PBIX from repo sources

```
pbi-tools compile ./Report
```

## .gitignore

Recommended settings for report development:

```
*.pbix
query.json
dataTransforms.json
```

## Extracting sources from PBIX

### Option 1: One-off, from offline file

```
pbi-tools extract ./Report.pbix
```

### Option 2: Watch Mode, Connected to PBI Desktop session

1. Discover PBI Desktop Process ID

```
pbi-tools info
```

2. Start extract/watch

```
pbi-tools extract -pid 12345 -watch
```

_Note that this process will be simplified in an upcoming release of `pbi-tools`._
