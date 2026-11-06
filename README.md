# football-platform

Plateforme data : données de suivi de matchs -> KPI et profils joueurs -> API et dashboard.
Données de départ : SkillCorner Open Data (licence MIT).

## Démarrer
    python -m venv .venv
    source .venv/bin/activate        # Windows : .venv\Scripts\activate
    pip install -e ".[dev]"
    pytest

## Branches
feature/<CLÉ-JIRA>-... -> dev -> recette -> main. Jamais de push direct sur dev, recette, main.