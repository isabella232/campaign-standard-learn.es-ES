---
title: 'PASO 4: Establecer identificador de push'
description: El **pushIdentifier** es una cadena que contiene el token del dispositivo para las notificaciones push. Este es el mismo token que envía Firebase y que se pasa al SDK mediante el método MobileCore.setPushIdentifier .
feature: Push
topic: MÓVIL
kt: 4828
doc-type: tutorial
activity: use
team: TM
exl-id: 08387b84-edaa-45ee-ae66-53bcbd5c7c39
translation-type: tm+mt
source-git-commit: ddbb0843ea45a83d9ab5bfa0877287f6ba7d6210
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 0%

---

# Paso 4: Establecer [!DNL pushidentifier]

El **[!DNL pushidentifier]** es una cadena que contiene el token del dispositivo para las notificaciones [!DNL Push]. Este es el mismo token que envía [!DNL Firebase] y que se pasa al SDK mediante el método [!DNL MobileCore.setPushIdentifier].

Abra el proyecto en [!DNL Android ]studio. Elimine todo el código en [!DNL MainActivity] **excepto la primera línea que es la instrucción del paquete**.

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
* El emulador [!DNL Android] debe iniciarse y debería ver la aplicación ejecutándose con [!DNL "Hello World" ]texto.
* Abra la ventana [!DNL logcat]. Busque &quot;[!DNL Got]&quot;. Debería ver el token que recibió de [!DNL Firebase] escrito en el registro como se muestra a continuación. La cadena larga después de &quot;[!DNL Got token]&quot; es la [!DNL pushidentifier ]que se envía a Adobe Campaign.

![logcat-token](assets/logcat-got-token.PNG)

### Comprobar suscriptores de aplicaciones móviles

Inicie sesión en la instancia de Adobe Campaign Standard.
Vaya a **[!UICONTROL Administration->Channels->Mobile App(AEP SDK)]**. Abra la aplicación móvil correspondiente. Tabule en la pestaña [!UICONTROL Mobile Application Subscribers]. Debería ver un [!UICONTROL registration token ]en la lista.

![mobile-application-subscribers](assets/mobile-application-subscribers.PNG)

>[!NOTE]
>
>Si no ve el token de registro en la pestaña [!UICONTROL Mobile Application Subscribers] DETENGA aquí antes de continuar.
