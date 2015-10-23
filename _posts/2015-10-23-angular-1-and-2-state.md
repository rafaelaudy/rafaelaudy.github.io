
---
layout: post
title: Current state of AngularJS 1 and 2
---

__Angular 1 has been around for almost 6 years. But what it had accomplished and until when is it going to be relevant?
Also why is Angular 2 looking so hot latelly?__

In this post I am going to talk about the status of Angular 1, what to expect from Angular 2 and how to be prepared for it.


# Angular 1

### Some interesting and quick stats:

According to Google, the framework already had 32 release and has an average of 1.1 million devs using its docs everyday.

You may not know it, but sites like Amazon, Paypal, Rayanair, Google Analytics, Plural Sight and others were built with Angular. You can check more of them on the [madewithangular](https://www.madewithangular.com/#/) website.

### Support for Angular 1.x:

Angular 1.x will continue to be updated while relevant.
Here is an updated picture of the ammount of peopple visiting the version 1.x against the 2.x:



Angular 1 will continue to be evolved together with Angular 2 with common features like routing, internacionalization & localization, animation and a lot of performance improvements.

PICTURE desktop

# Angular 2

### Objectives

#### Build for speed

There are loads of improveements to make Angular 2 faster then any other option.
There are optimizations on the load, compilation, rendering and re-rendering phases. Brad Green explained that after minute 6 of the keynote.

PICTURE 2

There is an awesome benchmark to test how much of this it true or just wishfull thinking :) The guys from meteor tested Angular 1, Angular 2, Blaze and React in this post http://info.meteor.com/blog/comparing-performance-of-blaze-react-angular-meteor-and-angular-2-with-meteor

They build a application to find waldos like the image bellow and the result was quite favorable to Angular 2 in all tests.

http://cdn2.hubspot.net/hubfs/520701/Blog/shmck/perfMethod.gif?t=1445451707926

Angular 2 was much faster then the other frameworks, even from the start! On the first picture is the time that it took to render all the waldos for the first time, and the second is the rerun:

PICTURE 1

PICTURE 2

This is the repo https://github.com/ShMcK/Framework-Performance-Tests-with-Meteor try for yourself :)

#### Simpler

Templating:
Bind directly to HTML properties [] and events (). That enabled the Angular team to drop a lot of existing directives and we will not need to create small directives just to change an html property or bind to an event that was not supported by Angular as a directive. This will also support future changes to HTML in general :)

PICTURE

Components:
Now Angular is just a collection of encapsulated components. There is no concept of a controller or a directive, they were merged into a component! Trust me this is much simpler :)

IMAGE

#### Language

You can build Angular 2 apps in ES5, ES6, TypeScript or Dart. I saw a huge preference to TypeScript during the AngularConnect event. Basically all the speakers were using it.

Here is the advantages of each:

ES5 -> You already know it and it is really easy to find devs who know it. It also does not need compilation.
ES6 -> Adds a lots of new features and sintatic sugar to Javascript.
TypeScript -> On tOp of ES6 features it also add types, helps with syntatic checking, refactoring, documentation and makes your tools more powerfull.
This is also the language that the Angular team is using to create Angular 2.

DART -> If you are strange! Kidding, I am just too opiniated about this. I am not sold on why you should adopt DART instead of Javascript :)

IMAGE

#### TOOLS

A while a go it was quite difficult to start writting ES6 code. You had to set up a transpiller, configure source maps and so on.
The Angular 2 team is building a angular-cli project to address thos configuration issues.
It is like a yeoman templating engine but will also take care of code setting up and compiling TypeScript for example.
It is still in beta and can be found here:
https://github.com/angular/angular-cli

IMAGE

Batarang is also back but is called Batarangle now and is going to have a boost in its quality.
Rangle.IO is going to be responsible for this and other Angular.js dev tools for Chrome.
You can start using today and here is a preview:
It is going to support performance analysis, template navigation and debugging.

https://github.com/rangle/batarangle

#### Browser support

IT IS GOING TO SUPPORT IE 9 :D
So you will not have to get stuck with Angular 1.x in the near future.

#### Learning

You can start learning Angular 2 now with a variaty of different sources.
In my humble opinion NG-BOOK 2 is the best starting point. :)

IMAGE

# Migrating to 2

IMAGE

The Angular team is going to release a library called Ng-Upgrade that is going to help you migrate your app little by little.
You will not need to make a big bang conversion and both versions of Angular will be able to coexist.

IMAGE

The Angular team is going to release a blog post explaining how it is going to be done.
For now you can have a look on this repository:

https://github.com/angular/angular/tree/master/modules/playground/src/upgrade

# Release status

From what I understood from the AngularConnect conference Angular 2 is almost being released.
I would bet to the Q1 next year.
Google already migrated to Angular 2 some of their own apps, including Google Adwords, which is theit biggest money makers.
This projects involves hundreds of developers and million lines of codes.


# That is it!
If you want to know more have a look on this amazing keynote from the AngularConnect conference.

[![AngularConnect keynote](http://img.youtube.com/vi/UxjgUjVpe24/0.jpg)](https://www.youtube.com/watch?v=UxjgUjVpe24)

I will be writting more about Angular 2 shortly, see you later!

Cheers :)