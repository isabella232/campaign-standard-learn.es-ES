---
title: 'Paso 2: Integración del SDK de Mobile'
description: En esta parte, integraremos la aplicación de Android con el SDK de Mobile. Para integrar el SDK móvil con la aplicación de Android
feature: Push
topics: Mobile
kt: 4826
doc-type: tutorial
activity: use
team: TM
translation-type: tm+mt
source-git-commit: 13b4f1d395dfe53f9fc5263e7b06be700e30b986
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 0%

---

# PASO 2: Integración [!UICONTROL Mobile SDK] con la aplicación Android

En esta parte, integraremos la [!DNL Android] aplicación con [!UICONTROL Mobile SDK]. Para integrarla [!UICONTROL mobile SDK] con la [!DNL Android] aplicación, siga los pasos siguientes:

* Abra el proyecto *ACSPushTutorial* en [!DNL Android Studio]
* Cree una nueva clase java llamada *MainApp* que se extienda [!DNL android.app.Application]
* La estructura del proyecto en este momento debería verse como a continuación

![main-app](assets/android-main-app.PNG)

* Expanda la [!DNL Gradle Scripts] carpeta. Doble haga clic en la [!DNL build.gradle] parte del módulo. Pegue las dependencias siguientes en la sección dependencias del [!DNL build.gradle] archivo. El [!DNL build.gradle] archivo debe tener el aspecto siguiente

<!--
Removed `{.line-numbers}` below
-->

```java
implementation 'com.adobe.marketing.mobile:campaign:1.+'
implementation 'com.adobe.marketing.mobile:userprofile:1.+'
implementation 'com.adobe.marketing.mobile:sdk-core:1.+'
```

![module-gradle](assets/module-build-gradle.PNG)

* Sincronice el [!DNL Android] proyecto haciendo clic en el botón Sincronizar ahora para sincronizar el proyecto

## Modificar [!DNL AndroidManifest.xml]{#modify-android-manifest}

Abra *AndroidManifest.xml* y pegue las dos líneas siguientes después del elemento manifest y antes del elemento application. Esto permite a la aplicación comunicarse con el mundo exterior

<!--
Removed `{.line-numbers}` below
-->

```xml
<uses-permission android:name="android.permission.INTERNET" />
<uses-permission android:name="android.permission.ACCESS_NETWORK_STATE" />
```

Copie la línea siguiente en el elemento[!DNL android:name=".MainApp"]de la aplicaciónGuarde el [!DNL AndroidManifest.xml]aspecto que [!DNL AndroidManifest.xml] debería tener

<!--
Removed `{.line-numbers}` below
-->

```xml
<?xml version="1.0" encoding="utf-8"?>
<manifest xmlns:android="http://schemas.android.com/apk/res/android"
    package="com.example.acspushtutorial">
    <uses-permission android:name="android.permission.INTERNET" />
    <uses-permission android:name="android.permission.ACCESS_NETWORK_STATE" />

<application
    android:name=".MainApp"
    android:allowBackup="true"
    android:icon="@mipmap/ic_launcher"
    android:label="@string/app_name"
    android:roundIcon="@mipmap/ic_launcher_round"
    android:supportsRtl="true"
    android:theme="@style/AppTheme">

<activity android:name=".MainActivity">
<intent-filter>
    <action android:name="android.intent.action.MAIN" />
    <category android:name="android.intent.category.LAUNCHER" />
</intent-filter>
</activity>
</application>

</manifest>
```
