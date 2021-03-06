---
id: deploy-app-store-app-store-connect
title: Criar uma ficha em App Store
---

<div class = "objectives"> 

**OBJECTIVES**

* Create an App ID on your Developer Account
* Create your app in App Store Connect</div> <div class = "prerequisites"> 

**PREREQUISITES**

[Apple Developer Program for organization](register-apple-developer-program-organization.html) or [individual](register-apple-developer-program-individual.html)</div> 

## PASSO 1. Criar uma ID de aplicação

#### O que é uma identificação (ID) de aplicação?

*An App ID is a two-part string used to identify one or more apps from a single development team. The string consists of a Team ID and a Bundle ID, with a period (.) separating the two parts (ex: TeamID.BundleID).*<div class = "tips"> 

**NOTA **

* If you have chosen an Apple Developer Account as an individual, your account is available immediately and you can create your App ID.
* If you have chosen an Apple Developer Account as an organization, you must wait for Apple validation to create your App ID.</div> 

To create your App ID, go to your developer account and select [Certificates, IDs & Profile](https://developer.apple.com/account/ios/identifier/bundle)

* Clique no símbolo + do lado de *Register iOS App IDs* para agregar um novo identificador de aplicação.

* Defina o nome e Bundle ID de sua aplicação.

![App ID](assets/en/deploy-app-store/Developer-account-App-ID.png)

* Defina os App Services para incluir à sua aplicação

![App Services](assets/en/deploy-app-store/App-Services-to-include.png)

* Confirme a identificação de aplicação clicando em **Register**.

![Confirm App ID](assets/en/deploy-app-store/Confirm-App-ID.png)

## PASSO 2. Inicie a sessão na App Store Connect

* Inicie a sessão na sua [Conta App Store Connect](https://appstoreconnect.apple.com)
* Clique em **My Apps**.

![App Store Connect](assets/en/deploy-app-store/App-Store-Connect-home-page.png)

## PASSO 3. Crie uma nova aplicação iOS

Click the **+** sign in the top left corner to create a new iOS App.

![Crie uma nova aplicação iOS](assets/en/deploy-app-store/Create-new-iOS-App.png)

Add the following information:

* **Platforms**: Selecione iOS.
* **Name**: o nome da aplicação.
* **Primary language**: o idioma principal de sua aplicação.
* **Bundle ID**: Selecione a Bundle ID de sua apicação a partir da lista suspensa.
* **SKU**: Uma identidade única para sua aplicação (isso permanece privado e não pode ser visto pelos usuários)
* **Limit User Access (opcional)**: Permite que limite o acesso à sua aplicação para os usuários com funções de Administração, Desenvolvedor, Comercial ou Vendas.

![Change BundleID](assets/en/deploy-app-store/Change-BundleID-Xcode-Project.png)<div class = "tips"> 

**NOTA **

If your Bundle ID is not available, it may already be used by another app in the App Store. You'll need to change yours in your Xcode project.</div> 

## PASSO 4. Informação sobre a aplicação

From App Store Connect > App Information:

* Define a Privacy Policy URL de sua aplicação (opcional).
* Digite um subtítulo para sua aplicação. Isso vai aparecer abaixo do nome de sua aplicação na App Store em iOS 11.
* Selecione uma categoria primária e secundária (opcional) na qual sua aplicação vai aparecer.

![Informação sobre a aplicação](assets/en/deploy-app-store/App-Store-Connect-app-information.png)

## PASSO 5. Preços e disponibilidade

This is where you define the price for your app.<div class = "tips"> 

**DICAS**

You can define limited-time discounts by specifying start and end dates.</div> 

## PASSO 6. Prepare para a inscrição

Add all of the assets for your app to appear in the App Store in **Version Information**:<div class = "tips"> 

**DICAS**

You can generate all of your screenshots in Simulator (File > New Screen Shot).</div> 

![Prepare para a inscrição](assets/en/deploy-app-store/Prepare-for-submission-screenshot-description.png)

* Agregue suas capturas de tela. Capturas de tela para iPhone 5,5" Super Retina Display e iPad 12.9" Retina Display são obrigatórias. Para maiores detalhes, veja [Screenshot specifications](https://help.apple.com/app-store-connect/#/devd274dd925).

* Role a tela para baixo e defina as palavras chaves **Keywords** e complete a **Description** (Isso é o que os usuários verão na App Store).

* Pode compartir atualizações de sua aplicação, incluídas novas promoções ou funcionalidades ou conteúdo, ofertas por tempo limitado, ou outros eventos dentro de sua aplicação adicionando um **Promotional Text** que aparece acima da sua descrição na App Store (para clientes com dispositivos com iOS 11 ou posterior).
* Insira uma **Support URL** que inclua informação de assistência ténica para sua aplicação. Esta URL vai ser visível na App Store.
* **Marketing URL** é opcional. Isso pode dirigir aos usuários a um website de marketing para sua aplicação. 

In the **iOS App section**:

![iOS App section](assets/en/deploy-app-store/Prepare-for-submission-build-icon.png)

Locate your build versions in **Build**.

* Na área **General App Information** ingresse os direitos de autor, a versão e informação de contato de sua aplicação.
* O ícone de sua aplicação é incluído no projeto gerado 4D para iOS.
* A classificação etária ou rating é uma propriedade usada para os controles parentais de App Store. Clique Edit e selecione a faixa etária apropriada para sua aplicação.

The **App Review Information** and **Version Release** sections include information required by the App Store. The information provided here will not be seen by users.

![App Review Information](assets/en/deploy-app-store/Prepare-for-submission-review-information.png)

* **App Review Information**: Informações confidenciais de contato e de segurança. 
* **Version Release**: especifica uma publicação automática ou manual.
* Finalmente, clique **Save**.