# Projet de création d'un générateur de citations en JavaScript

## Étapes:

### 1. Récupérer les éléments nécessaires:

- l'emplacement qui contient la citation.

- l'emplacement qui contient le nom de l'auteur.

- le bouton qui permet de générer une nouvelle citation.

### 2. Créer les variables utiles:

- [dernier] - contient l'index de la question actuellement affichée (par défaut, la citation affichée est la première du tableau, sa valeur est donc égale à 0).

- [nombreAleatoire] - contient le nombre aléatoire généré.

### 3. Détecter le clic du bouton _"Nouvelle Citation"_.

### 4. Générer un nombre aléatoire

- utiliser une boucle do...while pour cette étape. Ceci vous permettra de générer un nombre tant que ce dernier est égal au nombre de la variable dernier.

- Pour générer un nombre aléatoire avec JavaScript, il faut utiliser la fonction Math.random(). Le problème de cette fonction, c'est qu'elle génère un nombre à virgule (donc un flottant), entre 0 et 1. Nous, nous souhaitons un entier, entre 0 et 5 si nous avons 6 citations. Dans ce cas, il va falloir changer de fonctionnement !  
  Cette fonction genererNombreEntier(max), qui prend en paramètre le nombre d'éléments dans votre tableau de citations. N'hésitez pas à la réutiliser ! Cette fonction utilise la fonction Math.floor() qui renvoie le plus grand entier qui est inférieur ou égal à un nombre. Par exemple, si je fais Math.floor(5.8), elle me renvoie 5.  
  Ici, nous générons donc un nombre aléatoire, par exemple 0.7, que nous multiplions par notre nombre d'éléments. Si j'ai 6 éléments, j'ai donc 0.7 _ 6, ce qui fait 4.2. Ma fonction Math.floor() me retournera donc 4. Parfait : nous avons bien notre entier.  
   `function genererNombreEntier(max) {
  return Math.floor(Math.random() _ Math.floor(max));
  }`

### 5. Mettre à jour le contenu

Nous avons réussi à générer un nombre aléatoire non-utilisé par la précédente citation, il ne faut plus que :

- Stocker ce nombre dans la variable nombreAleatoire.

- Modifier le contenu de notre objet citation par la citation à l'index nombreAleatoire de notre tableau.

- Modifier l'auteur de notre objet auteur par l'auteur à l'index nombreAleatoire de notre tableau.
