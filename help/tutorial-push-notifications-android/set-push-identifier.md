---
title: 'PASO 4: Establecer identificador de push'
description: El **pushIdentifier** es una cadena que contiene el token del dispositivo para las notificaciones push. Es el mismo token que envía Firebase y se pasa al SDK mediante el método MobileCore.setPushIdentifier .
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

# Paso 4: Configurar [!DNL pushidentifier]

La variable **[!DNL pushidentifier]** es una cadena que contiene el token del dispositivo para [!DNL Push] notificaciones. Es el mismo token por el que se envía [!DNL Firebase] y se transfiere al SDK mediante la función [!DNL MobileCore.setPushIdentifier] método.

Abra el proyecto en [!DNL Android™ ]estudio. Elimine todo el código de [!DNL MainActivity] **excepto la primera línea que es la declaración del paquete**.

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

Ahora es un buen momento para probar la aplicación antes de ir más lejos.

* Ejecute la aplicación haciendo clic en la flecha verde o seleccione **[!DNL Run->Run'app']**.
* La variable [!DNL Android™] El emulador debería iniciarse y debería ver que la aplicación se está ejecutando con [!DNL "Hello World" ]texto.
* Abra el [!DNL logcat] ventana. Buscar &quot;[!DNL Got]&quot;. Debería ver el token que recibió de [!DNL Firebase] escrito en el registro como se muestra a continuación. La cadena larga después de &quot;[!DNL Got token]&quot; es la variable [!DNL pushidentifier ]que se envía a Adobe Campaign.

![logcat-token](assets/logcat-got-token.PNG)

### Comprobar suscriptores de aplicaciones móviles

Inicie sesión en la instancia de Adobe Campaign Standard.
Navegar **[!UICONTROL Administration->Channels->Mobile App(Experience Platform SDK)]**. Abra la aplicación móvil correspondiente. Tabule para [!UICONTROL Mobile Application Subscribers] pestaña . Debería ver un [!UICONTROL registration token ]en la lista.

![mobile-application-subscribers](assets/mobile-application-subscribers.PNG)

>[!NOTE]
>
>Si no ve el token de registro en la variable [!UICONTROL Mobile Application Subscribers] DETENGA aquí antes de continuar.
