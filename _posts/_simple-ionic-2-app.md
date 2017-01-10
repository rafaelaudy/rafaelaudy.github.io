---
layout: post
title: Creating your first Ionic 2 app
excerpt: Create your first Ionic 2 with Angular 2 and ES6 app. We are going to install everything, write the app and test it.
image: ''
imageAlt: Ionic 2 and Angular 2
keywords: Ionic 2, Angular 2, iOS, ES6, ECMAScript 6, Sample, Introduction, Rafael Audy, Rafael Glanzner, Rafael Audy Glanzner
---
This post will help you get your first [Ionic 2](http://ionicframework.com/docs/v2/) + [Angular 2](https://angular.io/) + [ES6](http://es6-features.org/#Constants) "hello world on asteroids" app ready to be deployed.
Please have a look on this [post](http://rafaelaudy.github.io/ionic-1-and-2-state/) first if you are wondering why you should learn Ionic 2 to begin with.

I used [this tutorial](http://ionicframework.com/docs/v2/getting-started/tutorial/), built by the Ionic 2 team to create the skelleton of this little app.
Then I had a look on their [conference app](https://github.com/driftyco/ionic-conference-app) to extend the app with shinny components.
[Here](https://github.com/rafaelaudy/ionic-2-donation) is the repository for the app that we are going to investigate.

When I wrote this post Ionic 2 and Angular 2 were both on the alpha stage.

# What are we building with Ionic 2?

We are going to create a simple app that will show you a list of sport gear and enable the user to select one of them for donation.
Here is a photo of our end goal:

![Ionic 2 and Angular 2](------------)

# Installing, starting and running an Ionic 2 app:

## Installing Ionic 2:

For now we just need to install Ionic 2 SDK!
In the next post I am going to show you how to run in your iOS device, then we will need to configure some more stuff.

`npm install -g ionic@alpha`

Great, now you can use the Ionic command to improve your productivity!
Type 'ionic' on the command line to have a look on all the things it can do.

![]()

## Bootstrapping an Ionic 2 app:

Run this command to start our new app:

`ionic start donateGear --v2`

Cool, now we have a sample app.

# Running the Ionic 2 app:

Now run this command to run it on your browser:

`cd donateGear`

`ionic serve`

In the next post I'll show how to run on a emulator or in your iOS device.

