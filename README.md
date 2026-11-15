# Comptage des phénotypes de F2BC de drosophile (lames 1 à 8 et images Mesurim)

Page + petite fonction Netlify (stockage Netlify Blobs, rien à configurer côté base de données).

## Déploiement (Netlify)
1. Dans ce dossier : `npm install`
2. `npx netlify-cli deploy --prod` (ou dépôt Git relié à Netlify). Le glisser-déposer simple ne convient pas : il n'embarque pas la fonction.
3. Netlify > Site configuration > Environment variables : créer `TEACHER_KEY` avec ta clé enseignant (jamais dans le code), puis redéployer.

## Utilisation
- Élèves : ouvrir l'adresse du site, choisir la lame ou l'image, saisir les 4 effectifs, envoyer.
- Toi : bouton « Enseignant » en bas de page (saisir la clé) : suppression d'une ligne, export CSV, remise à zéro du tableau.
- Échantillon compté plusieurs fois : le bilan fait la moyenne des comptages, donc il ne pèse qu'une fois.

## Modifier les listes
- Page : objet `CONFIG` en haut du script de `public/index.html`.
- Serveur : constante `ITEMS` de `netlify/functions/results.mjs` (mêmes identifiants : L1–L8, AAAX–AABE, AARR–AARV).
