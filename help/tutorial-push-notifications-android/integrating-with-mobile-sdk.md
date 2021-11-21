---
title: 'Paso 2: Integración del SDK de Mobile'
description: En esta parte, integraremos la aplicación de Android con el SDK de Mobile. Para integrar el SDK móvil con la aplicación Android
feature: Push
kt: 4826
doc-type: tutorial
activity: use
team: TM
exl-id: 0fa53536-8330-4e96-be2f-afc078609bcd
source-git-commit: ada0b029245190f53d58fa93c79c161719bfe9fd
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 3%

---

# PASO 2: Integrar [!UICONTROL Mobile SDK] con la aplicación Android

En esta parte integraremos el [!DNL Android] aplicación con [!UICONTROL Mobile SDK]. Para integrar [!UICONTROL mobile SDK] con la variable [!DNL Android] aplicación, siga los siguientes pasos:

* Abra el *ACSPushTutorial* proyecto en [!DNL Android Studio]
* Cree una nueva clase java llamada *Aplicación principal* que se extiende [!DNL android.app.Application]
* La estructura del proyecto en este punto debería ser similar a la siguiente

![aplicación principal](assets/android-main-app.PNG)

* Expanda el [!DNL Gradle Scripts] carpeta. Haga doble clic en el botón [!DNL build.gradle] del módulo. Pegue las siguientes dependencias en la sección dependencias de [!DNL build.gradle] archivo. Su [!DNL build.gradle] ahora debería ser como se muestra a continuación

<!--
Removed `{.line-numbers}` below
-->

```java
implementation 'com.adobe.marketing.mobile:campaign:1.+'
implementation 'com.adobe.marketing.mobile:userprofile:1.+'
implementation 'com.adobe.marketing.mobile:sdk-core:1.+'
```

![module-gradle](assets/module-build-gradle.PNG)

* Sincronice sus [!DNL Android] para sincronizar el proyecto, haga clic en el botón sincronizar ahora .

## Modificar [!DNL AndroidManifest.xml]{#modify-android-manifest}

Apertura *AndroidManifest.xml* y pegue las siguientes 2 líneas después del elemento manifest y antes del elemento application . Esto permite que la aplicación se comunique con el mundo exterior

<!--
Removed `{.line-numbers}` below
-->

```xml
<uses-permission android:name="android.permission.INTERNET" />
<uses-permission android:name="android.permission.ACCESS_NETWORK_STATE" />
```

Copie la línea siguiente en el elemento de la aplicación
[!DNL android:name=".MainApp"]
Guarde su [!DNL AndroidManifest.xml]
Su [!DNL AndroidManifest.xml] debería parecerse a esto

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
