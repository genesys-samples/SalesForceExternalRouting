---
title: "Botón de Chat"
chapter: true
weight: 70
---

Los botones de chat en SalesForce le permiten especificar cómo se dirigen las solicitudes de chat entrantes a los agentes. Estos son similares a los widgets de chat de Genesys si está familiarizado con ellos. Estos son literalmente los botones en los que los visitantes hacen clic para iniciar un chat cuando visitan su sitio web. Un botón consta de varias líneas de JavaScript que puede copiar y pegar en las páginas web de su sitio web.

## Create a Chat Button
1. En SalesForce, navegue hasta el portal de configuración. 
![SF Setup](/images/SFSetup.jpg)
2. En el cuadro de búsqueda rápida, busque y seleccione Invitaciones y botones de chat
3. Haga clic para crear un nuevo botón de chat y siga los siguientes componentes de configuración
     - Para el tipo, elija Botón de chat
     - Dar un nombre descriptivo
     - En Información de enrutamiento, configure el Tipo de enrutamiento como Omnicanal.
     - Marque la casilla para "Usar un flujo para el enrutamiento"
     - En el cuadro Flujo omnicanal, busque y encuentre el flujo que creamos al comienzo del taller.
     - Busca y selecciona tu cola que creamos en el taller
     - Marque la casilla para "Habilitar cola"
     - Establezca el tamaño de cola por agente en 5 (puede cambiar este número más tarde si lo desea)
     - Presiona guardar. Su configuración debería ser algo como esto: 
    ![Chat Button Config](/images/chatButtonConfig.jpg)