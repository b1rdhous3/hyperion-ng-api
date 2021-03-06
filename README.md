# Hyperion NG Api

#WARNING: PACKAGE IS NOT SUPPORTED ANYMORE. 

This is an early version. Still to do a lot. Testing, documentation and implementing more functionality.

### Installation
[![npm version](https://badge.fury.io/js/hyperion-ng-api.svg)](https://badge.fury.io/js/hyperion-ng-api)
```sh
$ npm install --save hyperion-ng-api
```

### Usage
```
const HyperionNg = require('hyperion-ng-api');

//Host, Port, WsTan, Priority (Use 1 if you want to overwrite WebUI priority. Remember WebUI is always priority 1.)
hyperion = new HyperionNg('192.168.178.23', 19444, 666, 1);

hyperion.getServerInfo(function (err, data){
  (err) ? console.log(err) : console.log(data);
})
```

### Changelog

0.0.4 (2018-06-07): Added functions "getStartupEffect" and "playStatupEffect"

0.0.3 (2018-06-01): Added more documentation. Deleted a duplicated function

0.0.2 (2018-06-01): Small file changes

0.0.1 (2018-06-01): First Version

### Table of Contents

-   [disableHyperion][1]
-   [enableHyperion][2]
-   [disableLedDevice][3]
-   [enableLedDevice][4]
-   [getServerInfo][5]
-   [getAllComponents][6]
-   [getAllEffects][7]
-   [getStartupEffect][8]
-   [getAllGrabbers][9]
-   [getAllLedDevices][10]
-   [getLedMappingType][11]
-   [getAllPriorities][12]
-   [getSysInfo][13]
-   [getServerConfig][14]
-   [getServerConfigSchema][15]
-   [setMappingTypeMulticolor][16]
-   [setMappingTypeUnicolor][17]
-   [setMappingType][18]
-   [setComponentState][19]
-   [setColor][20]
-   [setColorToBlackPermanently][21]
-   [setEffect][22]
-   [setBrightness][23]
-   [setSourceToAutoSelection][24]
-   [setSource][25]
-   [clearPriority][26]
-   [clearApiPriority][27]
-   [clearAllPriority][28]
-   [playStatupEffect][29]
-   [sendToHyperion][30]

## disableHyperion

disableHyperion: Disables all activated components. The Ng-Way to switch off.

**Parameters**

-   `callback` **[Function][31]** 

Returns **[Function][31]** callback return string from hyperion.ng

## enableHyperion

enableHyperion: Enables all previous activated components. The Ng-Way to switch on.

**Parameters**

-   `callback` **[Function][31]** 

Returns **[Function][31]** callback return string from hyperion.ng

## disableLedDevice

disableLedDevice: Disables the LED Device. You can see this as "send color black"

**Parameters**

-   `callback` **[Function][31]** 

Returns **[Function][31]** callback return string from hyperion.ng

## enableLedDevice

enableLedDevice: Activates the LED Device.

**Parameters**

-   `callback` **[Function][31]** 

Returns **[Function][31]** callback return string from hyperion.ng

## getServerInfo

getServerInfo: Get the server info JSON. All information you need from hyperion. There are more functions available to wrap this. Eg: getAllEffects

**Parameters**

-   `callback` **[Function][31]** 

Returns **[Function][31]** callback return string from hyperion.ng

## getAllComponents

getAllComponents: Get all components. Wrap function for getServerInfo

**Parameters**

-   `callback` **[Function][31]** 

Returns **[Function][31]** callback return string from hyperion.ng

## getAllEffects

getAllEffects: Get all effects. Wrap function for getServerInfo

**Parameters**

-   `callback` **[Function][31]** 

Returns **[Function][31]** callback return string from hyperion.ng

## getStartupEffect

getStartupEffect: Gets the effect which is used for startup

**Parameters**

-   `callback` **[Function][31]** 

Returns **[Function][31]** callback return string from hyperion.ng

## getAllGrabbers

getAllGrabbers: Get all Grabbers. Wrap function for getServerInfo

**Parameters**

-   `callback` **[Function][31]** 

Returns **[Function][31]** callback return string from hyperion.ng

## getAllLedDevices

getAllLedDevices: Get all led devices. Wrap function for getServerInfo

**Parameters**

-   `callback` **[Function][31]** 

Returns **[Function][31]** callback return string from hyperion.ng

## getLedMappingType

getLedMappingType: Get the current led mapping type. Wrap function for getServerInfo

**Parameters**

-   `callback` **[Function][31]** 

Returns **[Function][31]** callback return string from hyperion.ng

## getAllPriorities

getAllPriorities: Get all priorities. Wrap function for getServerInfo

**Parameters**

-   `callback` **[Function][31]** 

Returns **[Function][31]** callback return string from hyperion.ng

## getSysInfo

getSysInfo: Get system information about the operating system of hyperion.ng instance

**Parameters**

-   `callback` **[Function][31]** 

Returns **[Function][31]** callback return string from hyperion.ng

## getServerConfig

getServerConfig: Gets the current config file

**Parameters**

-   `callback` **[Function][31]** 

Returns **[Function][31]** callback return string from hyperion.ng

## getServerConfigSchema

getServerConfigSchema: Gets the current config schema

**Parameters**

-   `callback` **[Function][31]** 

Returns **[Function][31]** callback return string from hyperion.ng

## setMappingTypeMulticolor

setMappingTypeMulticolor: Set the Led Mapping Type to multicolor (classic atmolight)

**Parameters**

-   `callback` **[Function][31]** 

Returns **[Function][31]** callback return string from hyperion.ng

## setMappingTypeUnicolor

setMappingTypeMulticolor: Set the Led Mapping Type to unicolor (one color calculated and send to ALL leds)

**Parameters**

-   `callback` **[Function][31]** 

Returns **[Function][31]** callback return string from hyperion.ng

## setMappingType

setMappingType: Set the Led Mapping type. Currently 'unicolor_mean' and 'multicolor_mean' is supported. Inserting something other will likely result in an error

**Parameters**

-   `type` **[string][32]** for now only use 'unicolor_mean' or 'multicolor_mean'
-   `callback` **[Function][31]** 

Returns **[Function][31]** callback return string from hyperion.ng

## setComponentState

setComponentState: Sets a component to true or false

**Parameters**

-   `comp` **[string][32]** The component. You can use getAllComponents to get the names.
-   `state` **[boolean][33]** true or false
-   `callback` **[Function][31]** 

Returns **[Function][31]** callback return string from hyperion.ng

## setColor

setColor: Sets the color for a given priority and duration

**Parameters**

-   `r` **[number][34]** 
-   `g` **[number][34]** 
-   `b` **[number][34]** 
-   `duration` **[number][34]** in seconds. Use 0 for infinite
-   `callback` **[Function][31]** 

Returns **[Function][31]** callback return string from hyperion.ng

## setColorToBlackPermanently

setColorToBlackPermanently: Sets the color to black with duration 0

**Parameters**

-   `callback` **[Function][31]** 

Returns **[Function][31]** callback return string from hyperion.ng

## setEffect

setEffect: Sets an effect.

**Parameters**

-   `effectName` **[string][32]** You can use getAllEffects to get the name
-   `duration` **[number][34]** in seconds. Use 0 for infinite
-   `callback` **[Function][31]** 

Returns **[Function][31]** callback return string from hyperion.ng

## setBrightness

setBrightness: Set the led brightness

**Parameters**

-   `value` **[number][34]** 0 to 100
-   `callback` **[Function][31]** 

Returns **[Function][31]** callback return string from hyperion.ng

## setSourceToAutoSelection

setSourceToAutoSelection: Activates autoselection

**Parameters**

-   `callback` **[Function][31]** 

Returns **[Function][31]** callback return string from hyperion.ng

## setSource

setSource: set a source (priority) to active

**Parameters**

-   `priority` **[number][34]** You can use getAllPriorities to get the id
-   `callback` **[Function][31]** 

Returns **[Function][31]** callback return string from hyperion.ng

## clearPriority

clearPriority: clears the given priority

**Parameters**

-   `priority` **[number][34]** You can use getAllPriorities to get the id
-   `callback` **[Function][31]** 

Returns **[Function][31]** callback return string from hyperion.ng

## clearApiPriority

clearApiPriority: clears the priority which is used by this api

**Parameters**

-   `callback` **[Function][31]** 

Returns **[Function][31]** callback return string from hyperion.ng

## clearAllPriority

clearAllPriority: clears all priority

**Parameters**

-   `callback` **[Function][31]** 

Returns **[Function][31]** callback return string from hyperion.ng

## playStatupEffect

playStatupEffect: plays the startup effect with configured time

**Parameters**

-   `callback` **[Function][31]** 

Returns **[Function][31]** callback return string from hyperion.ng

## sendToHyperion

sendToHyperion: Main function to communicate with hyperion.ng. This function is calles by the other functions. If you know the commands you want to call on hyperion side you can call this function directly.

**Parameters**

-   `command` **[string][32]** 
-   `subcommand` **[string][32]** 
-   `msg` **[string][32]** 
-   `wsTan` **[number][34]** 
-   `callback` **[Function][31]** 

Returns **[Function][31]** callback return string from hyperion.ng

[1]: #disablehyperion

[2]: #enablehyperion

[3]: #disableleddevice

[4]: #enableleddevice

[5]: #getserverinfo

[6]: #getallcomponents

[7]: #getalleffects

[8]: #getstartupeffect

[9]: #getallgrabbers

[10]: #getallleddevices

[11]: #getledmappingtype

[12]: #getallpriorities

[13]: #getsysinfo

[14]: #getserverconfig

[15]: #getserverconfigschema

[16]: #setmappingtypemulticolor

[17]: #setmappingtypeunicolor

[18]: #setmappingtype

[19]: #setcomponentstate

[20]: #setcolor

[21]: #setcolortoblackpermanently

[22]: #seteffect

[23]: #setbrightness

[24]: #setsourcetoautoselection

[25]: #setsource

[26]: #clearpriority

[27]: #clearapipriority

[28]: #clearallpriority

[29]: #playstatupeffect

[30]: #sendtohyperion

[31]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Statements/function

[32]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String

[33]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Boolean

[34]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Number
