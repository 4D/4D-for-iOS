---
id: one-to-many-relations
title: One to Many relations
---

This tutorial will show you how easy it can be to include One to Many relations in 4D for iOS.<div class = "tips"> 

**NOTA**

In this tutorial, we will use the relation names between your tables. Dar nombres de enlaces descriptivos, puede facilitar la definición de la estructura de su proyecto.</div> 

Comencemos descargando el Proyecto Starter:

<div style="text-align: center; margin-top: 20px; margin-bottom: 20px">
  <p>
    

<a class="button"
href="https://github.com/4d-for-ios/tutorial-OneToManyRelations/archive/c006015afeb0e134d872152f53b8cd5e4dcb59bb.zip">ONE TO MANY STARTER PROJECT</a>

  </p>
</div>

In this tutorial, we are going to build a colorful **Task app** using 4D for iOS.

![Task App Final result](assets/en/relations/4D-for-iOS-dark-mode-card-relation-ios-13.gif)

But first, let's have a look at the structure of our database:

![Select link from structure section](assets/en/relations/Database-1-to-N-relations-4D-for-iOS.png)

As you can see, there is a One to Many link named **tasks** that we will use in our iOS app to display the employees'(**One**) tasks(**to Many**).

Now, go straight to Open menu > Mobile project... to select *Time Keeper* and go to the **Structure section**.

## Structure section

You can see the **tasks relation** we have seen earlier... Publish it !

This will now operate as any other field for the rest of the app creation process.

![Structure section Relations properties](assets/en/relations/Structure-section-relations-4D-for-iOS.png)<div class = "tips"> 

**RECOMENDACIONES**

* On mouse over, a tip displays the table name originating the relation.</div> 

## Labels & Icons section

The One to Many relation is now available in the [Labels and Icons](labels-and-icons.html) section.

It is important to know that including a One to Many relation will create a button into the genrated iOS app.

So, in the Labels & Icons section you will define:

* a button Label
* a button icon
* a [title](one-to-n-relations-title-definition.html) that will be displayed in the destination view (to indicate where you come from for example).

![Labels & Icons section Relations properties](assets/en/project-editor/Relations-properties-Labels-icons-section-4D-for-iOS.png)

## Forms section

* Go to the Forms section and drop the *tasks* relation on the Employee Task Detail form.

![Related field in Forms section](assets/en/relations/1-to-n-relations-forms-section.png)

## Crear y ejecutar

1. From the Employee List form, click on one employee 
2. This will open the employee's detail form, where you should see a new **Relation button** !
3. Click on this Relation button to display the employee's tasks. 

![Related field in Forms section](assets/en/relations/One-to-n-relations-task-ios-app.png)

And voila, this is how One to Many relations work in 4D for iOS !

<div style="text-align: center; margin-top: 20px; margin-bottom: 20px">
  <p>
    

<a class="button"
href="https://github.com/4d-for-ios/tutorial-OneToManyRelations/releases/latest/download/tutorial-OneToManyRelations.zip">ONE TO MANY FINAL PROJECT</a>

  </p>
</div>