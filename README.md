# Projet Data Science — MLOps

Projet réalisé dans le cadre du cours.

## Objectif
Mettre en place un projet Python structuré et reproductible,
avec Git et un premier test automatisé.

## Structure
- `src/` : code source
- `tests/` : tests automatisés
- `data/` : données
- `notebooks/` : exploration

## Installation
Dans le dossier du projet :

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
python -m pip install -r requirements.txt
```

## Lancer les tests
```powershell
python -m pytest
```

Cloner le dépôt puis entrer dans le dossier :

```powershell
git clone https://github.com/KAsmae4/projet-ds.git
cd projet-ds
```

Créer et activer l’environnement, puis installer les dépendances :


## Données
- Jeu : UCI Breast Cancer Wisconsin (Diagnostic), 569 observations.
- Cible : `diagnosis` (B=0, M=1), encodée par `src/prepare.py`.
- Déclarer le stockage : `dvc remote add-local -d storage <dossier>`
- Récupérer les données : `dvc pull` (ou les retélécharger via `python scripts/get_data.py`)
- Rejouer la préparation : `dvc repro`
- Version de référence : tag `data-bc-v1`