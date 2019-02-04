---
id: customize-your-ios-app
title: Customize your 4D for iOS App
---
Vamos fazer algumas modificações de storyboard... do simples ao complexo.

![Final result](assets/customize-with-xcode/Simlator-Before-After-Xcode-4D-for-iOS.png)

## PASSO 1. Modificação de etiqueta simples

Vamos começar modificando a fonte e cor de uma etiqueta:

* Abra o arquivo *ContactDetailsForm.storyboard* da guia de navegação. 
* Clique na etiqueta do primeiro nome (você pode também selecionar o construtor de interfaces no painel esquerdo).
* Selecione o painel Inspetor de atributos da área de utilitário.

![Attributes inspector](assets/customize-with-xcode/Attributes-inspector-Xcode-4D-for-iOS.png)

* Altere a fonte da Helvetica Neue bold para Futura bold. 

![Attributes inspector font](assets/customize-with-xcode/Attributes-inspector-font-Xcode-4D-for-iOS.png)

* Você também pode alterar a cor da fonte no mesmo painel.

![Attributes inspector color](assets/customize-with-xcode/Attributes-inspector-color-Xcode-4D-for-iOS.png)

## PASSO 2. Mudar a posição de imagem de perfil

All 4D for iOS templates use constraints for the app's elements to be well displayed on all devices.

No arquivo *ContactDetailsForm.storyboard*, as etiquetas de imagem, nome e sobrenome são todos atualmente alinhados ao centro.

Vamos mudá-lo para aparecer assim:

![Simulator result](assets/customize-with-xcode/Simlator-Final-Xcode-4D-for-iOS.png)

Primeiro, alinhe verticalmente as imagens e arraste as etiquetas nome e sobrenome para a direita da imagem.

Em seguida, selecione a imagem e vá para o painel de atributos de tamanho da área de Utility. Altere o valor de X de 161.67 a 40.67 e o valor de Y de 28 a 79.

![Profil picture position](assets/customize-with-xcode/Profil-picture-position-Xcode-4D-for-iOS.png)

Como você pode ver, a posição foi alterada, mas o Xcode está exibindo linhas amarelas... por quê? These yellow lines represent constraints which are no longer valid.

## PASSO 3. Atualizar as restrições de imagens de perfil

Para alinhar verticalmente a imagem no centro no Superview (a visão que a contém), precisamos eliminar as restrições existentes e adicionar novas.

The image currently has the following constraints:

* Width Equals: A fixed width of 78 pixels.
* Height Equals: A fixed height of 78 pixels.
* Align Center X: Centers the image on a previously defined horizontal axis.
* Top Space: A fixed amount of space from the top of the image to the top of the view.
* Bottom space to <first name>: The previously defined space between the First Name label and the image.

![Profil picture constraints](assets/customize-with-xcode/Profil-picture-constraints-Xcode-4D-for-iOS.png)

Apague todas as restrições exceto Width e Height (você vai modificá-las depois na seção Restrições no Size Inspector). O outline de imagem deve estar agora em vermelho, porque as restrições estão faltando.

Clique no botão Alinhar (no fundo da janela Interface) e marque a checkbox **Vertically in Container**.

![Profil picture Align](assets/customize-with-xcode/Profil-picture-Align-Xcode-4D-for-iOS.png)

Depois clique no botão **Adicione Novas Restrições** e adicione uma restrição de espaço entre linhas impressas (restrição esquerda).

![Profil picture new constraints](assets/customize-with-xcode/Profil-picture-new-constraints-4D-for-iOS.png)

Nesse ponto, todas as restrições de imagem de perfil devem estar em azul.

Parabéns! Your profile picture is now well positioned with the correct constraints.<div class = "tips"> 

**DICAS**

* Para criar uma restrição entre dois modos de exibição, pressione Ctrl e arraste uma das vistas para o outro. Quando você soltar o botão do mouse, a Interface Builder exibe um menu com uma lista de possíveis restrições.

* Você pode excluir as restrições, ou selecioná-las a partir do Inspetor de tamanho ou do Interface Builder.</div> 

## PASSO 4. Atualizar posições de etiqueta e restrições

#### Agora, vamos trabalhar na etiqueta Nome.

We'll begin by changing the position and width:

* Select the First Name label from the Interface Builder.
* Next, change the Width from 386 to 267 pixels.
* Change the X value from 8 to 127 pixels and the Y value from 28 to 79 pixels.

![First Name Label position](assets/customize-with-xcode/First-Name-Label-position-Xcode-4D-for-iOS.png)

Modify the remaining constraints:

* Delete the leading and the bottom space constraints from the Size inspector.
* Add a leading space constraint by clicking on the **Add New Constraints** button to position the First Name label to the right of the Profile picture.
* Press Ctrl and drag the First Name label to the Profile picture. Select the top constraint in the menu to top align both elements.

![First Name Label top constraint](assets/customize-with-xcode/First-Name-Label-top-constraint-Xcode-4D-for-iOS.png)

#### Finalmente, vamos trabalhar na etiqueta do sobrenome.

Change the position and width:

* Select the Last Name label from the Interface Builder.
* Change the width from 386 to 267 pixels.
* Change the X value from 8 to 127 pixels and the Y value from 144.33 to 118.33 pixels.

![Last Name Label position](assets/customize-with-xcode/Last-Name-Label-position-Xcode-4D-for-iOS.png)

Modify the remaining constraints:

* Delete the leading space constraints from the Size inspector.
* Add a leading space and top constraints by clicking on the Add New Constraints button. 

![Last Name Label constraint](assets/customize-with-xcode/Last-Name-Label-constraint-Xcode-4D-for-iOS.png)

Ambas as etiquetas de nome agora são reposicionadas.

Vamos ver os resultados no simulador!

![Simulator result](assets/customize-with-xcode/Simulator-Xcode-4D-for-iOS.png)

Hmmmm. Não é exatamente o resultado que queríamos...

* Select the First Name and Last Name labels and change the alignment from center to left in the Attributes inspector. 

![Labels Alignment](assets/customize-with-xcode/Labels-Alignment-Xcode-4D-for-iOS.png)

* Next, select the Profile picture and double click on the leading space constraint.
* Change the Constant value from 40.67 to 80 pixels.

![Constraints adjustments](assets/customize-with-xcode/Constraints-adjustments-Xcode-4D-for-iOS.png)

Much better! Now all constraints are working and the labels aren't breaking other constraints.

As you can see, customizing your app is very simple!