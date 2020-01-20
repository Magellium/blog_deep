# deepLearning Magellium

Le blog est disponible ici: http://deeplearning.magellium.fr

# Ecrire un article

Ecrire un fichier en markdown dans le répretoire `_posts`.

Le nom du fichier **DOIT** commencer par la date !

Plus d'info [ici](https://jekyllrb.com/docs/posts/).

## Les drafts

Comme pour les articles, sauf que le fichier doit être dans le répertoire `_drafts`.

__Note__: ne sont pas visible sur le post officiel, mais uniquement sur la version interne.


## les tags

Pour ajouter un tag à un article il faut ajouter dans l'en-tête de l'article ceci:

```
---
layout: post
title: "un titre"
tags:
  - tag1
  - tag2
---
```


## les catégories

Les catégories sont un peu comme des tags, à la différence qu'il faut leur associer une page du nom de la catégorie pour les rendre visible 

```
---
layout: post
title: "un autre titre"
categories:
  - cat1
---
```

Ici il faudra créer le fichier `category/cat1.html` pour la rendre visible.

Cf le projet: https://github.com/fongandrew/hydeout

La page de la catégorie: https://fongandrew.github.io/hydeout/category/edge-case

Le code associé: https://github.com/fongandrew/hydeout/blob/master/category/edge-case.md


# Tester le rendu 

Dès que vous avez commit / push sur gitana, le site interne est mis à jour (à l'aide de gitlab-ci).

Vous pouvez donc vérifier le rendu sur le site interne


# Publier le blog

Vous avez vérifier le rendu sur le site interne ?
Alors vous pouvez publier.

Pour cela, allez sur la page du projet sur rubrique pipelines. Trouvez le dernier pipeline executé:

![le dernier pipeline](docs/pipeline_1.png).

Lancez la publication manuelle vers github:

![publication manuelle](docs/pipeline_2.png)


# Archi

Le blog utilise [Jekyll](https://jekyllrb.com/) avec le template [HydeOut](https://github.com/fongandrew/hydeout).

* Le code est hébergé en interne à Magellium.
* On utilise `gitlab-ci` pour générer le site web à partir du code.
* le résultat du build (et uniquement le résultat, pas le code) est publié sur [github](https://github.com/Magellium/blog_deep).
