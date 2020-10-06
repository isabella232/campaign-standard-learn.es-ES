---
title: Panel de control de Campaign
description: El Panel de control de Campaign le permite supervisar y administrar su almacenamiento SFTP por instancia y añadir direcciones IP a la lista de permitidos.
feature: Control Panel
topics: Control Panel
kt: 4696
doc-type: feature video
activity: use
team: PM
translation-type: tm+mt
source-git-commit: a078367ce8ffece206d3b83bfeefc4df4f8078d6
workflow-type: tm+mt
source-wordcount: '364'
ht-degree: 100%

---


# [!UICONTROL Control Panel] {#control-panel}

>[!NOTE]
>
>Los términos &quot;[!UICONTROL whitelist]&quot; y &quot;[!UICONTROL blacklist]&quot; se han sustituido por &quot;[!UICONTROL allow list]&quot; y &quot;[!UICONTROL block list]&quot; en la documentación de Adobe Campaign. Algunas incidencias de estos términos pueden seguir existiendo en la interfaz de usuario del producto, los nombres de opciones, el código interno y los vídeos de tutoriales. Se reemplazarán en próximas versiones del panel de control de Campaign.

El [!UICONTROL Control Panel] permite a los administradores de Adobe Campaign monitorizar los activos clave y realizar tareas administrativas, como administrar el almacenamiento SFTP por instancia o por [!UICONTROL allow list] direcciones IP.

## Acceso [!UICONTROL Control Panel]

Para acceder al panel de control de Campaign, vaya a la página principal de Experience Cloud: [https://experiencecloud.adobe.com](https://experiencecloud.adobe.com):

* **[!UICONTROL Experience Cloud Home]** > **[!UICONTROL Quick Access]**

   o
* **[!UICONTROL Experience Cloud Home]**  > [!UICONTROL Solution picker]: **Campaign** > **[!UICONTROL Control Panel]tarjeta**

   o

* Directamente desde la dirección URL: [https://experience.adobe.com/#/controlpanel](https://experience.adobe.com/#/controlpanel)

## Requisitos previos

Antes de comenzar, complete los siguientes requisitos previos:

### Confirmar [!DNL IMS Org ID]

Debe conocer su [!DNL IMS org ID]. El siguiente vídeo describe dónde puede buscar la instancia de [!DNL IMS org ID].

>[!VIDEO](https://video.tv.adobe.com/v/27183?quality=12)

*Mire [!DNL IMS Org ID] (00:26 min)*

### Derechos de administrador

Se requieren derechos de administrador para acceder al [!UICONTROL Control Panel].
En el siguiente vídeo se explica cómo añadir un administrador a una instancia de Campaign

>[!VIDEO](https://video.tv.adobe.com/v/27147?quality=12)

*Cómo añadir un administrador al perfil de productos &quot;[!UICONTROL Administrators]&quot; para poder utilizarlo [!UICONTROL Control Panel] (1:03 min)*

## Tutoriales del Panel de control de Campaign

* **Administración de servidores SFTP**

   *Obtenga información sobre cómo monitorizar la capacidad del servidor, las listas de direcciones IP permitidas y la adición de claves SSH:*

   * [Monitorización de la capacidad del servidor, admisión de direcciones IP y adición de claves SSH](/help/administrating/control-panel/monitoring-server-capacity-allow-listing-adding-ssh-key.md)
   * [Generación de una clave SSH](/help/administrating/control-panel/generate-ssh-key.md)
   * [Conexión a un servidor SFTP](/help/administrating/control-panel/connect-to-sftp-server.md)
* **[Delegación de subdominios](/help/administrating/control-panel/subdomain-delegation.md)**

   *Aprenda a delegar completamente un subdominio a Adobe Campaign*
* **[Adición de certificados SSL](/help/administrating/control-panel/adding-ssl-certificates.md)**

   *Aprenda a añadir certificados SSL para proteger subdominios.*

* **[Administración de registros TXT de Google](/help/administrating/control-panel/google-txt-record-management.md)**

   *Aprenda a añadir el registro de verificación del sitio TXT de Google a todos los subdominios utilizados para enviar correos electrónicos a las direcciones de GMAIL a través del Panel de control de Campaign.*

* **Administración de claves GPG**

   *Aprenda cómo generar e instalar un par de claves pública y privada en una instancia específica de Campaign para el cifrado de datos salientes y para importar e instalar una clave pública en una instancia de Campaign para el descifrado de datos entrantes:*

   * [Generación e instalación de claves GPG para el cifrado de datos](./gpg-key-management/generating-and-installing-gpg-keys-for-data-encryption.md)
   * [Uso de una clave GPG para cifrar datos](./gpg-key-management/using-a-gpg-key-to-encrypt-data.md)
   * [Descifrado de datos](./gpg-key-management/decrypting-data.md)

* **[Solución de problemas](/help/administrating/control-panel/trouble-shooting.md)**

   *Solución de problemas del Panel de control de Campaign*

## Recursos adicionales

* [Centro de ayuda de panel de control de Campaign](https://docs.adobe.com/content/help/es-ES/control-panel/using/control-panel-home.html)

