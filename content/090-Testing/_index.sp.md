---
title: "Pruebas"
chapter: true
weight: 90
---

¡Felicitaciones! En este punto, ha configurado el enrutamiento externo de los chats de SalesForce a través del motor de enrutamiento Genesys Cloud CX. Ahora lo que debemos hacer es encontrar una manera de probar y asegurarnos de que todo funcione como esperamos. Para las siguientes instrucciones, supondré que no tiene su propio sitio web; sin embargo, si tiene su propio sitio web y desea probar en el sitio web, puede seguir estas instrucciones para hacerlo. https://help.salesforce.com/s/articleView?language=en_US&r=https%3A%2F%2Fwww.google.com%2F&id=sf.snapins_chat_get_code.htm&type=5#:~:text=Copy%20the%20chat%20code%20snippet,page%20as%20a%20Chat%20button. 

Si desea probar sin usar su propio sitio web, siga los siguientes pasos:
1. En SalesForce, navegue hasta el portal de configuración.
![SF Setup](/images/SFSetup.jpg)
2. En el cuadro de búsqueda rápida, busque y seleccione Todos los sitios en Experiencias digitales
![All Sites](/images/allSites.jpg)
3. Haga clic para crear un nuevo sitio.
4. Elija cualquier plantilla. Personalmente, me gusta la plantilla del Centro de ayuda.
     - Navegar a través de las opciones de configuración
     - Dale al sitio un nombre y URL
     - Estos ajustes no importan demasiado. Simplemente haga clic en el asistente para crear el sitio y presione finalizar
5. Una vez que haya creado su sitio, haga clic en Generador para editar su sitio web.
![Builder](/images/builder.jpg)
6. Vuelva a la página Configuración (es más fácil hacerlo en una pestaña separada)
7. Busque "Despliegues de servicios integrados" y haga clic para crear uno nuevo
8. Elija Chat integrado y haga clic en siguiente. Luego asigne un nombre descriptivo y seleccione el sitio que acaba de crear como punto final
![Embedded Service Deployment](/images/embeddedServiceDeployment.jpg)
9. De vuelta en la página de Experience Builder, haga clic en Componentes y luego seleccione Chat de servicio integrado. Puede arrastrar este componente a cualquier parte del sitio web.
![Embedded Service Chat](/images/embeddedServiceChat.jpg)
7. Algunos campos de configuración se abrirán cuando arrastre el componente Chat de servicio integrado en la pantalla. En Implementación de chat, seleccione la implementación del servicio integrado que creó en la lista desplegable. Puede editar cualquier otra cosa que desee, pero esa es la única que se requiere.
![Chat Deployment](/images/chatDeployment.jpg)
8. Ahora debería ver un widget en la parte inferior derecha de la pantalla que dice Agente sin conexión o Chat con un experto
![SalesForce Widget](/images/SFWidget.jpg)
9. Ahora necesitamos deshacernos de algunas configuraciones de seguridad de CSP. En el lado izquierdo, haga clic en el icono de configuración y luego en Seguridad y privacidad.
10. En Política de seguridad de contenido, cámbiela a CSP relajado. Si hay algo debajo de Errores de CSP, haga clic en Permitir.
![CSP Settings](/images/CSPSettings.jpg)
11. En la parte superior derecha de la pantalla, haga clic en vista previa
12. Si su widget dice Agente fuera de línea, abra una nueva pestaña y navegue a la Consola donde tiene implementado el widget de OmniChannel. Cambie su estado de OmniChannel a Disponible.
![OmniChannel Status](/images/omniChannelStatus.jpg)
13. Por último, vuelva al sitio web de Experience Builder y es posible que deba actualizar la pantalla. Una vez que su widget diga Chatea con un experto, puedes hacer clic en eso y completar el formulario.
     - sugerencia: si completa el formulario con un correo electrónico y un nombre que coincida con un contacto en su cuenta de SalesForce, el chat se asociará automáticamente con esa cuenta
    ![Chat Widget](/images/chatWidget.jpg)
14. Al regresar de su consola de SalesForce, puede aceptar el chat de la herramienta Genesys CTI que luego activará OmniChannel para crear un objeto de chat a través de OmniChannel.
![Handle Chat](/images/handleChat.jpg)

