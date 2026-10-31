# Frise Studio — Créateur de frises chronologiques

Une petite application web autonome pour créer des frises chronologiques illustrées, personnalisables et exportables, pensée pour la classe.

## Lancer l'application

L'application est contenue dans un seul fichier HTML et ne nécessite ni compilation ni installation de dépendances.

- Téléchargez le dépôt, puis ouvrez `index.html` dans un navigateur récent.
- **Cloudflare Workers** : `npx wrangler deploy` publie le site à partir de `wrangler.jsonc`. Le fichier `.assetsignore` évite de publier le README et la configuration.
- **GitHub Pages** : activez-le dans **Settings → Pages**, choisissez la branche `main` et le dossier `/(root)`.

## Fonctionnalités

- Définir le titre et les dates de début et de fin de la frise, et choisir l'affichage des dates (av./ap. J.-C. ou nombres relatifs).
- Ajouter, modifier et supprimer des périodes : couleur pleine ou hachurée, dates.
- Ajouter, modifier et supprimer des événements : date, description, couleur du texte, image, étiquette au-dessus ou en dessous de la frise.
- Condenser visuellement une longue durée (bords pointillés et cassure), sans prétendre que la largeur représente toujours la durée réelle.
- Afficher le repère « Naissance de Jésus » entre **1 av. J.-C.** et **1 apr. J.-C.**
- Sur la frise : cliquer sur une période ou un événement pour le modifier, glisser une étiquette verticalement, cliquer sur une date pour la masquer.
- Les étiquettes se répartissent automatiquement sur plusieurs rangées et la frise s'agrandit pour qu'elles ne se chevauchent pas.
- Exporter la frise en SVG ou PNG (haute résolution), exporter une **fiche vierge élèves** (textes masqués et listes mélangées à replacer), et exporter/importer le projet au format JSON.
- Sauvegarder automatiquement le projet dans le stockage local du navigateur.

## Convention chronologique

Le calendrier historique usuel ne comporte pas d'année 0 : 1 av. J.-C. est immédiatement suivi de 1 apr. J.-C. L'application place donc « Naissance de Jésus » au passage entre ces deux années. Le repère est visuel et ne crée pas une année historique supplémentaire.

## Données et confidentialité

Le projet est enregistré dans le navigateur utilisé. La sauvegarde locale n'est pas synchronisée automatiquement entre plusieurs appareils. Utilisez l'export JSON pour conserver une copie ou déplacer votre projet.

Les images ajoutées aux événements sont réduites automatiquement (640 px maximum) pour tenir dans le stockage du navigateur. Si le projet devient malgré tout trop lourd, un avertissement s'affiche : exportez alors le projet en JSON.

Un fichier JSON importé est vérifié et nettoyé (dates, couleurs, images) avant d'être chargé.
