---
title: 'Paso 1: Creación de aplicaciones de Android y configuración para utilizar la mensajería en la nube de Firebase'
description: En esta parte crearemos [!DNL Android] App to receive [!UICONTROL Push notifications] enviado desde Adobe Campaign Standard. Para poder recibir las notificaciones push, la aplicación debe registrarse con el  [!DNL Firebase Cloud Service] de Google.
feature: Push
topics: Mobile
kt: 4825
doc-type: tutorial
activity: use
team: TM
translation-type: tm+mt
source-git-commit: cdd78e97f2769503d3d4f26933ccc7f35e9b20b9
workflow-type: tm+mt
source-wordcount: '316'
ht-degree: 2%

---


# Paso 1: Creación de una aplicación [!DNL Android] y configuración para utilizar [!DNL Firebase Cloud Messaging]

En esta parte creará [!DNL Android] aplicación para recibir [!UICONTROL Push notifications] enviados desde Adobe Campaign Standard. Para recibir las notificaciones push, la aplicación debe estar registrada con el [!DNL Firebase Cloud Service] de Google.

1. Inicie sesión en su cuenta [!DNL Firebase].

   [!DNL Firebase] es la plataforma móvil de Google que le ayuda a desarrollar rápidamente aplicaciones de alta calidad. Si no tiene una cuenta [!DNL Firebase], cree una [desde aquí](https://firebase.google.com).

2. Iniciar [!DNL Android Studio]
3. Haga clic en **[!UICONTROL File]** > **[!UICONTROL New]** > **[!UICONTROL New Project].**
4. Seleccione **[!UICONTROL Empty Activity]** y haga clic en **[!UICONTROL Next].**

   ![android-project](assets/android-project.PNG)

5. Proporcione un nombre significativo al proyecto.

   A los efectos de esta demostración, hemos denominado nuestro proyecto como *[!DNL ACSPushTutorial]*

   ![android-project-configuration](assets/android-project-configuration.PNG)

6. Acepte los nombres de paquete predeterminados y haga clic en **[!DNL Finish]** para crear el proyecto.
7. La estructura del proyecto debe ser similar a la de la captura de pantalla siguiente

   ![android-project-structure](assets/android-project-structure.PNG)

8. Haga clic en **[!UICONTROL Tools]** > **[!UICONTROL Firebase].** (esto agrega el proyecto a  [!DNL Firebase])
9. Haga clic en **[!UICONTROL Set up Firebase Cloud Messaging].**

   ![configurar firebase](assets/android-project-firebase-messaging.PNG)

10. Haga clic en **[!UICONTROL Connect to Firebase].**
11. Una vez que la aplicación esté conectada a Firebase, haga clic en **[!UICONTROL Add FCM to your app].**
12. Haga clic en **[!UICONTROL Accept Changes].**

   Al agregar FCM a la aplicación, el asistente necesita su permiso para realizar algunos cambios en el proyecto.

   ![[!DNL add-fcm-to-your-app]](assets/firebase-add-fcm-to-app.PNG)

Si la aplicación se integra correctamente con Firebase, debería recibir un mensaje como el que se muestra a continuación:

![[!DNL fcm-successfull]](assets/android-firebase-success.PNG)

[Asegúrese de que el proyecto aparece en la  [!DNL Firebase ]consola](https://console.firebase.google.com/)

## Configuración de [!UICONTROL Push Channel]

1. Iniciar sesión en la consola [!DNL Firebase]
2. Abra el proyecto **[!UICONTROL ACSPushTutorial]**.
3. Haga clic en el icono **de engranaje** y abra la configuración del proyecto

   ![project-settings](assets/firebase-project-settings.PNG)

4. Tabulación a la ficha **[!UICONTROL Cloud Messaging]**.
5. Copiar la clave del servidor

   ![server-key](assets/firebase-server-key.PNG)

6. Inicie sesión en su instancia de Adobe Campaign Standard
7. Haga clic en **[!UICONTROL Adobe Campaign]** > **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Mobile App].**
8. Seleccione el **[!UICONTROL Mobile Application Property]apropiado.**
9. Haga clic en el icono **[!DNL Android]** en la sección **[!UICONTROL Push Channel settings]**.
10. Pegue la clave del servidor en el campo de la clave del servidor.

Si todo va bien, debería ver un mensaje de ÉXITO.

![push-canal-settings](assets/push-channel-settings.PNG)

Para resumir, hemos creado un [!DNL Android App] y conectado el [!DNL Android App] con [!DNL Firebase]. A continuación, conectamos la aplicación móvil en Adobe Campaign con la [!DNL Android App] pegando la clave de servidor de la aplicación [!DNL Android] en la aplicación móvil en Adobe Campaign Standard.
