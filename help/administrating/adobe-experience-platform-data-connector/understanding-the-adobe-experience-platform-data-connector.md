---
title: Explicación del conector de datos de Adobe Experience Platform
description: El conector de datos de Adobe Experience Platform ayuda a los clientes existentes a poner sus datos a disposición en el Adobe Experience Platform mediante la asignación de datos XTK (datos ingestados en Campaña) a datos del modelo de datos de experiencia (XDM) en el Adobe Experience Platform.
feature: Adobe Experience Platform Data Connector
topics: ACoP
kt: 2826
doc-type: feature video
activity: understand
team: TM
translation-type: tm+mt
source-git-commit: cb5d5bc58137fd374eafe165c6ea13288a60d7db
workflow-type: tm+mt
source-wordcount: '343'
ht-degree: 5%

---


# Explicación del Adobe Experience Platform [!UICONTROL Data Connector]

>[!NOTE]
>
>Esta capacidad está actualmente en fase beta y sujeta a frecuentes actualizaciones y modificaciones sin previo aviso.
>
>Póngase en contacto con [!UICONTROL Adobe Customer Support] si tiene previsto implementar esta capacidad.

## Información general

Adobe Experience Platform [!UICONTROL Data Connector] ayuda a los clientes existentes a poner sus datos a disposición en Adobe Experience Platform mediante la asignación de datos XTK (datos ingestados en Adobe Campaign) a datos [!DNL Experience Data Model] (XDM) en Adobe Experience Platform.

Tenga en cuenta que el conector es unidireccional y envía los datos de Adobe Campaign Standard a Adobe Experience Platform. Los datos nunca se envían del Adobe Experience Platform al Adobe Campaign Standard.

Adobe Experience Platform [!UICONTROL Data Connector] está dirigido a ingenieros de datos que entienden el Adobe Campaign Standard [!UICONTROL custom resources] y comprenden cómo debe estar dentro del Adobe Experience Platform el esquema general de datos del cliente.

>[!VIDEO](https://video.tv.adobe.com/v/27304?quality=12)

*Este vídeo ofrece información general sobre el Adobe Experience Platform[!UICONTROL Data Connector](09:35 min)*

>[!NOTE]
>
>No se admite la transferencia predeterminada de [!UICONTROL subscription events] . Para transferir [!UICONTROL subscription events], puede crear el XDM y el conjunto de datos correspondientes en Adobe Experience Platform y, a continuación, configurar una asignación de datos personalizada para estos datos.
>
>Los datos existentes [!UICONTROL experience events] no se pueden ingerir en Adobe Experience Platform, pero los generados en curso [!UICONTROL experience events] se transmitirán al Adobe Experience Platform.

## Pasos clave para realizar una asignación de datos

Los siguientes tutoriales describen los pasos clave para realizar una asignación de datos entre Campaign Standard y Adobe Experience Platform:

1. [Asignación de recursos personalizados](/help/administrating/adobe-experience-platform-data-connector/mapping-custom-resources.md)
2. [Asignación de Eventos de experiencias](/help/administrating/adobe-experience-platform-data-connector/mapping-experience-events.md)
3. [Asignación de datos de tabla de raíz](/help/administrating/adobe-experience-platform-data-connector/mapping-seed-table-data.md)
4. [Modificación de la asignación de datos](/help/administrating/adobe-experience-platform-data-connector/modifying-data-mapping.md)
5. [Comprobación del estado de los trabajos de inserción de datos](/help/administrating/adobe-experience-platform-data-connector/checking-status-of-data-ingestion-jobs.md)

## Recursos adicionales

* [Acerca de Adobe Experience Platform Data Connector](https://docs.adobe.com/content/help/en/campaign-standard/using/administrating/mapping-campaign-and-aep-data/aep-about-data-connector.html)
* [Descripción general del modelo de datos de experiencia](https://docs.adobe.com/content/help/en/campaign-standard/using/administrating/mapping-campaign-and-aep-data/aep-data-model-overview.html)
* [Definición de la asignación](https://docs.adobe.com/content/help/en/campaign-standard/using/administrating/mapping-campaign-and-aep-data/aep-mapping-definition.html)
* [Activación de la asignación](https://docs.adobe.com/content/help/en/campaign-standard/using/administrating/mapping-campaign-and-aep-data/aep-mapping-activation.html)
* [Activación de la ingesta de datos mediante API](https://docs.adobe.com/content/help/en/campaign-standard/using/administrating/mapping-campaign-and-aep-data/aep-triggering-data-ingestion.html)
