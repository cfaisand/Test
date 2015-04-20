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



