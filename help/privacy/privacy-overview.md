---
title: 'Solicitudes de privacidad con Adobe Campaign Standard (ACS): Información general'
description: El tutorial explica cómo crear solicitudes de privacidad mediante la interfaz de Adobe Campaign Standard (ACS).
feature: GDPR, CCAP
topic: Privacy
kt: 1480
doc-type: feature video
activity: use
team: TM
translation-type: ht
source-git-commit: 556bff4c94e16d3a94561dee1ccb311bc003b631
workflow-type: ht
source-wordcount: '371'
ht-degree: 100%

---


# Solicitudes de privacidad con la interfaz de usuario de Adobe Campaign Standard

Adobe Campaign ofrece a los responsables del tratamiento de datos tres métodos para realizar solicitudes de acceso y eliminación en relación con la información personal identificable de conformidad con las leyes sobre privacidad, como el RGPD (Reglamento General de Protección de Datos) y la CCPA (Ley de Privacidad del Consumidor de California):

* **A través de la integración del Servicio principal de privacidad:** Las solicitudes de privacidad enviadas desde [!UICONTROL Privacy Service] a todas las soluciones de Experience Cloud las gestiona Campaign de forma automática a través de un flujo de trabajo dedicado. Consulte [Adobe Experience Platform Privacy Service](https://adobe.io/apis/cloudplatform/gdpr.html) para obtener información sobre cómo crear solicitudes de privacidad desde el Servicio principal de privacidad

* **A través de la API:** Adobe Campaign proporciona una API que permite el procesamiento automático de solicitudes de privacidad mediante REST

* **A través de la interfaz de Adobe Campaign:** Por cada solicitud de privacidad, el controlador de datos crea una nueva solicitud de privacidad en Adobe Campaign

>[!NOTE]
>
> **CAMBIOS CON ACS 19.4:**
> 
> La integración de [Privacy Service](https://adobe.io/apis/cloudplatform/gdpr.html) es el método que debería usar para todas las solicitudes de acceso y eliminación. A partir de la versión 19.4, el uso de la API y de la interfaz de Campaign para las solicitudes de acceso y eliminación quedarán obsoletas. Para obtener más información sobre las funciones obsoletas y eliminadas de Campaign Standard, consulte [esta página](https://helpx.adobe.com/es/campaign/kb/acs-deprecated-and-removed-features.html).
>
>**Exclusión para la venta de información personal (CCPA)**
>
>A partir de la versión 19.4, el campo Exclusión de la CCPA vendrá de serie en la interfaz y la API de Campaign. Para utilizar esta información en la versión 19.3, debe crear este campo en Adobe Campaign Standard. Consulte la [documentación detallada](https://helpx.adobe.com/es/campaign/kb/acs-privacy.html#ccpa) para obtener más información.
>
> Puede comprobar la versión haciendo clic en el icono ? en la parte superior derecha de la interfaz y seleccione Acerca de.

## Tutoriales en vídeo

### Requisitos previos para las solicitudes de privacidad

1. [Creación de un área de nombres](/help/privacy/namespaces-for-privacy-requests.md)
1. [Modificación de recursos personalizados](/help/privacy/custom-resources-for-privacy-requests.md)

### Cree, rastree y ejecute solicitudes de privacidad a través de la interfaz de usuario de Adobe Campaign

* [Creación y seguimiento de solicitudes de privacidad a través de la interfaz de usuario de Adobe Campaign](/help/privacy/create-and-track-privacy-requests.md)
* [Ejecución de solicitudes de privacidad](/help/privacy/execute-privacy-requests.md)

## Recursos adicionales

* [Directrices generales de privacidad para Campaign](https://helpx.adobe.com/es/campaign/kb/campaign-privacy-overview.html)
* [CCPA para ACS](https://helpx.adobe.com/es/campaign/kb/acs-privacy.html#ccpa)
* [Adobe Experience Platform Privacy Service](https://adobe.io/apis/cloudplatform/gdpr.html)
* [Documentación de la API REST de Adobe Campaign Standard](https://final-docs.campaign.adobe.com/doc/standard/en/api/ACS_API.html#privacy-management)
