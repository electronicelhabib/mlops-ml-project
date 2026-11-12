# Mini-projet ML & Git

## 1. Présentation du projet

Ce projet consiste à construire une baseline de Machine Learning reproductible pour la classification des fleurs Iris.

Le projet utilise Python et Scikit-learn avec un modèle de régression logistique (Logistic Regression).

## 2. Structure du projet

```text
mlops-ml-project/
├── artifacts/
├── config/
│   └── train.yaml
├── data/
├── notebooks/
├── scripts/
│   ├── train.py
│   └── evaluate.py
├── src/
│   ├── data.py
│   ├── features.py
│   └── model.py
├── tests/
│   ├── conftest.py
│   └── test_config.py
├── README.md
└── requirements.txt
```

## 3. Technologies utilisées

- Python 3.10+
- Scikit-learn
- Pandas
- NumPy
- Matplotlib
- Joblib
- PyYAML
- Pytest
- Git

## 4. Installation

Créer un environnement virtuel :

```bash
python -m venv .venv
```

Activer l'environnement sous Windows :

```powershell
.venv\Scripts\Activate.ps1
```

Installer les dépendances :

```bash
pip install -r requirements.txt
```

## 5. Configuration

Les paramètres du projet sont définis dans :

`config/train.yaml`

Ce fichier contient notamment :
- Le type de dataset.
- La taille de l'ensemble de test.
- La graine aléatoire.
- Le modèle utilisé.
- Le nombre maximal d'itérations.

## 6. Entraînement du modèle

Exécuter :

```bash
python scripts/train.py
```

Le script entraîne le modèle et génère les artefacts suivants :

- `artifacts/model.joblib`
- `artifacts/metrics.json`
- `artifacts/confusion_matrix.png`

## 7. Évaluation du modèle

Exécuter :

```bash
python scripts/evaluate.py
```

Le rapport de classification est enregistré dans :

`artifacts/report.json`

## 8. Tests automatisés

Lancer les tests avec :

```bash
python -m pytest -q
```

Les tests vérifient la configuration, la validité de la taille du test et le chargement du dataset.

## 9. Résultats de la baseline

Résultats obtenus sur l'ensemble de test :

| Métrique | Résultat |
|---|---:|
| Accuracy | 93.33 % |
| F1-macro | 93.33 % |

Les trois tests automatisés sont réussis.

## 10. Versionnement Git

Le projet suit un workflow Git basé sur les branches :

- `main` : version stable.
- `dev` : branche de développement.
- `feature/*` : nouvelles fonctionnalités.

Les données et les artefacts générés ne sont pas versionnés dans Git.