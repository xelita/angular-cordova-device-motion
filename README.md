angular-device
==============

Bring Apache Cordova Device Motion API to AngularJS Apps...

Define a simple service to deal with Cordova Device Motion Plugin (https://github.com/apache/cordova-plugin-device-motion). 

[![Build Status](https://travis-ci.org/xelita/angular-device-motion.png?branch=master)](https://travis-ci.org/xelita/angular-device-motion)

Usage
-----
Include cordovaDeviceMotionModule.js in your Cordova application.

```html
<script src="js/cordovaDeviceMotionModule.js"></script>
```

or use the minified version:

```html
<script src="js/cordovaDeviceMotionModule.min.js"></script>
```

Add the module `cordovaDeviceMotionModule` as a dependency to your app module:

```js
var myapp = angular.module('myapp', ['cordovaDeviceMotionModule']);
```

Use the cordovaDeviceMotionModule as controller dependency and call cordovaDeviceMotionModule API:

```js
$scope.getCurrentAcceleration = function() {
    cordovaDeviceMotionService.getCurrentAcceleration(function(acceleration){
	    alert('Acceleration X: ' + acceleration.x + '\n' +
	          'Acceleration Y: ' + acceleration.y + '\n' +
	          'Acceleration Z: ' + acceleration.z + '\n' +
	          'Timestamp: '      + acceleration.timestamp + '\n'
	    );
    });
};
```

Sample
------
A sample based on Ionic Framework can be found here:
https://github.com/xelita/angular-cordova-plugins-sample
