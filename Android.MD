# RTLS Sensor SDK for Android

## Installation

> Maven
```xml
<dependency>
  <groupId>vip.corelink.rtls.app</groupId>
  <artifactId>sensor</artifactId>
  <version>0.0.3</version>
  <type>pom</type>
</dependency>
```

> Gradle
```gradle
compile 'vip.corelink.rtls.app:sensor:0.0.3'
```

> Ivy
```xml
<dependency org='vip.corelink.rtls.app' name='sensor' rev='0.0.3'>
  <artifact name='sensor' ext='pom' ></artifact>
</dependency>
```

## Usage

kotlin
```kt
import vip.corelink.rtls.app.sensor.Ble

val ble = Ble(context)
ble.start({ ->
    ok()
}, { errorCode ->
    fail(errorCode)
})

// Stop
ble.stop()
```

### Constructor
```kt
class Ble(context: Context)
```

### Properties
```kt
var id: Int
// 0 - 65535 default value: 0
var customFlag: Int
// 0 - 127 default value: 0
var alarm: Boolean
// default value: false
var battery: Int
// 0 - 10 default value: 0

var advertiseMode: Int
// 0 - 2 default value: AdvertiseSettings.ADVERTISE_MODE_BALANCED
var txPowerLevel: Int
// 0 - 3 default value: AdvertiseSettings.ADVERTISE_TX_POWER_HIGH
```

### Methods
```kt
/**
* Start advertising
*/
fun start()
fun start(callback: (() -> Unit)?)
fun start(callback: (() -> Unit)?, fail: ((errorCode: Int) -> Unit)?)

/**
* Stop advertising
*/
fun stop()
```
