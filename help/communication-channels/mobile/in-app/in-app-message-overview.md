---
title: Introducción a los mensajes en la aplicación
description: Obtenga información sobre cómo presentar al usuario mensajes en la aplicación contextualmente relevantes en respuesta al comportamiento de un cliente en tiempo real dentro de la aplicación móvil.
feature: In App
kt: 1911
doc-type: feature video
activity: use
team: TM
exl-id: c51716eb-7239-4fc0-9ccf-9f5f0a5fae65
role: User
level: Beginner
source-git-commit: 30e8e10575aad4dcf2b0473cdd9fd6d5fc2815f4
workflow-type: tm+mt
source-wordcount: '728'
ht-degree: 11%

---

# Introducción a [!UICONTROL In-App] messages {#introduction}

La variable [!UICONTROL In-App Messaging] canal le permite mostrar un mensaje cuando el usuario está activo en la aplicación móvil. Este canal requiere que las aplicaciones móviles estén integradas con [!UICONTROL Adobe Experience Platform SDK].

Este tutorial explica los pasos necesarios para configurar las propiedades móviles: [!UICONTROL Launch] para la variable [!UICONTROL In-App Messaging] canal, y cómo preparar, personalizar y enviar [!UICONTROL In-App] en Adobe Campaign Standard. Los vínculos conducen a los tutoriales en vídeo sobre cada uno de los temas destacados.

## Requisitos previos {#prerequisites}

1. Asegúrese de que puede acceder a la variable **[!UICONTROL In-App]** canal. Si no puede acceder a estos canales, póngase en contacto con el equipo de su cuenta.
1. Compruebe que su **usuario** tiene **permissions** en Adobe Campaign Standard y [!UICONTROL Launch].

   1. En Adobe Campaign Standard, asegúrese de que el usuario de IMS forma parte del [!UICONTROL Standard User] y [!UICONTROL Administrator] grupos.

      Este paso permite al usuario iniciar sesión en Adobe Campaign Standard, navegar a la página de la aplicación móvil del SDK de Experience Platform y ver las propiedades de la aplicación móvil que ha creado en [!UICONTROL Launch].

   1. En [!UICONTROL Launch], asegúrese de que su usuario de IMS forme parte de un [!UICONTROL Launch] perfil de producto. Este paso permite al usuario iniciar sesión en [!UICONTROL Launch] para crear y ver las propiedades. En el perfil de producto, no debe haber permisos establecidos en la empresa o en las propiedades, pero el usuario debe poder iniciar sesión.

1. En Adobe Experience Platform Launch:

   1. Cree la aplicación móvil creando una propiedad móvil e instrumente la aplicación móvil con el SDK de Experience Platform.
   1. Instale el **Adobe Campaign Standard** para su aplicación móvil.

Para obtener más información sobre las extensiones, consulte [Configuración de la extensión de Campaign Standard en Adobe Launch](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-campaign-standard) en la documentación.

## Pasos para configurar [!UICONTROL In-App] messages {#steps-to-set-up}

1. [Configuración de una aplicación móvil mediante el SDK de Adobe Experience Platform](/help/communication-channels/mobile/configure-mobile-apps-using-aep-sdk.md).
1. [Configurar eventos](/help/communication-channels/mobile/in-app/configure-events.md).

## Crear, administrar y publicar [!UICONTROL In-App] Entregas {#create-manage-publish}

Puede crear envíos en la aplicación una vez haciendo clic en el botón **[!UICONTROL Create an In-App Message]** tarjeta de la página principal, desde la [!UICONTROL Marketing Activities]o puede [Creación de un envío en la aplicación dentro de un flujo de trabajo](/help/communication-channels/mobile/in-app/in-app-activity.md).

Al configurar la entrega, tiene tres opciones para dirigirse a los usuarios eligiendo entre diferentes plantillas de envío:

1. [**Publicación de un mensaje en la aplicación**](/help/communication-channels/mobile/in-app/broadcast-in-app-message.md) para dirigirse a todos los usuarios de una aplicación móvil.

   Este tipo de mensaje le permite enviar mensajes a todos los usuarios (actuales o futuros) de la aplicación móvil aunque no tengan un perfil existente en Adobe Campaign. Por lo tanto, la personalización no es posible cuando se personalizan los mensajes, ya que el perfil de usuario no existe necesariamente en Adobe Campaign.

1. Diríjase a todos los usuarios según su perfil de aplicación móvil.

   Este tipo de mensaje le permite dirigirse a todos los usuarios conocidos o anónimos de una aplicación móvil que tengan un perfil móvil en Adobe Campaign. Este tipo de mensajes se puede personalizar utilizando únicamente atributos no personales y no confidenciales y no requiere un protocolo de autenticación seguro entre el SDK móvil y el servicio de mensajería en la aplicación de Adobe Campaign. Por lo tanto, la estrategia de personalización se basa en lo que ha aprendido sobre los usuarios a partir de su interacción con el dispositivo. Por ejemplo, diríjase a todos los usuarios que hayan iniciado la aplicación más de cinco veces en la última semana.

1. [**Usuarios de destino según su perfil de Campaign**](/help/communication-channels/mobile/in-app/target-users-based-on-campaign-profile.md).

   Este tipo de mensaje le permite dirigirse a perfiles de Adobe Campaign (perfiles CRM) que se han suscrito a su aplicación móvil. El mensaje se puede personalizar con todos los atributos de perfil disponibles en Adobe Campaign. Requiere un protocolo de enlace seguro entre el SDK móvil y el servicio de mensajería en la aplicación de Campaign para garantizar que solo los usuarios autorizados utilicen mensajes con información personal y confidencial.

Esta plantilla es útil para admitir casos de uso de orquestación entre canales, ya que ya ha segmentado usuarios en otros canales, como Correo electrónico o Push. En función de su respuesta, quiere que participen con un mensaje en la aplicación.

## Informar sobre los envíos en la aplicación {#report}

Una vez publicado el envío, puede [informe sobre su envío en la aplicación](/help/communication-channels/mobile/in-app/in-app-reporting.md).

## Recursos adicionales

* [Informe en la aplicación](https://experienceleague.adobe.com/docs/campaign-standard/using/reporting/list-of-reports/in-app-report.html?lang=en)
* [Configuración de una propiedad móvil](https://aep-sdks.gitbook.io/docs/getting-started/create-a-mobile-property)
* [Configuración de una aplicación móvil mediante los SDK para Adobe Experience Platform](https://experienceleague.adobe.com/docs/campaign-standard/using/administrating/configuring-channels/configuring-a-mobile-application.html?lang=en)
* [Preparación y envío de un mensaje en la aplicación](https://experienceleague.adobe.com/docs/campaign-standard/using/communication-channels/in-app-messaging/preparing-and-sending-an-in-app-message.html?lang=en)
* [Personalización de un mensaje en la aplicación](https://experienceleague.adobe.com/docs/campaign-standard/using/communication-channels/in-app-messaging/customizing-an-in-app-message.html?lang=en)
* [Envío de un mensaje en la aplicación dentro de un flujo de trabajo](https://experienceleague.adobe.com/docs/campaign-standard/using/managing-processes-and-data/channel-activities/in-app-delivery.html?lang=en)
* [Habilitar métricas del ciclo vital](https://aep-sdks.gitbook.io/docs/getting-started/initialize-the-sdk#enable-lifecycle-metrics)
