---
id: storyboard-listform-template
title: Storyboard
---
Il est temps de créer votre interface iOS de formulaire Liste avec Xcode !

Voici le résultat que nous souhaitons obtenir :

![Storyboard custom listform](assets/custom-listform/storyboard-custom-listform.png)

Pour chaque cellule, nous allons ajouter :

* Une photo de profil
* Un titre 
* Un sous-titre

## Ouvrir le fichier storyboard avec Xcode

Dans un premier temps, ouvrez votre fichier storyboard dans Xcode.

![Empty storyboard custom template](assets/custom-listform/empty-storyboard-custom-template.png)

Il est assez vide, nous allons donc y ajouter du contenu !

## Ajouter une vue image

A partir de l'**Object library** (la bibiliothèque d'objets), glissez et déposez un **Image View** (une vue d'image) dans une cellule. Vous pouvez rechercher une « Image View » dans la barre de recherche en bas de la bibliothèque d’objets.

![Add Image View storyboard](assets/custom-listform/add-imageview-storyboard.png)

A partir du **Size inspector** (sur le côté droit de l’Interface Builder), définissez la largeur de la vue de l’image à 110 et la valeur de sa hauteur à 110. Définissez ensuite la valeur de X sur 8 et la valeur de Y sur 3.

![Image View position height and width](assets/custom-listform/imageview-position-height-width.png)

Puis, ajoutez une contrainte (Leading : 8) en cliquant sur **Add New Constraints** (en bas de l’Interface Builder). Ajoutez également des contraintes de largeur et hauteur, comme suit :

![Image View leading space width height](assets/custom-listform/imageview-leading-space-width-height.png)

Enfin, cliquez sur le bouton **Align** (dans la partie inférieure de l'nterface Builder) et cochez la case "Vertically in Container".

![Image View align vertically](assets/custom-listform/imageview-align-vertically.png)

Votre vue d'image est maintenant bien placée !

![Image View final](assets/custom-listform/imageview-final.png)

Nous allons nous pencher maintenant sur les libellés de cellules.

## Ajouter des libellés de titre et de sous-titre

Nous allons commencer par **ajouter une vue**. Vous pouvez rechercher le terme « View » dans la **bibliothèque d'objets** et faire glisser la vue vers la cellule.

![Add View Storyboard](assets/custom-listform/add-view-storyboard.png)

A partir du **Size inspector** (sur le côté droit de l’Interface Builder), définissez la largeur de la vue de l’image sur 277 et la valeur de sa hauteur sur 94. Définissez ensuite la valeur de X sur126 et la valeur de Y sur 10.

![View position height and width](assets/custom-listform/view-position-height-width.png)

Concernant la vue d'image, ajoutez quatre contraintes en cliquant sur le bouton **Add New Constraints** (Trailing: 11, Leading: 8, Top: 11, and Bottom: 10.67) pour la positionner correctement, comme suit :

![View contraints Storyboard](assets/custom-listform/view-constraints-storyboard.png)

Glissez et déposez un libellé dans le "View" que vous venez d’ajouter à partir de la bibliothèque d’objets.

![Add label Storyboard](assets/custom-listform/add-label-storyboard.png)

A partir du **Size inspector**, définissez la largeur du libellé View sur 269 et sa valeur de hauteur sur 32. Définissez ensuite la valeur de X sur 8 et la valeur de Y sur 8.

**Dupliquez le libellé** et, dans le **Size inspector**, définissez la valeur de X sur 8 et la valeur de Y sur 48.

![Duplicate the label](assets/custom-listform/duplicated-label-storyboard.png)

Sélectionnez les deux labels et ajoutez quatre contraintes en cliquant sur le bouton **Add New Constraints** (Trailing: 0, Leading: 8, Top: 8, and Bottom: Multiple) comme suit :

![Labels contraints storyboard](assets/custom-listform/labels-contraints-storyboard.png)

Avec un libellé sélectionné, double-cliquez sur **Height constraint** pour le modifier.

![Label height constraint edition](assets/custom-listform/label-height-constraint-edition.png)

Remplacez la relation "Equal" par **Greater Than or Equal** afin que sa hauteur soit variable (pour gérer des libellés multilignes).

![Change relation label height constraint](assets/custom-listform/change-relation-label-height-constraint.png)

Répétez l’opération pour le deuxième libellé.

## Personnaliser le libellé

A partir de l’Attribute inspector (sur le côté droit de l’Interface Builder), vous pouvez personnaliser les couleurs de police du libellé. Appliquons la couleur **Dark Grey Color** au deuxième libellé :

![Label color dark grey](assets/custom-listform/label-color-dark-grey.png)

Vous pouvez également sélectionner la couleur principale de votre application :

![Label color background color](assets/custom-listform/label-color-background-color.png)

A partir de l’Attribute inspector, vous pouvez également personnaliser la police. Sélectionnez les deux libellés et sélectionnez Font > Custom > **Helvetica Neue** :

![Label font custom](assets/custom-listform/label-font-custom.png)

Pour finaliser les personnalisations, sélectionnez les deux libellés et, dans la fenêtre Inspector, **entrez la valeur 0 dans Lines**. Ainsi, le nombre de lignes peut être illimité.

![Label lines number](assets/custom-listform/label-lines-number.png)<div class = "tips"> 

**NOTE**

Le Storyboard qui vous a été fourni est optimisé pour que la **hauteur de cellule soit variable** en fonction du contenu de chaque cellule.

![Row height tableview cell](assets/custom-listform/row-height-tableview-cell.png)</div> 

## Comment entrer des données dans vos cellules

### Image View

Sélectionnez votre Vue Image, cliquez sur **Identity inspector** et allez dans User Defined Runtime Attributes. Cliquez sur le **bouton +** pour ajouter une ligne.

![User defined runtime attributes](assets/custom-listform/user-defined-runtime-attributes.png)

* **Key Path**: Commencer avec "bindTo" pour l'associer au composant. Entrez ```bindTo.record.___FIELD_1___```
* **Type **: Toujours ```String``` 
* **Value **: Le nom de l’attribut. Entrez ```___FIELD_1_BINDING_TYPE___```

![Identity inspector storyboard](assets/custom-listform/identity-inspector-storyboard.png)

### Libellés

Sélectionnez le premier libellé et ajoutez une ligne dans la zone "Defined Runtime Attributes" :

* **Key Path **: ```bindTo.record.___FIELD_2___```
* **Type **: ```String``` 
* **Value **: ```___FIELD_2_BINDING_TYPE___``` ![Field 2 Binding](assets/custom-listform/field-2-binding.png)

Sélectionnez le deuxième libellé et ajoutez une ligne dans la zone "Defined Runtime Attributes" :

* **Key Path **: ```bindTo.record.___FIELD_3___```
* **Type **: ```String``` 
* **Value **: ```___FIELD_3_BINDING_TYPE___``` ![Field 3 Binding](assets/custom-listform/field-3-binding.png)

Pour avoir une meilleure visibilité, vous avez la possibilité de modifier les **libellés du storyboard** :

* Double-cliquez sur le premier libellé pour le modifier et entrez ```___FIELD_2_LABEL___```
* Double-cliquez sur le deuxième libellé pour le modifier et entrez ```___FIELD_3_LABEL___```

![Storyboard label display names](assets/custom-listform/storyboard-label-display-name.png)

Ouvrez votre éditeur de projet, sélectionnez votre modèle de formulaire Liste depuis la section Formulaires, puis cliquez sur Créer & exécuter.

Voici le résultat du simulateur :

![Simulator result](assets/custom-listform/simulator-result.png)

## Personnaliser votre application

La dernière étape consiste à ajouter un rayon de bec à la vue d'image pour améliorer la conception.

Sélectionnez votre Vue Image et cliquez sur les deux lignes suivantes dans User Defined Runtime Attributes :

* **Key Path **: ```cornerRadius```
* **Type **: ```Number``` 
* **Value **: ```12```

et

* **Key Path **: ```layer.masksToBounds```
* **Type **: ```Boolean``` 
* **Value** : Cochez la case

![ImageView corner Radius](assets/custom-listform/imageview-corner-radius.png)

Vous pouvez désormais créer votre projet depuis l'éditeur de projet !

![Custom template final result](assets/custom-listform/custom-template-final-result.png)

## Que faire ensuite ?

Dans ce tutoriel, nous avons fait le tour des bases de la création de modèles de formulaires Liste. Vous êtes maintenant en mesure de créer vous-mêmes de simples modèles à l'aide des ressources du projet Starter. Mais ce n'est fini ! Dans le prochain tutoriel, vous apprendrez à créer des modèles de formulaires détaillés ! Cliquez sur le **Projet final** ci-dessous pour télécharger le dossier contenant la liste complète de modèles.

<div style="text-align: center; margin-top: 20px">
  <p>
    

<a class="button"
href="../assets/custom-listform/CustomListFormFinalTemplate.zip">MODÈLE FINAL DE FORMULAIRE LISTE PERSONNALISÉ</a>

  </p>
</div>