---
title: 'Solicitudes de privacidad con Adobe Campaign Standard (ACS): Información general'
description: El tutorial explica cómo crear solicitudes de privacidad a través de la interfaz de Adobe Campaign Standard.
feature: Herramientas de privacidad
kt: 1480
doc-type: feature video
activity: use
team: TM
exl-id: fb766403-694c-4a7b-b3d1-4a418df85891
source-git-commit: 481cbdcc9ac7446cc36fbff6e3d6e43fe333d30b
workflow-type: tm+mt
source-wordcount: '351'
ht-degree: 62%

---

# Solicitudes de privacidad con la interfaz de usuario de Adobe Campaign Standard

Adobe Campaign ofrece a los responsables del tratamiento de datos tres métodos para realizar solicitudes de acceso y eliminación en relación con la información personal identificable de conformidad con las leyes sobre privacidad, como el RGPD (Reglamento General de Protección de Datos) y la CCPA (Ley de Privacidad del Consumidor de California):

* **A través de la integración del Servicio principal de privacidad:** Las solicitudes de privacidad enviadas desde [!UICONTROL Privacy Service] a todas las soluciones de Experience Cloud las gestiona Campaign de forma automática a través de un flujo de trabajo dedicado. Para aprender a crear solicitudes de privacidad desde el Servicio principal de privacidad, consulte [Adobe Experience Platform Privacy Service](https://www.adobe.io/apis/experienceplatform/gdpr.html)

* **A través de la API:** Adobe Campaign proporciona una API que permite el procesamiento automático de solicitudes de privacidad mediante REST

* **A través de la interfaz de Adobe Campaign:** por cada solicitud de privacidad, el controlador de datos crea una solicitud de privacidad en Adobe Campaign

>[!NOTE]
>
> **CAMBIOS CON ACS 19.4:**
> 
> La integración de [Privacy Service](https://www.adobe.io/apis/experienceplatform/gdpr.html) es el método que debería usar para todas las solicitudes de acceso y eliminación. A partir de la versión 19.4, el uso de la API y de la interfaz de Campaign para las solicitudes de acceso y eliminación quedarán obsoletas. Para obtener más información sobre las funciones obsoletas y eliminadas de Campaign Standard, consulte [esta página](https://experienceleague.adobe.com/docs/campaign-standard/using/release-notes/deprecated-features.html?lang=en).
>
>**Exclusión para la venta de información personal (CCPA)**
>
> El campo Exclusión de la CCPA se proporciona de forma predeterminada en la interfaz y la API de Campaign.
>
> Puede comprobar su versión, haga clic en **?** en la parte superior derecha de la interfaz y seleccione Acerca de.

## Tutoriales en vídeo

### Requisitos previos para las solicitudes de privacidad

1. [Creación de un área de nombres](/help/privacy/namespaces-for-privacy-requests.md)
1. [Modificación de recursos personalizados](/help/privacy/custom-resources-for-privacy-requests.md)

### Cree, rastree y ejecute solicitudes de privacidad a través de la interfaz de usuario de Adobe Campaign

* [Creación y seguimiento de solicitudes de privacidad a través de la interfaz de usuario de Adobe Campaign](/help/privacy/create-and-track-privacy-requests.md)
* [Ejecución de solicitudes de privacidad](/help/privacy/execute-privacy-requests.md)

## Recursos adicionales

* [Directrices generales de privacidad para Campaign](https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/privacy/privacy-management.html?lang=en#getting-started)
* [CCPA para ACS](https://experienceleague.adobe.com/docs/campaign-standard/using/getting-started/privacy/privacy-requests.html?lang=en#privacy-requests)
* [Adobe Experience Platform Privacy Service](https://www.adobe.io/apis/experienceplatform/gdpr.html)
* [Documentación de la API REST de Adobe Campaign Standard](https://final-docs.campaign.adobe.com/doc/standard/en/api/ACS_API.html#privacy-management)
