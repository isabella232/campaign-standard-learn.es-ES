---
title: 'Paso 3: Registro de extensiones con la aplicación móvil'
description: En esta parte añadiremos el código para registrar las extensiones UserProfile, Identity, Lifecycle y Signal.
feature: Push
kt: 4827
doc-type: tutorial
activity: use
team: TM
exl-id: d8c0d8c6-2e04-4c27-b27a-d0de79dd953b
source-git-commit: ada0b029245190f53d58fa93c79c161719bfe9fd
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 11%

---

# Paso 3: Registro de extensiones con la aplicación móvil

En esta parte añadiremos el código para registrar las extensiones de perfil de usuario, identidad, ciclo vital y señal. Estas extensiones forman parte de [[!UICONTROL Mobile Core Extensions]](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/mobile-core). También tendremos que registrar la extensión de Adobe Campaign Standard como se muestra en el siguiente código.

Abra el proyecto en [!DNL Android] estudio. Eliminar todo el código en MainApp **excepto la primera línea, que es la instrucción del paquete**.

Pegue el siguiente código en MainApp

<!--
Removed `{.line-numbers}` below
-->

```java
import [!DNL android].app.Application;
import android.util.Log;

import com.adobe.marketing.mobile.AdobeCallback;
import com.adobe.marketing.mobile.Campaign;
import com.adobe.marketing.mobile.Identity;
import com.adobe.marketing.mobile.InvalidInitException;
import com.adobe.marketing.mobile.Lifecycle;
import com.adobe.marketing.mobile.LoggingMode;
import com.adobe.marketing.mobile.MobileCore;
import com.adobe.marketing.mobile.Signal;
import com.adobe.marketing.mobile.UserProfile;

public class MainApp extends Application {

@Override
public void onCreate() {
super.onCreate();

MobileCore.setApplication(this);
MobileCore.setLogLevel(LoggingMode.DEBUG);

try{
    Campaign.registerExtension();
    UserProfile.registerExtension();
    Identity.registerExtension();
    Lifecycle.registerExtension();
    Signal.registerExtension();
    MobileCore.start(new AdobeCallback () {
        @Override
        public void call(Object o) {
            MobileCore.configureWithAppID("copy your launch property id here");
        }
    });
} catch (InvalidInitException e) {
    Log.d("ACS Exception", "exception");
}
}
}
```

Línea 32, debe proporcionar su[!UICONTROL  Launch] ID de archivo de entorno de la propiedad. Se puede acceder a desde el [!UICONTROL environment tab] de su [!UICONTROL Launch] propiedad.

![launch-id](assets/launch-id-property.PNG)
