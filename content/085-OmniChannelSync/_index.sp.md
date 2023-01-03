---
title: "Sincronización Omnicanal"
chapter: true
weight: 85
---
En este taller de hoy, es importante saber que ahora tenemos un escenario en el que los agentes podrían manejar interacciones de Genesys Cloud CX o interacciones de SalesForce que se enrutan a través de Genesys Cloud CX. Por ese hecho, significa que los agentes tienen 2 aplicaciones separadas donde se establecen sus presencias: Genesys Cloud CX y SalesForce OmniChannel. Estas presencias son necesarias para el enrutamiento y, por lo tanto, necesitamos una sincronización fluida entre las presencias. Afortunadamente, el paquete Genesys Cloud for SalesForce lo hace muy fácil de administrar.

1. En SalesForce, navegue hasta el portal de configuración.
![SF Setup](/images/SFSetup.jpg)
2. Buscar paquetes instalados
3. Busque el paquete de Genesys Cloud para SalesForce y haga clic en configurar (este NO es el paquete de enrutamiento externo que instalamos anteriormente, tener este paquete instalado figuraba en nuestros requisitos previos)
![Configure Package](/images/configurePackage.jpg)
4. En Elegir un centro de llamadas, elija la opción Lightning
5. Navegue a la sección titulada "Configuración de sincronización omnicanal" y haga clic en el cuadro para habilitar la sincronización omnicanal
6. Actualice la configuración para que coincida con lo que ve en la imagen a continuación
     - opcionalmente, si tiene estados personalizados en SalesForce que desea usar, también puede usarlos.
![Sync Settings](/images/syncSettings.jpg)

Tenga en cuenta que si desea editar los estados de sincronización para que funcionen de manera diferente, puede hacerlo. Siempre puedes volver aquí y editarlos más tarde. ¡Ahora está listo para pasar a probar lo que hemos construido!