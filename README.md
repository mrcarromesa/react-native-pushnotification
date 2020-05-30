# PushNotification

## Android

- Referências:
  - [Artigo bem completo para IOS e Android utilizando o Firebase](https://medium.com/bouncingshield/react-native-push-notifications-with-firebase-d23ed0dfb3ae)
  - [Vídeo que mostra como fazer para android](https://www.youtube.com/watch?v=03-A9HdyB-Y)
  - [Alterar ícone e cor do icons quando for push notification](https://stackoverflow.com/questions/30795431/android-push-notifications-icon-not-displaying-in-notification-white-square-sh)
  - [Firebase para RN](https://rnfirebase.io/messaging/usage)
  - [Repositório React Native Push Notifications](https://github.com/zo0r/react-native-push-notification)

- Basicamente seguir as instruções da lib das duas ultimas referencias


- Problema que pode acontecer com android, seria o icone do push notification:

- Criei o arquivo de push seguind esses passos: (Android Studio 3.5) If you're a recent version of Android Studio, you can generate your notification images. Right click on your res folder > New > Image Asset. You will then see Configure Image Assets as shown in the image below. Change Icon Type to Notification Icons. Your images must be white and transparent. This Configure Image Assets will enforce that rule.
-  Ajustei no `AndroidManifest.xml`:

```xml
<meta-data
    android:name="com.google.firebase.messaging.default_notification_icon"
    android:resource="@drawable/ic_stat_name" />

<meta-data
    android:name="com.google.firebase.messaging.default_notification_color"
    android:resource="@color/black" />
```