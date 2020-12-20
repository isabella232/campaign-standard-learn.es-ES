---
title: 'Paso 3: Registro de extensiones con la aplicación móvil'
description: En esta parte agregaremos el código para registrar las extensiones UserProfile, Identity, Lifecycle y Signal.
feature: Push
topics: Mobile
kt: 4827
doc-type: tutorial
activity: use
team: TM
translation-type: tm+mt
source-git-commit: 13b4f1d395dfe53f9fc5263e7b06be700e30b986
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 0%

---


# Paso 3: Registro de extensiones con la aplicación móvil

En esta parte agregaremos el código para registrar las extensiones Perfil del usuario, identidad, ciclo de vida y señal. Estas extensiones forman parte de [[!UICONTROL Mobile Core Extensions]](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/mobile-core). También será necesario registrar la extensión de Adobe Campaign Standard como se muestra en el código siguiente.

Abra el proyecto en [!DNL Android] estudio. Elimine todo el código en MainApp **excepto la primera línea que es la instrucción del paquete**.

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

Línea 32 debe proporcionar la identificación del archivo de entorno de la propiedad[!UICONTROL  Launch]. Se puede acceder a esto desde [!UICONTROL environment tab] de la propiedad [!UICONTROL Launch].

![launch-id](assets/launch-id-property.PNG)
