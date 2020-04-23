---
id: version-18.0-filter-query-introduction
title: Búsquedas limitadas
original_id: filter-query-introduction
---

<div markdown="1" class = "objectives">
**OBJETIVOS**
Defining basic and user information-based query filters to display filtered content in the generated iOS app.</div> <div markdown="1" class = "prerequisites">
**REQUISITOS PREVIOS**
Haga clic [aquí](prerequisites.html) para ver lo que necesita para empezar.</div>

In this tutorial, we'll cover **restricted queries** with a simple use case: imagine you're an account manager and you want to consult your *In Progress* contracts simply by connecting to your app with your email address.

First, from the Data section we're going define a **basic filter query** to only display *In Progress* contracts. Then we're going to apply a **user information-based filter** which will depend on the account manager's email.

## Descargar el proyecto Starter

Before we begin, be sure to download the **Starter Project** which includes a **4DforiOSQueries.4dbase** file (a demo database with a ready-to-use mobile app project)

<div markdown="1" style="text-align: center; margin-top: 20px; margin-bottom: 20px">
<a class="button"
href="https://github.com/4d-for-ios/tutorial-RestrictedQueries/releases/latest/download/tutorial-RestrictedQueries.zip">PROYECTO STARTER</a>
</div>

The database includes a:

* **CRM table** with all the data we want to display in the generated iOS app
* **AccountManager table** with basic information about the account managers (email and name).

![CRM database](assets/en/restricted-queries/CRMDatabase.png)<div markdown="1" class = "tips">
**NOTA**
This project uses [custom templates](https://4d.github.io/4d-for-ios/docs/en/creating-listform-templates.html), [custom icons](https://4d.github.io/4d-for-ios/docs/en/using-icons.html) and custom [data formatters](https://4d.github.io/4d-for-ios/docs/en/creating-data-formatter.html).</div>

You're now ready to define your first restricted query!

Open the mobile project by clicking on Open > Mobile Project... and select CRM app > **project.4dmobileapp**.