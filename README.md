# Mesurez la valeur de votre IA, pas le buzz

Formation express (produit digital) pour solopreneur français — 6 modules, 3 heures, promesse mesurable : **« en 3 h, vous savez chiffrer la valeur réelle de chaque outil IA de votre entreprise »**.

## Arborescence

```
mesurer-ia/
├── index.html                     # Page de vente — design éditorial ambre/or (fond #120d08)
├── formation-mesurer-ia.md        # La formation complète (6 modules, niveau expert)
├── templates/
│   ├── business-case-ia.md        # Gabarit business case (baseline, TCO, 3 scénarios, décision)
│   ├── indicateurs-valeur.md      # Grille des 5 indicateurs + vérification anti double comptage
│   ├── grille-calcul-roi.md       # Grille de calcul ROI / payback / sensibilité
│   ├── rapport-direction.md       # Rapport direction prêt à remplir (3 pages)
│   └── objections-finance.md      # Les 5 objections de la finance + réponses + phrases à dire
└── README.md
```

## Offres (prix affichés sur la page)

| Formule | Contenu | Prix |
|---|---|---|
| **L'Essentiel** | Formation PDF seule (6 modules, 3 h) | **49 €** |
| **Pack complet** | Formation + 5 templates prêts à remplir | **89 €** |
| **Pack Direction** | Pack complet + session de co-construction 45 min | **149 €** |

## Stack & intégration EmailJS (réelle)

- Page statique autonome (`index.html`), zéro dépendance de build — s'ouvre en `file://` ou sur n'importe quel hébergeur statique.
- Formulaire de commande branché sur EmailJS (envoi réel, status 200 validé) :

```js
emailjs.init("8Pui4ZEqxW2jRVF7h");
emailjs.send("service_cy1ytdb", "template_xpo58cv", {
  site: 'Mesurez la valeur de votre IA',
  name: nom, email: email,
  question: 'Commande : <offre>' + (question ? ' — Question : ' + question : '')
});
```

- Le template EmailJS reçoit exactement les 4 clés `{site, name, email, question}`.
- Les boutons « Commander » des offres pré-remplissent le select et scrollent vers `#commander` (fonction `choisirOffre`).

## Workflow de vente (manuel, à la réception de chaque email EmailJS)

1. Recevoir la commande (email avec `site`, `name`, `email`, `question`).
2. Répondre sous 24 h ouvrées avec les instructions de paiement (virement / lien de paiement).
3. Dès réception du paiement, livrer par email : `formation-mesurer-ia.md` (PDF exporté) + `templates/` pour les packs.
4. Pack Direction : planifier la session de co-construction de 45 min par email.

## Design

- Palette : fond noir profond `#120d08`, accents ambre `#f59e0b`, crème `#f5e9d3`, cuivre `#b45309`.
- Architecture éditoriale premium : hero asymétrique (titre serif à gauche, colonne éditoriale à droite), filets dorés, numéros de modules géants (contour ambre), Georgia pour les titres, petites capitales sans-serif pour les labels. Aucune particule 3D.
- Typographie française respectée (espaces insécables avant `: ? !` et dans les guillemets).

## Contenu (cohérence chiffrée de bout en bout)

Tous les fichiers utilisent le même jeu de données pédagogique (chatbot support, 12 000 tickets/an) :
269 % de ROI an 1, payback 3,2 mois, 45 % de déflection, 110 840 €/an — exemples du module 4
repris dans la bande de chiffres de la page et dans le gabarit de rapport direction.

## ⚠️ Publication

**Ne pas publier sur GitHub ni ailleurs sans validation utilisateur.** Tant que le paiement n'est pas
réellement branché (lien de paiement actif), la page reste un livrable local. Pour un test en ligne
rapide : hébergement statique (tunnel cloudflared, Netlify Drop, etc.).

## Qualité

- Orthographe française vérifiée (zéro espace avant virgule/point ; espaces françaises respectées).
- Envoi EmailJS testé en navigateur réel (status 200).
- Page responsive (mobile ≤ 560 px, tablette ≤ 960 px), `prefers-reduced-motion` respecté, focus clavier visible.
