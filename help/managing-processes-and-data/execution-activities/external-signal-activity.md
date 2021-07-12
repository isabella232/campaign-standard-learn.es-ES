---
title: 'Actividad de señal externa: llame a un flujo de trabajo con parámetros'
description: Aprenda a iniciar un flujo de trabajo desde otro para admitir recorridos de cliente más complejos, mientras puede supervisar y reaccionar mejor ante los problemas.
feature: Actividad de ejecución
kt: 2750
thumbnail: 27249
doc-type: feature video
activity: use
team: TM
exl-id: d3996185-681c-4906-85f0-0543ab767519
role: User, Developer
level: Experienced
source-git-commit: 2be2719ddd84490b796d9abc6300376fa896ff0c
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 9%

---

# [!UICONTROL External Signal activity ]- Invocación de un flujo de trabajo con parámetros

El [!UICONTROL External Signal activity] se utiliza para organizar y orquestar diferentes procesos que forman parte del mismo recorrido del cliente en diferentes flujos de trabajo. Permite el inicio de un flujo de trabajo desde otro, lo que permite recorridos de clientes más complejos, mientras que se puede supervisar y reaccionar mejor en caso de problemas.

En ACS 19.2, el [!UICONTROL External Signal activity] no solo puede llamar a un flujo de trabajo, sino que también puede pasar parámetros al flujo de trabajo (un nombre de audiencia a destinatario, un nombre de archivo a importar, una parte del contenido del mensaje, etc.) al flujo de trabajo desde otro flujo de trabajo o una llamada a la API de REST para integrarlo con sus sistemas externos.

Esto también incluye una nueva actividad **Test** en la que puede ejecutar pruebas con esta funcionalidad.

En el siguiente vídeo se explican los pasos de configuración necesarios para:

1. **Recibir** parámetros externos de un sistema externo, como un sistema de administración de contenido (CRM):

   * Declarar los parámetros en la actividad Señal externa
   * Configure la llamada de API para definir los parámetros y el déclencheur de la actividad de señal externa del flujo de trabajo. Para obtener más información sobre cómo configurar una llamada de API, consulte [Activación de una actividad de señal](https://docs.campaign.adobe.com/doc/standard/en/api/ACS_API.html#triggering-a-signal-activity).

1. **Personalice un flujo de trabajo con parámetros**  externos (variables de eventos):

   Una vez activado el flujo de trabajo, los parámetros se incorporan en las variables de eventos del flujo de trabajo y se pueden utilizar en el flujo de trabajo. Consulte la [documentación](https://helpx.adobe.com/campaign/standard/automating/using/calling-a-workflow-with-external-parameters.html) para todas las actividades que se pueden personalizar con variables de evento:

   * Configurar la actividad de prueba (nuevo en 19.2)
   * Configurar la audiencia de lectura y la actividad de entrega de correo electrónico

1. **Configuración de una** actividad final para llamar a un flujo de trabajo con parámetros externos

>[!VIDEO](https://video.tv.adobe.com/v/27249/?quality=12)

## Recursos adicionales

* [Señal externa (documentación)](https://experienceleague.adobe.com/docs/campaign-standard/using/managing-processes-and-data/calling-workflow-external-parameters/calling-a-workflow-with-external-parameters.html)
