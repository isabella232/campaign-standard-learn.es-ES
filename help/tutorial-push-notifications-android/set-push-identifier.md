---
title: 'PASO 4: Definición de pushidentifier'
description: '**pushIdentifier** es una cadena que contiene el token del dispositivo para las notificaciones push. Es el mismo token que Firebase envía y que se pasa al SDK mediante el método MobileCore.setPushIdentifier.'
feature: Push
kt: 4828
doc-type: tutorial
activity: use
team: TM
exl-id: 08387b84-edaa-45ee-ae66-53bcbd5c7c39
source-git-commit: 5a2f8c9a78bf5100b272f9b4461131545b3aeb8b
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 0%

---

# Paso 4: Definición [!DNL pushidentifier]

El **[!DNL pushidentifier]** es una cadena que contiene el token de dispositivo para [!DNL Push] notificaciones. Es el mismo token que envía [!DNL Firebase] y se pasa al SDK mediante la variable [!DNL MobileCore.setPushIdentifier] método.

Abra el proyecto en [!DNL Android™ ]estudio. Elimine todo el código de en [!DNL MainActivity] **excepto la primera línea, que es la instrucción del paquete**.

Pegue el siguiente código en [!DNL MainActivity]:

<!--
Removed `{.line-numbers}` below
-->

```java
import androidx.annotation.NonNull;
import androidx.appcompat.app.AppCompatActivity;

import android.os.Bundle;
import android.util.Log;
import android.widget.Toast;

import com.adobe.marketing.mobile.MobileCore;
import com.google.android.gms.tasks.OnCompleteListener;
import com.google.android.gms.tasks.Task;
import com.google.firebase.iid.FirebaseInstanceId;
import com.google.firebase.iid.InstanceIdResult;

public class MainActivity extends AppCompatActivity {

@Override
protected void onCreate(Bundle savedInstanceState) {
super.onCreate(savedInstanceState);
setContentView(R.layout.activity_main);

registerToken();
}

void registerToken() {
FirebaseInstanceId.getInstance().getInstanceId()
    .addOnCompleteListener(new OnCompleteListener<InstanceIdResult>() {
        @Override
        public void onComplete(@NonNull Task<InstanceIdResult> task) {
            if (!task.isSuccessful()) {
                Log.w("Message App", "getInstanceId failed", task.getException());
                return;
            }

// Get new Instance ID token
String token = task.getResult().getToken();

Log.d("Got token", token);

MobileCore.setPushIdentifier(token);
}
});
}

@Override
public void onResume() {
super.onResume();
MobileCore.setApplication(getApplication());
MobileCore.lifecycleStart(null);
}

@Override
public void onPause() {
super.onPause();
MobileCore.lifecyclePause();
}
}
```

## Probar la aplicación

Este es un buen momento para probar la aplicación antes de continuar.

* Ejecute la aplicación haciendo clic en la flecha verde o seleccionando **[!DNL Run->Run'app']**.
* El [!DNL Android™] El emulador debe iniciarse y debería ver la aplicación en ejecución con. [!DNL "Hello World" ]texto.
* Abra el [!DNL logcat] ventana. Buscar &quot;[!DNL Got]&quot;. Debe ver el token que se recibió de [!DNL Firebase] se escribe en el registro como se muestra a continuación. La cadena larga después de &quot;[!DNL Got token]&quot; es el [!DNL pushidentifier ]que se envía a Adobe Campaign.

![logcat-token](assets/logcat-got-token.PNG)

### Comprobar suscriptores de aplicaciones móviles

Inicie sesión en la instancia de Adobe Campaign Standard.
Navegar **[!UICONTROL Administration->Channels->Mobile App(Experience Platform SDK)]**. Abra la aplicación móvil adecuada. Tabule hasta [!UICONTROL Mobile Application Subscribers] pestaña. Debería ver una [!UICONTROL registration token ]enumerados.

![mobile-application-subscribers](assets/mobile-application-subscribers.PNG)

>[!NOTE]
>
>Si no ve el token de registro en [!UICONTROL Mobile Application Subscribers] pestaña STOP aquí antes de continuar.
