# Native vs Hybrid Applications

## Contents

* **[Purpose of the document](#purpose)**
* **[Mobile Application Development Approaches](#approaches)**
	* [Native Applications](#native)
	* [Hybrid Applications](#hybrid)
	* [Web Applications](#webapps)
	* [Comparison of different approaches](#comparison)
* **[Features](#features)**
	* [Look and Feel](#looknfeel)
	* [Access to device specific APIs](#apis)
	* [Push notifications](#push-notifications)
	* [Performance](#performance)
	* [Security](#security)
	* [Monetization](#monetization)
	* [Testing](#testing)
	* [Maintenance and Updates](#updates)
* **[Choosing the Right Approach](#right-approach)**
  
## <a id=purpose></a> Purpose of the document 

At this moment we have a two different approaches for creating mobile applications: native and hybrid. Each of these approaches has its own drawbacks and benefits. But everytime it's very difficult to choose the right one to go. The purpose of this document is 
  

## <a id=approaches></a> Mobile Application Development Approaches 

### <a id=native></a> Native Applications

Native refers to building an app in a device’s native programming language. For iOS devices this means Objective-C, and for Android it’s Java. Native apps are typically fast, reliable, and can access all the the device’s hardware (camera, accelerometer, compass, etc). Because of this increased performance, mobile games are usually built as native apps. It also means, though, that your app is tied to the platform it is built for. An iOS app, for example, won’t run on an Android device without first re-coding the entire app to Java.


### <a id=hybrid></a> Hybrid Applications

A hybrid app is built using web technologies, and then wrapped in a platform-specific shell that allows it to be installed just like a native app. Thus it is sold/accessed through the device’s app store.

PhoneGap is an example of a framework that allows you take a web app and turn it into a native app for iOS, Android, BlackBerry, Windows 7, WebOS, Symbian and more. The hybrid frameworks typically have APIs as well, that allow you to access the device’s hardware and features that are locked out from the browser.



