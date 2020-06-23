---
title: Problemas al disparar al Panel de control
description: El Panel de control le permite supervisar y administrar su almacenamiento SFTP por instancia y permitir listas de direcciones IP.
feature: Control Panel
topics: null
kt: 2938
doc-type: article
activity: use
team: PM
translation-type: tm+mt
source-git-commit: b277b1ad17d9c03b307f8483d776b796e6c0cbef
workflow-type: tm+mt
source-wordcount: '336'
ht-degree: 1%

---


# Solución de problemas al disparar el [!UICONTROL Panel de control}

Obtenga información sobre cómo solucionar problemas al utilizar el Panel de control.

## Inicio de sesión y página principal

Problemas que se producen con el inicio de sesión y la página principal.

### Síntoma: No se puede iniciar sesión en Adobe Experience Cloud

**Qué hacer:**
El usuario debe localizar su [!DNL IMS Org ID] (xxx). El administrador debe agregar el usuario al [!UICONTROL product profile] para cada instancia [!DNL “Campaign-xxx-Admins”] que desee administrar. Si el usuario es administrador de todas las instancias, es posible que tenga que agregarse como *[!UICONTROL user]*.

### Síntoma: Los vínculos en el [!UICONTROL Adobe Experience Cloud Home] vínculo de acceso [!UICONTROL Control Panel] no aparecen para un usuario

**Causa:**
Los usuarios no verán los vínculos hasta que se agreguen como usuarios a [!UICONTROL product profile] `Campaign-xxx-Administrators/Admin`

**Qué hacer:**
El administrador debe agregar el usuario al [!UICONTROL product profile] para cada instancia *[!DNL Campaign-xxx-Admins]* que desee administrar. Si el usuario es administrador de todas las instancias, es posible que tenga que agregarse como *[!UICONTROL user]*.

### Síntoma: Una instancia no aparece en la lista de [!UICONTROL Control Panel]

**Causa:**
Es muy probable que el usuario deba agregarse como Perfil *[!UICONTROL user]* de producto `!DNL Campaign-xxx-Administrators/Admin` para la instancia que falta

**Qué hacer:**
El administrador debe agregar el usuario al Perfil de productos `Campaign-xxx-Admins` para cada instancia que desee administrar. Si el usuario es administrador de todas las instancias, es posible que tenga que agregarse como *[!UICONTROL user]*.

### Vídeos útiles

>[!VIDEO](https://video.tv.adobe.com/v/27183?quality=12)
*Comprobación[!DNL IMS Org ID](00:26 min)*

>[!VIDEO](https://video.tv.adobe.com/v/27147?quality=12)
*Cómo agregar un administrador al[!UICONTROL product profile]para poder *[!DNL administrators]*utilizarlo[!UICONTROL Control Panel](01:03 min)*

### Documentación útil

* [Descubrir el [!Panel de control UICONTROL]](https://helpx.adobe.com/campaign/kb/control-panel-overview.html)
* [Administración de permisos para el [!UICONTROL Panel de control]](https://helpx.adobe.com/campaign/kb/control-panel-access.html)

## Establecimiento de la conexión con el servidor SFTP (cliente o API)

La conexión a los servidores SFTP requiere:

* [!UICONTROL allow listing] la dirección IP desde la que se conecta al servidor SFTP
* Par de clave pública/privada que debe registrarse con Adobe Campaign
* Si se conecta directamente al servidor SFTP, también necesitará el software de cliente SFTP

### Documentación útil

* [Inicio de sesión en el servidor SFTP](https://helpx.adobe.com/campaign/kb/control-panel-sftp.html#LoggingintoyourSFTPserver)

