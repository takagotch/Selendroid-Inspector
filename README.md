### Selendroid-Inspector
---
http://selendroid.io/inspector.html

```
java -jar selendroid-standalone-0.17.0-with-dependencies.jar -app selendroid-test-app-0.17.apk
```

```
{
  status: 0,
  value: {
  "os": {
    "name": "Android"
  },
  "build": {
    "browsername": "selendroid",
    "version": "0.17.0"
  },
  "supportedApps": [{
    "appId": "io.selendroid.testapp:0.17.0",
    "mainActivity": "io.selendroid.testapp.HomeScreenActivity",
    "basePackage": "io.selendroid.testapp"
  }],
  "supportedDevices": [{
    "screenSize": "320x480",
    "targetPlatform": "ANDROID17",
    "emulator": true,
    "avdName": "latest"
  }, {
    "screenSize": "320x480",
    "targetPlatform": "ANDROID16",
    "emulator": true,
    "avdName": "es"
  }, {
    "screenSize": "320x480",
    "targetPlatform": "ANDROID10", 
    "emulator": true,
    "avdName": "AVD_fro_api10"
  }]
  }
}
```

```js
SelendroidCapabilities capa = new SlendroidCapabilities("io.selendroid.testapp:0.17.0");

WebDriver driver = new SelendroidDriver(capa);
WebElement inputFileld = driver.findElement(By.id("my_text_field"));
Assert.assertEquals("true", inputField.getAttribute("enabled"));
inputField.sendKeys("Selendroid");
Assert.assertEquals("Selendroid", inputField.getText());
driver.quit();

SelendroidCapabilities capa = new SelendroidCapabilities("io.selendroid.testapp:0.8.0");
capa.setPlatformVersion(DeviceTargetPlatform.ANDROID18);
capa.setEmulator(true);
capa.setModel("nexus 7");
```
