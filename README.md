# Native vs Hybrid Applications

## Contents

* **[Purpose of the document](#purpose)**
* **[Mobile Application Development Approaches](#approaches)**
	* [Native Applications](#native)
	* [Hybrid Applications](#hybrid)
	* [Comparison of different approaches](#comparison) - Pasha
* **[Features](#features)**
	* [Look and Feel](#looknfeel) - Pasha
	* [Access to device specific APIs](#apis) - Pasha
	* [Push notifications](#push-notifications) - Ilya
	* [Performance](#performance) - Ilya
	* [Security](#security) - Pasha
	* [Monetization](#monetization)  - Ilya
	* [Testing](#testing)  - Ilya
	* [Maintenance and Updates](#updates) - Ilya
* **[Choosing the Right Approach](#right-approach)**
* **[Helpful Resources](#sources)** - Ilya
  
## <a id=purpose></a> Purpose of the document 

There are two different approaches for creating mobile applications: native and hybrid. Each of them has its own limitations and benefits. Many factors influence the choice of the best approach: budget, functionality, project timeframe, target audience, number of platforms to support. 

The purpose of this document is to provide an overview of all existing approaches, determine their pros and cons, give answers to the common questions and define when to use each of the approaches.
  

## <a id=approaches></a> Mobile Application Development Approaches 

### <a id=native></a> Native Applications

Native applications are written in a device’s native programming language and are built into binary executable files that are installed and run on the device. The most popular way to download a native app is by visiting an application store such as Apple’s App Store, Android’s Marketplace, or BlackBerry’s App World, but other methods exist and are sometimes provided by the mobile vendor.

Native apps are typically fast, reliable, and can access all the the device’s hardware (camera, accelerometer, compass, etc). Because of this increased performance, mobile games are usually built as native apps. It also means, though, that your app is tied to the platform it is built for. An iOS app, for example, won’t run on an Android device without first re-coding the entire app to Java.


### <a id=hybrid></a> Hybrid Applications

Modern mobile devices provide web browsers that are advanced enough to be an engine for applications. Advancements in development of HTML, CSS and Javascript allow to create UI components, access to rich media types, geo-location services and offline availability. Rich websites that looks and behaves like an application and uses these advanced features are often referred to as web applications. A browser bookmark to such a service can be placed on a device homescreen and user will be able to launch it like any other application.

A hybrid app is a mix of a native and a web application. Basically it's a webapp wrapped in a platform-specific shell that allows it to be installed just like a native app and access device hardware capabilities. 

For cross platform reach, developers would need to code the native part separately for each platform but they can use the same HTML5 part across all of them.

PhoneGap is an example of a framework that allows you turn a web app into a native app for iOS, Android, BlackBerry, Windows 7, WebOS, Symbian and more. The hybrid frameworks typically have APIs as well, that allow you to access the device’s hardware and features that are locked out from the browser.
It is sold/accessed through the device’s app store. 

###<a id=comparison></a>Comparison of different approaches
 
Native excels in performance and device access, but suffers in cost and updates. Web is much simpler, less expensive and easier to update, but is currently limited in functionality and cannot achieve the exceptional level of user experience that can be obtained using native API calls. The hybrid approach provides a middle ground which, in many situations, is the best of both worlds, especially if the developer is targeting multiple operating systems.



