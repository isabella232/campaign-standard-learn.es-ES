---
title: Introducción a los mensajes en la aplicación
description: El canal de mensajería en la aplicación de Adobe Campaign Standard (ACS) le permite presentar al usuario mensajes en la aplicación contextualmente relevantes en respuesta al comportamiento en tiempo real de un cliente dentro de la aplicación móvil.
feature: In-App
topics: Mobile
kt: 1911
doc-type: feature video
activity: use
team: TM
translation-type: tm+mt
source-git-commit: 82fb2d39dc61a55c0aa20ca1fa215f35a7dd9088
workflow-type: tm+mt
source-wordcount: '753'
ht-degree: 9%

---


# Introducción a los [!UICONTROL In-App] mensajes {#introduction}

El [!UICONTROL In-App Messaging] canal le permite mostrar un mensaje cuando el usuario está activo en la aplicación móvil. Este canal requiere que las aplicaciones móviles estén integradas con [!UICONTROL Adobe Experience Platform SDK].

En este tutorial se explican los pasos necesarios para configurar las propiedades móviles, la [!UICONTROL Launch] extensión del [!UICONTROL In-App Messaging] canal y cómo preparar, personalizar y enviar [!UICONTROL In-App] mensajes en Adobe Campaign Standard. Los vínculos le llevarán a los tutoriales de vídeo sobre cada uno de los temas destacados.

## Requisitos previos {#prerequisites}

1. Asegúrese de tener acceso al **[!UICONTROL In-App]** canal. Si no puede acceder a estos canales, póngase en contacto con el equipo de su cuenta.
1. Verify that your **user** has the necessary **permissions** in Adobe Campaign Standard and [!UICONTROL Launch].

   1. En Adobe Campaign Standard, asegúrese de que el usuario de IMS forme parte de los [!UICONTROL Standard User] grupos y [!UICONTROL Administrator] .\
      Este paso permite al usuario iniciar sesión en Adobe Campaign Standard, desplazarse a la página de la aplicación móvil del SDK de Experience Platform y realizar la vista de las propiedades de la aplicación móvil que ha creado en [!UICONTROL Launch].
   1. En [!UICONTROL Launch], asegúrese de que el usuario de IMS forme parte de un perfil de [!UICONTROL Launch] producto.\
      Este paso permite al usuario iniciar sesión para [!UICONTROL Launch] crear y vista de las propiedades. Para obtener más información sobre los perfiles de productos en [!UICONTROL Launch], consulte [Crear el perfil](https://docs.adobelaunch.com/launch-reference/administration/user-permissions#3-create-your-product-profile)del producto. En el perfil del producto, no debe haber permisos establecidos en la compañía o en las propiedades, pero el usuario debe poder iniciar sesión.

1. En Adobe Experience Platform Launch:

   1. Cree una propiedad móvil e instrumente la aplicación móvil con el SDK de Experience Platform.
   1. Instale la extensión de **Adobe Campaign Standard** para la aplicación móvil.

Para obtener más información sobre las extensiones, consulte la [sección Configurar extensión de Campaign Standard en Inicio](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-campaign-standard) de Adobe en la [!UICONTROL Adobe Launch ]documentación.

## Pasos para configurar [!UICONTROL In-App] mensajes {#steps-to-set-up}

1. [Configure una aplicación móvil mediante el SDK](/help/communication-channels/mobile/configure-mobile-apps-using-aep-sdk.md)de Adobe Experience Platform.

1. [Configurar eventos](/help/communication-channels/mobile/in-app/configure-events.md).

## Creación, gestión y publicación de [!UICONTROL In-App] Envíos {#create-manage-publish}

Puede crear envíos en la aplicación una sola vez haciendo clic en la **[!UICONTROL Create an In-App Message]** tarjeta desde la página principal, desde la [!UICONTROL Marketing Activities], o bien puede [crear un envío en la aplicación dentro de un flujo de trabajo](/help/communication-channels/mobile/in-app/in-app-activity.md).

Al configurar el envío, dispone de tres opciones para el destinatario de los usuarios eligiendo entre distintas Plantillas de envíos:

1. [**Retransmisión de un mensaje **](/help/communication-channels/mobile/in-app/broadcast-in-app-message.md)en la aplicación para destinatario a todos los usuarios de una aplicación móvil.

   Este tipo de mensaje le permite enviar mensajes a todos los usuarios (actuales o futuros) de la aplicación móvil aunque no tengan un perfil existente en Adobe Campaign. Por lo tanto, la personalización no es posible cuando se personalizan los mensajes, ya que el perfil del usuario no existe necesariamente en Adobe Campaign.

1. Destinatario a todos los usuarios en función del perfil de su aplicación móvil.

   Este tipo de mensaje permite el destinatario de todos los usuarios conocidos o anónimos de una aplicación móvil que tengan un perfil móvil en Adobe Campaign. Este tipo de mensajes se puede personalizar utilizando únicamente atributos no personales y no confidenciales y no requiere un protocolo de autenticación seguro entre el SDK móvil y el servicio de mensajería en la aplicación de Adobe Campaign. Por lo tanto, la estrategia de personalización se basa en lo que ha aprendido sobre los usuarios a partir de su interacción con el dispositivo. Por ejemplo: destinatario a todos los usuarios que han iniciado la aplicación más de 5 veces en la última semana.

1. [**Destinatario a los usuarios en función de su perfil **](/help/communication-channels/mobile/in-app/target-users-based-on-campaign-profile.md)de Campaña.

   Este tipo de mensaje le permite destinatario de perfiles de Adobe Campaign (perfiles CRM) que se han suscrito a su aplicación móvil. El mensaje se puede personalizar con todos los atributos de perfil disponibles en Adobe Campaign, pero requiere un protocolo de enlace seguro entre el SDK móvil y el servicio de mensajería en la aplicación de la Campaña para garantizar que los mensajes con información personal y confidencial sean utilizados únicamente por usuarios autorizados.

Esta plantilla es útil para admitir casos de uso de orquestación entre canales, en los que ya ha segmentado usuarios en otros canales como Correo electrónico o Push y, en función de su respuesta, desea interactuar con ellos mediante un mensaje en la aplicación.

## Informe de sus envíos en la aplicación {#report}

Una vez que el envío se haya publicado, puede [informar sobre su envío](/help/communication-channels/mobile/in-app/in-app-reporting.md)en la aplicación.

## Recursos adicionales

* [Informe en la aplicación](https://docs.adobe.com/content/help/en/campaign-standard/using/reporting/list-of-reports/in-app-report.html)
* [Configuración de una propiedad móvil](https://aep-sdks.gitbook.io/docs/getting-started/create-a-mobile-property)
* [Configuración de una aplicación móvil mediante SDK de Adobe Experience Platform](https://helpx.adobe.com/es/campaign/kb/configuring-app-sdk.html)
* [Preparación y envío de un mensaje en la aplicación](https://docs.adobe.com/content/help/en/campaign-standard/using/communication-channels/in-app-messaging/preparing-and-sending-an-in-app-message.html)
* [Personalización de un mensaje en la aplicación](https://docs.adobe.com/content/help/en/campaign-standard/using/communication-channels/in-app-messaging/customizing-an-in-app-message.html)
* [Envío de un mensaje en la aplicación dentro de un flujo de trabajo](https://docs.adobe.com/content/help/en/campaign-standard/using/managing-processes-and-data/channel-activities/in-app-delivery.html)
* [Habilitar métricas del ciclo vital](https://aep-sdks.gitbook.io/docs/getting-started/initialize-the-sdk#enable-lifecycle-metrics)
