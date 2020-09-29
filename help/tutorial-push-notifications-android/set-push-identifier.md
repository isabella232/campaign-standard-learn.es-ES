---
title: 'PASO 4: Definir identificador de inserción'
description: El **pushIdentifier** es una cadena que contiene el autentificador del dispositivo para las notificaciones push. Este es el mismo token que envía Firebase y se pasa al SDK mediante el método MobileCore.setPushIdentifier.
feature: Push
topics: MOBILE
kt: 4828
doc-type: tutorial
activity: use
team: TM
translation-type: tm+mt
source-git-commit: aa01c2f8fe1560468d0d8f3fae6291bb82f9a21f
workflow-type: tm+mt
source-wordcount: '206'
ht-degree: 0%

---

# Paso 4: Conjunto [!DNL pushidentifier]

La **[!DNL pushidentifier]** es una cadena que contiene el autentificador del dispositivo para [!DNL Push] notificaciones. Es el mismo token que se envía [!DNL Firebase] y se pasa al SDK mediante el [!DNL MobileCore.setPushIdentifier] método .

Abra el proyecto en el [!DNL Android ]estudio. Elimine todo el código en [!DNL MainActivity] excepto la primera línea, que es la instrucción **** del paquete.

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

## Prueba de la aplicación

Ahora es un buen momento para probar la aplicación antes de ir más lejos.

* Para ejecutar la aplicación, haga clic en la flecha verde o seleccione **[!DNL Run->Run'app']**.
* El [!DNL Android] emulador debe tener inicio y debería ver la aplicación ejecutándose con [!DNL "Hello World" ]texto.
* Abra la [!DNL logcat] ventana. Busque &quot;[!DNL Got]&quot;. Debe ver el token que se recibió de [!DNL Firebase] escrito en el registro como se muestra a continuación. La cadena larga después de &quot;[!DNL Got token]&quot; es la [!DNL pushidentifier ]que se envía a Adobe Campaign.

![logcat-token](assets/logcat-got-token.PNG)

### Comprobar suscriptores de aplicaciones móviles

Inicie sesión en su instancia de Adobe Campaign Standard.
Navegar **[!UICONTROL Administration->Channels->Mobile App(AEP SDK)]**. Abra la aplicación móvil adecuada. Tab to the [!UICONTROL Mobile Application Subscribers] tab. Deberías ver una [!UICONTROL registration token ]lista.

![mobile-application-subscribers](assets/mobile-application-subscribers.PNG)

>[!NOTE]
>
>Si no ve el token de registro en la [!UICONTROL Mobile Application Subscribers] ficha DETENGA aquí antes de continuar.
