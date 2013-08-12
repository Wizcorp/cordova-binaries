# install-guide-ios

## Where?

Frameworks are already pre-built and included in the **bin** folder, for building your own to source see [Building your own from source](#building-your-own-from-source)

## How?

Add the cordova.framework to your Xcode project like you would with any other .framework. Done.

## Building your own from source

Included in the Cordova folder is the project to build your own Cordova .framework. You can modify any of the source files in the **Classes** folder, if you add or remove files, be sure to change **Compile Sources** under the Xcode project **Build Phases** tab.

**NOTE: After you have built the Cordova.framework, move all the header files from inside the Classes/ directory up one level previous. Still working on a fix for this.**


## Acknowledgements

To create the Cordova binaries we used the template universal framework builder by [Karl Stenerud](https://github.com/kstenerud/iOS-Universal-Framework). 