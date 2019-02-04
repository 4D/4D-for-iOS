---
id: contact-app
title: Contact App
---
<div class = "objectives"> 

**OBJETIVOS**

Create your first app with 4D for iOS</div> <div class = "prerequisites"> 

**PRERREQUISITOS**

Click [here](prerequisites.html) to see what you'll need to get started!</div> 

Este tutorial le permitirá lanzarse directamente en el desarrollo de 4D for iOS. Le permitirá rápida y fácilmente crear su primera aplicación.

*Escenario: usted es un director comercial y desea consultar su lista de contactos cuando no esté en su oficina.*

Vamos a crear una aplicación de directorio para iPhone para buscar los nombres de los contactos de una lista y luego ver los detalles de cada contacto. La llamamos "Contacto".

## PASO 1. Comencemos

Descargue nuestro proyecto Starter, que contiene un archivo de base de datos y el icono de proyecto, pero no todavía el proyecto móvil.

<div style="text-align: center; margin-top: 20px">
  <p>
    

<a class="button"
href="../assets/contact-app/ContactStarter.zip">PROYECTO STARTER</a>

  </p>
</div>

## PASO 2. Creación del proyecto

Vamos a empezar con una estructura muy simple, utilizando una sola tabla. De 4D, ir a **Nuevo > Proyecto móvil**.

De un nombre a su proyecto y haga clic en **Crear**.

![Creación de un proyecto](assets/contact-app/Project-creation-4D-for-iOS.png)

## PASO 3. Abrir el editor de proyectos

¡Bienvenido a 4D for iOS! La pantalla de bienvenida muestra las principales etapas de creación de aplicaciones de esta magnífica herramienta. 🙂

![Pantalla de bienvenida](assets/contact-app/Welcome-Screen-4D-for-iOS.png)

Haga clic en **Continuar**.

## PASO 4. Secciones - General

Aquí, podrá configurar la información principal de la aplicación:

* **Organización:**Escriba el nombre de su empresa y el identificador de aplicación (ej. "Mi empresa" y com.MiEmpresa).
* **Producto:**introduzca el nombre de su aplicación. Llamémosla "Contact".
* **ID:** (Paquete ID) se genera automáticamente y se compone del identificador de su empresa y del nombre de su producto.
* **Versión:**deje la versión 1.0 y defina los derechos de autor de su aplicación. Es muy recomendable utilizar los formatos ofrecidos por 4D for iOS.
* **Iconos:**arrastre y suelte un icono para su aplicación en el área del icono.
* **Desarrollador:**esta sub sección se rellena automáticamente a partir del nombre de usuario en su ordenador. Copie/pegue la referencia de su equipo de desarrolladores (desde su cuenta desarrollador) en el campo Equipo. También puede dejar vacío para generar su aplicación únicamente en el simulador.

![General](assets/contact-app/Contact-app-general-section-4D-for-iOS.png)

## PASO 5. Secciones - Estructura

Es en esta sección que define un subconjunto de sus datos (tablas y campos de la base) para mostrar en dispositivos móviles.

Para nuestro ejemplo, seleccione **ID**, **Nombre** **Apellido**, **Cargo**, **Empresa**, **Teléfono**, **Notas** y **Foto**.<div class = "tips"> 

**NOTA**

We highly recommend publishing your primary key in order to identify each record of your database</div> 

![Estructura](assets/contact-app/Contact-app-structure-section-4D-for-iOS.png)

## PASO 6. Secciones - Iconos y etiquetas

Ahora es el momento para definir algunas etiquetas e iconos para los campos y tablas seleccionados.

**Table Properties:**

* Define a short and a long label for your Contact table
* Click on the icon field. La librería icono aparecerá y usted puede seleccionar un icono para ilustrar la tabla de contactos. También puede optar por dejar vacío el campo icon. 4D for iOS generará un icono predeterminado

**Field Properties:**

* Define a short and a long label for your selected fields.
* Haga clic en el campo de icono y seleccione los iconos para cada campo. There are several options for field icons: 
    * You can select an icon for each field,
    * If at least one icon has been defined and other fields are left empty, 4D for iOS will generate default icons for you
    * You can simply leave them empty to not display any field icons. 

![Iconos y Etiquetas](assets/contact-app/Contact-app-icons-labels-section-4D-for-iOS.png)

## PASO 7. Secciones - menú principal

Lo siguiente es definir el orden de las tablas en el menú principal de la aplicación.

* **Tablas disponibles:** muestra las tablas a utilizar.
* **Tablas seleccionadas:** muestra los elementos de menú de su aplicación. Aunque nuestro ejemplo solo tiene un elemento, puede arrastrar y soltar los elementos para reordenarlos.

![Menú principal](assets/contact-app/Contact-app-main-menu-section-4D-for-iOS.png)

## PASO 8. Secciones - Formularios

We're almost done, but first we need to decide on the app's layout. Hay formularios listados y formularios detallados para elegir.

* Seleccione un modelo de formulario listado para mostrar su tabla como una lista. Para nuestra aplicación Contact, utilicemos la plantilla **Profile**.

![Plantilla de formulario listado](assets/contact-app/ListformTemplate-form-section-4D-for-iOS.png)

En este punto, la parte inferior de la ventana de configuración ha cambiado de selección de plantilla a definición de contenido.

* Arrastre y suelte los campos que desee mostrar en la plantilla, *es decir*, Last Name en los campos de título y búsqueda. Los campos Búsqueda y Sección son opcionales, por el momento, deje en blanco el campo Section.

![Contenido del formulario listado](assets/contact-app/ListformContent-form-section-4D-for-iOS.png)

Y por último, definimos el formulario detallado.

* Seleccione una plantilla que sea la más adecuada para su aplicación. Para nuestra aplicación Contact, vamos a utilizar la plantilla **Visual Contact**.

![Plantilla de formulario listado](assets/contact-app/DetailformTemplate-form-section-4D-for-iOS.png)

* Arrastre y suelte el contenido en los lugares adecuados en la plantilla de formulario detallado, *es decir*, Nombre, Apellido y foto.

![Contenido del formulario detallado](assets/contact-app/DetailformContent-form-section-4D-for-iOS.png)

## PASO 9. Creación de la aplicación

¡Ahora la parte divertida! Es hora de crear su aplicación y probarla en el simulador para ver el resultado final.

* Haga clic en la pestaña **Generar**.
* Seleccione un dispositivo a utilizar como Simulador haciendo clic en el botón dispositivo.
* Haga clic en **Generar y ejecutar**.
* Espere unos segundos y …. ¡Listo! ¡Su aplicación iOS está creada!

![Crear y ejecutar](assets/contact-app/Build-the-app-simulator.png)

## PASO 10. ¿Qué hacer ahora?

Hemos cubierto la creación básica de la aplicación de este tutorial, y ahora debe poder crear aplicaciones simples por sí mismo. Espere, ¡Hay más! En el siguiente tutorial, aprenderá cómo crear una aplicación aún más compleja. Haga clic en **Final Project** a continuación para descargar la aplicación Contact final.

<div style="text-align: center; margin-top: 20px; margin-bottom: 20px">
  <p>
    

<a class="button"
href="../assets/contact-app/ContactFinal.zip">PROYECTO FINAL</a>

  </p>
</div>