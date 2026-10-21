# Mettre Gestionnary en ligne gratuitement

Gestionnary est un site d'une seule page, sans serveur ni base de données. On l'héberge gratuitement sur **GitHub Pages**. Aucune carte bancaire n'est demandée, ni pour le compte ni pour le site.

Adresse finale : `https://TON-PSEUDO.github.io/gestionnary/`

## Ce que contient ce dossier

| Fichier | Rôle |
| --- | --- |
| `index.html` | L'outil complet |
| `manifest.webmanifest` | Permet d'installer l'outil sur le téléphone comme une application |
| `icon.svg`, `icon-192.png`, `icon-512.png` | L'icône |
| `sw.js` | Permet à l'outil de s'ouvrir même sans connexion |
| `LISEZMOI.md` | Ce guide (inutile de le mettre en ligne) |

## Étapes (15 minutes, une seule fois)

1. **Créer un compte gratuit** sur [github.com](https://github.com) (« Sign up »). Choisis bien ton pseudo : il apparaîtra dans l'adresse du site.
2. **Créer un dépôt** : bouton « + » en haut à droite › « New repository ».
   - Nom : `gestionnary`
   - Visibilité : **Public** (obligatoire pour la version gratuite de GitHub Pages)
   - Clique sur « Create repository ».
3. **Déposer les fichiers** : sur la page du dépôt, clique sur « uploading an existing file ». Glisse les 6 fichiers (tout sauf ce guide), puis clique sur « Commit changes » en bas.
4. **Activer le site** : onglet « Settings » du dépôt › « Pages » dans le menu de gauche.
   - Source : « Deploy from a branch »
   - Branch : `main`, dossier `/ (root)`
   - Clique sur « Save ».
5. **Attendre 1 à 2 minutes**, puis recharger la page « Pages ». L'adresse de ton site s'affiche en haut.

## Mettre à jour l'outil plus tard

Sur la page du dépôt : « Add file » › « Upload files », glisse le nouvel `index.html`, puis « Commit changes ». Le site se met à jour en une à deux minutes. Les données des étudiants ne sont pas touchées : elles sont dans leur navigateur, pas sur le site.

## Installer l'outil sur un téléphone

- **iPhone (Safari)** : bouton Partager › « Sur l'écran d'accueil ».
- **Android (Chrome)** : menu ⋮ › « Installer l'application » ou « Ajouter à l'écran d'accueil ».

## Ce qu'il faut savoir

- **Les données restent sur l'appareil de chaque étudiant.** Rien n'est envoyé ni stocké en ligne. Pour passer du téléphone à l'ordinateur, l'étudiant exporte sa sauvegarde (Réglages › Sauvegarde et synchro) et la restaure sur l'autre appareil.
- **Le code du site est public** sur GitHub. C'est normal et sans risque : il ne contient aucune donnée personnelle.
- **Coût : 0 €.** Un nom de domaine personnalisé (par exemple gestionnary.fr) coûterait environ 10 à 15 € par an, mais il n'est pas nécessaire.
- **Pour la V2** (synchro automatique, connexion directe à Google Agenda), il faudra une page de confidentialité sur le même site et une vérification Google. Cette vérification est gratuite.
