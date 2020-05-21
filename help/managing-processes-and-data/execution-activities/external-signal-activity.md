---
title: 'Actividad de señal externa: llame a un flujo de trabajo con parámetros'
description: La Actividad de señal externa se utiliza para organizar y orquestar diferentes procesos que forman parte del mismo viaje del cliente a diferentes flujos de trabajo. Permite el inicio de un flujo de trabajo desde otro, lo que permite soportar viajes de clientes más complejos, mientras que se puede supervisar y reaccionar mejor en caso de problemas.
feature: External Signal Activity
topics: Workflows
kt: 2750
doc-type: feature video
activity: use
team: TM
translation-type: tm+mt
source-git-commit: 556bff4c94e16d3a94561dee1ccb311bc003b631
workflow-type: tm+mt
source-wordcount: '332'
ht-degree: 0%

---


# [!UICONTROL External Signal activity ]- Llamar a un flujo de trabajo con parámetros

El [!UICONTROL External Signal activity] se utiliza para organizar y orquestar diferentes procesos que forman parte del mismo viaje del cliente a diferentes flujos de trabajo. Permite el inicio de un flujo de trabajo desde otro, lo que permite soportar viajes de clientes más complejos, mientras que se puede supervisar y reaccionar mejor en caso de problemas.

En ACS 19.2, [!UICONTROL External Signal activity] no solo puede llamar a un flujo de trabajo, sino que además pasa parámetros al flujo de trabajo (un nombre de audiencia a destinatario, un nombre de archivo para importar, una parte del contenido del mensaje, etc.) al flujo de trabajo desde otro flujo de trabajo o una llamada a la API de REST para integrarse con sus sistemas externos.

Esto también incluye una nueva Actividad **de pruebas** en la que puede ejecutar pruebas con esta funcionalidad.

En el siguiente vídeo se explican los pasos de configuración necesarios para:

1. **Recibir parámetros** externos de un sistema externo, como un sistema gestor de contenido (CRM):
   * Declarar los parámetros en la Actividad Señal externa
   * Configure la llamada de API para definir los parámetros y activar la Actividad de señal externa del flujo de trabajo. Para obtener más información sobre cómo configurar una llamada de API, consulte [Activación de una Actividad](https://docs.campaign.adobe.com/doc/standard/en/api/ACS_API.html#triggering-a-signal-activity)de señal.

1. **Personalice un flujo de trabajo con parámetros** externos (variables de eventos):
Una vez activado el flujo de trabajo, los parámetros se ingieren en las variables de eventos del flujo de trabajo y se pueden utilizar dentro del mismo. Consulte la [documentación](https://helpx.adobe.com/campaign/standard/automating/using/calling-a-workflow-with-external-parameters.html) de todas las actividades que se pueden personalizar con variables de evento:

   * Configurar la Actividad de prueba (nueva en 19.2)
   * Configurar la Actividad de Audiencia de lectura y Envío de correo electrónico

1. **Configurar una Actividad** final para llamar a un flujo de trabajo con parámetros externos

>[!VIDEO](https://video.tv.adobe.com/v/27249/?quality=12)

## Recursos adicionales

* [Señal externa (documentación)](https://docs.adobe.com/content/help/en/campaign-standard/using/managing-processes-and-data/data-management-activities/external-api.html)
