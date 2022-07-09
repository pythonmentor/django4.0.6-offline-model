# Creation d'un projet django offline - kit de démarrage

Le code contenu dans ce projet a pour objectif de permettre la création d'un projet django de démarrage sur une
machine qui n'est pas connectée à internet.


[<img src="https://i.gyazo.com/79e2dba25fe15d69df93f9d1c545017a.jpg" width="50%">)](https://vimeo.com/728358593/a8dec4e3dd "Installation offline d'un projet django")

## Instruction d'installation

Voici les instructions permettant de reproduire l'installation sur une machine non connectée au réseau:

### Phase 1: sur une machine connectée à internet

1. Téléchargez l'[archive zip suivante](https://github.com/pythonmentor/django4.0.6-offline-model/archive/refs/heads/main.zip)
2. Placez l'archive sur une clé USB pour permettre le transfert vers la machine hors connexion

### Phase 2: connecter la clé USB à la machine hors connexion

3. Décompressez l'archive zip contenue sur la clé USB dans un répertoire de votre choix
4. Ouvrez l'explorateur de fichier et rendez-vous dans votre répertoire du projet. Pour vérifier que c'est le bon répertoire, ce dernier doit contenir le fichier requirements.txt. 
5. Ouvrez un terminal powershell dans le répertoire du projet (Si windows >= 10). Voici la procédure pour cela:
    - Je suppose que vous être dans l'explorateur de fichier, dans le répertoire de votre projet
    - En maintenant la touche MAJ du clavier pressée, cliquez droit dans le répertoire du projet
    - Sélectionnez "Open Powershell window here" ou l'équivalent dans la langue de l'OS
    - Si vous avez une version de windows inférieure à 10 ou si l'option n'est pas disponible, **contactez-moi**
6. Pour vérifier que vous êtes dans le bon répertoire, tapez la commande `dir`. La liste des fichiers devrait alors faire apparaître les fichiers manage.py et requirements.txt
7. Permettez à Powershell d'exécuter les scripts en exécutant la commande `set-executionpolicy -executionpolicy remotesigned -scope currentuser`
8. Toujours dans le terminal powershell, créez un environnement virtuel pour le projet avec la commande `py -3.9 -m venv .venv`.
9. Encore dans le terminal powershell, activez l'environnement virtuel du projet avec la commande `.venv/scripts/activate`  
10. Installez maintenant les dépendances en exécutant de la commande suivante: `pip install --no-cache (get-item requirements/*)`
11. Exécutez encore les deux commandes suivantes à la suite: `python manage.py migrate` et `python manage.py runserver` pour lancer le serveur web de développement de django.
12. Visiter la page http://127.0.0.1:8000 dans un navigateur internet. La page d'accueil du nouveau projet django doit s'afficher

## Démarrer avec django

Pour démarrer django, je vous invite à suivre le [didacticiel officiel](https://docs.djangoproject.com/fr/4.0/intro/). Vous trouvez une version offline de ses tutoriels à la page 7 de ce [document PDF](https://media.readthedocs.org/pdf/django/4.0.x/django.pdf). Ne pas suivre le quick install guide, car nous avons déjà installé le projet et ses dépendances. Le guide d'installation du tutoriel ne fonctionnera pas offline.
