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
source-git-commit: c3ff1a137fb8ee9506a11f82e1a27d010bbd97e6
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 0%

---


# Paso 3: Registro de extensiones con la aplicación móvil

En esta parte agregaremos el código para registrar las extensiones Perfil del usuario, identidad, ciclo de vida y señal. Estas extensiones son parte de [[!UICONTROL Mobile Core Extensions]](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/mobile-core). También será necesario registrar la extensión de Adobe Campaign Standard como se muestra en el código siguiente.

Abra el proyecto en el [!DNL Android] estudio. Elimine todo el código en MainApp **excepto la primera línea, que es la instrucción** del paquete.

Pegue el siguiente código en MainApp

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

Línea 32 debe proporcionar la identificación del archivo de entorno de su[!UICONTROL  Launch] propiedad. Se puede acceder a ella desde la [!UICONTROL environment tab] propiedad de su [!UICONTROL Launch] propiedad.

![launch-id](assets/launch-id-property.PNG)
