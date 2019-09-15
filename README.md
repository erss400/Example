# NativeScript-Vue Application

> A native application built with NativeScript-Vue

## Steps to reproduce

``` bash
# Install Vue Cli globally
npm install -g @vue/cli @vue/cli-init

# Create a new project
$ vue init nativescript-vue/vue-cli-template <project-name>
$ cd <project-name>

# Install dependencies
npm install

# Install nativescript-plugin-firebase
tns plugin add nativescript-plugin-firebase
```

## Configure plugin in main.js

NativeScript Firebase Plugin Installation

No existing firebase.nativescript.json config file found, so let's configure the Firebase plugin!

prompt: Are you using this plugin ONLY as a Push Notification client for an external (non-Firebase) Push service? (y/n):  (n) n

prompt: Are you using iOS (y/n):  (y) y

prompt: Are you using Android (y/n):  (y) y

prompt: Are you using Firestore? (y/n):  (n) y

prompt: Are you using Realtime DB? (y/n):  (n) y

prompt: Are you using Firebase Authentication (pretty likely if you use Firestore or Realtime DB)? (y/n):  (y) y

prompt: Are you using Firebase RemoteConfig? (y/n):  (n) y

prompt: Are you using Performance Monitoring? (y/n):  (n) y

prompt: Are you using Firebase Cloud Messaging? (y/n):  (n) y

prompt: Are you using In-App Messaging? (y/n):  (n) y

prompt: Are you using Firebase Crashlytics? (y/n):  (n) y

prompt: Are you using Firebase Storage? (y/n):  (n) y

prompt: Are you using Firebase Cloud Functions? (y/n):  (n) y

prompt: Are you using Firebase Facebook Authentication? (y/n):  (n) y

prompt: Are you using Firebase Google Authentication? (y/n):  (n) y

prompt: Are you using AdMob? (y/n):  (n) y

prompt: Are you using Firebase Dynamic Links? (y/n):  (n) y

prompt: Are you using ML Kit? (y/n):  (n) n

Successfully created iOS (Pod) file.

Install google-service.json after-prepare copy hook.

Install google-service.json before-checkForChanges copy hook.

Install Crashlytics buildscript hook.

Successfully created Android (include.gradle) file.

Install google-service.json after-prepare copy hook.

Install google-service.json before-checkForChanges copy hook.

Firebase post install completed. To re-run this script, navigate to the root directory of `nativescript-plugin-firebase` in your `node_modules` folder and run: `npm run config`.

prompt: Do you want to save the selected configuration. Reinstalling the dependency will reuse the setup from: firebase.nativescript.json. CI will be easier. (y/n):  (y) y

## Setup plugin in main.js

`var firebase = require("nativescript-plugin-firebase");
`

  firebase.init({
    // Optionally pass in properties for database, authentication and cloud messaging,

    // see their respective docs.
  }).then(

    function () {
      console.log("firebase.init done");
    },
    function (error) {
      console.log("firebase.init error: " + error);
    });

## Enable multiDexEnabled in app.gradle

`android {`

`defaultConfig {`

    `minSdkVersion 17`

    generatedDensities = []

    multiDexEnabled true

`}`

`aaptOptions {`

    `additionalParameters "--no-version-vectors"`

`}`

`}`

## Run build

``` bash
# Build, watch for changes and run the application
tns run android
```
## Error message

`Failed with these Error`

`Note: Recompile with -Xlint:deprecation for details.`

`Skip com.google.errorprone.annotations.IncompatibleModifiers`

`Error: java.lang.NullPointerException`

`WARNING: Skipping interface org.apache.http.client.ResponseHandler implemented in com.google.firebase.perf.network.zzg as it cannot be resolved`

`Project successfully built.`

`The build result is located at: /home/erss400/Desktop/projects/jekalowa/apps/Example/platforms/android/app/build/outputs/apk/debug/app-debug.apk`

`Installing on device 8c5669bf...`

`Successfully installed on device with identifier '8c5669bf'.`

`Unable to apply changes on device: 8c5669bf. Error is: Socket connection timed out..
`
## Run build

``` bash
# Update project
tns update

# Build, watch for changes and run the application
tns run android
```

## Error message

`Failed with these Error`

`Note: Recompile with -Xlint:deprecation for details.`

`Skip com.google.errorprone.annotations.IncompatibleModifiers`

`Error: java.lang.NullPointerException`

`WARNING: Skipping interface org.apache.http.client.ResponseHandler implemented in com.google.firebase.perf.network.zzg as it cannot be resolved`

`Project successfully built.`

`The build result is located at: /home/erss400/Desktop/projects/jekalowa/apps/Example/platforms/android/app/build/outputs/apk/debug/app-debug.apk`

`Installing on device 8c5669bf...`

`Successfully installed on device with identifier '8c5669bf'.`

`Unable to apply changes on device: 8c5669bf. Error is: Socket connection timed out..
`
