<!--
* L'ARCHITECTURE LOGICIEL ROUTER + DESIGN PATTERN MVC
 Cette architecture prend son inspiration des design patterns :
    - Composite
    - Observer
    - Strategie
    & explication :
        Voir l'mage mvc_router.png
        -1- Le router :
            Le router correspondra au routage des différentes pages du site avec des url propres, explicites et surtout sécurisées.
            Le router est une classe qui analysera au niveau de son constructeur si il a affaire à un modèle ou à un contrôleur pour rajouter vos propres routes.
            Dans le schéma, c'est lui qui est appelé en premier.
        -2- Le contrôleur :
            Correspondra a la logique de fonctionnement du site web (les différents algorithmes).
            Il joue le rôle de chef d'orchestre entre les modèles et les vues.
        -3- Le modèle :
            Correspondra à une table de notre BDD avec le CRUD
        -4- La vue :
            Correspondra à l'interface d'utilisation du site web (le front)
    & création de la structure logiciel
        Voir arborescence du site
        Creé Le fichier .htaccess : c'est un fichier apache qui va nous permettre de dévérouiller la réecriture des des url dans le navigateur pour le routage.
        Créer le fichier config.php dans le dossier config qui va nous permetre de créer nos propres constantes globales de configuration.
        Créer le fichier classe Autoloader.php dans le dossier core
            Il va nous permettre de d'éviter l'utilisation des require_once() dans les fichiers classes.
            Il va permettre également d'implémenter correctement une classe dans un autre fichier grace à l'autocomplétion et l'instruction use.
        Créer le fichier classe ConnexionController.php.
            C'est la classe qui va nous permetre de nous connecter à la BDD en local ou en ligne.
        Créer les dossiers et fichiers dans le dossier assets (js, style, ...)
        Créer la BDD avec les tables avec PhpMyAdmin
            créer la table voiture
            créer la table membre
        Créer le fichier pageAccueil.php dans view/front/
            renseigner les fichiers include au niveau de assets/inc/front/
            renseigner la barre de navigation dans header.inc.php
        Créer votre 1ère classe modèle dans le dossier model, ici Voiture.php avec une méthode qui va nous remonter la liste des voitures.
        Créer le 1er controller VoitureController.php dans le dossier controller qui va connécter le modèle à le vue(view) avec un certain algorythme.
        Créer la vue pageAccueil.php où l'on va récupérer la variables $voitures et la manipuler pour l'affichage dans une boucle foreach

 -->