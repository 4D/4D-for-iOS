---
id: storyboard-detailform-template
title: Storyboard
---
Il est temps de créer votre interface iOS de formulaire détaillé avec Xcode !

Voici le résultat que nous souhaitons obtenir :

![Storyboard custom detailform](assets/custom-detailform/storyboard-custom-detailform.png)

Pour chaque cellule, nous allons ajouter :

* Une photo de profil dans l'en-tête 
* Un champ à dupliquer

## Ouvrir le fichier storyboard avec Xcode

Dans un premier temps, ouvrez votre fichier storyboard dans Xcode.

![Empty storyboard custom template](assets/custom-detailform/empty-storyboard-custom-detailform-template.png)

Il est assez vide, nous allons donc y ajouter du contenu !

## Ajouter une "Scroll View"

Pour que notre formulaire détaillé soit déroulant, la première étape consiste à faire glisser et déposer une « Scroll View » (vue de défilement) depuis la **Bibliothèque d'objets**.

![Add Scroll View Storyboard](assets/custom-detailform/add-scrollview-storyboard.png)

A partir du **Size inspector** (sur le côté droit de l’Interface Builder), définissez la largeur de la Scroll vue à 359 et la valeur de sa hauteur à 667. Définissez ensuite la valeur de X sur 8 et la valeur de Y sur 0.

![Scroll View position height and width](assets/custom-detailform/scrollview-position-height-width.png)

Ajoutez ensuite quatre contraintes en cliquant sur le bouton **Add New Constraints** (Trailing: 8, Leading: 8, Top: 0, et Bottom: Multiple) comme suit :

![Scrollview Constraints](assets/custom-detailform/scrollview-constraints.png)

## Ajouter une "Vertical Stack View"

Glissez et déposez un "Vertical Stack View" depuis la **bibliothèque d'objets** vers la "Scroll view". A partir du **Size inspector** (sur le côté droit de l’Interface Builder), définissez ensuite la largeur de la vue sur 359 et la valeur de la hauteur sur 202. Enfin, définissez la valeur de X sur 0 et la valeur de Y sur 8.

![Add stackview Storyboard](assets/custom-detailform/add-vertical-stackview-storyboard.png)

La hauteur et la largeur de Stack View étant définies par les éléments qu'elle contient, nous allons configurer les dimensions et les contraintes plus tard.

## Ajouter des vues au Stack Views

Glissez et déposez une vue depuis la **bibliothèque d'objets** vers la Stack View que vous venez d’ajouter à votre Storyboard. Nommons-la **Field View 1**.

![Add Field View 1](assets/custom-detailform/add-view1-storyboard.png)

Faites ensuite glisser directement une autre vue depuis la **bibliothèque d'objets** et déposez-la dans le Document Outline au même niveau que Field View 1 (pour l’intégrer à la Stack View) et nommez-la **Field View 2**.

![Add Field View 2](assets/custom-detailform/add-view2-storyboard.png)

Pour ajouter des espaces entre les vues, sélectionnez votre Stack View et affectez-lui une valeur d’espacement de 8 (dans l’Attributes Inspector).

![Stackview spacing](assets/custom-detailform/stackview-spacing.png)

Sélectionnez **Field View 1** et **Field View 2** et définissez, dans le **Size inspector** (à droite de l'Interface Builder), la valeur de la largeur sur 359 et celle de la hauteur à 97.

![views position height and width](assets/custom-detailform/views-position-height-width-storyboard.png)

Sélectionnez **Field View 1** et ajoutez trois contraintes en cliquant sur le bouton **Add New Constraints button** (Trailing: 0, Leading: 0, et Top: 0) :

![Field Views constraints](assets/custom-detailform/fieldView-1-Field-View-2-constraints.png)

Pour que Stack View et Scroll View soient de la même largeur, vous devez ajouter une contrainte :

Press Ctrl and drag the Stack View to the Scroll View. When you release the mouse button, the Interface Builder displays a menu with a list of possible constraints. Choose Equal Width!

![Stack View Equal Width](assets/custom-detailform/stackview-equal-width-scrollview.png)

Next, with the Stack View selected add four constraints by clicking on the **Add New Constraints button** (Trailing: 0, Leading: 0, Top: 8, and Bottom: 0) as shown below:

![Stackview constraints](assets/custom-detailform/stackview-constraints.png)

Here's what you'll see when constraints have been added :

![Stackview final constraints](assets/custom-detailform/stackview-constraints-final.png)

Now that you have two views in your Stack View and you've defined constraints, let's focus on Field View 1.

## Ajoutez une Image View au Field View 1

From the **Object library**, drag and drop an **Image View** into Field View 1.

![Add Image View storyboard](assets/custom-detailform/add-imageview-storyboard.png)

In the **Size inspector panel** (on the right side of the Interface Builder window), set the Image View Width value to 359 and the Height value to 97. Then set the X value to 0 and the Y value to 0.

![Image View position height and width](assets/custom-detailform/imageview-position-height-width.png)

Next, add four constraints by clicking on the **Add New Constraints button** (Trailing:0, Leading:0, Top:0, and Bottom:0) as shown below:

![Image View constraints](assets/custom-detailform/imageview-constraints.png)

In the **Size inspector panel** change the Intrinsic Size from **Default** to **Placeholder**.

![Intrinsic size Image View](assets/custom-detailform/intrinsic-size-imageview.png)

## Ajouter des libellés au Field View 2

### Libellé Titre

In the **Object library**, drag and drop a **Label** into Field View 2 and set the Width value to 343 and the Height value to 22. Then set the X value to 8 and the Y value to 8.

![Add label](assets/custom-detailform/add-label1-storyboard.png)

Double click on the label and name it "```___FIELD_LABEL___```". Then in the **attribute inspector** set the font to **Helvetica Neue Light 18.0** and the color to **BackgroundColor**:

![Title label font and color](assets/custom-detailform/title-label-font-and-color.png)

### Libellé Contenu

Duplicate the Title label and set the duplicate's Width value to 339 and the Height value to 44. Then set the X value to 12 and the Y value to 37.

![Add label](assets/custom-detailform/add-label2-storyboard.png)

Double click on the label and name it "```<___FIELD_LABEL___>```". Then from the **attribute inspector** set the font to **Helvetica Neue Light 20.0** and the color to **Black Color**:

![Content label font and color](assets/custom-detailform/content-label-font-and-color.png)

Select the Content and Title labels and add four contraints by clicking on the **Add New Constraints button** (Trailing: 8, Leading: Multiple, Top: Multiple, and Bottom: Multiple) as shown below:

![Title and Content labels constraints](assets/custom-detailform/titlelabel-contentlabel-contraints.png)

You're done with graphical elements! All of your constraints are well defined :)

## Comment entrer des données dans vos cellules

### Image View

Select your Image View and go to **Identity inspector** > User Defined Runtime Attributes. Click the **+ button** to add a row.

![User defined runtime attributes](assets/custom-detailform/user-defined-runtime-attributes.png)

* **Key Path**: Start with bindTo to activate binding on the component. Enter ```bindTo.record.___FIELD_1___```
* **Type**: Always ```String``` 
* **Value**: The attribute name. Enter ```___FIELD_1_BINDING_TYPE___```

![Identity inspector storyboard](assets/custom-detailform/identity-inspector-storyboard.png)

### Libellés

For the **first label** we are going to add several lines mainly to display icons:

![Label1 User Defined Runtime Attributes](assets/custom-detailform/label1-user-defined-runtime-attributes.png)

You also need to set the Class to ```IconLabel``` and check the **Inherit Module From Target** checkbox as we can see below:

![Label1 Custom Class](assets/custom-detailform/label1-custom-class.png)

Select the **second label** and add a row in the Defined Runtime Attributes:

* **Key Path **: ```bindTo.record.___FIELD___```
* **Type**: ```String``` 
* **Value**: ```___FIELD_BINDING_TYPE___```

![Label2 User Defined Runtime Attributes](assets/custom-detailform/label2-user-defined-runtime-attributes.png)

## Ajouter des TAGS aux cellules dupliquées

Field View 2 includes elements that will be duplicated so you can have as many field as you define in the project editor.

Each storyboard element has a Object ID. For example, if you select Field View 2 and go to the **Identity inspector**, you'll see its Object ID:

![Object ID Storyboard](assets/custom-detailform/object-id-storyboard.png)

In order to tell the project editor that all of the elements included in this view will be duplicated, we need to add TAG to each element and constraints.

The process is a little bit tricky... Let's begin by opening the storyboard file with your favorite code editor!

### Field View 2

* Select **Field View 2** and get its Object ID from the Identity Inspector (on the right side of the Interface Builder window). In our project, Field View 2 ID is: **SiX-3H-lNB**.

* Search for this ID in the storyboard xml code and replace it with **TAG-FD-001** each time it appears. As you can see, this Object ID is mentioned several times so be careful!

![Storyboard xml](assets/custom-detailform/storyboard-xml.png)

Save the storyboard xml file. As you can see, the Field View 2 Object ID has changed in your storyboard in Xcode:

![Field View 2 Object ID](assets/custom-detailform/field-view-2-object-id.png)

### Premier libellé

* Now, get the **first label** Object ID from the Identity Inspector and replace it with **TAG-FD-002** each time it appears in the storyboard xml code.

![Label 1 Object ID](assets/custom-detailform/label1-object-id.png)

Done with the first label!

### Deuxième libellé

* Next, get the **second label** Oject ID from the Identity Inspector and replace it with **TAG-FD-003** each time it appears in the storyboard xml code.

![Label 2 Object ID](assets/custom-detailform/label2-object-id.png)

Voilà!

### Contraintes

Both labels have constraints that we need to tag, too:

![Tag constraints](assets/custom-detailform/duplicated-constraints.png)

Just like View Field 2 and label, get all **7 Constraints** Object IDs from the Identity Inspector and replace them with: **TAG-FD-004**, **TAG-FD-005**, **TAG-FD-006**, **TAG-FD-007**, **TAG-FD-008**, **TAG-FD-009** and **TAG-FD-010**.

Go to your project editor and select your detail template from the Forms section, then click on Build.

![Custom detail template forms](assets/custom-detailform/custom-detail-template-forms.png)

Not bad for a first attempt! :)

![iPhone Demo](assets/custom-detailform/iphone-demo.png)

Field View 2 is well duplicated! Let's see if we can make this app a bit more interesting!

### Personnaliser votre application

We're going to add a corner radius to the Image View, as well as Field View 2.

Select your Image View and add the two following lines in the User Defined Runtime Attributes:

* **Key Path**: ```cornerRadius```
* **Type**: ```Number``` 
* **Value**: ```12```

and

* **Key Path **: ```layer.masksToBounds```
* **Type **: ```Boolean``` 
* **Value**: Check the box

![iPhone Demo](assets/custom-detailform/imageview-corner-radius.png)

Next, select Field View 2 and add the following:

* **Key Path** : ```cornerRadius```
* **Type **: ```Number``` 
* **Value**: ```12```

![iPhone Demo](assets/custom-detailform/fieldview2-corner-radius.png)

You can now build your project from the project editor!

![Custom template final result](assets/custom-detailform/custom-template-final-result.png)

## Que faire ensuite ?

In this tutorial, we've covered the basics for creating detail form templates. You can now create simple templates on your own using the Starter Project resources. Click on **Final Project** below to download the completed template folder.

<div style="text-align: center; margin-top: 20px">
  <p>
    

<a class="button"
href="../assets/custom-detailform/CustomDetailFormFinalTemplate.zip">MODÈLE FINAL DE FORMULAIRE DÉTAILLÉ PERSONNALISÉ</a>

  </p>
</div>