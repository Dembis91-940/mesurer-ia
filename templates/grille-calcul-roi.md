# Template — Grille de calcul ROI

> La grille qui transforme les mesures en ROI, payback et scénarios.
> Toutes les formules sont indiquées : remplacez les valeurs, pas les formules.

---

## 1. Coûts (TCO complet)

| Ligne | Poste | Récurrent ? | Montant |
|---|---|---|---|
| C1 | Licences / abonnement | oui | |
| C2 | Intégration technique | non | |
| C3 | Formation des équipes | non | |
| C4 | Accompagnement / changement | non | |
| C5 | Supervision et maintenance | oui | |
| C6 | Coût de sortie (si arrêt) | non | |
| C7 | Autres | | |
| | **Total année 1** = C1+C2+C3+C4+C5+C6+C7 | | |
| | **Récurrent année 2+** = C1+C5+C7(récurrent) | | |

## 2. Bénéfices (ligne par ligne, formule + montant)

| Ligne | Indicateur | Formule (facteurs) | Hypothèse clé | Montant €/an |
|---|---|---|---|---|
| B1 | Temps réalloué | heures/jour × nb × jours × €/h × % réalloué | | |
| B2 | Qualité | erreurs évitées × coût unitaire | | |
| B3 | Capacité | volume en plus × marge unitaire (si facturé) | | |
| B4 | Vitesse | pénalités / manque à gagner évités | | |
| B5 | Argent | revenus additionnels ou coûts évités | | |
| | **Total bénéfices** = B1+B2+B3+B4+B5 (après vérification anti double comptage) | | | |

> ⚠️ Rappel : si B1 (heures) et B3/B5 (revenus) mesurent la même valeur, ne retenez
> que le revenu. La règle : un euro ne se compte qu'une fois.

## 3. Résultats

| Formule | Calcul | Résultat |
|---|---|---|
| **ROI an 1** = (total bénéfices − total coûts an 1) ÷ total coûts an 1 | | ______ % |
| **Payback (mois)** = total coûts an 1 ÷ (total bénéfices ÷ 12) | | ______ mois |
| **Valeur annualisée** = total bénéfices − récurrent année 2+ | | ______ €/an |

## 4. Analyse de sensibilité — 3 scénarios

Faites varier **la variable la plus incertaine** (déflection, volume, coût horaire, taux d'erreur).

| Variable | Valeur pessimiste | Valeur réaliste | Valeur optimiste |
|---|---|---|---|
| ______________ | | | |
| Bénéfices résultants | | | |
| ROI an 1 | | | |
| Payback | | | |

**Règle de décision** : si le scénario pessimiste reste rentable (ROI > 0, payback < 12 mois),
le projet est finançable. Sinon, réduisez le périmètre jusqu'à ce qu'il le soit.

## 5. Synthèse pour le rapport direction

- **Le chiffre en tête** : « ______________ €/an de valeur mesurée, ROI de ______ %, retour en ______ mois. »
- **Coût de ne rien faire** (3 ans) : ______________ €
- **Prochaine revue** : ______ (90 jours), sur les indicateurs : ____________
