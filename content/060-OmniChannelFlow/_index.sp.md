---
title: "Flujo omnicanal"
chapter: true
weight: 60
---

# Flujo omnicanal
Los flujos omnicanal se pueden iniciar cuando un cliente inicia una conversación de chat, voz o mensajería desde SalesForce. Este flujo omnicanal es lo que creará la solicitud de enrutamiento externo, lo que activará la interacción de SalesForce para enrutar a través del flujo de mensajes que configuramos en Architect en Genesys Cloud CX. Configuremos eso para su instancia ahora.

## Crear el flujo omnicanal
1. En SalesForce, navegue hasta el portal de configuración. 
![SF Setup](/images/SFSetup.jpg)
2. En el cuadro de búsqueda rápida, busque Flujos.
![Flows](/images/flows.jpg)
3. Haga clic para crear un nuevo flujo. Luego haga clic en la pestaña "Todos + Plantillas" y luego en la pestaña Flujo omnicanal. Elija el Flujo omnicanal predeterminado y haga clic en Crear.
![Create Flow](/images/createFlow.jpg)
4. En la caja de herramientas, haga clic en Administrador y luego en Nuevo recurso.
     - el nuevo tipo de recurso será de variable
     - para el nombre de la API, ingrese *recordId* (debe ser este nombre específicamente)
     - para Tipo de datos, elija Texto
     - marque *Disponible para entrada* para disponibilidad para uso fuera del flujo
    ![Record Id](/images/recordId.jpg)
5. Una vez más, en el tooblox, haga clic en Administrador y luego en Nuevo recurso.
     - este nuevo tipo de recurso también será de variable
     - para el nombre de la API, ingrese *input_record*
     - para Tipo de datos, elija Registro
     - para Objeto, elija Transcripción de chat
     - marque *Disponible para entrada* para disponibilidad para uso fuera del flujo
    ![Input Record](/images/input_Record.jpg)
6. En la interfaz gráfica, presione el signo + para agregar un nuevo elemento entre el inicio y el final del flujo de OmniCanal. Elija Ruta de trabajo como el elemento.
![Route Work](/images/routeWork.jpg)
7. Al configurar la acción Ruta de trabajo, ingrese los siguientes valores:
     - La etiqueta y el nombre de la API pueden ser cualquier cosa descriptiva que desee. Incluso podría convertirlo en "Ruta de trabajo".
     - En Establecer valores de entrada e ID de registro, elija la variable recordId que creó
     - En Establecer valores de entrada y canal de servicio, elija el canal de servicio que creó anteriormente
     - Para la ruta a, seleccione Cola
     - Al seleccionar una cola, elija la cola que configuró previamente
     - Luego haga clic en Listo
    ![Route Work Config](/images/routeWorkConfig.jpg)
8. Ahora vamos a crear otro elemento justo después del elemento de trabajo de ruta que acabamos de crear. Este elemento será un elemento Crear registros
![Create Records](/images/createRecords.jpg)
9. Al crear la acción Crear registros, ingrese los siguientes valores:
     - La etiqueta y el nombre de la API pueden ser cualquier cosa descriptiva que desee. Incluso podría convertirlo en "Solicitud de enrutamiento externo"
     - Para cuántos registros crear, simplemente elija uno
     - En Cómo configurar los campos de registro, elija "Usar recursos separados y valores literales"
     - De la lista de objetos, elija Solicitud de enrutamiento externo
     - En Establecer valores de campo para solicitud de enrutamiento externo, vamos a establecer 2 campos.
         1. Open_Messaging_Integration__c: establezca el valor en la plataforma de integración de Open Messaging que configuró en Genesys Cloud CX desde la lista de selección
         2. Work_Item_ID__c: establezca el valor en la variable recordId que creamos anteriormente
     - Luego haga clic en Listo
        ![Create Record Config](/images/createRecordConfig.jpg)
10. Finalmente, haga clic en Guardar y luego haga clic en Activar

Si desea ver un video de estos pasos, puede verlo aquí. https://youtu.be/Of6BkfCdgJ0 

## Activar el flujo de Solicitud de Eliminación
Cuando descargó el paquete para enrutamiento externo, incluía un flujo denominado Eliminación de solicitud de enrutamiento externo. Este flujo limpiará los registros de solicitud que se crean cuando ocurre lo siguiente:
   
- Elementos de trabajo desconectados que se enrutan y completan con éxito
- El usuario cierra el chat antes de que se enrute a un agente

Failsafe's como este son importantes para cualquier implementación. Necesitamos activar este flujo, así que sigue estos pasos:

1. En SalesForce, navegue hasta el portal de configuración. 
![SF Setup](/images/SFSetup.jpg)
2. In the quick find box, search for Flows.
![Flows](/images/flows.jpg)
3. Busque el flujo llamado Eliminación de solicitud de enrutamiento externo y haga clic en él, y luego presione Activar

Ahora está listo para pasar a la siguiente sección. 
