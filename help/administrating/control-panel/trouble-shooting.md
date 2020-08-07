---
title: Solución de problemas del Panel de control de Campaign
description: El Panel de control de Campaign le permite supervisar y administrar su almacenamiento SFTP por instancia y añadir direcciones IP a la lista de permitidos.
feature: Control Panel
topics: null
kt: 2938
doc-type: article
activity: use
team: PM
translation-type: tm+mt
source-git-commit: 2f0527f3d9e2248eea68079e00855cce7a96fce4
workflow-type: tm+mt
source-wordcount: '330'
ht-degree: 100%

---


# Solución de problemas del 

Obtenga información sobre cómo solucionar problemas al usar el Panel de control de Campaign.

## Inicio de sesión y página principal

Problemas que se producen en el inicio de sesión y la página principal.

### Síntoma: no se puede iniciar sesión en Adobe Experience Cloud

**Qué hacer:**
el usuario debe localizar su [!DNL IMS Org ID] (xxx). El administrador debe agregar al usuario al [!UICONTROL product profile] [!DNL “Campaign-xxx-Admins”] por cada instancia que desee administrar. Si el usuario es administrador de todas las instancias, es posible que tenga que agregarse como *[!UICONTROL user]*.

### Síntoma: Los vínculos en la [!UICONTROL Adobe Experience Cloud Home] para acceder a [!UICONTROL Control Panel] no aparecen para un usuario

**Causa:**
los usuarios no verán los vínculos hasta que se agreguen como usuarios a [!UICONTROL product profile] `Campaign-xxx-Administrators/Admin`

**Qué hacer:**
El administrador debe agregar el usuario al [!UICONTROL product profile] *[!DNL Campaign-xxx-Admins]* por cada instancia que desee administrar. Si el usuario es administrador de todas las instancias, es posible que tenga que agregarse como *[!UICONTROL user]*.

### Síntoma: Una instancia no aparece en el [!UICONTROL Control Panel]

**Causa:**
Es muy probable que el usuario deba agregarse como *[!UICONTROL user]* Perfil de producto `!DNL Campaign-xxx-Administrators/Admin` para la instancia que falta

**Qué hacer:**
El administrador debe agregar el usuario al Perfil de productos `Campaign-xxx-Admins` por cada instancia que desee administrar. Si el usuario es administrador de todas las instancias, es posible que tenga que agregarse como *[!UICONTROL user]*.

### Vídeos útiles

>[!VIDEO](https://video.tv.adobe.com/v/27183?quality=12)
*Comprobación de[!DNL IMS Org ID](00:26 min)*

>[!VIDEO](https://video.tv.adobe.com/v/27147?quality=12)
*Adición de un administrador al[!UICONTROL product profile]*[!DNL administrators]*para utilizarlo[!UICONTROL Control Panel](01:03 min)*

### Documentación útil

* [Exploración de [!UICONTROL Control Panel]](https://docs.adobe.com/content/help/es-ES/control-panel/using/control-panel-home.html)
* [Administración de permisos del [!UICONTROL Control Panel]](https://docs.adobe.com/content/help/es-ES/control-panel/using/control-panel-home.html)

## Establecimiento de la conexión con el servidor SFTP (cliente o API)

La conexión a los servidores SFTP requiere lo siguiente:

* Añadir a la [!UICONTROL allow listing] la dirección IP desde la que se conecta al servidor SFTP
* Par de claves públicas/privadas que debe registrarse con Adobe Campaign
* Si se conecta directamente al servidor SFTP, también necesitará el software de cliente SFTP

### Documentación útil

* [Inicio de sesión en el servidor SFTP](https://docs.adobe.com/content/help/es-ES/control-panel/using/control-panel-home.html#LoggingintoyourSFTPserver)

