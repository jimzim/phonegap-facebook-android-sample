Phonegap Facebook Android Sample
================================

It took me a while to figure out how to get this to work by having to go through pull requests, phonegap documentation and different threads.  The whole time i was just wishing I had a downloadable sample that just worked.  This is why I put this up here.  When the official plug-in is updated, this sample may be updated or they may have a better way to do it once it is done.  I had to get some work done and could not wait so I just got it working.

A simple sample to show how to use the Facebook native login with Phonegap 3.0 and a modified version of https://github.com/phonegap/phonegap-facebook-plugin with this pull request: https://github.com/phonegap/phonegap-facebook-plugin/pull/348  and some other config options found in this thread.

First you need to make sure you have your android build settings set up to match your sdk path, and build targets.  Typically this would not be checked into source control, but I am trying to make this as painless as possible to get started with a demo.

Open this file:  [platforms/android/local.properties](https://github.com/jimzim/phonegap-facebook-android-sample/blob/master/platforms/android/local.properties#L10) and put the appropriate path in your environment here
```
sdk.dir=/Users/jimzimmerman/Documents/adt-bundle-mac-x86_64/sdk
```

Open this file:  [platforms/android/project.properties](https://github.com/jimzim/phonegap-facebook-android-sample/blob/master/platforms/android/project.properties#L14) and put the appropriate target you have installed, in my case it is version 18, yours may be 17
```
target=android-18
```

Open this file: [platforms/android/AndroidManifest.xml](https://github.com/jimzim/phonegap-facebook-android-sample/blob/master/platforms/android/AndroidManifest.xml#L14), change this to 17 if you don't have 18 installed.
```
android:targetSdkVersion="18" 
```


Add your Facebook app id in index.html

```js
FB.init({ 
      appId: "", 
      nativeInterface: CDV.FB, 
      useCachedDialogs: false 
    });
```

As long as you have phonegap installed, just run this command and it will install on your android device or open the emulator.  This assumes you have your phonegap environment set up.
```bash
phonegap install android
```

