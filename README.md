# xwalk-chromedriver
This Chromedriver can be used to work with Appium and Crosswalk

This was tested with Appium 1.4.16.

Just put the patched android-hybrid.js to your Appium folder -> `.../appium/lib/devices/android/`

You can now launch Appium with the following command:

`appium --chromedriver-executable=path/to/patched/chromedriver`

Don't forget to pass the right capabilities!

Java:

```
desiredCapabilities.setCapability("androidDeviceSocket", APP_PACKAGE + "_devtools_remote");
ChromeOptions chromeOptions = new ChromeOptions();
chromeOptions.setExperimentalOption("androidDeviceSocket", APP_PACKAGE + "_devtools_remote");
desiredCapabilities.setCapability(ChromeOptions.CAPABILITY, chromeOptions);
```

Have fun!
