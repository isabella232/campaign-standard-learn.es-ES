---
title: 'Paso 1: Creación de una aplicación para Android y configuración para utilizar Firebase Cloud Messaging'
description: En esta parte crearemos [!DNL Android] Aplicación para recibir [!UICONTROL Push notifications] enviado desde Adobe Campaign Standard. Para recibir las notificaciones push, la aplicación debe registrarse en el de Google [!DNL Firebase Cloud Service].
feature: Push
kt: 4825
doc-type: tutorial
activity: use
team: TM
recommendations: noDisplay
exl-id: f087d9f2-cce9-4903-977f-3c5b47522c06
source-git-commit: 57dbf456625d22cd2e4526d92e5a8c20a048d339
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 3%

---

# Paso 1: Creación [!DNL Android] Aplicación y configuración para usar [!DNL Firebase Cloud Messaging]

En esta parte creará [!DNL Android] Aplicación para recibir [!UICONTROL Push notifications] enviado desde Adobe Campaign Standard. Para recibir las notificaciones push, la aplicación debe registrarse en el de Google [!DNL Firebase Cloud Service].

1. Inicie sesión en su [!DNL Firebase] cuenta.

   [!DNL Firebase] es la plataforma móvil de Google que le ayuda a desarrollar rápidamente aplicaciones de alta calidad. Si no tiene un [!DNL Firebase] cuenta, cree una [desde aquí](https://firebase.google.com).

2. Launch [!DNL Android Studio]
3. Clic **[!UICONTROL File]** > **[!UICONTROL New]** > **[!UICONTROL New Project].**
4. Seleccione **[!UICONTROL Empty Activity]** y haga clic en **[!UICONTROL Next].**

   ![android-project](assets/android-project.PNG)

5. Proporcione un nombre significativo al proyecto.

   Para el propósito de esta demostración, hemos nombrado nuestro proyecto como *[!DNL ACSPushTutorial]*

   ![android-project-configuration](assets/android-project-configuration.PNG)

6. Acepte los nombres de paquete predeterminados y haga clic en **[!DNL Finish]** para crear el proyecto.
7. La estructura del proyecto debe ser similar a la captura de pantalla siguiente

   ![android-project-structure](assets/android-project-structure.PNG)

8. Haga clic en **[!UICONTROL Tools]** > **[!UICONTROL Firebase].** (esto agrega el proyecto a [!DNL Firebase])
9. Haga clic en **[!UICONTROL Set up Firebase Cloud Messaging].**

   ![configurar firebase](assets/android-project-firebase-messaging.PNG)

10. Haga clic en **[!UICONTROL Connect to Firebase].**
11. Cuando la aplicación esté conectada a Firebase, haga clic en **[!UICONTROL Add FCM to your app].**
12. Haga clic en **[!UICONTROL Accept Changes].**

   Cuando agregue FCM a la aplicación, el asistente necesitará su permiso para realizar algunos cambios en el proyecto.

   ![[!DNL add-fcm-to-your-app]](assets/firebase-add-fcm-to-app.PNG)

Si la integración de la aplicación con Firebase se realiza correctamente, recibirá un mensaje similar al que se muestra a continuación:

![[!DNL fcm-successfull]](assets/android-firebase-success.PNG)

[Asegúrese de que el proyecto esté en la lista [!DNL Firebase ]consolar](https://console.firebase.google.com/)

## Configurar [!UICONTROL Push Channel] Configuración

1. Inicie sesión en [!DNL Firebase] consolar
2. Abra el **[!UICONTROL ACSPushTutorial]** proyecto.
3. Haga clic en **icono de engranaje** y abra la configuración del proyecto.

   ![project-settings](assets/firebase-project-settings.PNG)

4. Tabule hasta **[!UICONTROL Cloud Messaging]** pestaña.
5. Copiar la clave del servidor

   ![server-key](assets/firebase-server-key.PNG)

6. Inicie sesión en su instancia de Adobe Campaign Standard
7. Clic **[!UICONTROL Adobe Campaign]** > **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Mobile App].**
8. Seleccione el adecuado **[!UICONTROL Mobile Application Property].**
9. Haga clic en **[!DNL Android]icono** en el **[!UICONTROL Push Channel settings]** sección.
10. Pegue la clave del servidor en el campo server key.

Si todo va bien, debería ver un mensaje de ÉXITO.

![push-channel-settings](assets/push-channel-settings.PNG)

En resumen, hemos creado un [!DNL Android App] y conectó el [!DNL Android App] con [!DNL Firebase]. A continuación, conectamos la aplicación móvil en Adobe Campaign con [!DNL Android App] al pegar el [!DNL Android] Clave de servidor de la aplicación en la aplicación móvil en Adobe Campaign Standard.
