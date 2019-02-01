---
id: deploy-app-store-archive-and-upload
title: Archiver et télécharger un projet
sidebar_label: Archiver et télécharger un projet
---
<div class = "objectives"> 

**OBJECTIFS**

* Archiver et publier votre projet sur l'App Store Connect</div> 

## ÉTAPE 1. Configurez Xcode

* Si vous avez choisi un compte Apple Developer, celui-ci est immédiatement disponible. 
* Si vous avez choisi un compte de développeur Apple en tant qu’entreprise, vous devez attendre la validation d’Apple.
* Lorsque votre compte est accessible, ajoutez-le à Xcode dans Preferences > Accounts.
* Xcode installera automatiquement les certificats et les éléments de provisioning nécessaires. 

## ÉTAPE 2. Obtenez votre Team ID

* Connectez-vous à votre compte de développeur Apple. Vous trouverez votre Team ID dans Membership.

![Obtenez votre Team ID](assets/deploy-in-house/Team-ID-4D-for-iOS.png)

## ÉTAPE 3. Configurez 4D for iOS

* Lancez 4D for iOS

* Dans l’onglet SECTIONS :

**Général : Entrez votre Team ID**

![Team ID](assets/deploy-app-store/Team-ID.png)

**Publication : Entrez votre URL de production**

(HTTPS est obligatoire pour le déploiement).

![Publishing](assets/deploy-app-store/Publishing.png)

* Dans l’onglet GÉNÉRATION :

**Créer et exécuter : Créez votre projet**

![BuildTab](assets/deploy-app-store/BuildTab.png)

## ÉTAPE 4. Ouvrez votre projet avec Xcode

* À partir de l’onglet GÉNÉRATION de l'éditeur de projet, cliquez sur Projet > Ouvrir le produit avec Xcode

![Ouvrez votre projet avec Xcode](assets/deploy-in-house/Open-your-project-Xcode-4D-for-iOS.png)

## ÉTAPE 5. Archivez votre projet à partir de Xcode

* À partir de Xcode, accédez au Menu du simulateur et sélectionnez **Generic iOS Device**.

![Generic iOS Device](assets/deploy-in-house/Deployment-Generic-iOS-Device.png)

* Puis, dans le menu, cliquez sur Product et sélectionnez **Archive**

![Archivez votre projet à partir de Xcode](assets/deploy-in-house/Archive-your-Project.png)

## ÉTAPE 6. Validez votre projet

* À la fin de l’archivage, la fenêtre de l’organisateur apparaît avec l’archive que vous venez de créer.

* Cliquez sur le bouton **Validate** pour démarrer le processus de validation.

![Validez votre projet](assets/deploy-app-store/Organizer-Project-Validation.png)

* La première étape consiste à sélectionner les options de distribution de l'App Store.

![App Store distribution options](assets/deploy-app-store/App-Store-Distribution-options.png)

* Vous devez ensuite re-signer votre application. Laisser à Xcode le soin de gérer cette étape en cochant l'option **Automatically manage signing**.

![Re-sign your app](assets/deploy-app-store/Re-sign-your-App.png)

* Revoyez le contenu de votre application.

![App review](assets/deploy-app-store/Review-App.png)

* Si votre projet réussit le processus de validation, le message suivant devrait s'afficher :

![Validation](assets/deploy-app-store/Archive-validation-complete.png)

Si une erreur se produit, un message s’affichera. Ces erreurs doivent être corrigées avant de recommencer le processus de validation.

* Cliquez sur **Done**. Cela vous renverra à la fenêtre de l’organisateur.

## ÉTAPE 7. Téléchargez sur l’App Store

Une fois la validation terminée, vous êtes prêt à ajouter votre application sur l’App Store.

* Cliquez sur le bouton **Upload to App Store**.

![Téléchargez sur l’App Store](assets/deploy-app-store/Upload-to-AppStore.png)

* Lorsque votre projet a été téléchargé avec succès, vous verrez cette fenêtre s'afficher :

![Upload successful](assets/deploy-app-store/upload-Successful.png)

## ÉTAPE 8. Sélectionnez la version destinée à l’App Store

* Depuis l’App Store Connect > App Store > iOS App, sélectionnez votre application et cliquez sur le bouton **+** qui apparaît dans la section Build

![Add build](assets/deploy-app-store/Add-build-app-store-connect.png)

* Sélectionnez la version que vous souhaitez envoyer et cliquez sur **Done**.

![Build selection](assets/deploy-app-store/Select-build-app-store-connect.png)

* Enfin, cliquez sur le bouton **Submit for Review**.

## ÉTAPE 9. Envoyez pour révision

* La dernière étape consiste à répondre à quelques questions relatives à votre application. 

![Envoyez pour révision](assets/deploy-app-store/Export-Compliance-Content-Rights-Advertising-Identifer.png)

* Une fois l'étape des réponses aux questions terminée, cliquez sur **Submit**.

* En moyenne, la durée de révision d'App Store est de deux jours !