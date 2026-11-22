# claude-toolkit

Ein Claude-Code-Plugin-Marktplatz mit vier Plugins:

| Plugin | Inhalt | Quelle | Lizenz |
|---|---|---|---|
| `agency-agents` | 283 Subagenten (Engineering, Design, Marketing, Sales, Finance, Security, Testing u. v. m.) | [msitarzewski/agency-agents](https://github.com/msitarzewski/agency-agents) @ `8ae6164` | MIT |
| `google-maps-scraper` | Skill + Befehle `/scrape`, `/scrape-setup`, `/scrape-batch`, `/scrape-jobs` für Lead-Listen aus Google Maps | [Mahanaicoach/google-maps-scraper-kit](https://github.com/Mahanaicoach/google-maps-scraper-kit) @ `c3e63f1` | AGPL-3.0 |
| `linkedin-skills` | 12 LinkedIn-Skills (Post-Writer, Kommentare, Humanizer, Profil-Optimierer …) | [sergebulaev/linkedin-skills](https://github.com/sergebulaev/linkedin-skills) @ `32083c0` | MIT |
| `openseo` | 12 SEO-Skills + OpenSEO-MCP-Server | [every-app/open-seo](https://github.com/every-app/open-seo) @ `af3f995` | MIT |

## Installation

In Claude Code:

```
/plugin marketplace add Unikatsecuritydienstleistung/claude-toolkit
```

Dann einzelne Plugins installieren:

```
/plugin install agency-agents@claude-toolkit
/plugin install google-maps-scraper@claude-toolkit
/plugin install linkedin-skills@claude-toolkit
/plugin install openseo@claude-toolkit
```

Oder interaktiv über `/plugin` → *Browse Plugins* auswählen. Aktualisieren mit `/plugin marketplace update claude-toolkit`.

## Hinweise je Plugin

- **agency-agents:** Nach der Installation stehen die Agenten unter `/agents` bzw. per Name („Nutze den Backend Architect …“) zur Verfügung. 283 Agenten belegen Kontext; wer nur einzelne braucht, kann Dateien aus `plugins/agency-agents/agents/` direkt nach `~/.claude/agents/` kopieren.
- **google-maps-scraper:** Braucht lokal Python 3 und Chrome (oder Docker). Der Skill ruft die Skripte des Kits auf (`scripts/engine.py`, `scripts/scrape.py`). Zuerst `/scrape-setup` ausführen; Details in `plugins/google-maps-scraper/SETUP.md`. Lizenz AGPL-3.0: Änderungen am Code bei Weitergabe offenlegen.
- **linkedin-skills:** Manche Skills nutzen Python-Skripte, Abhängigkeiten in `plugins/linkedin-skills/requirements.txt`.
- **openseo:** Verbindet den gehosteten MCP-Server `https://app.openseo.so/mcp`. Für Daten wird ein OpenSEO-Konto benötigt (kostenpflichtig, Credits).

## Aktualisieren der Quellen

Die Plugins sind Kopien der genannten Upstream-Commits. Zum Aktualisieren den jeweiligen Upstream-Stand neu einkopieren und die Commit-IDs oben anpassen.
