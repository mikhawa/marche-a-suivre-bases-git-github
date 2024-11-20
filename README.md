# Marche à suivre bases Git-Github

Voici quelques procédures simples pour utiliser `Git` et `Github`.

`Git` doit être installé sur votre machine, si ce n'est pas le cas, installez-le via le site officiel : 

https://git-scm.com/

Pour créer votre compte sur `Github` et le lier en `SSH` à votre utilisateur sur votre `OS`, suivez le mode d'emploi ici :

[Compte Github](https://github.com/WebDevCF2m2025/prefo-git/blob/main/README.md#compte-github) et [Lier votre compte à votre OS](https://github.com/WebDevCF2m2025/prefo-git/blob/main/README.md#lier-votre-compte-et-votre-pc)

## Nouveau projet en local

### Initialiser un projet Git

Si vous n'avez pas encore initialisé votre projet avec Git, commencez par ouvrir votre terminal et exécuter les commandes suivantes.

**Initialisation d'un dépôt Git :**

```bash
# Allez dans le répertoire de votre projet
cd /chemin/vers/ton/projet

# Initialisez un dépôt Git dans votre répertoire
git init
```

Cela crée un répertoire caché en `.git` qui contiendra toutes les informations de versioning pour votre projet.

**Attention de ne pas mettre un projet `Git` dans un autre projet `Git` !**

### Liez le projet à un dépôt GitHub

Avant d’envoyer votre projet sur `GitHub`, vous devez créer un nouveau dépôt sur `GitHub`, puis lier ce dépôt à votre projet en local.

Vous devez être connecté à votre compte !

**Créer un dépôt sur GitHub :**

Allez sur [GitHub](https://github.com/).

Créez un nouveau dépôt (`repository`) en cliquant sur le bouton vert "New" dans l'onglet des dépôts sur la gauche, ou le `+` en haut à droite puis "New Repository".

Choisissez un `nom de répertoire`, vous avez le choix de le rendre `public` ou `privé`, mais ne cochez pas les autres options.

Ne cochez pas l'option "Initialize this repository with : Add a README file" si vous avez déjà initialisé votre projet localement.

Cliquez sur "Create repository" en vert.

**Lier le projet local à GitHub :**

Dans votre terminal, exécutez les commandes suivantes pour lier votre projet local à votre dépôt GitHub :

Remplacez 'SSH_DU_DEPOT' par la clef SSH de votre dépôt GitHub, vous la trouverez sur la page de votre dépôt GitHub :

    code > Clone > SSH

Copiez le lien `SSH` (qui commence par `git@github.com:`) et remplacez-le dans la commande ci-dessous :

```bash
# Ajoutez l'URL de votre dépôt GitHub   
git remote add origin SSH_DU_DEPOT
```

### Ajouter ou supprimer des fichiers dans le staged

`Git` utilise la notion de `staging area` (zone de préparation) pour que vous puissiez préparer vos fichiers avant de les sauvegarder (`commit`). Voici comment ajouter ou supprimer des fichiers dans le `staged` :

**Ajouter des fichiers au staging :**

Si tu veux ajouter des fichiers spécifiques ou tous les fichiers modifiés :

```bash
# Ajouter un fichier spécifique
git add nom_du_fichier

# Ajouter tous les fichiers modifiés dans le projet
git add .
```

**Supprimer des fichiers du staging :**
Si vous avez ajouté un fichier par erreur, vous pouvez le retirer de la `zone de staging` :

```bash
# Supprimer un fichier du staging (mais ne le supprime pas du répertoire local)
git reset nom_du_fichier
```

### Faire des commits
Une fois que vous avez ajouté ou supprimé des fichiers dans le staging, vous pouvez enregistrer vos changements dans l’historique de `Git` en effectuant un `commit`.

**Faire un commit :**
    
```bash
# Créer un commit avec un message descriptif
git commit -m "Message de commit décrivant les changements"
``` 

### Envoyer les commits sur GitHub

Une fois le commit effectué localement, vous pouvez envoyer vos changements vers votre dépôt GitHub (`push`).

**Envoyer les modifications sur la branche principale (généralement 'main' ou 'master')**

```bash
git push origin main
```

### Résumé des étapes

1. Initialiser le projet Git : `git init`.
2. Créer un dépôt GitHub et lier le projet local à GitHub : `git remote add origin SSH_DU_DEPOT`.
3. Ajouter des fichiers au staging : `git add nom_du_fichier` ou `git add .`.
4. Supprimer des fichiers du staging : `git reset nom_du_fichier`.
5. Faire un commit : `git commit -m "message"`.
6. Envoyer les commits vers GitHub : `git push origin main`.

Cela constitue un flux de travail de base pour utiliser Git et GitHub.

