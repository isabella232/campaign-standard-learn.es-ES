---
title: 'Paso 5: Propagar notificaciones'
description: En esta parte, propagaremos el mensaje recibido de Adobe Campaign mediante Android Notification Manager.Firebase
feature: Push
topics: Mobile
kt: 4829
doc-type: tutorial
activity: use
team: TM
translation-type: tm+mt
source-git-commit: afe1ae6c8d73b7b776e0eec327fa16db76c23ce1
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 0%

---

# Añadir servicio para enviar notificación

En esta parte, propagaremos el mensaje recibido de Adobe Campaign mediante [!DNL Android Notification Manager]. [!DNL Notification manager] se utiliza para notificar al usuario los eventos que se producen.
Así es como se le dice al usuario que algo ha pasado en segundo plano:

* Iniciar [!DNL Android Studio]
* Abrir *[!DNL ACSPushTutorial]* proyecto
* Expandir la estructura del proyecto
* Haga clic con el botón derecho en la carpeta del paquete ([!DNL com.example.acspushtutorial]) y [!DNL New ->Java Class]
* Asigne un nombre a esta clase *[!DNL MyService]* y asegúrese de que se extiende [!DNL FirebaseMessagingService]
* Crear *[!DNL sendNotification]* método en esta clase. En este método debe establecer el contenido y el canal de la notificación mediante un [!DNL NotificationCompat.Builder] objeto. Para que aparezca la notificación, llame [!DNL NotificationManagerCompat.notify()]y pase un ID único para la notificación y el resultado de [!DNL NotificationCompat.Builder.build()].

```java {.line-numbers}
package com.example.pushmessaging;
import android.app.NotificationChannel;
import android.app.NotificationManager;
import android.app.PendingIntent;
import android.content.Context;
import android.content.Intent;
import android.media.RingtoneManager;
import android.net.Uri;
import android.os.Build;
import android.util.Log;

import androidx.core.app.NotificationCompat;

import com.google.firebase.messaging.FirebaseMessagingService;
import com.google.firebase.messaging.RemoteMessage;

import java.util.Map;

public class MyService extends FirebaseMessagingService {
@Override
public void onMessageReceived(RemoteMessage remoteMessage)
{
Map<String,String> data  = remoteMessage.getData();
Log.d("data payload: ", data.toString());
sendNotification(remoteMessage);
}


private void sendNotification(RemoteMessage message) {
Intent intent = new Intent(this, MainActivity.class);
intent.addFlags(Intent.FLAG_ACTIVITY_CLEAR_TOP);
PendingIntent pendingIntent = PendingIntent.getActivity(this, 0 /* Request code */, intent, PendingIntent.FLAG_ONE_SHOT);

String channelId = "0";
Uri defaultSoundUri = RingtoneManager.getDefaultUri(RingtoneManager.TYPE_NOTIFICATION);
NotificationCompat.Builder notificationBuilder =
        new NotificationCompat.Builder(this, channelId)
                .setSmallIcon(R.drawable.ic_launcher_background)
                .setContentTitle("Message from AEM")
                .setContentText(message.getData().get("body"))
                .setAutoCancel(true)
                .setSound(defaultSoundUri)
                .setContentIntent(pendingIntent);

NotificationManager notificationManager =
        (NotificationManager) getSystemService(Context.NOTIFICATION_SERVICE);

// Since android Oreo notification channel is needed.
if (Build.VERSION.SDK_INT >= Build.VERSION_CODES.O) {
    NotificationChannel channel = new NotificationChannel(channelId,
            "Channel human readable title",
            NotificationManager.IMPORTANCE_DEFAULT);
    notificationManager.createNotificationChannel(channel);
}

notificationManager.notify(0 /* ID of notification */, notificationBuilder.build());
}
}
```

## Modificar [!DNL AndroidManifest.xml]

Añada el servicio que se creó en su [!DNL AndroidManifest.xml]. El final [!DNL AndroidManifest.xml] debería ser como el siguiente:

```xml {.line-numbers}
<?xml version="1.0" encoding="utf-8"?>
<manifest xmlns:android="http://schemas.android.com/apk/res/android"
    package="com.example.pushmessaging">

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
        <service
            android:name=".MyService"
            android:exported="false">
            <intent-filter>
                <action android:name="com.google.firebase.MESSAGING_EVENT" />
            </intent-filter>
        </service>

        <activity android:name=".MainActivity">
            <intent-filter>
                <action android:name="android.intent.action.MAIN" />

                <category android:name="android.intent.category.LAUNCHER" />
            </intent-filter>
        </activity>
    </application>

</manifest>
```

## Ejecución de la aplicación

Ejecute la aplicación haciendo clic en la flecha **** verde de la barra de herramientas o del [!DNL Run] menú.
