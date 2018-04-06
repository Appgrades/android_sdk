<p align="center" >
  <img align="center" src="https://appgrades.io/img/dash.png" alt="Appgrades" title="Appgrades">
</p>

[![Platform](https://img.shields.io/badge/platform-android-green.svg)](https://docs.appgrades.io/appgrades_io)
[![Version](https://img.shields.io/badge/version-v1.0.0-orange.svg)](https://docs.appgrades.io/appgrades_io)
[![Licence](https://img.shields.io/badge/licence-Commercial-lightgray.svg)](https://docs.appgrades.io/appgrades_io)
[![Twitter](https://img.shields.io/badge/twitter-@appgrades_io-blue.svg?style=flat)](https://twitter.com/appgrades_io)

Appgrades is a light version management platform for mobile apps. It provides iOS and Android SDKs to be integrated in your mobile apps and a rich user friendly Dashboard to manage your apps versions adoption rates. With few clicks, you can convert all your old versions users to the newest one. No code needed while providing a visual preview of the UI componement you can display to your users during the conversion process.

Choose Appgrades for all your projects, you never know when you will really need to push your users to use a recent version of your app!

## How To Get Started

- Check out the [documentation](https://docs.appgrades.io) for a comprehensive look at all needed steps to get your app configured with Appgrades.
- Make sure you have installed **Android Studio** and **Android SDK**

## Communication

- If you **need help**, use [Stack Overflow](https://stackoverflow.com/questions/tagged/appgrades). (Tag 'appgrades') or contact us at contact@appgrades.io
- If you **found a bug**, _and can provide steps to reliably reproduce it_, open an issue.
- If you **have a feature request**, contact us at contact@appgrades.io
- You can, at any moment, chat with us from your [Appgrades Dashboard](https://dash.appgrades.io)


## Installation

#### Download the SDK


- Download the SDK [here](https://docs.appgrades.io/android/Appgrades-android.zip)


#### Manage Dependencies

Copy `appgrades.aar` library file under your app `libs` directory. 
Reference the aar file by adding a directory repository of the libs folder of your app module:

```groovy
allprojects {
    repositories {
        jcenter()
        flatDir {
            dirs 'libs'
        }
    }
}
```

Finally, reference the library in the dependency section:

```groovy
dependencies {
    compile(name:'appgrades', ext:'aar')
}
```

Now, the library is fully integrated to the app and you can start using it.

## Run the service

#### Import the Appgrades class

From your app `MainActivity` class, import the Appgrades class:

```java
import io.appgrades.sdk.Appgrades;
```

#### Get your Developer Key

Get your Developer Key from the Appgrades Dashboard. From the Dashboard, click on `Copy Key to clipboard`.

<p align="center" >
  <img align="center" src="https://docs.appgrades.io/android/assets/key.png" alt="Appgrades" title="Get your developer key">
</p>

#### Start the service

From your app `MainActivity` class, in `onCreate` method, call the run function to start appgrades and pass your Developer key and the current application context:

```java
Appgrades.run("YOUR_DEVELOPER_KEY", this.getApplicationContext());
```
          
                                    

## Check the integration

#### Enable the logger

Optionally, you can enable to the logger. Use the following code to set a logging level to the logger:

```java
Appgrades.logger.setLogLevel(LogLevel.VERBOSE);
```
                                    
You can choose one of the following logging levels:

```java
VERBOSE
INFO
WARNING
ERROR
NONE
```

#### Run the app

Run your application on Emulator or device.

#### Check the Dashboard
Visit the [Appgrades Dashboard](https://dash.appgrades.io). You should see appearing your app listed.

<p align="center" >
  <img align="center" src="https://docs.appgrades.io/android/assets/dashboard.png" alt="Appgrades" title="Appgrades Dashboard">
</p>


## License

Appgrades is released under a Commercial license. See [LICENSE](https://dash.appgrades.io/terms) for details.
