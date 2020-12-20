---
title: Configuración de eventos
description: 'Al configurar un mensaje en la aplicación en eventos de Adobe Campaign Standard (ACS), defina qué acción iniciada por el usuario activará la visualización del mensaje. '
feature: In-App
topics: Mobile
kt: 2548
thumbnail: 26245.jpg
doc-type: feature video
activity: use
team: TM
translation-type: tm+mt
source-git-commit: 11263e247184ddc6a8e3df6a8ed0899907fbb366
workflow-type: tm+mt
source-wordcount: '220'
ht-degree: 2%

---


# Configurar [!UICONTROL Events] {#configuring-events}

Al configurar un mensaje [!UICONTROL In-App], debe definir qué acción iniciada por el usuario activa la visualización del mensaje. Estas acciones se denominan [!UICONTROL events]. Hay tres categorías disponibles de [!UICONTROL events]: [!UICONTROL Mobile Application events], [!UICONTROL Life Cycle events] y [!UICONTROL Analytics events].

## [!UICONTROL Mobile Application Events] {#mobile-application-events}

[!UICONTROL Mobile Application events] son  [!UICONTROL custom events] implementadas en la aplicación móvil.

Algunos ejemplos son:

* Un cliente ha visto un artículo
* Un cliente agrega un artículo al carro de compras
* Abandono del carro de compras
* Un cliente ha comprado algo

Debe configurar estos [!UICONTROL events] en Adobe Campaign. El siguiente vídeo describe cómo hacerlo.

>[!VIDEO](https://video.tv.adobe.com/v/26245?quality=12)

## [!UICONTROL Life Cycle events]  {#life-cycle-events}

[!UICONTROL Lifecycle events] están listos para usar  [!UICONTROL events]. Están disponibles los siguientes [!UICONTROL events]:

* [!UICONTROL launched]
* [!UICONTROL upgraded]
* [!UICONTROL crashed]

Un caso de uso de ejemplo podría ser un mensaje que introduce nuevas funciones después de una actualización o una promoción de evento.

>[!NOTE]
>
>El [!UICONTROL Lifecycle module] debe configurarse en la aplicación móvil. Consulte aquí para obtener más información sobre [Cómo agregar el ciclo vital a su aplicación](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/mobile-core/lifecycle)

## [!UICONTROL Analytics Events] {#analytics-events}

Se admiten las tres categorías siguientes en función de la instrumentación de la aplicación móvil:

* Adobe Analytics
* [!UICONTROL Context data]
* [!UICONTROL View state]

>[!NOTE]
>
>[!UICONTROL Analytics events] requiere una licencia de Adobe Analytics. Una vez configurada la [[!DNL Analytics] extensión](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-analytics#configure-analytics-extension-in-launch) y que haya agregado [Analytics a su aplicación](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-analytics#add-analytics-to-your-app), estos eventos estarán disponibles en la configuración [!UICONTROL In-App] en ACS.

## Recursos adicionales

* [Habilitar métricas del ciclo vital (documentación)](https://aep-sdks.gitbook.io/docs/getting-started/initialize-the-sdk#enable-lifecycle-metrics)
