# projet-android
ProjetAndroid : Voiture télécommandée via une application Android sur la base d'une carte IOIO

## Préambule
Dans la majorité des cas, les étudiants débutant ce projet n'ont pas de connaissance en programmation JAVA.

Cette apport de code a pour but d'aider à la prise en main rapide du projet Android proposé par l'IUT.

## Débuter la programmation Android

1) Lancer Android Studio
2) Cliquer sur "Start a new Android Studio Project
3) Choisissez "Empty Activity"
4) Donnez un nom à votre application, choisissez l'emplacement. Minimum API Level : API 19 Android 4.4 (KitKat). Cliquez sur finish
5) Les fichiers dans lequels vous travaillerez principalement sont les suivants :
  - app > java > 1er dossier > MainActivity.java
  - res > Layout > activity_main.xml
  - app > manifests > AndroidManifest.xml
 
 ## Démarches
 
 ### AndroidManifest.xml
 Ce fichier a pour but de définir les différentes caractéristiques du projet (matériel, paramètres de sécurité, nom de l'application, logo)
 
 Dans celui-ci, nous allons ajouter du code permettant d'autoriser l'accès à Internet ainsi qu'au module Bluetooth du téléphone.
 /!\ Si vous n'ajoutez pas ce code, lorsque l'application tentera de se connecter au Bluetooth du téléphone, celle-ci se fermera automatiquement car elle n'en possède pas les droits.
 
 Entre les balises `<manifest>`, ajouter le morceau de code suivant :
 
 ```
<uses-permission android:name="android.permission.INTERNET" />
<uses-permission android:name="android.permission.BLUETOOTH" />
<uses-permission android:name="android.permission.BLUETOOTH_ADMIN" />
```

### activity_main.xml
Ce fichier est un fichier texte qui est éditable en mode visuel permettant de définir les éléments physiques qui seront affichés sur l'application.

A travers ce fichier, vous pourrez ainsi ajouter un bouton ou un texte à afficher.

Par exemple, nous pouvons utiliser un ToggleButton : il s'agit d'un bouton poussoir avec auto-maintien. Pour qu'il puisse être positionné selon l'emplacement que vous souhaitez, vous devez contraindre ce bouton au cadre de l'application.

![alt tag](https://raw.githubusercontent.com/ioio-geii/projet-android/master/Capture%20d%E2%80%99e%CC%81cran%202019-04-01%20a%CC%80%2016.32.20.png)

### MainActivity.java



## Les causes possibles d'un plantage de l'application
Lorsque vous lancer l'application Android sur votre smartphone, il arrive que l'application ne démarre pas et se ferme.
Ce plantage provient de votre code.
Voici les différents cas à vérifier, cela peut vous aider :
- Vous avez défini le mauvais type de variable !
- Mauvaise utilisation d'une fonction
- Utilisation d'une boucle infinie
