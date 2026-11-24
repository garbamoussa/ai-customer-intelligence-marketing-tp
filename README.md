# Customer Intelligence & AI Marketing Strategy
**TP intégral — AI CONTENT & DATA | Marketing stratégique, Data Science et IA**

## Cas
Une enseigne e-commerce fictive, **NovaMarket**, veut mieux connaître ses clients, anticiper le churn, identifier des segments actionnables, personnaliser ses recommandations et améliorer la performance de ses contenus marketing.

Toutes les données de ce dépôt sont **synthétiques** et créées à des fins pédagogiques. Aucun client réel n'est représenté.

## Objectifs pédagogiques
À l'issue du TP, l'étudiant saura :
1. Traduire un enjeu marketing en tâche analytique, données et algorithme.
2. Préparer et contrôler des données clients multi-sources.
3. Réaliser une segmentation non supervisée.
4. Construire un modèle supervisé de prédiction du churn et interpréter ses performances.
5. Formuler des recommandations marketing personnalisées.
6. Mesurer une performance éditoriale avec des KPI.
7. Concevoir un mini pipeline de contenu assisté par IA, avec vérification humaine.
8. Présenter des décisions marketing argumentées et responsables.

## Correspondance avec le cours
- Machine Learning : tâche / données / algorithme ; supervisé et non supervisé.
- Customer Intelligence : sources multiples, surcharge informationnelle, pertinence des données.
- Prédiction et personnalisation : achat, churn, CLV, segmentation, offres et parcours.
- Classification / régression / clustering.
- Recommandation : filtrage collaboratif, basé sur le contenu et approche hybride.
- NLP : extraction de sentiments et thématiques à partir des avis.
- AI Content : prompt engineering, adaptation audience/canal, contrôle éditorial.
- Performance : objectifs SMART, visibilité, engagement, conversion, fidélisation, ROI.
- IA responsable : hallucinations, biais, confidentialité, vérification des faits.

## Installation
Python 3.10+ recommandé.

```bash
python -m venv .venv
# Windows : .venv\Scripts\activate
source .venv/bin/activate
pip install -r requirements.txt
```

## Exécution rapide
```bash
python src/run_all.py
```
Les sorties sont enregistrées dans `reports/`.

Pour ouvrir le tableau de bord :
```bash
streamlit run src/dashboard.py
```

## Structure
```text
.
├── data/                 # CSV synthétiques
├── notebooks/            # parcours guidé / notes de TP
├── src/
│   ├── analysis.py       # préparation, segmentation, churn, NLP, KPI
│   ├── dashboard.py      # tableau de bord Streamlit
│   └── run_all.py        # exécution reproductible
├── reports/              # résultats générés
├── tests/                # tests de cohérence simples
├── docs/                 # sujet étudiant et corrigé enseignant
├── requirements.txt
└── README.md
```

## Résultats attendus
- `customer_segments.csv`
- `churn_predictions.csv`
- `sentiment_summary.csv`
- `content_kpis.csv`
- `marketing_recommendations.md`
- `model_metrics.json`

## Limites d'interprétation
Le dataset est synthétique et volontairement simplifié. Le modèle ne doit pas être utilisé pour une décision réelle. Une association statistique n'établit pas une causalité. Le seuil de classification et les actions marketing doivent être discutés avec les équipes métier.

## Dépôt GitHub
1. Créer un dépôt vide sur GitHub.
2. Décompresser ce projet.
3. Depuis le dossier :
```bash
git init
git add .
git commit -m "Initial commit - Customer Intelligence AI Marketing TP"
git branch -M main
git remote add origin https://github.com/VOTRE-UTILISATEUR/customer-intelligence-ai-marketing-tp.git
git push -u origin main
```
Ne jamais publier de données clients réelles, secrets ou clés API.
