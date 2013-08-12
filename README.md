# cordova-binaries

## About

Cordova-binaries repository contains plug 'n play [Cordova](http://cordova.apache.org/) binary / library / frameworks for native applications. No third party dependencies necessary.

## Install Guide

- [iOS](ios/docs/install-guide-ios.md)


## Building your own from source

Included in the repositiory are platform specific **Cordova** folders containing projects for building your own Cordova source to binary.

## Reminder

Most hardcore Cordova features (splashscreen, File API) are now separate plugins. You will need to acquire the plugin class files and setup a ```cordova_plugins.js``` file. **You can, and probably should, use the [CLI tools](http://cordova.apache.org/docs/en/3.0.0/guide_cli_index.md.html#The%20Command-line%20Interface) to install plugins.**

However, if you wish to still maintain a compiled library + plugins this can easy be done - see the platform specific documentation for more info.