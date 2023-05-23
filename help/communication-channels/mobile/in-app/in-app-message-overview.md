---
title: Introducción a los mensajes en la aplicación
description: Aprenda a presentar al usuario mensajes en la aplicación relevantes para el contexto en respuesta al comportamiento en tiempo real de un cliente dentro de la aplicación móvil.
feature: In App
kt: 1911
doc-type: feature video
activity: use
team: TM
exl-id: c51716eb-7239-4fc0-9ccf-9f5f0a5fae65
role: User
level: Beginner
source-git-commit: 57dbf456625d22cd2e4526d92e5a8c20a048d339
workflow-type: tm+mt
source-wordcount: '629'
ht-degree: 10%

---

# Introducción a [!UICONTROL In-App] messages {#introduction}

El [!UICONTROL In-App Messaging] canal le permite mostrar un mensaje cuando el usuario está activo en la aplicación móvil. Este canal requiere que las aplicaciones móviles se integren con [!UICONTROL Adobe Experience Platform SDK].

Este tutorial explica los pasos necesarios para configurar las propiedades móviles, la variable [!UICONTROL Launch] extensión para [!UICONTROL In-App Messaging] y cómo preparar, personalizar y enviar mensajes [!UICONTROL In-App] mensajes en Adobe Campaign Standard. Los vínculos llevan a los tutoriales en vídeo sobre cada uno de los temas resaltados.

## Requisitos previos {#prerequisites}

1. Asegúrese de que puede acceder a **[!UICONTROL In-App]** canal. Si no puede acceder a estos canales, póngase en contacto con el equipo de su cuenta.
1. Compruebe que su **usuario** tiene lo necesario **permissions** en Adobe Campaign Standard y [!UICONTROL Launch].

   1. En Adobe Campaign Standard, asegúrese de que el usuario de IMS forme parte de la [!UICONTROL Standard User] y [!UICONTROL Administrator] grupos.

      Este paso permite al usuario iniciar sesión en Adobe Campaign Standard, navegar a la página de la aplicación móvil del SDK de Experience Platform y ver las propiedades de la aplicación móvil que ha creado en [!UICONTROL Launch].

   1. Entrada [!UICONTROL Launch], asegúrese de que el usuario de IMS forme parte de un [!UICONTROL Launch] perfil del producto. Este paso permite al usuario iniciar sesión en [!UICONTROL Launch] para crear y ver las propiedades. En el perfil del producto no debe haber permisos establecidos en la empresa o las propiedades, pero el usuario debe poder iniciar sesión.

1. En Adobe Experience Platform Launch:

   1. Cree la aplicación móvil creando una propiedad móvil e instrumente la aplicación móvil con el SDK de Experience Platform.
   1. Instale el **Adobe Campaign Standard** para su aplicación móvil.

Para obtener más información, consulte [Configuración de la extensión de Campaign Standard en Adobe Launch](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-campaign-standard) en la documentación.

## Pasos para la configuración [!UICONTROL In-App] messages {#steps-to-set-up}

1. [Configuración de una aplicación móvil mediante el SDK de Adobe Experience Platform](/help/communication-channels/mobile/configure-mobile-apps-using-aep-sdk.md).
1. [Configuración de eventos](/help/communication-channels/mobile/in-app/configure-events.md).

## Crear, administrar y publicar [!UICONTROL In-App] Envíos {#create-manage-publish}

Puede crear envíos únicos en la aplicación haciendo clic en el **[!UICONTROL Create an In-App Message]** de la página de inicio, de la [!UICONTROL Marketing Activities], o puede [Creación de un envío en la aplicación dentro de un flujo de trabajo](/help/communication-channels/mobile/in-app/in-app-activity.md).

Al configurar la entrega, tiene tres opciones para dirigirse a los usuarios eligiendo entre diferentes plantillas de entrega:

1. [**Publicación de un mensaje en la aplicación**](/help/communication-channels/mobile/in-app/broadcast-in-app-message.md) para dirigirse a todos los usuarios de una aplicación móvil.

   Este tipo de mensaje le permite enviar mensajes a todos los usuarios (actuales o futuros) de la aplicación móvil aunque no tengan un perfil existente en Adobe Campaign. Por lo tanto, la personalización no es posible cuando se personalizan los mensajes, ya que el perfil del usuario no existe necesariamente en Adobe Campaign.

1. Segmente a todos los usuarios en función de su perfil de aplicación móvil.

   Este tipo de mensaje le permite dirigirse a todos los usuarios conocidos o anónimos de una aplicación móvil que tengan un perfil móvil en Adobe Campaign. Este tipo de mensajes se puede personalizar utilizando únicamente atributos no personales y no confidenciales y no requiere un protocolo de autenticación seguro entre el SDK móvil y el servicio de mensajería en la aplicación de Adobe Campaign. Por lo tanto, la estrategia de personalización se basa en lo que ha aprendido acerca de los usuarios en su interacción con el dispositivo. Por ejemplo, diríjase a todos los usuarios que hayan iniciado su aplicación más de cinco veces en la última semana.

1. [**Usuarios de destino según su perfil de Campaign**](/help/communication-channels/mobile/in-app/target-users-based-on-campaign-profile.md).

   Este tipo de mensaje le permite dirigirse a perfiles de Adobe Campaign (perfiles CRM) que se han suscrito a su aplicación móvil. El mensaje se puede personalizar con todos los atributos de perfil disponibles en Adobe Campaign. Requiere un protocolo de enlace seguro entre el SDK móvil y el servicio de mensajería en la aplicación de Campaign para garantizar que los mensajes con información personal y confidencial sean utilizados únicamente por usuarios autorizados.

Esta plantilla es útil para admitir casos de uso de orquestación entre canales, en los que ya ha segmentado usuarios en otros canales como correo electrónico o push. En función de su respuesta, querrá que participen con un mensaje en la aplicación.

## Creación de informes sobre los envíos en la aplicación {#report}

Una vez publicada la entrega, puede hacer lo siguiente [Creación de informes sobre su envío en la aplicación](/help/communication-channels/mobile/in-app/in-app-reporting.md).
