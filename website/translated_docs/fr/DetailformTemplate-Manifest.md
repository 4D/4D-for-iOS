---
id: manifest-detailform-template
title: Manifest.json
---
Le fichier manifest contient des informations sur votre modèle de formulaire détaillé, telles que le **type de Storyboard** (formulaire liste ou formulaire détaillé), **le nom**, **le nombre de champs statiques** et **les propriétés de l'icône**.

    {
    //1
      "type": "detailform",
    
    //2
      "name": "Custom Detail form",
    
    //3
      "fields": {
        "count": 1
           },
    
    //4
      "assets": {
        "size": {
          "width": 16,
          "height": 16
        }
      }
    }
    
    

Par exemple, le fichier manifest du modèle de formulaire détaillé ci-dessous inclut les informations suivantes :

1. **Type de Storyboard :** detailform
2. **Nom du modèle :** Custom Detail form
3. **Nombre de champs :** un champ statique et 0 pour les champs dupliqués infinis (une image d'en-tête et des champs dupliqués)
4. **Propriétés de l'icône :** largeur et hauteur de l'icône