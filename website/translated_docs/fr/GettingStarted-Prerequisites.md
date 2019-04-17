---
id: prerequisites
title: Conditions préalables
---
## Configuration logicielle requise

* 4D Developer Pro v17 R2 64 bits (développement)
* 4D Server v17 R2 64 bits (déploiement) 
* [Apple configurator 2](https://itunes.apple.com/us/app/apple-configurator-2/id1037126344) installé sur votre Mac (facultatif). 

Apple configurator 2 nécessite **macOS 10.14** ou une version plus récente. Installez ce logiciel si vous souhaitez installer votre application automatiquement sur votre appareil.

Xcode 10.2 nécessite **macOS 10.14** ou une version plus récente.

## Tableau de comparaison des versions

| Xcode | Swift | iOS      | 4D   |
| ----- | ----- | -------- | ---- |
| 10.2  | 4.2.1 | iOS 12.2 | 17R5 |
| 10.1  | 4.2.1 | iOS 12   | 17R4 |
| 10.0  | 4.2   | iOS 12   | 17R3 |
| 9.4   | 4.1.2 | iOS 11.4 | 17R2 |
| 9.3.1 | 4.1   | iOS 11.3 | 17R2 |

### Utilisation de 17R4 avec Xcode 10.2

En raison de l’instabilité de l'ABI dans le langage Swift d'Apple, vous ne pouvez pas utiliser la version standard 4D 17R4 avec Xcode 10.2.

Heureusement, nous vous proposons un composant de substitution compatible avec Xcode 10.2.

Vous pouvez remplacer le composant interne de l’utilisateur `4D App.4dbase Mobile`, qui se trouve dans `... /4D.app/contents/Resources/Internal User Components/`, par celui que nous vous proposons :

<a class="button"
href="https://download.4d.com/Products/Current/4D_v17R4/4D%20Mobile%20App%20-%20Xcode%2010.2/4D%20Mobile%20App.4dbase.zip">4D Mobile App.4dbase.zip</a>

## Configuration matérielle requise

* 8 Go de RAM (Minimum recommandé)

## Configuration 4D

* Dans les propriétés de la base de 4D, affichez la page de compatibilité et cochez la case **Utiliser la notation objet pour accéder aux propriétés des objets (Unicode nécessaire).**

![Utilisation de la notation objet](assets/en/prerequisites/Use-object-notation.png)

* Les ports HTTP et HTTPS doivent être correctement configurés. Le port HTTPS est obligatoire pour le déploiement de 4D for iOS.

![Configuration Web](assets/en/prerequisites/Web-Configuration.png)

* Votre serveur Web doit être lancé. Il est accessible depuis le menu Exécution :

![Démarrage du serveur web](assets/en/prerequisites/Start-web-server.png)