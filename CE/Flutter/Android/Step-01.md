## Step1: Installing CEE Flutter Plugin

Implement plugin in pubspecs.yaml file under dependencies:

By using pub
```
smartech_base: ^3.2.1
```

## For Android SDK Setup

To initiate the CEE SDK, Add below in Application class

Java code snippet
```
override fun onCreate() {
    super.onCreate()
    SmartechBasePlugin.Companion.initializePlugin(this);
}
```

Kotlin code snippet
```
override fun onCreate() {
    super.onCreate()
    SmartechBasePlugin.initializePlugin(this)
}
```
