1- Faites votre premier commit

Pour commencer, créez un nouveau dossier et positionnez vous dedans avec la console

Vous ne voulez pas versionner l'intégralité de votre ordinateur en lançant  git init dans un dossier comme "Mes Documents" ou "Applications" !

Une fois que vous vous êtes placés dans votre nouveau dossier grâce à la commandecd de votre Terminal, créez un nouveau dossier 'monPremierRepo' en lançant la commande suivante : 

mkdir monPremierRepo

Pour activer un dossier comme repository Git, il suffit de se placer dans ce dossier avec le Terminal puis d'utiliser la commande git init. 

Lorsque vous créez un fichier dans un repository, vous devez donc l'ajouter à l'index Git à l'aide de la commande git add nomDeVotreFichier.extension. Par exemple :

git add checklist-vacances.md

Pour gagner du temps, vous pouvez ajouter tous les fichiers dans le répertoire courant en tapant

git add .

dans la console. Évidemment, faites bien attention quand vous utilisez ce raccourci à ne pas rajouter trop de fichiers à l'index.

Lorsque vous modifiez votre repository, vous devez demander à Git d'enregistrer vos modifications en faisant un git commit. L'option-m vous permet de lui envoyer un message décrivant les modifications effectuées, ce qui s'avèrera très utile pour vous par la suite, you'll see! :) Par exemple : 

git commit -m "Ajouté ma checklist-vacances.md (woohoo!)"

2- Lisez l'historique

Comment vous y retrouver dans l'historique de vos commits ?

Grâce à la commande  git log qui vous affiche la liste de tous les commits que vous avez réalisés !

vous pouvez condenser ces deux étapes de la façon suivante : 

git commit -a -m "Ajouté itinéraire dans checklist-vacances.md"

3- Positionnez-vous sur un commit donné

Pour vous positionner sur un commit donné de votre historique, il vous suffit d'utiliser la commande git checkout de la façon suivante : 

git checkout SHADuCommit

Pour revenir à votre branche principale (au commit le plus récent), on utilise la même commande : 

git checkout master


On ne peut pas vraiment "supprimer" un commit, mais on a plusieurs options pour l'annuler. Cependant, ces options ont des limites et sont à utiliser avec prudence et parcimonie !

Je vous présente une de ces options : vous pouvez "revert" un commit, c'est-à-dire créer un nouveau commit qui fait l'inverse du précédent, avec la commande suivante :

git revert SHADuCommit

Sinon, si vous voulez simplement modifier le message de votre dernier commit, vous pouvez utiliser la commande suivante :

git commit --amend -m "Votre nouveau message"


Je n'ai pas encore fait mon nouveau commit, mais je veux annuler tous les changements que je n'ai pas encore commités. Possible ?

 Possible avec un reset !

git reset --hard

4- Découvrez les remotes

Une fois que vous avez travaillé sur votre code et effectué vos commits, vous allez donc les envoyer sur un remote, c'est-à-dire une autre machine qui peut être : 

interne (si vous avez la chance d'avoir plusieurs ordinateurs ;) )

ou externe (grâce à des services comme GitHub ou BitBucket). Utiliser un remote externe va aussi vous permettre de travailler sur des projets à plusieurs, pour que tout le monde ait accès aux dernières modifications de chacun sur un remote partagé. 

5- GitHub, qu'est-ce que c'est ?

pour mieux vous y retrouver dans votre code en ligne : appuyez sur la touche t, vous pourrez alors faire une recherche dans vos noms de fichiers en tapant un mot / des lettres clé ! 

6- Récupérez du code d'un autre repository

Dans cette vidéo, nous avons cloné le repo de la librairie React.js, une librairie créée par Facebook et qui permet de mieux gérer ses interfaces graphiques grâce à JavaScript. Nous avons donc effectué sur notre machine la commande :

git clone https://github.com/facebook/react.git

7- Créez votre premier repository

... et en parlant de la commande git clone, notez que vous pouvez cloner votre repo avec deux options : 

L'option HTTPS que je vous ai  invité à utiliser dans ce cours : c'est l'option la plus simple, qui demande de fournir vos identifiants GitHub (nom d'utilisateur et mot de passe) à chaque fois que vous faites un git clone. 

L'option SSH qui est plus pratique car elle ne vous demande pas vos identifiants à chaque fois. Par contre, pour l'utiliser, il faut générer une clé SSH, ce qui est un peu plus compliqué pour ce cours d'initiation. Mais une fois que vous vous sentez plus à l'aise, je vous invite à consulter la marche à suivre dans la documentation de GitHub et à utiliser cette option SSH. 



