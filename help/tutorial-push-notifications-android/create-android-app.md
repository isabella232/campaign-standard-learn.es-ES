---
title: 'Paso 1: Creación de aplicaciones de Android y configuración para utilizar la mensajería en la nube de Firebase'
description: En esta parte [!DNL Android] App to receive [!UICONTROL Push notifications] crearemos a partir del Adobe Campaign Standard. Para poder recibir las notificaciones push, la aplicación debe registrarse en el registro de Google [!DNL Firebase Cloud Service].
feature: Push
topics: Mobile
kt: 4825
doc-type: tutorial
activity: use
team: TM
translation-type: tm+mt
source-git-commit: afe1ae6c8d73b7b776e0eec327fa16db76c23ce1
workflow-type: tm+mt
source-wordcount: '316'
ht-degree: 2%

---


# Paso 1: Creación de [!DNL Android] aplicaciones y configuración para su uso [!DNL Firebase Cloud Messaging]

En esta parte, creará [!DNL Android] la aplicación para recibir [!UICONTROL Push notifications] el envío desde Adobe Campaign Standard. Para recibir las notificaciones push, la aplicación debe registrarse en Google [!DNL Firebase Cloud Service].

1. Inicie sesión en su [!DNL Firebase] cuenta.

   [!DNL Firebase] es la plataforma móvil de Google que le ayuda a desarrollar rápidamente aplicaciones de alta calidad. Si no tiene una [!DNL Firebase] cuenta, cree una [desde aquí](https://firebase.google.com).

2. Iniciar [!DNL Android Studio]
3. Click **[!UICONTROL File]** > **[!UICONTROL New]** > **[!UICONTROL New Project].**
4. Seleccione **[!UICONTROL Empty Activity]** y haga clic en **[!UICONTROL Next].**

   ![android-project](assets/android-project.PNG)

5. Proporcione un nombre significativo al proyecto.

   A los efectos de esta demostración, hemos nombrado nuestro proyecto como *[!DNL ACSPushTutorial]*

   ![android-project-configuration](assets/android-project-configuration.PNG)

6. Acepte los nombres de paquete predeterminados y haga clic en **[!DNL Finish]** para crear el proyecto.
7. La estructura del proyecto debe ser similar a la de la captura de pantalla siguiente

   ![android-project-structure](assets/android-project-structure.PNG)

8. Haga clic en **[!UICONTROL Tools]** > **[!UICONTROL Firebase].**(esto agrega el proyecto a[!DNL Firebase])
9. Haga clic en **[!UICONTROL Set up Firebase Cloud Messaging].**

   ![configurar firebase](assets/android-project-firebase-messaging.PNG)

10. Haga clic en **[!UICONTROL Connect to Firebase].**
11. Una vez que la aplicación esté conectada a Firebase, haga clic en **[!UICONTROL Add FCM to your app].**
12. Haga clic en **[!UICONTROL Accept Changes].**

   Al agregar FCM a la aplicación, el asistente necesita su permiso para realizar algunos cambios en el proyecto.

   ![[!DNL add-fcm-to-your-app]](assets/firebase-add-fcm-to-app.PNG)

Si la aplicación se integra correctamente con Firebase, debería recibir un mensaje como el que se muestra a continuación:

![[!DNL fcm-successfull]](assets/android-firebase-success.PNG)

[Asegúrese de que el proyecto aparece en la [!DNL Firebase ]consola](https://console.firebase.google.com/)

## Configuración [!UICONTROL Push Channel] de configuración

1. Iniciar sesión en la [!DNL Firebase] consola
2. Abra el **[!UICONTROL ACSPushTutorial]** proyecto.
3. Haga clic en el icono **del** engranaje y abra los ajustes del proyecto

   ![project-settings](assets/firebase-project-settings.PNG)

4. Tab to the **[!UICONTROL Cloud Messaging]** tab.
5. Copiar la clave del servidor

   ![server-key](assets/firebase-server-key.PNG)

6. Inicie sesión en la instancia de Adobe Campaign Standard
7. Click **[!UICONTROL Adobe Campaign]** > **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Mobile App].**
8. Seleccione el **[!UICONTROL Mobile Application Property].**
9. Click the **[!DNL Android]icon **in the **[!UICONTROL Push Channel settings]**section.
10. Pegue la clave del servidor en el campo de la clave del servidor.

Si todo va bien, debería ver un mensaje de ÉXITO.

![push-canal-settings](assets/push-channel-settings.PNG)

Para resumir, hemos creado un [!DNL Android App] y conectado el [!DNL Android App] con [!DNL Firebase]. A continuación, conectamos la aplicación móvil en Adobe Campaign con la aplicación [!DNL Android App] pegando la clave de servidor de la [!DNL Android] aplicación en la aplicación móvil en Adobe Campaign Standard.
