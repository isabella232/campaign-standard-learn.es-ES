---
title: Explicación de Adobe Experience Platform Data Connector
description: Data Connectors de Adobe Experience Platform ayuda a los clientes existentes a poner sus datos a disposición en Adobe Experience Platform asignando datos XTK (datos incorporados en Campaign) a datos del Modelo de datos de Experience (XDM) en Adobe Experience Platform.
kt: 2826
thumbnail: 27304.jpg
doc-type: feature video
activity: understand
team: TM
exl-id: 686961f9-5374-4cc6-8b36-7ee0584ea720
source-git-commit: 5a2f8c9a78bf5100b272f9b4461131545b3aeb8b
workflow-type: tm+mt
source-wordcount: '343'
ht-degree: 10%

---

# Explicación de Adobe Experience Platform [!UICONTROL Data Connector]

>[!NOTE]
>
>Esta capacidad está actualmente en fase beta y sujeta a frecuentes actualizaciones y modificaciones sin previo aviso.
>
>Póngase en contacto con [!UICONTROL Adobe Customer Support] si planea implementar esta capacidad.

## Información general

Adobe Experience Platform [!UICONTROL Data Connector] ayuda a los clientes existentes a que hagan disponibles sus datos en Adobe Experience Platform asignando datos XTK (datos incorporados en Adobe Campaign) a datos [!DNL Experience Data Model] (XDM) en Adobe Experience Platform.

Tenga en cuenta que el conector es unidireccional y envía los datos de Adobe Campaign Standard a Adobe Experience Platform. Los datos nunca se envían de Adobe Experience Platform a Adobe Campaign Standard.

Adobe Experience Platform [!UICONTROL Data Connector] está diseñado para ingenieros de datos que entienden Adobe Campaign Standard [!UICONTROL custom resources] y que comprenden cómo debe estar el esquema de datos general del cliente dentro de Adobe Experience Platform.

>[!VIDEO](https://video.tv.adobe.com/v/27304?quality=12)

*Este vídeo ofrece información general sobre Adobe Experience Platform  [!UICONTROL Data Connector] (9:35 min)*

>[!NOTE]
>
>No se admite la transferencia predeterminada de [!UICONTROL subscription events]. Para transferir [!UICONTROL subscription events], puede crear el XDM y el conjunto de datos correspondientes en Adobe Experience Platform y, a continuación, configurar una asignación de datos personalizada para estos datos.
>
>No se puede ingerir el [!UICONTROL experience events] existente en Adobe Experience Platform, pero el [!UICONTROL experience events] generado en curso se transmitirá a Adobe Experience Platform.

## Pasos clave para realizar una asignación de datos

Los siguientes tutoriales describen los pasos clave para realizar una asignación de datos entre Campaign Standard y Adobe Experience Platform:

1. [Asignación de recursos personalizados](/help/administrating/adobe-experience-platform-data-connector/mapping-custom-resources.md)
2. [Asignación de eventos de experiencias](/help/administrating/adobe-experience-platform-data-connector/mapping-experience-events.md)
3. [Asignación de datos de tabla semilla](/help/administrating/adobe-experience-platform-data-connector/mapping-seed-table-data.md)
4. [Modificación de la asignación de datos](/help/administrating/adobe-experience-platform-data-connector/modifying-data-mapping.md)
5. [Comprobación del estado de los trabajos de ingesta de datos](/help/administrating/adobe-experience-platform-data-connector/checking-status-of-data-ingestion-jobs.md)

## Recursos adicionales

* [Acerca de Adobe Experience Platform Data Connector](https://docs.adobe.com/content/help/en/campaign-standard/using/administrating/mapping-campaign-and-aep-data/aep-about-data-connector.html)
* [Información general del Modelo de datos de experiencia](https://docs.adobe.com/content/help/en/campaign-standard/using/administrating/mapping-campaign-and-aep-data/aep-data-model-overview.html)
* [Definición de la asignación](https://docs.adobe.com/content/help/en/campaign-standard/using/administrating/mapping-campaign-and-aep-data/aep-mapping-definition.html)
* [Activación de la asignación](https://docs.adobe.com/content/help/en/campaign-standard/using/administrating/mapping-campaign-and-aep-data/aep-mapping-activation.html)
* [Activación de la ingesta de datos mediante API](https://docs.adobe.com/content/help/en/campaign-standard/using/administrating/mapping-campaign-and-aep-data/aep-triggering-data-ingestion.html)
