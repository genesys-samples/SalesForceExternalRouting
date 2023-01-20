---
title: "Introducción y requisitos previos"
chapter: true
weight: 10
---

# Agenda de aprendizaje de hoy
1. La asociación de Genesys y SalesForce
2. Cómo instalar, configurar y probar el enrutamiento de un chat de SalesForce a través del motor de enrutamiento Genesys Cloud CX
3. Cómo configurar la sincronización de presencia OmniChannel con Genesys Cloud CX

# requisitos previos
1. Cuenta Genesys Cloud CX con acceso de administrador
2. Cuenta de SalesForce con acceso de administrador
3. Instale Genesys Cloud for SalesForce Managed Package
    - https://help.mypurecloud.com/articles/install-or-upgrade-the-genesys-cloud-for-salesforce-managed-package/
4. Rol de agente de SalesForce asignado al usuario en Genesys Cloud CX

Una combinación de Genesys y SalesForce es un dúo poderoso. Combina Genesys, un sistema de compromiso de clase mundial, con SalesForce, un sistema de registro de clase mundial. Hoy nos centraremos específicamente en cómo integrar SalesForce OmniChannel con el motor de enrutamiento Genesys Cloud CX. Pero, ¿qué es OmniChannel?

OmniChannel es una función de SalesForce Service Cloud. Permite a los clientes comunicarse con los agentes que trabajan en SalesForce a través de casi cualquier canal (SMS, chat web, Facebook, etc.), como se indica en el nombre. Si está familiarizado con Genesys, es posible que esté pensando "pero espere, Genesys puede proporcionar la misma funcionalidad". Tendría razón, pero hay algunos escenarios en los que las empresas pueden preferir enrutar elementos de SalesForce OmniChannel a través de Genesys Cloud CX para nuestras sólidas capacidades de enrutamiento. Analicemos eso y comencemos con las diferencias en la interfaz de usuario para un agente que trabaja en SalesForce.

#### Experiencia de usuario de Genesys Cloud CX Objects
![Genesys Chat UI](/images/genesysChatUI.jpg)
Aquí puede ver que los agentes manejan las interacciones basadas en texto en un widget emergente llamado "GenesysCloudInteractionUtility". Toda la funcionalidad aquí es Genesys: un enrutamiento de chat de Genesys a través de Architect en una cola de Genesys.

#### Experiencia de usuario de objetos de SalesForce OmniChannel
![OmniChannel Chat UI](/images/omniChannelChatUI.jpg)
Con la integración de OmniChannel, la experiencia del usuario para los agentes está más integrada en la página. Puede ver que cuando un chat coincide con un contacto, crea un nuevo objeto de chat en SalesForce y lo asocia con un contacto. El agente puede entonces responder al chat sin necesidad de ningún tipo de widget emergente. Aquí, la funcionalidad se divide entre SalesForce y Genesys: el chat en sí es SalesForce, pero Genesys realiza el enrutamiento.

#### Otros escenarios en los que las empresas podrían gravitar hacia un enfoque de integración de Genesys Cloud y OmniChannel
1. La empresa ya usa OmniChannel para digital y está contenta con él, pero está buscando un centro de contacto de nivel más empresarial.
2. La empresa quiere aprovechar las capacidades de gestión del conocimiento de SalesForce einstein con OmniChannel
3. Las empresas quieren aprovechar las campañas salientes de Genesys dentro de SalesForce junto con OmniChannel para las interacciones entrantes digitales
4. Cada negocio es único, por lo que habrá otros escenarios que no se enumeran aquí

