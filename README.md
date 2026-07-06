# DnD-Portal — Phandalins Krønike

Spiller-vendt portal til *Dragons of Icespire Peak*-kampagnen. Indeholder **kun** spiller-sikkert
indhold — ingen DC-værdier, loot-spoilere eller DM-hemmeligheder må nogensinde ligge her.

**Live side:** `https://amazingraven.github.io/DnD-Portal/` (aktiveres i repo-indstillinger →
Pages, kilde: `main`-branch, `/root`).

## Struktur

```
index.html         → selve portalen (henter data fra JSON-filerne herunder)
data/npcs.json      → "Folk vi har mødt"
data/items.json     → "Fund & genstande"
data/podcasts.json  → links til session-optagelser
data/sessions.json  → session-logs / recaps
```

## Sådan opdaterer I indhold

Rediger den relevante JSON-fil under `data/` og commit/push (eller bed Claude om det i en
samtale — giv repo-navn + en fine-grained access token med *Contents: Read and write* på dette
repo).

### `npcs.json`
```json
{ "name": "Navn", "title": "Rolle/titel", "location": "Sted", "description": "Kort, spoiler-fri beskrivelse." }
```

### `items.json`
```json
{ "name": "Navn", "rarity": "Common/Uncommon/Rare/...", "description": "Kort beskrivelse." }
```

### `podcasts.json`
```json
{ "title": "Session-titel", "session_number": 7, "date": "2026-07-01", "description": "Kort teaser.", "url": "https://open.spotify.com/..." }
```

### `sessions.json`
```json
{ "title": "Session-titel", "number": 7, "date": "2026-07-01", "recap": "Spoiler-fri opsummering.", "podcast_url": "https://..." }
```

## Vigtigt

Dette repo er **offentligt** (krav for gratis GitHub Pages). Læg derfor aldrig DM-noter,
DC-værdier eller uafslørede plot-elementer her — kun det spillerne allerede ved eller må vide.
Selve session-builderen (med DM-hemmeligheder) forbliver et separat, lokalt værktøj.
