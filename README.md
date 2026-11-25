# Orconovo

Gioco stile Arkanoid per Android.
- Inclina lo smartphone per muovere l'astronave
- Tocca ovunque per lanciare la palla e per sparare (il laser usa energia che si ricarica)
- 5 livelli, bonus (W allarga, S rallenta, M multipalla, L vita, E energia), musica e suoni generati in tempo reale

## Ottenere l'APK senza installare nulla (GitHub)
1. Crea un repository su GitHub e carica il contenuto di questa cartella.
2. Vai nella scheda **Actions** → "Build APK Orconovo" → attendi circa 5 minuti.
3. Scarica l'artefatto **Orconovo-apk**, estrai `app-debug.apk` e copialo sul telefono.
4. Sul telefono abilita "Installa app da origini sconosciute" e apri il file.

## In locale (serve Android Studio / SDK, Node 22, Java 21)
```
npm install
npx cap add android
# in android/app/src/main/AndroidManifest.xml aggiungi android:screenOrientation="portrait" al tag <activity>
npx cap sync android
cd android && ./gradlew assembleDebug
```
L'APK si trova in `android/app/build/outputs/apk/debug/app-debug.apk`.

## Prova rapida senza APK
Apri `www/index.html` col browser del telefono (da un server HTTPS): funziona anche così.
Su PC: frecce o mouse per muovere, spazio/click per sparare.
