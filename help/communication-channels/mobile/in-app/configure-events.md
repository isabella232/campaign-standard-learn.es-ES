---
title: Configuración de eventos
description: '"Comprenda cómo definen los eventos qué acción emprendida por el usuario déclencheur que se muestre un mensaje en la aplicación. ”'
feature: In App
kt: 2548
thumbnail: 26245.jpg
doc-type: feature video
activity: use
team: TM
exl-id: 2c7937f4-b0da-46e5-934e-c660012c2c6f
role: User, Developer
level: Beginner, Intermediate
source-git-commit: 2be2719ddd84490b796d9abc6300376fa896ff0c
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 2%

---

# Configurar [!UICONTROL Events] {#configuring-events}

Al configurar un [!UICONTROL In-App] , debe definir qué acción iniciada por el usuario déclencheur el mensaje que se va a mostrar. Estas acciones se denominan [!UICONTROL events]. Tres categorías de [!UICONTROL events] están disponibles: [!UICONTROL Mobile Application events], [!UICONTROL Life Cycle events]y [!UICONTROL Analytics events].

## [!UICONTROL Mobile Application Events] {#mobile-application-events}

[!UICONTROL Mobile Application events] are [!UICONTROL custom events] que se implementan en la aplicación móvil.

Algunos ejemplos son:

* Un cliente ha visto un artículo
* Un cliente agrega un artículo al carro de compras
* Abandono del carro de compras
* Un cliente ha comprado algo

Debe configurar estas [!UICONTROL events] en Adobe Campaign. En el siguiente vídeo se describe cómo hacerlo.

>[!VIDEO](https://video.tv.adobe.com/v/26245?quality=12)

## [!UICONTROL Life Cycle events] {#life-cycle-events}

[!UICONTROL Lifecycle events] están listos para usar [!UICONTROL events]. Lo siguiente [!UICONTROL events] están disponibles:

* [!UICONTROL launched]
* [!UICONTROL upgraded]
* [!UICONTROL crashed]

Un ejemplo de caso de uso podría ser un mensaje que introduce nuevas funciones después de una actualización o una promoción de eventos.

>[!NOTE]
>
>La variable [!UICONTROL Lifecycle module] debe configurarse en la aplicación móvil. Consulte aquí para obtener más información sobre [Cómo añadir el ciclo vital a la aplicación](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/mobile-core/lifecycle)

## [!UICONTROL Analytics Events] {#analytics-events}

Se admiten las tres categorías siguientes en función de la instrumentación de la aplicación móvil:

* Adobe Analytics
* [!UICONTROL Context data]
* [!UICONTROL View state]

>[!NOTE]
>
>[!UICONTROL Analytics events] requieren una licencia de Adobe Analytics. Una vez que tenga la variable [[!DNL Analytics] extensión configurada](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-analytics#configure-analytics-extension-in-launch) y han añadido [Analytics para su aplicación](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-analytics#add-analytics-to-your-app), estos eventos pasan a estar disponibles en la variable [!UICONTROL In-App] en ACS.

## Recursos adicionales

* [Habilitar métricas del ciclo vital (documentación)](https://aep-sdks.gitbook.io/docs/getting-started/initialize-the-sdk#enable-lifecycle-metrics)
