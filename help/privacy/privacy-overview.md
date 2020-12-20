---
title: 'Solicitudes de privacidad con Adobe Campaign Standard (ACS): información general'
description: El tutorial explica cómo crear solicitudes de privacidad mediante la interfaz Adobe Campaign Standard (ACS).
feature: GDPR, CCAP
topic: Privacy
kt: 1480
doc-type: feature video
activity: use
team: TM
translation-type: tm+mt
source-git-commit: 556bff4c94e16d3a94561dee1ccb311bc003b631
workflow-type: tm+mt
source-wordcount: '368'
ht-degree: 25%

---


# Solicitudes de privacidad con la interfaz de usuario de Adobe Campaign Standard

Adobe Campaign oferta a los controladores de datos tres métodos para realizar el acceso a la privacidad y eliminar solicitudes de datos de PII de conformidad con leyes de privacidad como GDPR (General Data Protection Regulation) y CCPA (California Consumer Privacy Act):

* **Mediante la integración de Privacy Core Service:las solicitudes de** privacidad insertadas  [!UICONTROL Privacy Service] a todas las soluciones de Experience Cloud se gestionan automáticamente mediante la Campaña mediante un flujo de trabajo dedicado. Consulte [Adobe Experience Platform Privacy Service](https://adobe.io/apis/cloudplatform/gdpr.html) para obtener información sobre cómo crear solicitudes de privacidad desde el servicio principal de privacidad

* **A través de la API:** Adobe Campaign proporciona una API que permite el proceso automático de solicitudes de privacidad mediante REST

* **A través de la interfaz de Adobe Campaign:** para cada solicitud de privacidad, el controlador de datos crea una nueva solicitud de privacidad en Adobe Campaign

>[!NOTE]
>
> **CAMBIOS CON ACS 19.4:**
> 
> La [integración de Privacy Service](https://adobe.io/apis/cloudplatform/gdpr.html) es el método que debe utilizar para todas las solicitudes de acceso y eliminación. A partir de la versión 19.4, el uso de la API y la interfaz de Campaign para las solicitudes de acceso y eliminación quedarán obsoletas. Para obtener más información acerca de las funciones eliminadas y obsoletas del Campaign Standard, consulte [esta página](https://helpx.adobe.com/es/campaign/kb/acs-deprecated-and-removed-features.html).
>
>**Exclusión para la venta de información personal (CCPA)**
>
>A partir de la versión 19.4, el campo Exclusión de la CCPA vendrá de serie en la interfaz y la API de Campaign. Para 19.3, para aprovechar esta información, debe crear este campo en Adobe Campaign Standard. Consulte la [documentación detallada](https://helpx.adobe.com/es/campaign/kb/acs-privacy.html#ccpa) para obtener más información.
>
> Puede comprobar la versión haciendo clic en el icono ? en la parte superior derecha de la interfaz y seleccione Acerca de.

## Tutoriales en vídeo

### Requisitos previos para las solicitudes de privacidad

1. [Crear una Área de nombres](/help/privacy/namespaces-for-privacy-requests.md)
1. [Modificar recursos personalizados](/help/privacy/custom-resources-for-privacy-requests.md)

### Crear, rastrear y ejecutar solicitudes de privacidad a través de la interfaz de usuario de Adobe Campaign

* [Creación y seguimiento de solicitudes de privacidad a través de la interfaz de usuario de Adobe Campaign](/help/privacy/create-and-track-privacy-requests.md)
* [Ejecutar solicitudes de privacidad](/help/privacy/execute-privacy-requests.md)

## Recursos adicionales

* [Directrices generales de privacidad para Campaign](https://helpx.adobe.com/es/campaign/kb/campaign-privacy-overview.html)
* [CCPA para ACS](https://helpx.adobe.com/campaign/kb/acs-privacy.html#ccpa)
* [Adobe Experience Platform Privacy Service](https://adobe.io/apis/cloudplatform/gdpr.html)
* [Documentación de la API de Adobe Campaign Standard REST](https://final-docs.campaign.adobe.com/doc/standard/en/api/ACS_API.html#privacy-management)
