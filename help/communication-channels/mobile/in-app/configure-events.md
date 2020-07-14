---
title: Configurar Eventos
description: 'Al configurar un mensaje en la aplicación en eventos de Adobe Campaign Standard (ACS), defina qué acción iniciada por el usuario activará la visualización del mensaje. '
feature: In-App
topics: Mobile
kt: 2548
doc-type: feature video
activity: use
team: TM
translation-type: tm+mt
source-git-commit: 82fb2d39dc61a55c0aa20ca1fa215f35a7dd9088
workflow-type: tm+mt
source-wordcount: '220'
ht-degree: 1%

---


# Configurar [!UICONTROL Events] {#configuring-events}

Al configurar un [!UICONTROL In-App] mensaje, debe definir qué acción iniciada por el usuario activa la visualización del mensaje. Se llaman a estas acciones [!UICONTROL events]. Hay tres categorías disponibles de [!UICONTROL events] : [!UICONTROL Mobile Application events], [!UICONTROL Life Cycle events], y [!UICONTROL Analytics events].

## [!UICONTROL Mobile Application Events] {#mobile-application-events}

[!UICONTROL Mobile Application events] que [!UICONTROL custom events] están implementadas en la aplicación móvil.

Algunos ejemplos son:

* Un cliente ha visto un artículo
* Un cliente agrega un artículo al carro
* Abandono del carro de compras
* Un cliente ha comprado algo

Debe configurarlos [!UICONTROL events] en Adobe Campaign. El siguiente vídeo describe cómo hacerlo.

>[!VIDEO](https://video.tv.adobe.com/v/26245?quality=12)

## [!UICONTROL Life Cycle events]  {#life-cycle-events}

[!UICONTROL Lifecycle events] están listos para usar [!UICONTROL events]. The following [!UICONTROL events] are available:

* [!UICONTROL launched]
* [!UICONTROL upgraded]
* [!UICONTROL crashed]

Un caso de uso de ejemplo podría ser un mensaje que introduce nuevas funciones después de una actualización o una promoción de evento.

>[!NOTE]
>
>El [!UICONTROL Lifecycle module] debe configurarse en la aplicación móvil. Consulte aquí para obtener más información sobre [cómo agregar el ciclo vital a la aplicación](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/mobile-core/lifecycle)

## [!UICONTROL Analytics Events] {#analytics-events}

Se admiten las tres categorías siguientes en función de la instrumentación de la aplicación móvil:

* Adobe Analytics
* [!UICONTROL Context data]
* [!UICONTROL View state]

>[!NOTE]
>
>[!UICONTROL Analytics events] requiere una licencia de Adobe Analytics. Una vez configurada [[!DNL Analytics] la](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-analytics#configure-analytics-extension-in-launch) extensión y que haya agregado [Analytics a la aplicación](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-analytics#add-analytics-to-your-app), estos eventos estarán disponibles en la configuración de ACS [!UICONTROL In-App] .

## Recursos adicionales

* [Habilitar métricas del ciclo vital (documentación)](https://aep-sdks.gitbook.io/docs/getting-started/initialize-the-sdk#enable-lifecycle-metrics)
