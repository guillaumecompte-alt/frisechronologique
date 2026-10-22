# Frise Studio — Créateur de frises chronologiques

Une petite application web autonome pour créer des frises chronologiques illustrées, personnalisables et exportables.

## Lancer l'application

L'application est contenue dans un seul fichier HTML et ne nécessite ni compilation ni installation de dépendances.

- Téléchargez le dépôt, puis ouvrez `index.html` dans un navigateur récent.
- Pour publier la frise en ligne, activez **GitHub Pages** dans **Settings → Pages**, choisissez la branche `main` et le dossier `/(root)`.

## Fonctionnalités

- Définir le titre et les dates de début et de fin de la frise.
- Ajouter, modifier et supprimer des périodes, choisir leur couleur et régler leurs dates.
- Ajouter, modifier et supprimer des événements, avec leur date, leur description et la position de leur étiquette.
- Condenser visuellement une longue durée avec des bords en vaguelettes ou pointillés, sans prétendre que la largeur représente toujours la durée réelle.
- Afficher le repère « Naissance de Jésus » entre **1 av. J.-C.** et **1 apr. J.-C.**
- Exporter la frise en SVG ou PNG, et exporter/importer le projet au format JSON.
- Sauvegarder automatiquement le projet dans le stockage local du navigateur.

## Convention chronologique

Le calendrier historique usuel ne comporte pas d'année 0 : 1 av. J.-C. est immédiatement suivi de 1 apr. J.-C. L'application place donc « Naissance de Jésus » au passage entre ces deux années. Le repère est visuel et ne crée pas une année historique supplémentaire.

## Données et confidentialité

Le projet est enregistré dans le navigateur utilisé. La sauvegarde locale n'est pas synchronisée automatiquement entre plusieurs appareils. Utilisez l'export JSON pour conserver une copie ou déplacer votre projet.
