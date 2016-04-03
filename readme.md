Notre groupe est constitué de Sabri Tanich, Paul Zeino et Tassin Mael Jose Tchuembou.


Comment lancer le jeu :

Pour générer le jar sous linux:
   - Nous nous plaçons dans le répertoire de projet en utilisant la commande cd ...../src/
   - Nous lançons la commande jar cvf tetris.jar Principale.class

Pour lancer l'application sous linux:

   - Nous nous plaçons dans le répertoire de projet en utilisant la commande cd ...../src/
   - Nous lançons la commande java Principale
   
   
 Les features que nous avons faites/ajouté :
 
 
 
 Pour jouer au Tetris :
 
 Les commandes de jeux sont:

  -Au lancement du jeux vous appuyer sur la touche "Entrée" pour lancer une partie
  - Pour déplacer à gauche appuyez sur <--
  - Pour déplacer à gauche appuyez sur -->
  - Pour accélerer le difilement de la pièce vers le bas apuuyez sur la flèche vers le bas
  - Pour retourner la pièce appuyez sur la flèche vers le haut.
  - Pour suspendre le jeux appuyez sur la touche "p".
  
  Exercice d'architecture :
  
  Pour la conception de notre application nous avons adopté une architecture modulaire, ainsi nous avons découper le programme en trois modules:

 - Module graphique: contient les classes résponsables de la gestion des interfaces graphique de l'application
 - Module Mouvement: contient les classes et les méthodes de la gestion des évenements, et le déplacement des pièces dans le jeux
 - Module Temporel: Contient les méthodes résponsable de la gestion temporelle de jeux, représenté par une horloge régissant les différents "pas
 temporels" intervenant dans la gestion des mouvements et déplacement des différentes pièces.
 
 
 Exercice Design Pattern :
 
 Illustration de trois principes de SOLID utilisés
 
Single Responsibilty Principle
 +Nous avons respecté ce principe dans toutes les classes que nous avons implémenté, ainsi chaque classe possède une 
 et une seule responsabilité ce qui nous a permis d'avoir un code flexible et la modification de la responsabilité de chaque classe 
 est beaucoup plus facile et flexible et ne se propage pas sur les autres.
 Les responsabilités de nos classes sont définies comme suit :
 
 +•	Classe principale : Cette classe est responsable de lancement du jeu (le noyau et l'interface graphique), et ne se préoccupe pas des autres tâches effectuées en arrière-plan par les différentes méthodes de l’autre classe.
 +•	Classe Pièce : Cette classe a comme unique responsabilité, la définition et le paramétrage des différentes pièces composant le jeu.
 +•	Classe Panneau Affichage : Cette classe est seulement responsable de la création et l'affichage du panneau comportant les statistiques et les commandes de jeu.
 +•	Classe Horloge : Est responsable de la gestion des paramètres temporels du jeu, ainsi elle définit la vitesse de jeu, les cycles de mouvements des pièces,….
 +•	Classe Grille : Est responsable de la définition et de la gestion de l'aire de jeu.
 +
 +Open Closed Principle
 +Nous avons respecté ce principe lors de l'implantation et ceci en donnant plus de liberté d'extension pour les différentes méthodes 
 et modules de nos classes ; Ce principe est par exemple illustré dans les constructeurs des différentes classes de notre projet, 
 ainsi aucun constructeur ne contient des instanciations conditionnelles. En respectant ce principe, nos méthodes et modules 
 peuvent être étendues en s'adaptant aux différentes implémentations (Open for extension), sans autant être amené à les 
 modifier (Closed for modification).
 
 (Voir diagramme aussi d'architecture dans les fichiers)
 +
 +
 +
 +

