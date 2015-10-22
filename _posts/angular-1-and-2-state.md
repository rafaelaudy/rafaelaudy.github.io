
---
layout: post
title: Current state of AngularJS 1 and 2
---

So after almost 6 years of Angular where is the framework now and where is it heading?

# Angular 1

### Angular 1.x stats:

- 32 release
- Around 1.1 million devs using the docs everiday
- We have some gigantic apps built using it!
Like Amazon, Paypal, Rayanair, Google Analytics, Plural Sight and so on.
Check more here:
https://www.madewithangular.com/#/

### Support for Angular 1.x
Angular 1.x will continue to be updated while relevant.
Here is an updated picture of the ammount of peopple visiting the version 1.x against the 2.x:

### Evolution
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
TypeScript -> On tip of ES6 features it also add strong typing, helps with syntatic checking and makes your tools more powerfull.

DART -> If you are strange! Kidding, really don't see why people would shy awat from Javascript :)



https://www.youtube.com/watch?v=UxjgUjVpe24
