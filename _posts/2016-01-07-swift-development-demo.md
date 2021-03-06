---
layout: post
title:  "iOS Swift App Demo"
date: 2016-01-07 09:50:28
categories: coding
author_name : Jesse
author_url : /author/jesse
author_avatar: jesse
show_avatar : true
read_time : 5
feature_image: xcode
show_related_posts: false
square_related: recommend-wolf
description : "iOS Development from a Rubyists' perspective"
---

I recently put a swift demo app together as a way to show interest and at least passing familiarity with Swift / Xcode 7 / iOS Development. (Other than the fact that I wrote a book about it ;) This is simply a random fact display app that shows rather benign little facts about me such as the fact that I enjoy eating spaghetti and like to go hiking.

![Jesse Waites App](http://i.imgur.com/nRNKOA2.png")


Here are a few things that crossed my mind when building this app.

* Really neat to see the MVC implementation on the handset (iPhone) I've used for years.

* There is no method on an array in Swift that will return a random element of the array, such as array.sample in Ruby. That seems kind of ridiculous. Apple has recently open sourced Swift and one hopes an implementation of that will soon be possible.

* Building for iOS in Xcode is a hell of a lot of fun. Much like Rails, it seems everything has its place in an Xcode project, and it is obvious that the better one is with the tooling (in this case, Xcode) the more productive and capable the developer will be.

* Adding an app icon for the homepage was a breeze.

* Adding a launch screen was a total pain and I was not successful. This seems to be due to a change in Xcode 7 and iOS 9. Didn't want to burn more time attempting to resolve the issue so I moved on. I used Photoshop and created my image, placed it in what I thought was the proper location, but it simply didn't work. Whatever.

* Implementing a button that launched the in-app Safari browser was a breeze.

* There is no mail client in the simulator so hardcoding an "email me" button into the app may work in the actual app on a real iPhone but will throw an error in the Xcode Simulator. I had this in my build but removed it (That code is still in the controller) because it was also causing a lot of drama in my UI layout. Specifically, my buttons were overlapping. See next bullet point.

* I found layout and autolayout extremely difficult. I can see that I will need to put much more time into that to master it.

* I'm very much a 'looks matter' type of developer and look forward to experimenting with cocoapods and using some of the preexisting UI libraries to make my stuff look really great.

* If I were building an app for, lets say a restaurant, it would be wise to build the menu from an external JSON endpoint, rather than hardcoding everything like meals and prices into the app. This way one could update the menu externally without having to recode the app and go back through the app store submission and review process. This JSON server would probably be great for something like that. https://github.com/typicode/json-server

* Based on my research, SwiftyJSON seems to be the ideal tool to process the JSON on the client / iOS device side: https://github.com/SwiftyJSON/SwiftyJSON

* Xcode projects don't have readme.md files, so I had to manually create one by creating a folder, moving the Xcode project into it, cd-ing into the folder and using the command touch readme.md to create it.

[Here's the Github link.](https://github.com/piratebroadcast/ios_swift_demo_app)


Next Steps: Build a Rails API app, like a simple little TODO app or something, (Make sure I scope the API routes like V1 or whatever) and then create an iOS front-end for it that reads things from the list and allows to post new TODOs from the App to the database. Would also be fun to experiment with Oauth and iOS, like signing in with Facebook, passing the token back to the Rails app, and authorizing or not authorizing on the iOS device.

Actually scratch that - Next step is to build a simple app that reads JSON from an endpoint somewhere (like government data or something, lots of options there) and displays it on the screen. This will give me another shot to work on effective UI and not get overwhelmed by attempting to do too many new things at once.

Cheers.
