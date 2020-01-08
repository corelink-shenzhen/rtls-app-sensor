# Cordova Plugin for Corelink RTLS Sensor 

- [ ] ios
- [x] android

## Installation

```
cordova plugin add cordova-plugin-corelink-rtls-sensor --save
```
or via ionic
```
ionic cordova plugin add cordova-plugin-corelink-rtls-sensor
```

## Relative Dependencies

[cordova-support-kotlin](https://github.com/kainonly/cordova-support-kotlin)

```
cordova plugin add cordova-support-kotlin --save
```
or via ionic
```
ionic cordova plugin add cordova-support-kotlin
```

## Usage

### Ble.start
##### Definition

```ts
Ble.start(successCallback: () => void, failedCallback(errCode: number) => void)
```
##### Example
```js
Ble.start(() => {
  console.log('started');
}, errCode => {
  console.error('Failed to start,', errCode);
});
```

### Ble.stop
##### Definition
```ts
Ble.stop(successCallback: () => void, failedCallback(errCode: number) => void)
```
##### Example
```js
Ble.stop(() => {
  console.log('stopped');
}, errCode => {
  console.error('Failed to stop,', errCode);
});
```

### Ble.setId
##### Definition
```ts
Ble.setId(id: number, successCallback: () => void, failedCallback(errCode: number) => void)
```
##### Example
```js
Ble.setId(0, () => {
  console.log('set id to 0');
}, errCode => {
  console.error('failed to set id', errCode);
});
```

> Id is a number from 0 to 0xffff.

### Ble.setCustomFlag
##### Definition
```ts
Ble.setCustomFlag(customFlag: number, successCallback: () => void, failedCallback(errCode: number) => void)
```
##### Example
```js
Ble.setCustomFlag(0, () => {
  console.log('set customFlag to 0');
}, errCode => {
  console.error('failed to set customFlag', errCode);
});
```

> CustomFlag is a number from 0 to 127.

### Ble.setAlarm
##### Definition
```ts
Ble.setAlarm(alarm: boolean, successCallback: () => void, failedCallback(errCode: number) => void)
```
##### Example
```js
Ble.setAlarm(true, () => {
  console.log('set alarm to true');
}, errCode => {
  console.error('failed to set alarm', errCode);
});
```

### Ble.setBattery
##### Definition
```ts
Ble.setBattery(battery: number, successCallback: () => void, failedCallback(errCode: number) => void)
```
##### Example
```js
Ble.setBattery(0, () => {
  console.log('set battery to 0');
}, errCode => {
  console.error('failed to set battery', errCode);
});
```

> Battery is a number from 0 to 10.

### Ble.setTxPowerLevel
##### Definition
```ts
Ble.setTxPowerLevel(txPowerLevel: number, successCallback: () => void, failedCallback(errCode: number) => void)
```
##### Example
```js
Ble.setTxPowerLevel(0, () => {
  console.log('set txPowerLevel to 0');
}, errCode => {
  console.error('failed to set txPowerLevel', errCode);
});
```
> TxPowerLevel 
- 0: ADVERTISE_TX_POWER_ULTRA_LOW
- 1: ADVERTISE_TX_POWER_LOW
- 2: ADVERTISE_TX_POWER_MEDIUM
- 3: ADVERTISE_TX_POWER_HIGH (default)

### Ble.setAdvertiseMode
##### Definition
```ts
Ble.setAdvertiseMode(AdvertiseMode: number, successCallback: () => void, failedCallback(errCode: number) => void)
```
##### Example
```js
Ble.setAdvertiseMode(0, () => {
  console.log('set advertiseMode to 0');
}, errCode => {
  console.error('failed to set advertiseMode', errCode);
});
```

> AdvertiseMode
- 0: ADVERTISE_MODE_LOW_POWER
- 1: ADVERTISE_MODE_BALANCED (default)
- 2: ADVERTISE_MODE_LOW_LATENCY

