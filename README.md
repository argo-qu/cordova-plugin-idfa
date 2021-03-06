# cordova-plugin-idfa<br>[![NPM version][npm-version]][npm-url] [![NPM downloads][npm-downloads]][npm-url] [![Twitter][twitter-follow]][twitter-url]
Cordova plugin to get Advertising ID (IDFA or AAID)

## Installation

    cordova plugin add cordova-plugin-idfa --save

Plugin depends on [cordova-support-google-services](https://github.com/chemerisuk/cordova-support-google-services) for setting up google services properly. Please read the [README](https://github.com/chemerisuk/cordova-support-google-services/blob/master/README.md) carefully in order to avoid common issues with a project configuration.

## Supported Platforms

- iOS
- Android

## Methods
Every method returns a promise that fulfills when a call was successful.

### getInfo()
Returns advertising id with `limitAdTracking` flag. On iOS use `idfa` property, on Android use `aaid`.
```js
cordova.plugins.idfa.getInfo().then(function(info) {
    if (!info.limitAdTracking) {
        console.log(info.idfa || info.aaid);
    }
});
```
[npm-url]: https://www.npmjs.com/package/cordova-plugin-idfa
[npm-version]: https://img.shields.io/npm/v/cordova-plugin-idfa.svg
[npm-downloads]: https://img.shields.io/npm/dm/cordova-plugin-idfa.svg
[twitter-url]: https://twitter.com/chemerisuk
[twitter-follow]: https://img.shields.io/twitter/follow/chemerisuk.svg?style=social&label=Follow%20me
