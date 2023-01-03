---
title: "Creación de un Flujo de Mensajes e Integración de Mensajería Abierta"
chapter: true
weight: 40
---

Una integración de Message Flow y Open Messaging es la forma en que Genesys puede proporcionar capacidades de enrutamiento, opciones de autoservicio, búsquedas de datos a través de integraciones y mucho más. El flujo de mensajes se controla desde Architect y, si está familiarizado con Genesys Cloud CX, probablemente esté familiarizado con Architect. Architect es un generador de respuestas interactivas de autoservicio para todos los canales en Genesys Cloud CX; ya sea voz, correo electrónico, chat, mensajes, creación de bots, etc. La integración de Open Messaging es el punto final que facilita la mensajería con sistemas de terceros y servicios de mensajería externos. En este escenario, ese servicio de mensajería externo será SalesForce OmniChannel.

## Creación de un flujo de mensajes e integración de mensajería abierta
1. Antes de sumergirnos en Architect, asegúrese de que su usuario en Genesys Cloud CX sea parte de una cola. De lo contrario, siga estas instrucciones para crear una nueva cola y agregar a su usuario como miembro.
    - https://help.mypurecloud.com/articles/create-queues/
2. En Genesys Cloud CX Admin, busque Architect y navegue hasta él. Dentro de Architect, de la lista de flujos, seleccione Mensaje entrante.
![Inbound Message](/images/inboundMessage.jpg)
3. Haga clic en Agregar para crear un nuevo flujo y asígnele un nombre descriptivo.
     - Opcionalmente, si ya tiene un flujo que le gustaría usar, puede pasar directamente al Paso 6.
    ![Create Inbound Flow](/images/createInboundFlow.jpg)
4. En el Estado inicial, arrastre una opción Transferir a ACD debajo del punto de inicio. En las opciones que se muestran a la derecha, elija su cola de la lista desplegable.
     - Opcionalmente, si está familiarizado con Architect y desea agregar su propia lógica, puede hacerlo ahora.
    ![Transfer to ACD](/images/transferToACD.jpg)
5. Presiona publicar.
6. Vuelva a la página de administración de Genesys Cloud CX y busque Plataformas en el contenedor Mensaje.
![Platforms](/images/platforms.jpg)
7. Haga clic para crear una nueva integración y elija Open Messaging como tipo.
![Open Messaging](/images/openMessaging.jpg)
8. Asigne a la integración Open Messaging un nombre descriptivo. Para la URL del webhook de notificación saliente, no importa lo que ponga aquí. En realidad, puede simplemente poner https://whatever.com y luego el token secreto de firma de webhook de notificación saliente necesita que ponga un valor, pero el valor no importará. Simplemente puede poner "123". Luego presione guardar. Esta es una integración preempaquetada que tenemos con SalesForce, por lo que estos campos no se usan realmente.
![Open Messaging Config](/images/openMessagingConfig.jpg)
9. Ahora navegue de regreso a la consola de administración de Genesys Cloud CX y luego busque Enrutamiento de mensajes
![Message Routing](/images/messageRouting.jpg)
10. Abra Enrutamiento de mensajes y luego haga clic en la esquina superior derecha para crear una nueva ruta de mensajes
11. Para la opción Flujo, elija el flujo de mensajes que creó anteriormente. Y para la dirección, elige la plataforma que acabas de crear. Una vez que haya hecho esto, ¡estará listo para sincronizar sus cambios con SalesForce!
![Message Route](/images/messageRoute.jpg)


## Sincronizar sus cambios con SalesForce
1. En SalesForce, haga clic en Configuración
![SF Setup](/images/SFSetup.jpg)
2. Buscar paquetes instalados
3. En esta página, ubique el paquete Genesys Cloud for SalesForce External Routing y haga clic en Configure
![Package Configure](/images/packageConfigure.jpg)
4. Por último, presione Opciones de recuperación. Esto consultará su cuenta de Genesys Cloud CX para colas e integraciones de mensajería para sincronizar con su instancia de SalesForce. Entonces podremos usar la integración de colas y mensajes que creó para configurar el enrutamiento externo dentro de SalesForce.
![Retrieve Options](/images/retrieveOptions.jpg)
