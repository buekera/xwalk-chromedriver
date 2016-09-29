# xwalk-chromedriver
This Chromedriver can be used to work with Appium and Crosswalk on Linux based systems

Unfortunately I had to uploead the chromedriver elsewhere because it's too big for github (I don't know why it's that big...)
You can download it here: http://www.megafileupload.com/fo3m/chromedriver

This is only working with Appium 1.4.16 or older!

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
