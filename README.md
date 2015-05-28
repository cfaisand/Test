# Test
Récupérer une copie en local

  git clone URL

    http : https://github.com/login/folder.git

    ssh : git@github.com:login/folder.gif


Voir dans quel état on se trouve :

	git status

Enregistrer les modifications :

	1: Ajouter les changements à enregistrer dans l'index

		git add file1 [file2] ...

	2: Faire le commit

		git commit -m message



Ajouter automatiquement les fichiers déja sur git :

	git commit -a -m message


Revoir les commits

	gitk (interface graphique)

	git log (affiche les commits)

	git log -p (affiche les modifications pour chacun des commits)

	git log --stat --summary (version plus courte du précédent)

	git log --oneline (une ligne par commit)


Envoyer les fichiers vers le serveur git :

	git push

Recevoir les fichiers :

	git pull (récupère et intègre les changements)

	git fetch (récupère simplement les changements)

Ajouts, suppression de fichiers :

	ajout : 

		git add fichiers
	
	suppression :

		git rm fichiers

	renommer-déplacer :
	
		git mv source destination (revient à supprimer et ajouter -> voir git log --summary [-M])

Mettre du travail de côté :

	git stash (met les modifs de côté)

	git stash pop [id] (dépile et applique les dernières modifs sauvegardées par git stash)

	git stash drop [id]

	git stash show [id]

	git stash list

	(voir man git stash)

Fichier .gitignore :

	créer le fichier .gitignore

	indiquer à l'intérieur les fichiers ou extensions de fichiers qu'on ne veut pas enregistrer sur git (ex : Essai.java, *.o, etc)

	ne pas oublier d'enregistrer .gitignore sur git

Les branches :

	Création de branche :

		git branch name

	Liste des branches :

		git branch

	Changer de branche :
		
		git checkout name

	Fusionner 1 branche avec master :
		
		git merge name (si il y a conflit, le merge s'arrête et les points problématiques sont affichés -> voir git diff)

Etiqueter une version :

	git tag nom
	
	Ex : git tag v1.0

	Pour voir la liste des tags :
		
		git tag

Identifier l'origine des changements :

	git blame Fichier

Identifier le commit à l'origine d'un problème :

	git bisect
	
	git bisect start

	git bisect bad

	git bisect good Version

Choisir ce qu'on ajoute pour un commit :

	git add -p Fichier

Annuler un commit :

	git revert identifiant

Compléter le dernier commit (avant de partager avec git push) :

	git commit --amend

Annuler des changements / les derniers commits :

	! : à éviter si les commits ont déjà été partagés

	git reset [mode] [id de commit]

	Modes :

		--soft : réinitialise le dépôt seulement

		--mixed : réinitialise le dépôt et l'index (valeur par défaut)

		--hard : réinitialise tout, répertoire de travail compris

		Ex : git reset HEAD^^  : supprime les 2 derniers commits

		Ex : git reset --hard : réinitialise le répertoire de travail au dernier commit

