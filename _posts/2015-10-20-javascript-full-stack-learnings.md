---
layout: post
title: AngularJS, NodeJS and Couchbase - Personal Retrospective and Learnings
---

![Gandalf thinking about the project](http://mulubinba.typepad.com/.a/6a00d8341dd88553ef014e5f56216c970c-pi)

Since I have been working for almost a year in a big project built with AngularJS, NodeJS and Couchbase

I thought it would be a good idea to review it and write about all the cool things I learned and the pitfalls that we encountered.

The application was targeted to be globally available and had to handle a lot of data so there was no shortage of challenges.

I'll be writing about those topics in the followings months, this post is a kind of backlog.
So please comment if you want me to prioritize one of the subjects and thank you for your patience. :)

If you don't agree with the way we handled one of these challenges let me know, I would love the feedback!

# AngularJS and other UI bits

## Things that I liked to do:

#### IE8 Support

If you are supporting IE8 you have to use AngularJS 1.2. Which is a shame since 1.3 and beyond have some major improvements in performance. You are also probably going to need to add the es5 shims and shams. Have a look here: https://github.com/es-shims/es5-shim

#### Tests

I may write a post about this soon. :)
<br>I will talk about how to write unit and end to end tests, how to mock services and how to add test coverage.

#### SASS

#### AngularJS

I may write one or more post about the following soon:

* Interesting techniques aroud the __resolve method and caching__;
* How to enable __localization__;
* The best way to __structure__ 90% of your AngularJS __apps__;
* I to simplify and share some __interesting directives__ that we have done around date pickers;
* How to add __validation banners__ with scroll, focus and higlights;
* Implementing modals;
* Talk about the controller as sintax and __John Papa's style guide__;
* How to convert from __View model to DTO__ and vice versa;
* How to use __factories__ in AngularJS.

#### Dev process

I may write one or more post about the following soon:

* How to run your app in __dev and prod__ environments;
* How to set up __live browser update__ and __run the tests after changes__;
* Improving __grunt__ creating internal variables and __separating its content in different files__;
* Implementing __feature switch__;
* Adding __static analysis__;
* Hot to deploy an AngularJS app, I will talk about, concatenating files, minifying them, adding version to generated assets, caching them, creating a distribution folder and more.

## Challenges that we faced:

![Spider man does not want to support IE8](http://cdn.meme.am/instances/500x/55274752.jpg)

#### Time to run the tests

We have loads of unit and especially end to end tests and they can take up to 9 minutes to run without the API mocks. With the mocks and different optimization techniques we managed to drop that number to 3 minutes, which is still a relevant wait.

I have some ideas to improve that in the following projects and I will discuss that it in a future post.

#### Performance

We encountered some performance issues because of our UX guidelines, which made us add to many bindable controls visible on the screen at the same time. We also encountered problems optimizing directives.

I will talk about the solutions that we encountered in another post.

#### IE8

Do I really have to say something? :) Supporting old versions of IE is a pain. This means not being able to migrate to newer versions of Angular and also dealing with weird CSS and Javascript problems.

#### Phantom

I was impressed but the amount of times that we had e2e tests failing just on phantom for a variety of reasons. After we discovered that we could also have headless browser testing with chrome we completely abandoned Phantom and our lives were much better ever since :)

#### Unit tests

I think we did not achieve a healthy ratio of unit X e2e tests. Although our code coverage was above 90% of the app a small percentage of that number came from unit tests. That means that our test suite was nor as fast as we would like. I will talk more about this in a future post.

#### Build process

Our build process was quite slow in the beginning due to some inefficacies and the test replication across different branches. We now changed that and the process is much quicker. I will talk more about this in a future post.


# NodeJS

![NodeJS is awesome](http://www.quickmeme.com/img/00/006fd811b42bb561542996b7ffb15bb36f25449f5f063eacac886919da848ce6.jpg)

## Things that I liked to do:

#### Project setup
* Logging with logstash;
* Config strategy;
* Folder structure;

#### API
* Schema validation;
* XML to JS;
* JS to XML;
* Request;
* Bluebird promisses;
* Defining routes;
* Shut down nodejs on error;
* Middleware examples;

#### Tests
* Memory leak assessment;
* Code coverage;

#### Couchbase
* Couchbase API
* Setting up views / documents

# Other

#### Sharing data beetwen javascript apps
#### Get a MAC