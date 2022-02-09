---
title: Solución de problemas del Panel de control de Campaign
description: El Panel de control de Campaign le permite monitorizar y administrar su almacenamiento SFTP por instancia y lista de permitidos de direcciones IP.
feature: Control Panel
kt: 2938
doc-type: article
activity: use
team: PM
recommendations: noDisplay
exl-id: f546f791-a69b-4586-abfa-3e626b8feb17
source-git-commit: 57dbf456625d22cd2e4526d92e5a8c20a048d339
workflow-type: tm+mt
source-wordcount: '318'
ht-degree: 47%

---

# Solución de problemas del [!UICONTROL Control Panel]

Obtenga información sobre cómo solucionar problemas al usar el Panel de control de Campaign.

## Inicio de sesión y página principal

Problemas que se producen en el inicio de sesión y la página principal.

### Síntoma: No se puede iniciar sesión en Adobe Experience Cloud

**Qué hacer:**
El usuario debe localizar su [!DNL IMS Org ID] xxx. El administrador debe agregar el usuario al [!UICONTROL product profile] [!DNL “Campaign-xxx-Admins”] para cada instancia que desee administrar. Si el usuario es administrador de todas las instancias, debe añadirse como *[!UICONTROL user]*.

### Síntoma: Los vínculos en la [!UICONTROL Adobe Experience Cloud Home] para acceder a [!UICONTROL Control Panel] no aparecen para un usuario

**Causa:**
los usuarios no verán los vínculos hasta que se agreguen como usuarios a [!UICONTROL product profile] `Campaign-xxx-Administrators/Admin`

**Qué hacer:**
El administrador debe agregar el usuario al [!UICONTROL product profile] *[!DNL Campaign-xxx-Admins]* para cada instancia que desee administrar. Si el usuario es administrador de todas las instancias, debe añadirse como *[!UICONTROL user]*.

### Síntoma: una instancia no aparece en la lista de [!UICONTROL Control Panel]

**Causa:**
Lo más probable es que el usuario deba agregarse como *[!UICONTROL user]* Perfil del producto `Campaign-xxx-Administrators/Admin` para la instancia que falta

**Qué hacer:**
El administrador debe agregar el usuario al perfil de producto `Campaign-xxx-Admins` para cada instancia que desee administrar. Si el usuario es administrador de todas las instancias, debe añadirse como *[!UICONTROL user]*.

### Vídeos útiles

>[!VIDEO](https://video.tv.adobe.com/v/27183?quality=12)

*Mire [!DNL IMS Org ID] (00:26 min)*

>[!VIDEO](https://video.tv.adobe.com/v/27147?quality=12)

*Adición de un administrador al [!UICONTROL product profile] [!DNL administrators] para utilizarlo [!UICONTROL Control Panel] (01:03 min)*

### Documentación útil

* [Exploración de [!UICONTROL Control Panel]](https://experienceleague.adobe.com/docs/control-panel/using/control-panel-home.html?lang=es)
* [Administración de permisos del [!UICONTROL Control Panel]](https://experienceleague.adobe.com/docs/control-panel/using/control-panel-home.html?lang=en)

## Establecimiento de la conexión con el servidor SFTP (cliente o API)

La conexión a los servidores SFTP requiere lo siguiente:

* [!UICONTROL allow listing] la dirección IP desde la que se está conectando al servidor SFTP.
* Par de claves públicas/privadas que debe registrarse con Adobe Campaign
* Si se conecta directamente al servidor SFTP, necesitará el software de cliente SFTP

### Documentación útil {#helpful-docs}

* [Inicio de sesión en el servidor SFTP](https://experienceleague.adobe.com/docs/control-panel/using/control-panel-home.html?lang=en)
