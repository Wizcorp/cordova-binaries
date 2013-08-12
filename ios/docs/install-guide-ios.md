# install-guide-ios

## Where?

Frameworks are already pre-built and included in the **bin** folder, for building your own to source see [Building your own from source](#building-your-own-from-source)

## How?

Add the cordova.framework to your Xcode project like you would with any other .framework. Done.

## Compiling your own from source

Included in the Cordova folder is the project to build your own Cordova .framework. You can modify any of the source files in the **Classes** folder, if you add or remove files, be sure to change **Compile Sources** under the Xcode project **Build Phases** tab.

**NOTE: After you have built the Cordova.framework, move all the header files from inside the Classes/ directory up one level previous. Still working on a fix for this.**

## Compiling in plugins

This is actually pretty easy. The following is step-by-step for adding the Splashscreen Plugin to your Cordova.framework

1) Grab the source

- Github ```git clone https://github.com/apache/cordova-plugin-splashscreen```

- Phonegap CLI ```phonegap local plugin add https://git-wip-us.apache.org/repos/asf/cordova-plugin-splashscreen.git``` 

2) Add the .m .h files to the **/classes** folder in the **Cordova.xcodeproj**

3) Build the framework maker project.

4) Add the created Cordova.framework to your project. 

***Note: some Cordova plugins have other .framework dependencies (Splashscreen has none)***

5) Create or add to the ```cordova_plugins.js```. This will sit next to your cordova.js file in your /www folder. Looks like this;

	cordova.define('cordova/plugin_list', function(require, exports, module) {
	module.exports = [
    	{
    	    "file": "plugins/org.apache.cordova.core.splashscreen/www/splashscreen.js",
        	"id": "org.apache.cordova.core.splashscreen.SplashScreen",
       		"clobbers": [
        		"navigator.splashscreen"
        	]	
    	}];
	};

This file must exist at JavaScript runtime, Cordova.js will look for this file.

6) As usual, do not forget yout config.xml

	<feature name="SplashScreen">
	    <param name="ios-package" value="CDVSplashScreen" />
	</feature>	
