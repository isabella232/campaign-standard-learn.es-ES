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
ht-degree: 3%

---

# PASO 2: Integrar [!UICONTROL Mobile SDK] con la aplicación de Android

En esta parte, integraremos la aplicación [!DNL Android] con [!UICONTROL Mobile SDK]. Para integrar [!UICONTROL mobile SDK] con la aplicación [!DNL Android], siga los siguientes pasos:

* Abra el proyecto *ACSPushTutorial* en [!DNL Android Studio]
* Cree una nueva clase java llamada *MainApp* que se extienda [!DNL android.app.Application]
* La estructura del proyecto en este momento debería verse como a continuación

![main-app](assets/android-main-app.PNG)

* Expanda la carpeta [!DNL Gradle Scripts]. Doble haga clic en el [!DNL build.gradle] del módulo. Pegue las siguientes dependencias en la sección dependencias del archivo [!DNL build.gradle]. El archivo [!DNL build.gradle] debe tener el aspecto siguiente

<!--
Removed `{.line-numbers}` below
-->

```java
implementation 'com.adobe.marketing.mobile:campaign:1.+'
implementation 'com.adobe.marketing.mobile:userprofile:1.+'
implementation 'com.adobe.marketing.mobile:sdk-core:1.+'
```

![module-gradle](assets/module-build-gradle.PNG)

* Sincronice su proyecto [!DNL Android] haciendo clic en el botón sincronizar ahora para sincronizar el proyecto

## Modificar [!DNL AndroidManifest.xml]{#modify-android-manifest}

Abra *AndroidManifest.xml* y pegue las dos líneas siguientes después del elemento manifest y antes del elemento application. Esto permite a la aplicación comunicarse con el mundo exterior

<!--
Removed `{.line-numbers}` below
-->

```xml
<uses-permission android:name="android.permission.INTERNET" />
<uses-permission android:name="android.permission.ACCESS_NETWORK_STATE" />
```

Copiar la línea siguiente en el elemento de la aplicación
[!DNL android:name=".MainApp"]
Guarde su [!DNL AndroidManifest.xml]
Su [!DNL AndroidManifest.xml] debe tener este aspecto

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
