---
layout: post
keywords: AngularJS, NodeJS, Couchbase, retrospective, Rafael Audy, Rafael Glanzner, Rafael Audy Glanzner
---

Since I have been working for almost an year in a big project built with AngularJS, NodeJS and Couchbase I thought it would be a good idea to do a small review and register the coolest things I learned and some of the pitfalls my team encountered.

![Gandalf thinking about the project](http://mulubinba.typepad.com/.a/6a00d8341dd88553ef014e5f56216c970c-pi)

The application was targeted to be globally available and had to handle a lot of data so there was no shortage of challenges.

I'll be writing about some of those topics in the followings months, this post is a kind of a backlog.
So please shout at the comments if you want me to prioritize one of these subjects and thank you for your patience. :)

If you disagree with the way we handled one of these challenges let me know, I would love the feedback!

# AngularJS and other UI bits

## Things I enjoyed doing:

#### IE8 Support

If you are supporting IE8 and using AngularJS you have to use version 1.2. Which is a shame since 1.3 and beyond have some major improvements in performance. You are also probably need to add the es5 [shims and shams](https://github.com/es-shims/es5-shim).

#### Tests

I may write a post about this soon. :)
<br>I will talk about how to write unit and end to end tests, how to mock services and how to add test coverage.

#### SASS

#### AngularJS

One or more post about the following may be written soon:

* Interesting techniques around the __resolve method and caching__;
* How to enable __localization__;
* The best way to __structure__ 90% of your AngularJS __apps__;
* How to add __validation banners__ with scroll, focus and highlights;
* Implementing modals;
* Controller as syntax and __John Papa's style guide__;
* How to convert from __View model to DTO__ and vice versa;
* How to use __factories__ in AngularJS.

#### Dev process

I may also write one or more posts about the following:

* How to run your app in __dev and prod__ environments;
* How to set up __live browser update__ and __run the tests after changes__;
* Improving __grunt__, creating internal variables and __separating its content in different files__;
* Implementing __feature switch__;
* Adding __static analysis__;
* How to concatenate files for deploy, minify them, add version to generated assets, cach them, create a distribution folder and more.

## Challenges we faced:

![Spider man does not want to support IE8](http://cdn.meme.am/instances/500x/55274752.jpg)

#### Time to run the tests

We have loads of unit and especially end to end tests and they can take up to 9 minutes to run without the API mocks. With the mocks and different optimization techniques we managed to drop this number to 3 minutes, which is still a relevant wait.

I have some ideas to improve that in the following projects and I will discuss that in a future post.

#### Performance

We encountered some performance issues because of our UX guidelines, which made us add too many bindable controls visible on the screen at the same time. We also encountered problems optimizing directives.

I will talk about the solutions we encountered in another post.

#### IE8

Do I really have to say something? :) Supporting old versions of IE is a pain. This means not being able to migrate to newer versions of Angular and also dealing with weird CSS and Javascript problems.

#### Phantom

I was impressed by the amount of times we had e2e tests failing just on phantom for a variety of weird reasons. After we discovered that we could also have headless browser testing with chrome we completely abandoned Phantom and our lives got much better ever since :)

#### Unit tests

I think we didn't achieve a healthy ratio of unit X e2e tests. Although our code coverage was above 90% of the app a small percentage of that number came from unit tests. That means our test suite was not as fast as we would like. I will talk more about this in a future post.

#### Build process

Our build process was quite slow in the beginning due to some inefficacies and the test replication across different branches. We now changed that and the process is much quicker. I will also talk more about this in another post.


# NodeJS

![NodeJS is awesome](http://www.quickmeme.com/img/00/006fd811b42bb561542996b7ffb15bb36f25449f5f063eacac886919da848ce6.jpg)

## Things I enjoyed doing:

#### Project setup
* Using logstash, Kibana and Winston for logging;
* Using nconf to organize configuration files;
* Code organization and folder structure.

#### API
* Using JSON schema validation to validate incoming json objects;
* Converting XML to json and vice versa;
* Using Request extensively to connect to other APIs;
* Using Bluebird to transform callbacks into promises;
* Organizing Express routes;
* Restarting Node.js process on errors;
* Creating a variety of Express middlewares.

#### Tests
* Adding code coverage to Mocha tests.

#### Couchbase
* Implementing a small wrapper to the Couchbase API;
* Setting up views / documents.

# Other

#### Sharing data between javascript apps
#### Get a MAC
Seriously, get a MAC if you don't have one :)
I started with a Windows box, then changed to Linux and finally got a MAC.
Although I like Linux for programming purposes a MAC is much better is all other regards.

__Cheers :)__