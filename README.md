# Customer Intelligence & AI Marketing Strategy
**TP intégral — AI CONTENT & DATA | Marketing stratégique, Data Science et IA**

## Cas
Une enseigne e-commerce fictive, **NovaMarket**, veut mieux connaître ses clients, anticiper le churn, identifier des segments actionnables, personnaliser ses recommandations et améliorer la performance de ses contenus marketing.

Toutes les données de ce dépôt sont **synthétiques** et créées à des fins pédagogiques. Aucun client réel n'est représenté.
# ÉNONCÉ DU TP — Customer Intelligence & AI Marketing Strategy

## 1. Contexte professionnel
NovaMarket est une marque e-commerce française fictive spécialisée dans les produits de beauté et accessoires. La direction marketing constate une hausse des clients inactifs, une pression sur les coûts d'acquisition et une performance éditoriale inégale selon les canaux.

Vous êtes une équipe de consultants en **marketing stratégique et data marketing**. Votre mission : construire une recommandation pilotée par les données pour améliorer acquisition, conversion, fidélisation et valeur client.

## 2. Problématique centrale
**Comment exploiter les données clients et l'IA pour identifier les segments prioritaires, anticiper le risque de départ et concevoir des actions marketing personnalisées mesurables ?**

## 3. Données disponibles
- `customers.csv` : profil, récence, fréquence d'achat, valeur, interactions, satisfaction et cible churn à 90 jours.
- `transactions.csv` : historique de transactions et catégories produits.
- `reviews.csv` : avis textuels clients.
- `content_performance.csv` : performance de contenus par canal et format.

Les données sont synthétiques. Vérifiez les valeurs manquantes, doublons, types, distributions et cohérence avant toute modélisation.

## 4. Travail demandé — 8 missions

### Mission 1 — Cadrage stratégique et data
1. Reformuler le problème métier.
2. Définir trois objectifs SMART (ex. réduction du churn, hausse du réachat, progression du taux de conversion).
3. Construire une chaîne : objectif → résultat attendu → KPI → source.
4. Pour chaque objectif analytique, préciser tâche, données, algorithme et décision métier.
5. Cartographier les sources et les risques de qualité/confidentialité.

**Livrable :** note de cadrage (1 à 2 pages).

### Mission 2 — Audit et préparation des données
1. Charger les quatre CSV.
2. Mesurer dimensions, doublons, valeurs manquantes et types.
3. Contrôler les bornes (satisfaction 1–5, montants positifs, clics ≤ impressions/portée selon le cas).
4. Documenter les transformations.
5. Expliquer les limites de représentativité du dataset.

**Livrable :** notebook ou rapport d'audit.

### Mission 3 — Segmentation clients (non supervisé)
1. Sélectionner des variables pertinentes (récence, fréquence, montant, sessions, satisfaction).
2. Standardiser les variables.
3. Tester K-Means pour plusieurs valeurs de k (au moins 2 à 6).
4. Justifier le nombre de clusters à l'aide d'indicateurs et d'une interprétation métier.
5. Décrire chaque segment : taille, valeur, engagement, satisfaction, récence.
6. Nommer les segments et proposer une action différenciée.

**Livrable :** profil des segments + recommandations.

### Mission 4 — Prédiction du churn (supervisé)
1. Définir `churn_90d` comme variable cible.
2. Séparer train/test avec stratification.
3. Construire au minimum une régression logistique et un arbre de décision.
4. Mesurer accuracy, precision, recall, F1 et ROC-AUC.
5. Interpréter la matrice de confusion et les variables importantes.
6. Choisir un seuil en fonction du coût métier des faux négatifs et faux positifs.
7. Transformer le score en scénario de campagne de rétention.

**Livrable :** tableau comparatif des modèles + liste de clients à traiter (IDs fictifs uniquement).

### Mission 5 — Voix du client et NLP
1. Explorer les avis.
2. Produire une classification de sentiment pédagogique (lexique simple fourni dans le code).
3. Comparer les résultats à une lecture manuelle d'un échantillon.
4. Identifier les irritants et thèmes récurrents.
5. Proposer des actions correctives.

**Livrable :** synthèse de la voix du client et limites de l'approche lexicale.

### Mission 6 — Personnalisation et recommandation
1. Définir des règles de recommandation à partir des catégories achetées.
2. Expliquer les différences entre filtrage collaboratif, basé sur le contenu et hybride.
3. Proposer une stratégie de démarrage à froid.
4. Construire une matrice segment × besoin × message × offre × canal.
5. Préciser les limites et le contrôle de pression commerciale.

**Livrable :** plan de personnalisation exploitable par un CRM.

### Mission 7 — Stratégie de contenu IA et mesure
1. Analyser `content_performance.csv`.
2. Calculer taux d'engagement = interactions / portée × 100.
3. Calculer CTR = clics / impressions (ici portée utilisée comme proxy) × 100.
4. Calculer taux de conversion = conversions / clics × 100.
5. Calculer CPL = coût / conversions (proxy pédagogique).
6. Comparer canaux et formats sans confondre corrélation et causalité.
7. Rédiger un prompt structuré pour décliner un message en LinkedIn, Instagram et newsletter : rôle, cible, objectif, contexte, contraintes, format, preuve et contrôle.
8. Prévoir une validation humaine : faits, ton de marque, biais, confidentialité, droits et conformité.

**Livrable :** calendrier éditorial de 2 semaines + 3 contenus déclinés + tableau KPI.

### Mission 8 — Recommandation stratégique finale
Présenter un plan d'action sur 90 jours :
- Priorités et segments ciblés.
- Campagnes d'acquisition, conversion et fidélisation.
- Déclencheurs CRM et scénarios.
- Budget indicatif et hypothèses.
- KPI de pilotage et fréquence de mesure.
- Risques, garde-fous et plan de test A/B.

**Livrable :** présentation de 10 à 12 slides et synthèse exécutive.

## 5. Questions de recul
- Pourquoi un modèle supervisé exige-t-il une variable cible ?
- Pourquoi le clustering ne produit-il pas automatiquement des segments marketing pertinents ?
- Quel est le coût d'un faux négatif dans une campagne anti-churn ?
- En quoi la qualité des données conditionne-t-elle les résultats ?
- Quels risques apparaissent avec un LLM et comment les contrôler ?
- Comment démontrer qu'une campagne a causé une hausse du réachat ?

## 6. Organisation et calendrier indicatif
Travail en groupes de 3 à 5 personnes — 12 à 15 heures.
| Séquence | Durée | Activité |
|---|---:|---|
| Cadrage + audit | 2 h | Problème, SMART, data quality |
| Segmentation | 2 h | Clustering et profils |
| Churn | 3 h | Classification et interprétation |
| NLP + recommandations | 2 h | Voix client et personnalisation |
| Contenu + KPI | 2 h | Stratégie éditoriale et performance |
| Restitution | 2–4 h | Plan 90 jours et soutenance |

## 7. Barème sur 100
| Critère | Points |
|---|---:|
| Cadrage stratégique, SMART et choix des données | 10 |
| Audit, nettoyage et documentation | 10 |
| Segmentation et interprétation marketing | 15 |
| Modélisation churn et évaluation | 20 |
| NLP et voix du client | 10 |
| Personnalisation et recommandations | 10 |
| Stratégie de contenu, KPI et mesure | 15 |
| Qualité de restitution, éthique et reproductibilité | 10 |

**Exigence :** chaque recommandation doit être reliée à un constat issu des données, à un objectif et à un KPI.


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
