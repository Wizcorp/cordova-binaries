# cordova-binaries

## About

Cordova-binaries repository contains plug 'n play [Cordova](http://cordova.apache.org/) binary / library / frameworks for native applications. No third party dependencies necessary. The following code material may also be used to heavily customise Cordova source.

## Foreword

**BORING IMPORTANT NOTES** : This is NOT a replacement for [Cordova CLI tools](https://github.com/apache/cordova-cli/blob/master/README.md), which is the recommended installation and setup method for Cordova based projects. This guide and code material aims to help developers with native projects that are not based on Cordova, rather Cordova is used to manipulate a WebView component in the project for example.

**This is NOT the official release channel for Cordova/Phonegap nor is there any affilication with this repository to Cordova/Phonegap etc. Go [here](http://cordova.apache.org/#download) for that.**

**All code materials are subject to the [Apache license](http://www.apache.org/licenses/LICENSE-2.0).**

## Install Guide

- [iOS](ios/docs/install-guide-ios.md)


## Building your own from source

Included in the repositiory are platform specific **Cordova** folders containing projects for building your own Cordova source to binary.

## Reminder

Most hardcore Cordova features (splashscreen, File API) are now separate plugins (Since round-about Cordova 3.0). You will need to acquire the plugin class files and setup an additional JavaScript file. **You can, and probably should, use the [CLI tools](http://cordova.apache.org/docs/en/3.0.0/guide_cli_index.md.html#The%20Command-line%20Interface) to install plugins.** However, if you wish to still maintain a compiled library + custom plugins this can easy be done - see the platform specific documentation for more info.
