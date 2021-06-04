# hellofx-jni-awt-bug
Sample project demonstrating bug that causes dlopen failed: cannot locate symbol "JNI_OnLoad_awt" error when building an android native image.

### To Reproduce

Connect android device via adb. Build and link, package an apk, and install then run it on an adb connected android device via the command below. `client:run` will run the already installed app on the phone, and setup logcat outputting the app logs. Opening the app on the device should immediately result in a crash.

```mvn -Pandroid clean client:build client:package client:install client:run```

This will generate an apk under `target/client/aarch64-android/gvm`. 
