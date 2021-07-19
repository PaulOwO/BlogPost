# Blog Post

Bienvenue sur le blog post technique de mon moteur de jeu réaliser lors de la deuxième partie du module GPR920 à la SAE Institute.
Lors de se blogpost je vais essayer de vous montrer se que le module ma apporté acompagné de quelque détails technique.

## Moteur de jeu

Nous avons tout d'abord commencé le projet par finir les dossiers vecteurs en rajoutant des "operators" qui nous permettent d'éffectuer le calcule désirer sans le réécrire à chause fois. Celà fut très important car les vecteurs furent utilisé du début à la fin du projet.

![image](https://user-images.githubusercontent.com/71375990/126193762-27c1256c-889e-44dd-9edb-7022630af686.png)
Un operator permettent d'aditionner les vecteurs entre eux.

Nous avons aussi pour la première fois découvert une partie cruciale de la programation et du travail en entreprise. En effet les Tests nous servent sur plusieurs points, ils nous aident à savoir si le programme nous donne le résultat désirer pour des exemples en particulier, puis aprés avoir déterminer quel partie du code il faut refaire ils sont d'une grande aide pour déboguer. De plus en entreprise ils sont les seules qui permetent de prouver que notre code fonctionner avant de le mettre en commun et qui donc si les tests ne passe plus après celà, se n'est pas notre faute. J'ai donc retenue que malgrés le temps suplémentaire que nous prennont à les mettres en place, les tests sont vraimment utiles et peuvent mêmes nous faire gagner du temps, il faut donc en faire à un maximum d'endroits possible.

![image](https://user-images.githubusercontent.com/71375990/126197453-4ffcef6e-e387-40e7-8024-83daf7ae00fb.png)

Test de taille et du centre de plusieurs rectangle.

Suite à celà nous avons de nombreuses structures de données accompagné de leurs calcules et tests.

![image](https://user-images.githubusercontent.com/71375990/126197506-d368858c-6582-4c30-98e1-f1ded191e594.png)

AABB entour les polygone d'un carré puis on les projettes en x et y pour voir si il ya contact.

Durant cette partie grâce à mes nombreuses questions je penses avoir améliorer mon niveau en c++, en géométrie et en math. J'ai aussi apris pour la première fois comment utilisé un matrice.

![image](https://user-images.githubusercontent.com/71375990/126194261-c032d48b-977e-4aee-afc6-a5223b808aa5.png)

Lors d'une deuxième partie nous avons reçu un programme qui pouvait déssiner des cercles qui tomber et nous avons pour objectif de les faires rebondire et avoir des collisions réaliste. Cette partie fût plus compliquer pour moi. Voici quelque exemple de code, la fontion RelocateCenter nous permet de faire en sorte que les balles ne fusionnent pas.

![image](https://user-images.githubusercontent.com/71375990/126194350-8f93a1a4-5bd6-44bc-b853-a4ef0bec2667.png)

Le code suivant signifie que si il ya une intersection entre deux balles on replace le centre des deux balles pour les empecher de fusionner et on met leur vélocité a celle que nous avons calculé précédemment grâce a un theore de math - R qui est une constante qui représente l'énergie perdu lors du rebond.

![image](https://user-images.githubusercontent.com/71375990/126194507-77ea2daa-90d5-4c24-8311-92514429c5f7.png)

On obtient donc une simulation presque réaliste. Mais il ya un petit problème dans la programation, en effet on calcule les collisions entre tout les cercles même si il ne sont trés clairement pas en collision se qui fai très rapidement beaucoup de calcul et créer beaucoup de problème de collision.

Nous avons donc eu le choix entre régler se problème grâce au space partitionnig ou de rajouter toute sorte de polygone au collsions.

J'ai choisi le space partitionnig car je voulais que mes collisions marche a 100%, le space partionning constiste à couper le monde en une gride et de vérifier les collisions seulement entre objet étant dans le même carré, grâce à celà on baisse grandement le nombre de calcul à effectuer.










## Welcome to GitHub Pages

You can use the [editor on GitHub](https://github.com/PaulOwO/BlogPost/edit/gh-pages/index.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/PaulOwO/BlogPost/settings/pages). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://support.github.com/contact) and we’ll help you sort it out.
