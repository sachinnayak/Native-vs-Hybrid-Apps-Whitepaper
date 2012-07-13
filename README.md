<style>
table { margin-bottom: .6em }
th { text-align: left }
th, td { padding: .6em }
</style>

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
	* [Performance](#performance) - Ilya
	* [Security](#security) - Ilya
	* [Push notifications](#push-notifications) - Ilya
	* [Monetization](#monetization)  - Ilya
	* [Testing](#testing)  - Ilya
	* [Maintenance and Updates](#updates) - Ilya
* **[Choosing the Right Approach](#right-approach)** - Ilya
* **[Helpful Sources](#sources)**
  
## <a id=purpose></a> Purpose of the document 

 There are two different approaches for creating mobile applications: native and hybrid. Each of them has its own limitations and benefits. Many factors influence the choice of the best approach: budget, functionality, project timeframe, target audience, number of platforms to support. 

 The purpose of this document is to provide an overview of all existing approaches, determine their pros and cons, give answers to the common questions and define when to use each of the approaches.
  

## <a id=approaches></a> Mobile Application Development Approaches 

### <a id=native></a> Native Applications

 Native applications are written in a device’s native programming language and are built into binary executable files that are installed and run on the device. The most popular way to download a native app is by visiting an application store such as Apple’s App Store, Android’s Marketplace, or BlackBerry’s App World, but other methods exist and are sometimes provided by the mobile vendor.

 Native apps are typically fast, reliable, and can access all the the device’s hardware (camera, accelerometer, compass, etc). Because of this increased performance, mobile games are usually built as native apps. It also means, though, that your app is tied to the platform it is built for. An iOS app, for example, won’t run on an Android device without first re-coding the entire app to Java.


### <a id=hybrid></a> Hybrid Applications

 Modern mobile devices provide web browsers that are advanced enough to be an engine for applications. Advancements in development of HTML, CSS and Javascript allow to create UI components, access to rich media types, geo-location services and offline availability. Rich websites that looks and behaves like an application and uses these advanced features are often referred to as web applications. A browser bookmark to such a service can be placed on a device homescreen and user will be able to launch it like any other application.

A hybrid app is a mix of a native and a web application. Basically it's a webapp wrapped in a platform-specific shell that allows it to be installed just like a native app and access device hardware capabilities. For cross platform reach, developers would need to code the native part separately for each platform but they can use the same HTML5 part across all of them.

PhoneGap is an example of a framework that allows you turn a web app into a native app for iOS, Android, BlackBerry, Windows 7, WebOS, Symbian and more. The hybrid frameworks typically have APIs as well, that allow you to access the device’s hardware and features that are locked out from the browser.
It is sold/accessed through the device’s app store. 

###<a id=comparison></a>Comparison of different approaches
 
 Native excels in performance and device access, but suffers in cost and updates. Web is much simpler, less expensive and easier to update, but is currently limited in functionality and cannot achieve the exceptional level of user experience that can be obtained using native API calls. The hybrid approach provides a middle ground which, in many situations, is the best of both worlds, especially if the developer is targeting multiple operating systems.

<table>
 <tr>
   <th> Features
   <th> Native
   <th> Hybrid
 <tr>
 <tr>
 	<th> Development language
 	<td> Native only
 	<td> Native and web / Web only
 </tr>
 <tr>
 	<th> Code portability
 	<td> None
 	<td> High
 </tr>
 <tr>
 	<th> Device specific features
 	<td> High
 	<td> Moderate
 </tr>
 <tr>
 	<th> Access to native APIs
 	<td> High
 	<td> Moderate
 </tr>
 <tr>
 	<th> Advanced graphics
 	<td> High
 	<td> Moderate
 </tr>
 <tr>
 	<th> UI/UX
 	<td> High
 	<td> Moderate
 </tr>
 <tr>
 	<th> Upgrade flexibility
 	<td> Low <br><small>(always through appstore)</small>
 	<td> Moderate <br><small>(generally through appstore)</small>
 </tr> 
 </tbody>
</table>


## <a id=features></a> Features

### Look and Feel

 One of the defining features of any platform is its look and feel. Users come to expect controls to be presented consistently and manipiulated in the same way. There are certain idioms which vary from platform to platform, e.g. what happens when the user performs a "long hold" (keep touching an element for several seconds)? Plaforms have standard idioms for such things, and you can't satisfy them all with a single HTML5 app.

 Furthermore, platform look-and-feel is determined by the platform's native software library, whose widgets encapsulate the kind of look and feel users expect. You get a lot of the expected look-and-feel "for free" just by using the native toolkit.

 In a hybrid app you'll most likely have to create UI elements that look the same across platforms. This is not necessarily a bad thing, but that means that adhering to Human Interface Guidelines (HIG) of each necessary platform will be not possible or rather hard.

 When developing a hybrid app you are restricted to CSS and Javascript features native browsers support. Many interface elements with native-like behavior can be created using Javascript, but they'll never look as rich and fast as native.



## <a id=apis></a> Access to device specific APIs

 Native is called so for a reason. Native apps have direct access to all hardware and system-level features. They can easily get hold of swipe events, mutlitouch even, for those platforms which support it. They can typically act on hard keys being pressed, like Android's search button and volume controls. They can access hardware too, like GPS and camera.

 An operating system like Android provides different ways for apps to interact with users, and indeed, with other apps. You have active widgets on the homepage. You have notifications, which show up in the device's status bar. And you have intents, which allow your app to announce itself as providing a general service which other apps might require on occasion.

 It's true that many in-app features are simply beyond reach for an HTML5 app. Inside a webpage, which a web application basically is, a developer is restricted to the APIs the web browser provides.  Web standards are evolving rapidly, and modern mobile browsers are keeping pace. Offline storage, geolocation, canvas graphics, and video/audio playback all enjoy widespread support among modern smarpthones, for example. Browser access to camera, battery status, phone contact list, SMS and other facilities are currently being developed and implemented, but it will take some time before we can rely on these features.

 For the time being we need the native wrapper libraries like Phonegap (a.k.a. Cordova) to provide access to device APIs for hybrid applications. They fill the gap by exposing native features as web services, which the web view calls using a standard networking API. When you build a hybrid app like this, you're also able to hook into those platform features like widgets, notifications, and intents. 


## <a id=performance></a> Performance

It's evident that native applications have the benefit of accessing device hadrware directly, GPU acceleration, multithreading other performance boosters, and thus will always be faster than hybrid apps which are confined to web browser wrapper environment.  Native applications have snappier animations, transitions and faster load time, but actually it's more noticeable on slow cheap devices (for example iPhone 3G or old Androids). So if you are developing an application where performance is critical like bleeding-edge 3D games, your only option is to go native.

The performance of hybrid apps is not great, but often it's not that important for the kind of tasks they do, because majority of mobile apps are fundamentally information-based: news, mail, timetables, social networks, etc. 

Web browsers in general and mobile browsers in particular start to gain advanced performance features like multithreading, GPU acceleration, which were recently available only to native apps. Not to say that browser Javascript engines get virtually times faster by the year. 


## <a id=push-notifications></a> Push notifications
Push notifications are the messages pushed to a central location server and delivered to the end user. “Notifications are "pushed" by the event producer component (the event "source"), they are not "pulled" by the event consumer component. The producer decides when to send the notification, because it knows about the event before the consumer does.” (Gartner: Hype Cycle for Application Architecture, 2011).

Push notifications are available from Apple iOS 3, Google Android 2.2, RIM BlackBerry 5.5 and Microsoft Windows Phone 7. From the 1000 foot view the principle how push notifications work is the following:

* As user runs an app on his device it communicates with push notifications service server to register the device for receiving notifications 
* When there is a need to notify user about something application server (backend system/service written in Java, PHP, Ruby, anything else) sends the data (message) to push notifications service server
* Push notifications service takes care about delivering message to the end user (there's a need to say that all notification services don't guarantee that messages will be delivered).

<table>
 <tr>
   <th> OS
   <th> Version
   <th> Push Notifications Service
   <th> Amount of data per push
 <tr>
 <tr>
 	<th> Apple iOS </th>
 	<td> 3+ </td>
 	<td> APN </td>
 	<td> 256 bytes </td>
 </tr>
 <tr>
 	<th> Google Android </th>
 	<td> 2.2+ </td>
 	<td> C2DM </td>
 	<td> 1024 bytes </td>
 </tr>
 <tr>
 	<th> RIM BlackBerry </th>
 	<td> 5.5+  </td>
 	<td> BB Push </td>
 	<td> 8192 bytes </td>
 </tr>
 <tr>
 	<th> Microsoft Windows Phone </th>
 	<td> 7+ </td>
 	<td> MPNS </td>
 	<td> 3072 bytes + 1024 bytes for header</td>
 </tr>
 </tbody>
</table>
The main problem with cross-platform push notifications is that it's very difficult to integrate all the multiple notification API's for multiple platforms on the both server side and client side (hybrid mobile application). When we are talking about native mobile applications for only one platform it's pretty easy, because the only one API will be used on the server side and there is already the infrastructure for "user tapping on the notification" event capturing in the native SDK's and frameworks.

Do not be upset, there are already complete solutions for cross-platform push notifications for hybrid applications (but are not free). For example, [Urban Airship Push Notifications](http://urbanairship.com/products/in-app-purchase/) will cost $200-$2000 per month depending on the count of application users.

## <a id=monetization></a> Monetization

Platform and device vendors run app markets to let developers make their apps discoverable and monetizable. Mobile platforms offer several ways for developers to get money from their apps. Since hybrid applications are distributed the same way as native they share monetization techniques.

The simplest way to monetize is to charge for your app to use it forever. Showing ads is also popular, but to mak good money the app needs a lot of downloads. For a magazine and similar types of services that provide content of some kind subscriptions is a viable option. Another popular monetization strategy is in-app purchases. A user could buy a "premium" version of an app, or unlock particular functionality, or buy some kind of tokens or unlock levels (think games).

There's a problem with in-app purchases that it's not easy to integrate them in multiple platforms simultaneously. When building a native app the standard codes necessary for integration with app stores is provided by platform development kits, while for hybrid apps those are not directly usable and external solutions are necessary. Luckily they are available, but are not free, e.g. [Urban Airship In-App Purchase](http://urbanairship.com/products/in-app-purchase/) will charge you from $200 to $2000 per month depending on your userbase.

## <a id=testing></a> Testing
TBD	

## <a id=updates></a> Maintenance and Updates
Two ways: tpl on server and tpl on device (~native updates). But be careful of using native UI elements in hybrid apps (in cause of server tpls and updates).  

## <a id=right-approach></a> Choosing the Right Approach
There is no winner or loser in this battle. Every approach is suitable for different cases alike every approach solves different problems.

Native approach is suitable for the situations when:
* A single mobile OS is a target
* Some native functionality is required
* Requirements contain rich extraordinary UI
* There are existing in-house skills for creating native apps for all platforms

Hybrid approach is good for you when:
* Multiple mobile OSes is a target and budget is not so huge
* There are existing in-house web skills
* You are thinking about the future (web technologies evoluting faster) 

![image](http://st.webnotbombs.com/Vdyd+)

[Mobile Application Development Choices](http://st.webnotbombs.com/Vdyd+)

But it must be highlighted, that together with hybrid application for a lot of platforms we get a web application that runs directly from browser. It's a very nice addition for companies that are choosing  hybrid applications as their mobile application strategy, because of difference in the level of app usage frequency, user habits, etc.



## <a id=sources></a> Helpful Sources
* [Worklight: HTML5, Hybrid or Native Mobile App Development](http://www.worklight.com/assets/files/HTML5,%20Hybrid%20or%20Native%20Mobile%20App%20Development.pdf)
* [Hybrid vs. Native vs. Mobile web comparison chart](http://www.mrc-productivity.com/blog/2012/03/hybrid-vs-native-vs-mobile-web-comparison-chart/)
* [Native, Native, Web and Hybrid Apps – Understanding the Difference](http://www.xcubelabs.com/blog/native-web-and-hybrid-apps-understanding-the-difference/)
* [Native, Hybrid or Web Apps?](http://buildmobile.com/native-hybrid-or-web-apps/)
* [Hybrid HTML5 Apps Are Less Costly to Develop Than Native](http://www.readwriteweb.com/mobile/2012/01/hybrid-html5-apps-are-more-les.php)
* [HTML5 vs. Native: The Mobile App Debate](http://www.html5rocks.com/en/mobile/nativedebate/)






 






