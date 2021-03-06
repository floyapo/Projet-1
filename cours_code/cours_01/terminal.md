 <h2>1. Le terminal </h2> 
  <h3>1.1. Introduction </h3>

Dans cette ressource, tu vas découvrir les bases du terminal, un outils très puissant qui permet de "parler" à son ordinateur. Nous allons voir les bases: comment interagir avec le terminal, comment jouer avec ses premiers fichier, et bien d'autres.
  1.1.1 Ce que tu vas apprendre dans cette ressource
Voila la liste des questions auxquelles tu vas pouvoir répondre avec cette ressource:
* Qu'est ce que le terminal?
* Que veut dire GUI et CLI ?
* Comment exécuter ses premières fonctions avec un terminal ?
* Pourquoi la notion de géographie est très importante dans un terminal ?
* Qu'est ce que VIM et comment s'en servir ?

 <h3>1.2. Historique </h3>
Le terminal est ce qu'on appelle plus communément un interpréteur de commande (ou comman-line interpreter (CLI)en anglais), est un outil qui permet d'interpréter les commandes qu'un utilisateur tape au clavier dans l'interface en ligne de commande.

A la base, ordinateurs tournaient sans interface graphique, donc les utilisateurs passaient exclusivement par les CLI. Avec l'arrivée des systèmes d'exploitation graphique (Windows, Apple, Linux) le CLI n'a pas perdu en popularité, puisqu'il permet de faire des tâches extrêmement précises.

En gros, c'est un version texte de l'explorateur de fichiers: on peut ouvrir des dossiers, créer des fichiers, les lancer, les renommer, installer des programmes, et bien d'autres choses. On dit que c'est une CLI (Command Line Interface), comparée à la GUI (Graphical User Interface) de l'explorateur normal. Tout est fait via clavier, donc pas besoin de souris dans le terminal.

 <h3>1.3. Le terminal </h3>
  <h4>1.3.1. Qu'est ce que le terminal ? </h4>

Le terminal est un outil intimidant aux premiers abords, mais au final se révèle pas compliqué. [J'ai réalisé une vidéo qui explique le terminal](https://www.youtube.com/watch?time_continue=350&v=myz6xrDwR4) 

  <h4>1.3.2. Comment le lancer ? </h4>

 Sur Linux: CTRL + ALT + T
 Sur macOS: CMD + SPACE, puis écrire Terminal (ou iTerm), Enter.
     ALERTE BONNE ASTUCE 

    Si tu utilises Linux, passe ton termianl en anglais. Quand ce dernier te renverra une erreur, c'est bien mieux qu'elle soit en anglais. L'anglais est la la,gue d'internet, donc la majorité des gens qui ont ton problème vont le poster en anglais. Et ainsi tu auras 100 fois plus de résultats sur Google que si tu postais ton erreur en français.

  <h4>1.3.3. Premières fonctions ? </h4>

Pour faire marcher le terminal, rien de plus simple: il suffit de rentrer le texte correspondant à la fontion et cela s'exécutera. Par exemple si dans l'explorateur en GUI il suffit de double cliquer sur mon_fichier.txt pour l'ouvrir, il faudra faire dans le terminal open mon_fichier.txt (sur macOS) ou xdg-open mon_fichier.txt (sur Linux) pour l'ouvrir avec le terminal. On va tester avec notre première fonction:
$ echo "Hello world !" 
(je commence toutes les commandes du terminal avec un $, c'est une convention)

Si tu exécutes cette commande le terminal devrait te renvoyer Hello wordl ! (cette phrase est [un grand classique de la programmation](https://fr.wikipedia.org/wiki/Hello_world)). Et là tu viens de d'exécuter ta première commande de terminal 
Maintenant nous allons voir les premières commandes de base.

   <h5>1.3.3.1. PWD </h5>

pwd est l'acronyme de Print Working Directory, une commande qui affiche le dossier dans lequel tu es actuellement.
$ pwd
Pour moi, pwd me renvoie:
/Users/felix
C'est comme dans l'explorateur en GUI, quans tu doucle-clique sur felix, il te déplace dans le dossier felix qui est dans le dossier Users 

     ALERTE BONNE ASTUCE
    pwd est généralement la première commande que l'on tape quand on arrive dans le terminal de quelqu'un: c'est idéal pour s'y retrouver 

   <h5>1.3.3.2. LS </h5>

ls est le diminutif pour list ,cetete fonction affiche les fichiers et dossiers qu'il y a dans mon dossier actuel.
$ ls
Pour moi, ls me renvoie:
Applications/ Dropbox/ Music/ Desktop/ Pictures/ Documents/ Library/ Public/ Downloads/ Movies

Dans le terminal, nous pouvons donner des options aux fonctions, en faisant > $ fonction -option. Par exemple,je peux faire ls -a, ce qui a pour effet d'afficher aussi les fichiers commençant par un . (fichiers de devs en général), ou je peux faire >ls -l pour afficher la liste au format long. Et je peux même combiner les deux en faisant >ls -al pour afficher aussi les fichiers commençants par un >. tout au format long.

   <h5>1.3.3.3 MAN </h5>

>man est le diminutif de manual. Man lance un programme qui permet de lire la manuel d'une fonction précise. Pratique pour savoir toutes ses spécificités. Pour s'en servir il suffit de taper: >man fonction. Par exemple pour afficher le manuel de ls, je dois taper/
$ man ls

Ce qui m'ouvrira son manuel, que je peux quitter à tout moment en tapant >q .

  <h5>1.3.4 Où sommes-nous ? </h5>

Une notion **fondamentale** pour le terminal: la notion de géographie. Comme dans l'explorateur en GUi, on se déplace de dossiers en dossiers dans le terminal. Si jamais tu veix ouvrir un fichier en tapant >open file.txt (sur macOS) ou >xdg-open file.txt (sur Linux) et que tu ne te trouves pas dans le bon dossier, le terminal te renverra une erreur. Un peu comme si tu essayais de double-cliquer sur file.txt dans le mauvais dossier: imossible car il n'y est pas.

Tu vas devoir te déplacer donc de dossiers en dossiers pour ouvrir et interagir avec les bons fichiers.

 <h4>1.3.5 CD </h4>

>cd est l'acronyme de _Change Directory_, qui te permet de naviguer entre dossiers. L'équivalent d'un double-clic sur un dossier en quelque sorte

$ cd nomdudossier

Tu te déplaceras dans le dossier nommé >nom du dossier (s'il existe dans le dossier dans lequel tu te trouves).

Tu peux aussi te déplacer vers le dossier parent en faisant > $ cd ...

     ALERTE BONNE ASTUCE
    Utliser la touche >TAB permet de faire de l'autocompletion, très pratique pour cette méthode. Aussi, faire >cd + [ESPACE] + >TAB + >TAB affiche les dossiers disponibles

 <h4>1.3.6. Autres fonctions </h4>
  <h5>1.3.6.1. Créer un fichier </h5>
En tapant: 
$ touch nomdufichier

Cela aura pour effet de créer un fichier qui s'appelle nomdufichier

   <h5>1.3.6.2. Copier </h5>

 Pour copier un fichier ou un dossier d'un endroit à un autre, il suffit de rentrer:
$ cp fichier_à_copier lieu_de_destination

   <h5>1.3.6.3. Déplacer </h5>

 Pour déplacer (couper) un fichier ou un dossier d'un endroit à un autre, il suffit de rentrer:
 mv [fichier_à_déplacer] [lieu de destination]

 Protip: >mv est très pratique pour renommer un fichier. Imaginons que tu as créé un fichier "hello.rv" au lieu de "hello.rb". Oups, malheur. Heureusement, faire >$ mv hello.rv hello.rb résoud ceci en quelques coups de clavier !

  <h5>1.3.6.4. Remove </h5>

  $ rm nomdudossier

      INSTANT CULTURE GE

>rm est à l'origine d'une blague vieille comme le monde. En effet, ajouter l'option >-f permet de forcer la suppression d'un fichier, même s'il est important pour l'ordinateur, et finir par >/ ou >* dit à votre ordinateur de prendre absolument tous les fichiers. Ainsi, si tu tapes >$ rm -rf/ ou >$ rm -rf * dans ton terminal, tu dis à ce dernier de tout prendre et de tout effacer, en forçant. Et figure toi que >rm est très rapide, et donc effacera l'intégralité de ton ordinateur en quelques secondes à peine. **A ne jamais jamais jamais faire** donc.

   <h5>1.3.6.5 Vim </h5>
 Vim est un des éditeurs de texte les plus respectés au monde. Comme il passe uniquement par le terminal, il se marie extrêmement bien avec cet outil. Et comme vim utilise exclusivement le clavier, ses raccourcis permettent d'aller extrêmement vite, pour qui ose grimper la très dure courbe d'apprentissage (quelques semaines à plein temps). De ce fait, je te montrerai vim pour ta culture générale, mais te demanderai de passer par un autre éditeur de texte.

$ vim nomdufichier
Permet d'ouvrir vim sur le fichier nomdufichier et de l'éditer. Pour quitter vim, il faut entrer >:q!

  <h4>1.3.7 Autres astuces </h4>

> CTRL + C annule la fonction en cours. Pratique quand on a une boucle infinie

La casse est très importante, idem pour les espaces.

Il y a des raccourcis pratiques, par exemple >CTRL + U efface la ligne en cours.

Les touches du haut et du bas permettent de naviguer dans l'historique des commandes. Très pratique pour par exemple re-éxécuter une commande que tu viens de faire.

<h3>1.4. Les points importants </h3>

Voici les points à retenir de la ressource:
* Pour lancer le terminal sur Linux: >CTRL + ALT + T ; pour le lancer sur macOS: >CMD + SPACE; puis écrire >Terminal (ou iTerm), Enter.
* >man est le manuel qui permet de lancer la manuel des fonction
* >pwd affiche le dossier dans lequel tu es actuellement
* >ls est une commande qui affiche les fichiers et dossiers qu'il y a dans mon dossier actuel 
* la notion de géographie est fondamentale: le terminal n'arrivera pas à ouvrir les fichiers s'ils ne se trouve pas dans le bon dossier
* >cd permet de changer de dossier
* >touch permet de créer un fichier 
* >cp permet de déplacer un fichier ou un dossier
* >rm permet de supprimer un fichier

 <h3>1.5 Aller plus loin </h3>

Voici un excellent [cours express](https://www.vikingcodeschool.com/web-development-basics/a-command-line-crash-course) pour avoir quelques bases sur le terminal. Il est un peu similaire au mien, mais aborde d'autres sujets intéressants tels que le PATH.

Viking Code School ont aussi fait un [cours sur le pimp de terminal](www.vikingcodeschool.com/web-development-basics/a-command-line-crash-course) pour avoir plein de couleurs de BGs sur le tien.

Michael Hartl a fait une célèbre introduction au terminal nommée [Learn Enough Command Line to Be Dangerous](www.learnenough.com/command-line-tutorial). Cette ressource permet d'aller assez loin en détails dans le terminal.

Pour ceux qui veulent découvrir Vim, voici [une marche à suivre](https://medium.com/actualize-network/how-to-learn-vim-a-four-week-plan-cd8b376a9b85) pour être champion de Vim rapidement.







