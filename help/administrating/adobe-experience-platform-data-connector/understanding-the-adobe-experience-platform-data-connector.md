---
title: Comprender el conector de datos de Adobe Experience Platform
description: El conector de datos de Adobe Experience Platform ayuda a los clientes existentes a ofrecer sus datos en Adobe Experience Platform asignando datos XTK (datos incorporados en Campaign) a datos del modelo de datos de experiencia (XDM) en Adobe Experience Platform.
feature: People Core Service Integration
jira: KT-2826
thumbnail: 27304.jpg
role: User
level: Experienced
doc-type: feature video
activity: understand
team: TM
exl-id: 686961f9-5374-4cc6-8b36-7ee0584ea720
source-git-commit: d46e4c84a7d162085016722005cca4aadb4feb3c
workflow-type: tm+mt
source-wordcount: '268'
ht-degree: 4%

---

# Comprender Adobe Experience Platform [!UICONTROL Data Connector]

>[!NOTE]
>
>Esta funcionalidad está en versión beta y sujeta a frecuentes actualizaciones y modificaciones sin previo aviso.
>
>Póngase en contacto con [!UICONTROL Adobe Customer Support] si planea implementar esta capacidad.

## Información general

Adobe Experience Platform [!UICONTROL Data Connector] ayuda a los clientes existentes a hacer que sus datos estén disponibles en Adobe Experience Platform asignando datos XTK (datos incorporados en Adobe Campaign) a [!DNL Experience Data Model] Datos de (XDM) en Adobe Experience Platform.

El conector es unidireccional y envía los datos de Adobe Campaign Standard a Adobe Experience Platform. Los datos nunca se envían desde Adobe Experience Platform a Adobe Campaign Standard.

Adobe Experience Platform [!UICONTROL Data Connector] está dirigido a ingenieros de datos que comprenden Adobe Campaign Standard [!UICONTROL custom resources] y comprenda cómo debe estar el esquema de datos general del cliente dentro de Adobe Experience Platform.

>[!VIDEO](https://video.tv.adobe.com/v/27304?quality=12&learn=on)

*Este vídeo ofrece información general sobre Adobe Experience Platform [!UICONTROL Data Connector] (09:35 min)*

>[!NOTE]
>
>La transferencia lista para usar de [!UICONTROL subscription events] no es compatible. Para transferir [!UICONTROL subscription events], puede crear el XDM y el conjunto de datos correspondientes en Adobe Experience Platform y, a continuación, configurar una asignación de datos personalizada para estos datos.
>
>Existente [!UICONTROL experience events] no se puede ingerir en Adobe Experience Platform, pero se está generando [!UICONTROL experience events] se transmiten a Adobe Experience Platform.

## Pasos clave para realizar una asignación de datos

En los siguientes tutoriales se describen los pasos clave para realizar una asignación de datos entre Campaign Standard y Adobe Experience Platform:

1. [Asignación de recursos personalizados](/help/administrating/adobe-experience-platform-data-connector/mapping-custom-resources.md)
2. [Asignación de eventos de experiencias](/help/administrating/adobe-experience-platform-data-connector/mapping-experience-events.md)
3. [Asignación de datos de tabla semilla](/help/administrating/adobe-experience-platform-data-connector/mapping-seed-table-data.md)
4. [Modificación de la asignación de datos](/help/administrating/adobe-experience-platform-data-connector/modifying-data-mapping.md)
5. [Comprobación del estado de un trabajo de ingesta de datos](/help/administrating/adobe-experience-platform-data-connector/checking-status-of-data-ingestion-jobs.md)

