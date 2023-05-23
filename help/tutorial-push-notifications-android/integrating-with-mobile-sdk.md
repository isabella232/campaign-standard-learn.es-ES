---
title: 'Paso 2: Integración del SDK de Mobile'
description: En esta parte, integramos la aplicación de Android con el SDK móvil. Para integrar el SDK móvil con la aplicación de Android
feature: Push
kt: 4826
doc-type: tutorial
activity: use
team: TM
recommendations: noDisplay
exl-id: 0fa53536-8330-4e96-be2f-afc078609bcd
source-git-commit: 57dbf456625d22cd2e4526d92e5a8c20a048d339
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 3%

---

# PASO 2: Integración [!UICONTROL Mobile SDK] con la aplicación Android

En esta parte, integraremos el [!DNL Android] aplicación con [!UICONTROL Mobile SDK]. Para integrar [!UICONTROL mobile SDK] con el [!DNL Android] Aplicación, siga los siguientes pasos:

* Abra el *ACSPushTutorial* proyecto en [!DNL Android Studio]
* Cree una nueva clase java llamada *MainApp* que amplía [!DNL android.app.Application]
* La estructura del proyecto en este punto debería ser la siguiente

![main-app](assets/android-main-app.PNG)

* Expanda el [!DNL Gradle Scripts] carpeta. Haga doble clic en [!DNL build.gradle] del módulo. Pegue las siguientes dependencias en la sección de dependencias de la [!DNL build.gradle] archivo. Su [!DNL build.gradle] el archivo debería tener el aspecto siguiente

<!--
Removed `{.line-numbers}` below
-->

```java
implementation 'com.adobe.marketing.mobile:campaign:1.+'
implementation 'com.adobe.marketing.mobile:userprofile:1.+'
implementation 'com.adobe.marketing.mobile:sdk-core:1.+'
```

![gradle de módulos](assets/module-build-gradle.PNG)

* Sincronice su [!DNL Android] proyecto haciendo clic en el botón sincronizar ahora para sincronizar el proyecto

## Modificar [!DNL AndroidManifest.xml]{#modify-android-manifest}

Abrir *AndroidManifest.xml* y pegue las 2 líneas siguientes después del elemento manifest y antes del elemento application. Esto permite que la aplicación se comunique con el mundo exterior

<!--
Removed `{.line-numbers}` below
-->

```xml
<uses-permission android:name="android.permission.INTERNET" />
<uses-permission android:name="android.permission.ACCESS_NETWORK_STATE" />
```

Copie la línea siguiente en el elemento de aplicación
[!DNL android:name=".MainApp"]
Guarde su [!DNL AndroidManifest.xml]
Su [!DNL AndroidManifest.xml] debería tener este aspecto

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
