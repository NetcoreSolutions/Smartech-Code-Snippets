## Step 2: Integrate the latest Smartech SDK

Make the following changes in the app-level build.gradle
```shell-session
apply plugin: 'com.android.application'

android {
    defaultConfig { ... }
    buildTypes {}
}

repositories {
    maven { url 'https://artifacts.netcore.co.in/artifactory/android' }
}

dependencies {
    implementation 'com.netcore.android:smartech-sdk:3.5.6'
    // WorkManager Version 2.7.0 is required for apps targeting Android 12 (S), uncomment the below line based on the app side requirement

    // (Java only enable below)
    // implementation 'androidx.work:work-runtime:2.7.0'

    // Kotlin + coroutines enable below
    // implementation 'androidx.work:work-runtime-ktx:2.7.0'
}

buildscript {
}
```
