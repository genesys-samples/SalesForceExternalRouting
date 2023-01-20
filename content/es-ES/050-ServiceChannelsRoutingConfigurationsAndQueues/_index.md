---
title: "Canales de servicio, configuraciones de enrutamiento y colas"
chapter: true
weight: 50
---

## Canales de servicio
Los canales de atención nos permitirán convertir los objetos de SalesForce en un registro de trabajo. También le permitirán administrar las fuentes de trabajo y su prioridad en comparación con otros elementos de trabajo. Una vez que cree los canales de servicio, puede asociarlos con colas que, en última instancia, determinarán cómo se enrutan los elementos de trabajo a sus agentes.

1. Navegue a la página de configuración de SalesForce
![SF Setup](/images/SFSetup.jpg)
2. En el cuadro de búsqueda rápida, busque Canales de servicio
![Service Channels](/images/serviceChannels.jpg)
3. Haga clic para crear un nuevo canal de servicio
     - La única configuración que debe cambiar es el objeto SalesForce. Para este menú desplegable, elija "Transcripción de chat".
     - Opcional: puede marcar la casilla para "Minimizar el widget de OmniCanal cuando se acepta el trabajo"
     - Al final, su configuración debería verse así.
    ![Service Channel Settings](/images/serviceChannelSettings.jpg)

## Configuraciones de enrutamiento
Las configuraciones de enrutamiento especifican cómo se enrutan los elementos de trabajo a los agentes. Por ejemplo, puede definir la prioridad. Un elemento enrutado a través de una configuración de enrutamiento con mayor prioridad que un elemento de trabajo diferente se enrutará más rápido. También puede definir el modelo de enrutamiento que se utiliza aquí, que será importante para nosotros hoy. Vamos a utilizar un modelo de enrutamiento externo ya que estamos enrutando chats usando Genesys Cloud CX. Siga junto con estos pasos.

1. Vaya a la página de configuración de SalesForce
![SF Setup](/images/SFSetup.jpg)
2. En el cuadro de búsqueda rápida, busque Configuraciones de enrutamiento
![Routing Config Search](/images/routingConfigSearch.jpg)
3. Haga clic para crear una nueva configuración de enrutamiento (o si ya tiene un canal de servicio para chat, puede editarlo)
     - Edite los siguientes ajustes:
         - Proporcione un nombre de configuración de enrutamiento descriptivo
         - Establezca la prioridad de enrutamiento en 1 (esto le dará a esta configuración de enrutamiento la prioridad más alta)
         - Cambiar modelo de enrutamiento a enrutamiento externo
         - Establecer las Unidades de Capacidad a 1
             - esto significa que este elemento de trabajo solo ocupará una unidad de capacidad. Por el contrario, a una caja se le puede asignar un peso de 3 unidades de capacidad. En este escenario, digamos que la capacidad máxima de un agente es 5. Esto significa que podrían manejar 2 chats y 1 caso (1+1+3=5).
         - Al final, sus ajustes de configuración de enrutamiento deberían verse así:
            ![Routing Config Settings](/images/routingConfigSettings.jpg)

## Colas
Una cola es una ubicación donde los registros se pueden enrutar para esperar que los procese un miembro del grupo. Puedes pensar en una cola como una fila en el banco. Al final de la fila, hay cajeros que están esperando para atender su solicitud. Una cola en SalesForce también tiene miembros asignados a la cola que están esperando para manejar la solicitud una vez que estén listos para ser procesados. Los supervisores pueden monitorear el desempeño de la cola y ver cuán eficientemente los miembros manejan las solicitudes. Es importante para nuestro escenario que las colas se vinculen a una configuración de enrutamiento. Si recuerda, nuestra configuración de enrutamiento utilizó un método de enrutamiento externo. Este vínculo entre la cola y la configuración de enrutamiento es lo que permitirá que los miembros de la cola en SalesForce sean objetos enrutados por Genesys Cloud CX. Siga junto con estos pasos.

1. Vaya a la página de configuración de SalesForce
![SF Setup](/images/SFSetup.jpg)
2. En el cuadro de busqueda rapida, busque Colas
![Queue Search](/images/queueSearch.jpg)
3. Haga clic para crear una nueva cola
     - Edite las siguientes configuraciones
         - Dar una etiqueta descriptiva y un nombre de cola
         - Para Configuración de enrutamiento, busque y seleccione la configuración de enrutamiento que hicimos en el paso anterior
         - En Objetos admitidos, mueva "Transcripción de chat" al lado de Objetos seleccionados
         - En Miembros de la cola, busque en función de los usuarios y luego agréguese a usted y a cualquier otro usuario de SalesForce que desee en la cola.
         - Su configuración debería verse así
        ![Queue Setting 1](/images/queueSetting1.jpg)
        ![Queue Setting 2](/images/queueSetting2.jpg)



