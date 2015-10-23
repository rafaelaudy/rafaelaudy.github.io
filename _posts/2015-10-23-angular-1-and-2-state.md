---
layout: post
title: Current state of AngularJS 1 and 2
---

__Angular 1 has been around for almost 6 years. But what it had accomplished and until when is it going to be relevant?
Also why is Angular 2 looking so hot lately?__

In this post I am going to talk about the status of Angular 1, what to expect from Angular 2 and how to be prepared for it.


# Angular 1

## Some interesting and quick stats:

According to Google, the framework already had 32 releases and has an average of 1.1 million devs using its docs everyday.

You may not know it, but sites like Amazon, PayPal, Ryanair, Google Analytics, Plural Sight and others were built with Angular. You can check more of them on the [madewithangular](https://www.madewithangular.com/#/) website.

## Support for Angular 1.x:

Angular 1.x will continue to be updated while relevant. Goggle is going to release constant updates on the usage of their docs for both Angular 1 and 2. Below you have an update from Oct/2015. This means that Angular 1 will probably going to be supported for a couple of years ahead.

![Developers visiting Angular docs](https://github.com/rafaelaudy/rafaelaudy.github.io/blob/master/images/posts/angular/angular-1-and-2-state/developers-visiting-angular-docs.png?raw=true)

Some of the features from Angular 2 will also be merged to Angular 1. There are already plans to integrate new modules for routing, internationalization & localization, animation and a lot of other performance improvements.

# Angular 2

## Objectives

#### Build for speed

There are loads of improvements aiming to make Angular 2 faster then any other current option.
There are optimizations on the load, compilation, rendering and re-rendering phases. You can learn more about these improvements watching the video at the end of the post after the minute 6.

![Improvements to Angular 2 speed](https://raw.githubusercontent.com/rafaelaudy/rafaelaudy.github.io/master/images/posts/angular/angular-1-and-2-state/angular-2-performance-improve.png)

There is an awesome benchmark that proves that this is not just wishful thinking :) The guys from meteor compared the performance from Angular 1, Angular 2, Blaze and React. They built an application to find Waldos (animation bellow) and the result was quite favorable to Angular 2 in all the tests.

![Angular find Waldos Angular](http://cdn2.hubspot.net/hubfs/520701/Blog/shmck/perfMethod.gif?t=1445451707926)

Below you can see the time that it took to render all the Waldos for the first time, and the second is the rerun:

![Load Waldos Angular 2](https://raw.githubusercontent.com/rafaelaudy/rafaelaudy.github.io/master/images/posts/angular/angular-1-and-2-state/angular-2-performance-comparison.png)

![Re-render waldos Angular 2](https://raw.githubusercontent.com/rafaelaudy/rafaelaudy.github.io/master/images/posts/angular/angular-1-and-2-state/angular-2-performance-comparison2.png)

You can use [this repo](https://github.com/ShMcK/Framework-Performance-Tests-with-Meteor try for yourself) to run the tests yourself, change the parameter or do whatever you like! [This blog post](http://info.meteor.com/blog/comparing-performance-of-blaze-react-angular-meteor-and-angular-2-with-meteor) analyzed the data showed here in much more detail.

#### Simpler

It should be easier to build templates with Angular now. In Angular 2 we don't need directives to access HTML properties or events, we just use [] and () respectively.

![Angular 2 binding example](https://raw.githubusercontent.com/rafaelaudy/rafaelaudy.github.io/master/images/posts/angular/angular-1-and-2-state/Angular-2-style.png)

That enabled the Angular team to drop a lot of existing directives and we will not need to create small directives just to change an html property or bind to an event that was not supported by Angular as a directive. This will also support future changes to HTML in general :)

Another big change is that now Angular 2 is just a tree of components. There is no concept of a controller or a directive, they were merged into a component! Trust me this is much simpler :)

![Angular components](https://raw.githubusercontent.com/rafaelaudy/rafaelaudy.github.io/master/images/posts/angular/angular-1-and-2-state/angular-2-components.png)


#### Languages and tools to get productivity

You can build Angular 2 apps in ES5, ES6, TypeScript or Dart (even more languages theoretically). TypeScript got a lot of traction during the AngularConnect event, the majority of the speakers were using and loving it.

Here is something to help you choose the best language:

* ES5 -> You already know it and it is really easy to find devs who also know it. It does not need compilation step in your pipeline.
* ES6 -> Adds a lots of new features and syntactic sugar to JavaScript. Needs compilation.
* TypeScript -> On top of ES6 features it also add types, helps with syntactic checking, refactoring, documentation and makes your tools more powerful.
This is also the language that the Angular team is using to create Angular 2 and that I will start using :D.

* DART -> If you are strange! Kidding, I am just not sold on why you should adopt DART instead of JavaScript :)

![Angular 2 possible languages](https://raw.githubusercontent.com/rafaelaudy/rafaelaudy.github.io/master/images/posts/angular/angular-1-and-2-state/angular-2-languages.png)

It was quite difficult to write ES6 code some months ago. You had to set up a transpiler, configure source maps and so on. To address that the Angular 2 team is building a angular-cli project to bootstrap the your app and its build process. It is like a mixture yeoman of Yeoman and Grunt :p It will help you to create, build, serve and deploy your application. It is still in beta and can be [found here](https://github.com/angular/angular-cli).

![angular-cli](https://raw.githubusercontent.com/rafaelaudy/rafaelaudy.github.io/master/images/posts/angular/angular-1-and-2-state/angular-cli.png)

Do you remember Batarang? It is coming back with the codename Batarangle and is going to have a boost in its quality. Rangle.IO is going to be responsible for this and other Angular dev tools for Chrome. You can check it out [here](https://github.com/rangle/batarangle). The new plugin is aiming to support performance analysis, template navigation and debugging.

## Browser support:

This is huge: <br>
__IT IS GOING TO SUPPORT IE 9 :D__ <br>
This was one of the major criticisms to Angular 2. I thought I would get stuck in Angular 1.x because our clients would have to support at least IE 9. I am super happy about this announcement!

## Learning opportunities:

You can start learning Angular 2 now with a variety of different sources.
In my humble opinion NG-BOOK 2 is the best starting point. :)

![Learning resources for Angular 2](https://raw.githubusercontent.com/rafaelaudy/rafaelaudy.github.io/master/images/posts/angular/angular-1-and-2-state/angular-2-resources.png)

# Migrating to 2

Do you feel this way? I used to before the [AngularConnect](http://angularconnect.com/).

![Jumping to Angular 2](https://raw.githubusercontent.com/rafaelaudy/rafaelaudy.github.io/master/images/posts/angular/angular-1-and-2-state/angular-2-jump.png)

Hopefully the Angular team is going to release a library called Ng-Upgrade that is going to help us migrate our apps little by little.
We will not need to make a big bang conversion and both versions of Angular will be able to coexist.

![ng-migrate](https://raw.githubusercontent.com/rafaelaudy/rafaelaudy.github.io/master/images/posts/angular/angular-1-and-2-state/angular-2-migration.png)

The Angular team is going to release a blog post explaining how it is going to be done. For now you can have a look on [this repository](https://github.com/angular/angular/tree/master/modules/playground/src/upgrade).

# Release status

After AgularConnect my spider senses tell me that Angular 2 is almost being released, I would bet on Q1 next year.

Google already migrated to Angular 2 some of their own apps, including Google Adwords, which is their biggest money maker. This involves hundreds of developers and million lines of codes. Also the core of Angular 2 is already pretty stable and they don't expect more major changes.

# That is it!
If you want to know more about this topic have a look on this amazing keynote from the AngularConnect conference:

[![AngularConnect keynote](http://img.youtube.com/vi/UxjgUjVpe24/0.jpg)](https://www.youtube.com/watch?v=UxjgUjVpe24)

I will be writting more about Angular 2 shortly, see you later!

__Cheers :)__