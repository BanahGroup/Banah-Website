[README.md](https://github.com/user-attachments/files/31787835/README.md)
# Banāh Event — site + pages clients (Pilotage Partagé)

Ce dépôt contient votre site (à ajouter) et le dossier `pilotage/`, qui contiendra une page
par client (mariage ou événement) — mise à jour automatiquement sur Netlify à chaque ajout de fichier.

## Mise en place (une seule fois)

1. **Créer un compte GitHub** (gratuit) sur https://github.com si vous n'en avez pas.
2. **Créer un nouveau dépôt** ("New repository") — nommez-le par exemple `banah-site`. Laissez-le public
   ou privé, peu importe pour Netlify.
3. **Ajouter le contenu de votre site actuel** à la racine de ce dépôt : les fichiers que vous déposez
   aujourd'hui manuellement sur Netlify (index.html, images, etc.) — via "Add file → Upload files" sur
   la page du dépôt GitHub (glisser-déposer, pas de ligne de commande).
4. **Ajouter ce dossier `pilotage/`** avec son fichier d'exemple (`exemple-client.html`) au même endroit,
   à la racine du dépôt.
5. Dans **Netlify** : *Add new site → Import an existing project → Deploy with GitHub* → autorisez l'accès
   → sélectionnez le dépôt que vous venez de créer → laissez les réglages par défaut → *Deploy*.

À partir de cette étape, **chaque changement sur GitHub republie automatiquement tout le site** — plus
besoin de redéposer manuellement l'existant.

## À chaque nouveau client

1. Donnez-moi le **nom/référence du client** et la **date du mariage** — je vous génère le fichier HTML
   de sa page (sur le même modèle que `exemple-client.html`).
2. **Dupliquez le Google Sheet modèle** (Banah_Suivi_Client_Modele) pour ce client, renommez-le, et
   partagez-le en *"Anyone with the link – Viewer"* (Fichier → Partager).
3. Récupérez l'**ID du Sheet** dans son URL (`.../d/CET-ID/edit`) et les **gid** de chaque onglet
   (visible dans l'URL quand vous cliquez sur l'onglet : `...#gid=123456`). Donnez-les-moi, je les
   intègre dans la page du client, ou modifiez-les vous-même en haut du fichier HTML
   (`SHEET_ID`, `GID_PRESTATAIRES`, `GID_PAIEMENTS`).
4. **Glissez le fichier HTML** du client dans le dossier `pilotage/` sur GitHub ("Add file → Upload files").
   Netlify republie automatiquement en moins d'une minute.
5. Le lien à envoyer au client est : `https://votre-site.netlify.app/pilotage/nom-du-fichier.html`
   (ou `https://banah-group.fr/pilotage/nom-du-fichier.html` une fois votre domaine personnalisé
   reconnecté à ce nouveau dépôt).

## Pour mettre à jour les prestataires / paiements d'un client

Rien à republier : ouvrez son Google Sheet, cochez le statut à jour (Confirmé / En attente / À sourcer,
Payé / À échoir / En retard). La page du client va chercher l'information à chaque ouverture.

## Le logo Banāh

Le fichier d'exemple utilise pour l'instant un simple bloc "B" en guise de logo (`.brand-mark` dans le
CSS). Envoyez-moi votre fichier logo (PNG ou SVG, fond transparent de préférence) et je l'intègre à la
place, sur toutes les pages clients.

## Prochaine étape (pas encore construite)

Les alertes mensuelles automatiques par email ne sont pas incluses dans ce dépôt — c'est un chantier
séparé qu'on abordera une fois cette première étape en place.
