# Activer la sauvegarde Google Drive

À faire **une seule fois**, après la mise en ligne du site sur GitHub (voir `LISEZMOI.md`). Compte environ 20 minutes. C'est gratuit et aucune carte bancaire n'est demandée.

Remplace partout `TON-PSEUDO` par ton pseudo GitHub. Google renomme parfois ses menus : si un intitulé diffère légèrement, cherche le plus proche.

## 1. Remplir la page de confidentialité

Ouvre `confidentialite.html` et remplace les trois mentions entre crochets : `[NOM DE L'ÉDITRICE OU VZN Unlimited]` et `[ADRESSE E-MAIL DE CONTACT]` (deux fois). Dépose ensuite le fichier sur GitHub avec les autres.

Vérifie qu'elle s'ouvre bien à l'adresse : `https://TON-PSEUDO.github.io/gestionnary/confidentialite.html`

## 2. Prouver à Google que le site est à toi

1. Va sur [search.google.com/search-console](https://search.google.com/search-console) avec ton compte Google.
2. « Ajouter une propriété » › « Préfixe de l'URL » › saisis `https://TON-PSEUDO.github.io/`
3. Choisis la méthode « Fichier HTML » : télécharge le petit fichier proposé.
4. Pour cette étape, il faut un **second dépôt GitHub** nommé exactement `TON-PSEUDO.github.io`. Crée-le en Public, déposes-y ce fichier, puis active Pages comme pour le premier (Settings › Pages › main › Save).
5. Reviens dans Search Console et clique sur « Valider ».

## 3. Créer le projet Google Cloud

1. Va sur [console.cloud.google.com](https://console.cloud.google.com) et accepte les conditions si c'est ta première visite.
2. En haut, sélecteur de projet › « Nouveau projet » › nom : `Gestionnary` › Créer.
3. Menu › « API et services » › « Bibliothèque » › cherche **Google Drive API** › « Activer ».

## 4. Configurer l'écran de connexion

Menu › « Google Auth Platform » (ou « Écran de consentement OAuth »).

- **Informations sur l'application** : nom `Gestionnary`, adresse e-mail d'assistance (la tienne).
- **Audience** : « Externe ».
- **Coordonnées** : ton adresse e-mail.
- **Branding** :
  - Page d'accueil : `https://TON-PSEUDO.github.io/gestionnary/`
  - Règles de confidentialité : `https://TON-PSEUDO.github.io/gestionnary/confidentialite.html`
  - Domaine autorisé : `TON-PSEUDO.github.io`
- **Accès aux données** › « Ajouter ou supprimer des niveaux d'accès » › colle `https://www.googleapis.com/auth/drive.appdata` › Mettre à jour. Elle doit apparaître dans « Niveaux d'accès non sensibles ».

## 5. Créer l'identifiant client

Menu › « Clients » (ou « Identifiants ») › « Créer un client ».

- Type d'application : **Application Web**
- Nom : `Gestionnary web`
- Origines JavaScript autorisées : `https://TON-PSEUDO.github.io` (sans barre oblique à la fin, sans `/gestionnary`)
- Créer, puis **copie l'ID client**. Il ressemble à `1234567890-abc123.apps.googleusercontent.com`.

## 6. Ouvrir l'outil à tout le monde

« Audience » › « Publier l'application » › passer en **production**. Tant que l'application reste en mode « Test », seuls les comptes que tu ajoutes à la main peuvent se connecter.

La permission demandée est classée non sensible : Google n'exige pas de vérification de sécurité. Il peut proposer une vérification de la marque (nom, logo), qui se fait en général automatiquement en quelques minutes.

## 7. Brancher l'identifiant dans l'outil

Envoie-moi l'ID client et je te renvoie le fichier `index.html` prêt.

Tu peux aussi le faire toi-même : ouvre `index.html` avec un éditeur de texte, cherche la ligne `const GOOGLE_CLIENT_ID='';` et colle l'identifiant entre les apostrophes. Dépose ensuite le fichier sur GitHub (« Add file » › « Upload files » › « Commit changes »).

## Vérifier que tout marche

1. Ouvre le site sur ton ordinateur, puis Réglages › « Connecter mon Google Drive ».
2. Ajoute une tâche.
3. Ouvre le site sur ton téléphone, puis « J'utilise déjà Gestionnary ». Ta tâche doit apparaître.
