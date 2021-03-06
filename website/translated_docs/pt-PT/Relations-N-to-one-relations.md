---
id: many-to-one-relations
title: Relações Muitos para Um
---

4D v17 R5 inclui um novo conceito: as relações Muitos para Um (N a 1)<div class = "tips"> 

**NOTA **

In this tutorial, we will use the relation names between your tables. Dar nomes de relação bem descritivos ajuda a facilitar a definição de sua estrutura de projeto.</div> 

Vamos começar baixando o Projeto Starter:

<div style="text-align: center; margin-top: 20px; margin-bottom: 20px">
  <p>
    

<a class="button"
href="https://github.com/4d-for-ios/tutorial-ManyToOneRelations/releases/latest/download/tutorial-ManyToOneRelations.zip">MANY TO ONE STARTER PROJECT</a>

  </p>
</div>

Here we want to display the category for each task in the detail form of your generated app. To do so, open the **StarteriOSProject** from **Open > Mobile Project...**

Depois vá para a seção Estrutura e selecione a **tabela Task**.

### Structure section

* Pode verificar que a **relação TaskCategory** está sublinhado

* Ao clicar nele, serão mostrados os campos disponíveis através dessa relação.

* Selecione o **campo Name**

![Select link from structure section](assets/en/relations/select-link-from-structure.png)

* Este campo funcionará como qualquer outro campo durante o resto do processo de criação da aplicação

* Pode também filtrar seu conteúdo de app usando campos relacionados da seção Data. Para fazer isso digite ```TaskCategory.Name != 'Personal'``` no filtro de pesquisa para excluir as tarefas pessoais.
    
    ![Related field from Data section](assets/en/relations/Related-field-from-Data-section.png)

* Então pode selecionar um **ícone** assim como **formatadores** e definir **etiquetas curtas e longas** na seção Etiquetas e Ícones

![Related field from Labels and Icons section](assets/en/relations/related-field-from-labels-icons.png)

* Vá para a seção Formulários e arraste o campo no formulário detalhado Tasks

![Related field in Forms section](assets/en/relations/related-field-forms.png)

* Criar e executar

Seu campo relacionado deve aparecer no formulário detalhado do app!

![Related field in Forms section](assets/en/relations/final-result-n-to-one-relations.png)