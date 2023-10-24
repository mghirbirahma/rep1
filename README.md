                                                *********************************Compte Rendu - Configuration et Utilisation de Git**************************************
/////////Ce compte rendu détaille les étapes pour configurer l'environnement Git, créer un nouveau projet, comprendre les concepts de base de Git, collaborer sur Git, et utiliser GitFlow pour la gestion des versions.
****Partie 1 : Préparation de l'environnement Git****
1. Création de clé SSH
Pour sécuriser vos connexions à des dépôts distants comme GitHub, vous devez générer une clé SSH. Voici comment faire :

a. Générez votre clé SSH en utilisant la commande suivante :
   ssh-keygen -t rsa -b 4096 -C votreadresse@email.com
b. Copiez votre clé publique SSH avec la commande :
   cat ~/.ssh/id_rsa.pub
c. Ajoutez votre clé publique SSH à votre compte sur le dépôt distant, par exemple, GitHub.

2. Configuration de Git
Pour que vos commits soient correctement identifiés, configurez votre nom et adresse e-mail :
    git config --global user.name "Votre Nom"
    git config --global user.email votre@email.com

3. Connexion SSH aux dépôts distants
Testez votre connexion SSH en utilisant la commande suivante (remplacez l'adresse du serveur distant si nécessaire) :
    ssh -T git@github.com



****Partie 2 : Création d'un nouveau projet****
   
1-Connectez-vous à votre compte GitHub (ou GitLab).

2-Cliquez sur le bouton "Nouveau" pour créer un nouveau projet, donnez-lui un nom significatif, choisissez les options appropriées, puis cliquez sur "Créer le référentiel" (ou "Create Repository").

3-Notez l'URL de votre projet pour une utilisation ultérieure.

4-Clonez le projet sur votre machine locale :
   git clone [URL de votre projet]
   
****Partie 3 : Concepts de base de Git****
1. Travailler avec les fichiers
Créez un fichier index.html dans votre répertoire de projet, ajoutez-y du contenu, puis ajoutez-le à l'index et effectuez un commit :
   touch index.html
   echo "Contenu de votre fichier" > index.html
   git add index.html
   git commit -m "Premier commit : ajout de index.html"
   
3. Historique des commits
Visualisez l'historique des commits avec la commande :
   git log
Pour afficher les différences entre deux commits :
   git diff commit_id_1 commit_id_2

   
****Partie 4 : Collaborer sur Git****
1-Créez une nouvelle branche pour travailler sur une fonctionnalité spécifique de votre projet :
   git branch ma-fonctionnalite
   git checkout ma-fonctionnalite
   
2-Effectuez des modifications, ajoutez-les à l'index, faites un commit et poussez les modifications vers le dépôt distant.

3-Gestion des conflits : Simulez un conflit, fusionnez les branches et résolvez le conflit.



****Partie 5 : Utilisation de GitFlow****
1-Initialisation de GitFlow :
   git flow init
   
2-Création d'une nouvelle fonctionnalité :
  git flow feature start ma-fonctionnalite
  
3-Création d'une nouvelle version :
  git flow release start ma-version
  
4-Fusionnez la branche de fonctionnalité dans la branche de développement.

5-Création d'un correctif :
   git flow hotfix start mon-correctif

****************Ceci résume les principales étapes pour configurer Git, créer un projet,travailler avec Git, collaborer avec d'autres personnes, et utiliser GitFlow pour la gestion des versions.********************** 







