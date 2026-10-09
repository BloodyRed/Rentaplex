# Rentaplex

Calculateur de rentabilité d'immeubles locatifs au Québec. *Rental property profitability calculator for Québec (French / English).*

Version 1.5

## Fonctionnalités

- Verdict en couleur (rentable, de justesse, pas rentable) et profit net par mois et par année, après hypothèque, dépenses et impôt
- Taxe de bienvenue 2026 : barème de base du Québec ou de Montréal, avec bouton d'estimation
- Prime SCHL, intérêt composé semestriellement, DPA optionnelle, mode « j'y habite »
- Ratios : TGA, MRB, couverture de la dette, point mort, cash-on-cash, TRI
- Projection année par année et calcul à la revente
- Onglets nommés pour plusieurs immeubles et tableau de comparaison
- Archives : retirer un onglet de la barre sans le supprimer, puis le restaurer
- Sauvegarde optionnelle dans un bin JSONBin.io (chargement, envoi automatique, création de bin)
- Interface en français et en anglais
- Données sauvegardées dans le navigateur (localStorage), rien n'est envoyé à un serveur

## Structure

```
index.html    Application complète (HTML, CSS et JavaScript dans un seul fichier)
favicon.svg   Icône
.nojekyll     Indique à GitHub Pages de servir les fichiers tels quels
README.md     Ce fichier
```

Aucune dépendance, aucune étape de build. Seules les polices IBM Plex sont chargées depuis Google Fonts.

## Mise en ligne avec GitHub Pages

1. Créez un dépôt sur GitHub (par exemple `rentaplex`).
2. Ajoutez les fichiers de ce dossier à la racine du dépôt :
   ```bash
   git init
   git add .
   git commit -m "Rentaplex 1.5"
   git branch -M main
   git remote add origin https://github.com/VOTRE-NOM/rentaplex.git
   git push -u origin main
   ```
3. Dans le dépôt : **Settings > Pages**, source **Deploy from a branch**, branche `main`, dossier `/ (root)`.
4. Le site sera disponible à `https://VOTRE-NOM.github.io/rentaplex/` après une ou deux minutes.

## Test en local

Ouvrez simplement `index.html` dans un navigateur, ou lancez un petit serveur :

```bash
npx serve .
```

## Sauvegarde JSONBin

1. Sur jsonbin.io, page **API Keys**, créez une **Access Key** avec les permissions de lecture et de mise à jour des bins (et de création si vous voulez créer le bin depuis l'application).
2. Dans Rentaplex, ouvrez **Sauvegarde JSONBin**, choisissez `X-Access-Key`, collez la clé.
3. Entrez l'ID d'un bin existant puis cliquez sur **Envoyer vers JSONBin**, ou cliquez sur **Créer un nouveau bin**.
4. Sur un autre appareil, entrez le même ID et la même clé puis cliquez sur **Charger depuis JSONBin**.

La clé est enregistrée en clair dans le navigateur si vous cochez « Se souvenir de la clé ». N'utilisez pas votre Master Key sur un ordinateur partagé. Ne mettez jamais de clé dans le code du dépôt.

## Avertissement

Les résultats sont des estimations basées sur les hypothèses saisies. Cet outil ne remplace pas l'avis d'un comptable, d'un courtier hypothécaire ou d'un notaire. Les barèmes de taxe de bienvenue (2026) et de primes SCHL doivent être revus chaque année.
