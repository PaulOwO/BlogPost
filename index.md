# Blog Post

Bienvenue sur le blog post technique de mon moteur de jeu réalisé lors de la deuxième partie du module GPR920 à la SAE Institute.
Lors de ce blogpost je vais essayer de vous montrer ce que le module m'a apporté, acompagné de quelques détails techniques.

## Moteur de jeu

Nous avons tout d'abord commencé le projet en finissant les dossiers vecteurs et en rajoutant des "operators" qui nous permettent d'effectuer le calcul désiré sans le réécrire à chaque fois. Cela fut très important car les vecteurs furent utilisés du début à la fin du projet.

![image](https://user-images.githubusercontent.com/71375990/126193762-27c1256c-889e-44dd-9edb-7022630af686.png)

_Les operators permettent d'additionner les vecteurs entre eux._

Nous avons aussi pour la première fois découvert une partie cruciale de la programmation et du travail en entreprise. En effet les  **tests** nous servent sur plusieurs points, ils nous aident à savoir si le programme nous donne le résultat désiré pour des exemples en particulier, puis après avoir déterminé quelle partie du code il faut refaire ils sont d'une grande aide pour déboguer. De plus, en entreprise ils sont les seuls qui permettent de prouver que notre code fonctionnait avant de le mettre en commun et qu'ainsi, si les tests ne passent plus après cela, ce n'est pas notre faute. J'ai donc retenu que malgrés le temps supplémentaire que nous prennons à les mettres en place, les tests sont vraiment utiles et peuvent mêmes nous faire gagner du temps. Il faut donc en faire à un maximum d'endroits possible.

![image](https://user-images.githubusercontent.com/71375990/126197453-4ffcef6e-e387-40e7-8024-83daf7ae00fb.png)

_Test de taille et du centre de plusieurs rectangles._

Suite à cela nous avons créé de nombreuses structures de données accompagnées de leurs calculs et tests.

![image](https://user-images.githubusercontent.com/71375990/126197506-d368858c-6582-4c30-98e1-f1ded191e594.png)

AABB entours les polygones d'un carré puis on les projette en "x" et "y" pour voir si contact a lieu.

Durant cette partie grâce à mes nombreuses questions je pense avoir amélioré mon niveau en c++, en géométrie et en math. J'ai aussi appris pour la première fois comment utiliser une matrice.

![image](https://user-images.githubusercontent.com/71375990/126194261-c032d48b-977e-4aee-afc6-a5223b808aa5.png)

Résolution de matrice grâce à la méthode de cramer (necessite le déterminent)


Lors d'une deuxième partie nous avons reçu un programme qui pouvait dessiner des cercles qui tombaient et nous avons pour objectif de les faire rebondir et avoir des collisions réalistes. Cette partie fût plus compliquée pour moi. Voici quelques exemples de code, la fonction RelocateCenter nous permet de faire en sorte que les balles ne fusionnent pas.

![image](https://user-images.githubusercontent.com/71375990/126194350-8f93a1a4-5bd6-44bc-b853-a4ef0bec2667.png)

Le code suivant signifie que si il y a une intersection entre deux balles on replace le centre des deux balles pour les empêcher de fusionner et on met leur vélocité à celle que nous avons calculé précédemment, grâce à une formule de math, -R qui est une constante qui représente l'énergie perdue lors du rebond.

![image](https://user-images.githubusercontent.com/71375990/126194507-77ea2daa-90d5-4c24-8311-92514429c5f7.png)

On obtient donc une simulation presque réaliste. Mais il y a un petit problème dans la programmation, en effet on calcule les collisions entre tous les cercles même si ils ne sont très clairement pas en collision ce qui fait très rapidement beaucoup de calculs et créer beaucoup de problèmes de collision.

Nous avons donc eu le choix entre régler ce problème grâce au space partitioning ou de rajouter toute sorte de polygone aux collisions.

J'ai choisi le space partitioning car je voulais que mes collisions marchent à 100%, le space partitioning consiste à couper le monde en une grille et de vérifier les collisions seulement entre objet étant dans le même carré, grâce à cela on baisse grandement le nombre de calcul à effectuer.
