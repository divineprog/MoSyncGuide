MoSyncGuide
===========

An easy to use Guide to mobile ppp development with [MoSync](http://mosync.com/).

Work-in-progress ;)

# An Easy Guide to Mobile App Development with MoSync

By Mikael Kindborg, mikael.kindborg@mosync.com

**This is a first draft, feedback is welcome!**

If you want get started with mobile app development for Android, iOS, or Windows Phone, [MoSync](http://www.mosync.com/) is the tool of choice for you. With MoSync you can quickly create mobile apps using JavaScript and HTML/CSS.

This guide takes you through the steps involved in developing a mobile application, from getting started to publishing your finished app.

What you need:

* Laptop/desktop computer with Windows or Mac OS X
* A mobile device or emulator: Android, iPhone/iPad/iPod touch, or Windows Phone
* Basic HTML/JavaScript knowledge
* 5-20 hours to get started
* Bowl with favourite snacks (optional)

## Step One: Download MoSync

Start out by [downloading the MoSync Software Development Kit](http://www.mosync.com/download) (SDK). This is an Eclipse-based programming environment that you install on your computer.

**Potential confusion:** There are two downloads, the MoSync SDK and MoSync Reload. In this guide we will use the MoSync SDK. (Reload is also way cool, but you will need the SDK to be able to build and publish your app.)

## Step Two: Install MoSync

You need to have [Java](http://www.java.com/) installed to run the MoSync SDK.

For Mac, the built-it Java version should work. If not, upgrade it.

**Potential hassle on Windows:** If the installer complains about Java, make sure you have Java installed. For Windows, the 32-bit version is the safest bet.

## Step Three: Build your first app

Next, launch MoSync Eclipse and create an app from one of the templates that are provided and run it on your device.

The guide [Getting Started with HTML5 and JavaScript](http://www.mosync.com/documentation/manualpages/getting-started-html5-and-javascript) is your safest bet for completing this step.

If you get stuck, go to the [MoSync HTML5/JavaScript forum](http://www.mosync.com/forum/592) and ask for help:

The resulting app has one user interface component, called a **WebView**. This is like a web browser. You can use any HTML/CSS/JavaScript in that WebView. (Almost. Mobile browsers have some limitations compared to desktop browsers.) There are also several JavaScript libraries available for mobile app development (like the MoSync Wormhole library). More on this later.

**Potential hassle:** As of writing this guide, not all of the MoSync APIs are supported on Windows Phone. Consult the MoSync documentation to make sure that the APIs you wish use are expected to work on your target platforms.

## Step Four: Explore how a MoSync project is structured

Take some time in Eclipse and explore how a MoSync project is structured. It is useful to understand the file and directory layout, as you at times may need to add/edit files manually.  

To know where on the disk your project is located, right-click the project name in the Project Explorer, and select Properties. Under the Resource section in the Properties dialog box you can see the path to the directory where the project is saved.

Open a file browser window (outside of Eclipse) and navigate to the location of your project. Then go to folder LocalFiles. This is where your HTML/CSS/JavaScript files are located. You can open index.html in a web browser, which is handy when you wish to tweak the HTML/CSS and quickly view the result. You can also edit these files using your favourite text editor, if you prefer that over using the editor in Eclipse.

To learn more about how a MoSync HTML/JavaScript project is structured, read the article [Developing Apps in HTML5 and JavaScript](http://www.mosync.com/documentation/manualpages/how-create-html5-project-mosync).

**Potential confusion:** If you update/add/remove files outside of Eclipse, refresh your project view in Eclipse by pressing F5, otherwise Eclipse will be out of sync with the file system and build errors may occur.

Rebuilding the project in Eclipse and deploy to a device takes some time, which is why the trick of using a web browser to preview your project can be useful, cutting time for each edit/test run from minutes to seconds. The drawback is that you do not get the same look and feel as on a device, and you won't get any MoSync functionality, such as access to device services. This is when you will want to use [MoSync Reload](http://www.mosync.com/content/using-mosync-reload), which allows you to quickly develop your project using a device. But you still need the MoSync SDK (Eclipse) to build the actual app to be able to deploy it to an app store.

## Step Five: Master JavaScript and HTML/CSS

A great way to learn is to experiment. If you are new to JavaScript and HTML/CSS, you can start out by modifying the app you created from the project template, changing the text of the buttons, change colors, add a button, make it do something, and so on. If you are more advanced you can start by making a new user interface design, add functionality to the app, start exploring the Wormhole library, and so on.

JavaScript, HTML and CSS are widely used, and there are lots of tutorials and examples available on the Internet. A good way to learn is to copy example code, paste it into your project, and play around with it. If you have an existing web site, you can use that code and adapt it to a mobile screen format to quickly get a starting point for a mobile app.

### JavaScript

The Mozilla [JavaScript documentation](https://developer.mozilla.org/en/JavaScript) is a useful reference.

[JavaScript Garden](http://bonsaiden.github.com/JavaScript-Garden/) is a guide to best practices of JavaScript programming, which includes valuable information about preferred programming styles, what to avoid in the language, and potential pitfalls.

### Mobile Web UI design and programming

HTML5Rocks is a community driven site where you can learn about [HTML5 and mobile development](http://www.html5rocks.com/en/mobile). Making a Web UI that [scales to different screen sizes](http://www.html5rocks.com/en/mobile/cross-device/) is very useful when doing cross-platform mobile app development for phones and tablets.

The articles [A tale of two viewports - part one](http://www.quirksmode.org/mobile/viewports.html) and [A tale of two viewports - part two](http://www.quirksmode.org/mobile/viewports2.html), explain how the coordinate system used by mobile web browsers works. This is useful to know when doing mobile Web UI design.

You can learn about how to make mobile Web UIs from the following books by Jonathan Stark, [Building Android Apps with HTML, CSS, and JavaScript, 2nd Edition](http://ofps.oreilly.com/titles/9781449316419/), and [Building iPhone Apps with HTML, CSS, and JavaScript](http://ofps.oreilly.com/titles/9780596805784/).

### Mobile Web UI frameworks

There are several JavaScript frameworks that make it easier to create good looking Web UIs for mobile devices. All libraries designed for mobile browsers should work with MoSync apps.

Here is a series of blog posts that compare Mobile Web UI frameworks, [Part One](http://www.codefessions.com/2012/04/mobile-javascript-frameworks-evaluation.html), [Part Two](http://www.codefessions.com/2012/04/which-mobile-javascript-framework-is.html), [Part Three](http://www.codefessions.com/2012/05/which-mobile-javascript-framework-is.html).

One framework missing from the above comparison is [Zepto.js](http://zeptojs.com/), which is a trimmed-down version of jQuery with enhanced functionality for mobile devices.

### Canvas and touch events

The HTML5 canvas element gives mobile Web UIs a flexible way of rendering graphics. Mozilla has a [Canvas tutorial](https://developer.mozilla.org/en/Canvas_tutorial/), and a tutorial covering [https://developer.mozilla.org/en/DOM/Touch_events](touch events).

HTML5Rocks has another [touch event](http://www.html5rocks.com/en/mobile/touch/) tutorial.

### Accessing device functionality

The MoSync [Wormhole](http://www.mosync.com/files/imports/doxygen/latest/html5/index.html) JavaScript library provides access to device functionality like camera, sensors, file system, storage, networking, and so on. The Wormhole library is compatible with the popular [PhoneGap](http://docs.phonegap.com/) library and W3C standards.

MoSync comes with several Wormhole tutorials and example programs, here is a selection:

* [Reading Sensors from JavaScript](http://www.mosync.com/documentation/manualpages/reading-sensors-javascript) shows how to use the Sensor API and render graphics on a canvas.

* [WormholeDemo](http://www.mosync.com/documentation/manualpages/wormholedemo) is an example app that shows several parts of the API.

* [WormholeNativeUI](http://www.mosync.com/documentation/manualpages/wormholenativeui) is an example program that shows how to use Native UI components from JavaScript.

* [Screencast](www.mosync.com/screencasts/using-nativeui-javascript) that shows how to use NativeUI components from JavaScript.

* [PhotoGallery](http://www.mosync.com/documentation/manualpages/building-photo-gallery) is an example app that shows how to use the Capture API and FileTansfer API, along with several other useful programming techniques (including extending JavaScript with C++).

## Step Six: Become creative

There are lots of ways to come up with great ideas and designs. My personal view is that there are two ways to approach the design process:

* First approach is to design all of the app as the initial step, do detailed graphical design and work out exactly how the app should work, then implement it (this is bound to fail).

* Second approach is to take some existing example app, then start experimenting and playing around with it, working out and refining your idea and design as you go along and code it (much more likely to succeed).

In the second approach you work with the medium, in the first you risk ending up working against it, spending endless hours trying to implement the exact design you have made up, constantly bumping into stumbling blocks on the way. When working with the material, you explore its possibilities, and discover new design ideas as you go along. Interaction designers talk about "exploring the design space", which means trying out different variations and combinations of an idea or design.

My advice is that you for your first mobile app project choose the first approach. Pick an idea or some twist of an existing idea, and move along in small steps, experimenting on the way. You should be able to move along much quicker by experimenting with an existing template or example app, compared to making a completely new design from scratch.

The approach of designing by coding can be especially productive if you are new to app development and not yet up to speed with the programming technologies available. For bigger projects, however, doing an overall design before coding is advised, but I would still recommend experimenting as you go along also in this case.

## Step Seven: Create an icon for your app

Every app should have its own cool icon. The guide **Developing Apps in HTML5 and JavaScript** has a section about [how to add an icon to your MoSync app](http://www.mosync.com/documentation/manualpages/how-create-html5-project-mosync#adding-an-application-icon).

## Step Eight: Publish your app

To publish your app can be easy or hard, depending on the platform. Android is flexible and has several options available. iPhone/iPad and Windows Phone have official app stores and reviewing procedures that need to be confirmed to.

### Android

On Android, you have several choices for publishing apps.

[Google Play](http://www.android.com/developers/) is the main app store for Android (previously called "Android Market"). When you publish your app on Google Play you can charge for it (up to 200 USD), or make it available for free.

There are alternative app stores for Android, where you can publish your app, for example [AndroidGuys](http://store.androidguys.com/) (which is a [MobiHand](http://corporate.mobihand.com/developers.asp) store). You can also find articles on the Internet that list [alternative app stores](http://danatheteacher.hubpages.com/hub/Top-Android-Market-Alternative-App-Stores).

Another category of app stores is local stores. In Sweden, for instance, there is an Android app store called [AppLand](http://www.appland.se/) (the name is a play with the word "Lappland", which is the name of the biggest province in Sweden).

If you wish to publish your app on your own website, this is really easy to do. If you have a free app, or an in-house corporate app, this can be a good option. However, if you want to sell your app, an app store is a much better option.

To publish an Android app on your website,  just build your project in Eclipse, and upload the resulting .apk file to the site (you can find the path of the .apk file in the Eclipse console output window, at the end of the build output). User can then install your app by entering the URL of the .apk file in the web browser of the device.

For users that have a Barcode Scanner app, a QR-code that points to the URL of the .apk file is a handy way to install your app.  You can create a QR-code at for example [kaywa.com](http://qrcode.kaywa.com/). Just copy and publish the generated image on your site (or anywhere on the Internet, or on paper or a T-shirt).

For users that have no QR-code reader, they can open the web browser on the device and type in the URL to the .apk file, or visit a web page and click a link or button pointing to the file.

If you use [GitHub](http://www.github.com/), it is easy to publish the .apk as a downloadable file, and a QR-code will be created automatically for you.

### iOS (iPhone, iPad, iPod touch)

Apple has documentation that describes how to publish apps for the iOS family of devices on the [Apple App Store](http://developer.apple.com/library/ios/#DOCUMENTATION/General/Conceptual/ApplicationDevelopmentOverview/DeliverYourAppontheAppStore/DeliverYourAppontheAppStore.html).

### Windows Phone

Microsoft has information about how to publish apps on [Windows Phone Marketplace](http://msdn.microsoft.com/en-us/library/hh202939%28v=vs.92%29), the official app store for Windows Phone.

## Step Nine: Market and improve your app

Once your app is published, people start using it and users may share their experience with it, with you and with each other. If your app will become a success or failure is not written in stone, determined by destiny. You are the prime force for making your app successful, by listening to users and constantly improving your app. You also have the responsibility to market your app, to make it known in relevant user communities.

The mobile app market shares several characteristics with the shareware market. Author Steve Pavlina has written about what it takes to make [successful shareware](http://www.sodaware.net/dev/articles/shareware-amateurs-vs-shareware-professionals.htm), and much of this is applicable also to mobile apps.  
