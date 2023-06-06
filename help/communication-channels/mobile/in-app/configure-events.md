---
title: Configuración de eventos
description: '"Descubra cómo los eventos definen qué acción iniciada por el usuario déclencheur que se muestre un mensaje en la aplicación. ”'
feature: In App
kt: 2548
thumbnail: 26245.jpg
doc-type: feature video
activity: use
team: TM
exl-id: 2c7937f4-b0da-46e5-934e-c660012c2c6f
role: User, Developer
level: Beginner, Intermediate
source-git-commit: 56b973566e9dee412aeee1412fe6271537fc1295
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 2%

---

# Configurar [!UICONTROL Events] {#configuring-events}

Al configurar un [!UICONTROL In-App] Mensaje, debe definir qué acción iniciada por el usuario almacena en déclencheur el mensaje que se va a mostrar. Estas acciones se denominan [!UICONTROL events]. Tres categorías de [!UICONTROL events] están disponibles: [!UICONTROL Mobile Application events], [!UICONTROL Life-Cycle events], y [!UICONTROL Analytics events].

## [!UICONTROL Mobile Application Events] {#mobile-application-events}

[!UICONTROL Mobile Application events] son [!UICONTROL custom events] que se implementan en la aplicación móvil.

Algunos ejemplos son:

* Un cliente ha visto un artículo
* Un cliente agrega un artículo al carro de compras
* Abandono del carro
* Un cliente ha comprado algo

Debe configurar estos [!UICONTROL events] en Adobe Campaign. En el siguiente vídeo se describe cómo hacerlo.

>[!VIDEO](https://video.tv.adobe.com/v/26245?quality=12&learn=on)

## [!UICONTROL Life-Cycle events] {#life-cycle-events}

[!UICONTROL Lifecycle events] ya está listo para usar [!UICONTROL events]. Lo siguiente [!UICONTROL events] están disponibles:

* [!UICONTROL launched]
* [!UICONTROL upgraded]
* [!UICONTROL crashed]

Un ejemplo de caso de uso podría ser un mensaje que introduce nuevas funciones después de una actualización o una promoción de evento.

>[!NOTE]
>
>El [!UICONTROL Lifecycle module] debe configurarse en la aplicación móvil. Consulte aquí para obtener más información sobre [Cómo añadir el ciclo vital a la aplicación](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/mobile-core/lifecycle)

## [!UICONTROL Analytics Events] {#analytics-events}

Se admiten las tres categorías siguientes en función de la instrumentación de la aplicación móvil:

* Adobe Analytics
* [!UICONTROL Context data]
* [!UICONTROL View state]

>[!NOTE]
>
>[!UICONTROL Analytics events] requiere una licencia de Adobe Analytics. Una vez que tenga el [!DNL Analytics] configurado y haya añadido Analytics a su aplicación, estos eventos estarán disponibles en el [!UICONTROL In-App] en ACS.
