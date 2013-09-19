phonegap-facebook-android-sample
================================

A simple sample to show how to use the Facebook native login with Phonegap 3.0 and a modified version of phonegap-facebook-plugin

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