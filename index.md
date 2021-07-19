# Blog Post

Bienvenue sur le blog post technique de mon moteur de jeu réaliser lors de la deuxième partie du module GPR920 à la SAE Institute.
Lors de se blogpost je vais essayer de vous montrer se que le module ma apporté acompagné de quelque détails technique.

## Moteur de jeu

Nous avons tout d'abord commencé le projet par finir les dossiers vecteurs en rajoutant des "operators" qui nous permettent d'éffectuer le calcule désirer sans le réécrire à chause fois. Celà fut très important car les vecteurs furent utilisé du début à la fin du projet.

Nous avons aussi pour la première fois découvert une partie cruciale de la programation et du travail en entreprise. En effet les Tests nous servent sur plusieurs points, ils nous aident à savoir si le programme nous donne le résultat désirer pour des exemples en particulier, puis aprés avoir déterminer quel partie du code il faut refaire ils sont d'une grande aide pour déboguer. De plus en entreprise ils sont les seules qui permetent de prouver que notre code fonctionner avant de le mettre en commun et qui donc si les tests ne passe plus après celà, se n'est pas notre faute. J'ai donc retenue que malgrés le temps suplémentaire que nous prennont à les mettres en place, les tests sont vraimment utiles et peuvent mêmes nous faire gagner du temps, il faut donc en faire à un maximum d'endroits possible. : mettre exemples


Suite à celà nous avons de nombreuses structures de données accompagné de leurs calcules et tests. Comme par exemple les rectangles et AABB qui sert a déterminer si deux polygones sont en contact : mettre exemple.

Durant cette partie grâce à mes nombreuses questions je penses avoir améliorer mon niveau en c++, en géométrie et en math. J'ai aussi apris pour la première fois comment utilisé un matrice exemple cramer.

Lors d'une deuxième partie nous avons reçu un programme qui pouvait déssiner des cercles qui tomber et nous avons pour objectif de les faires rebondire et avoir des collisions réaliste. Cette partie fût plus compliquer pour moi. Voici quelque exemple de code : la fontion RelocateCenter nous permet de faire en sorte que les balles ne fusionnent pas .

se code signifie que si il ya une intersection entre deux balles on replace le centre des deux balles pour les empecher de fusionner et on met leur vélocité a celle que nous avons calculé précédemment grâce a un theore de math - R qui est une constante qui représente l'énergie perdu lors du rebond.

On obtient donc une simulation presque réaliste. Mais il ya un petit problème dans la programation, en effet on calcule les collisions entre tout les cercles même si il ne sont trés clairement pas en collision se qui fai très rapidement beaucoup de calcul et créer beaucoup de problème de collision.

Nous avons donc eu le choix entre régler se problème grâce au space partitionnig ou de rajouter toute sorte de polygone au collsions.

J'ai choisi le space partitionnig car je voulais que mes collisions marche a 100%, le space partionning constiste à couper le monde en une gride et de vérifier les collisions seulement entre objet étant dans le même carré, grâce à celà on baisse grandement le nombre de calcul à effectuer.

![Image](https://github.com/PaulOwO/BlogPost/blob/gh-pages/assets/css/1.png)





















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
