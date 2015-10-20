---
layout: post
title: AngularJS, NodeJS and Couchbase - Personal Retrospective and Learnings
---

Since I have been working for almost a year in a big project built with AngularJS, NodeJS and Couchbase
<br>I thought it would be a good idea to review it and write about all the cool things I learned and the pitfalls
that we encountered.

The application was targeted to be globally available and had to handle a lot of data so there was no shortage of challenges.

I'll be writing about those topics in the followings months, this post is a kind of backlog.
<br>So please comment if you want me to prioritize one of the subjects and thank you for your patience. :)

If you don't agree with the way we handled one of these challenges let me know, I would love the feedback! :)

# AngularJS
## The good

* IE8 Support

	If you are supporting IE8 you have to use AngularJS 1.3. Which is a shame since 1.4 and beyond have some major improvements in performance.
	<br>You are also probably going to need to add the es5 shims and shams.
	<br>Have a look here: https://github.com/es-shims/es5-shim

* Tests

	I may write a post about this soon. :)
	<br>I will talk about how to write unit and end to end tests, how to mock services and how to add test coverage.

* SASS

	I may write a post about this soon. :)

* AngularJS

	I may write one or more post about the following soon:

	Interesting techniques aroud the __resolve method and caching__;
	<br>How to enable __localization__;
	<br>The best way to __structure__ 90% of your AngularJS __apps__;
	<br>I to simplify and share some __interesting directives__ that we have done around date pickers;
	<br>How to add __validation banners__ with scroll, focus and higlights;
	<br>Implementing modals;
	<br>Talk about the controller as sintax and __John Papa's style guide__;
	<br>How to convert from __View model to DTO__ and vice versa;
	<br>How to use __factories__ in AngularJS.

* Dev process

	I may write one or more post about the following soon:

	How to run your app in __dev and prod__ environments;
	<br>How to set up __live browser update__ and __run the tests after changes__;
	<br>Improving __grunt__ creating internal variables and __separating its content in different files__;
	<br>Implementing __feature switch__;
	<br>Adding __static analysis__;
	<br>Hot to deploy an AngularJS app, I will talk about, concatenating files, minifying them, adding version to generated assets, caching them, creating a distribution folder and more.


### The bad

* Time to run the tests

	We have loads of unit and specially end to end tests and they can take up to 9 minutes to run without the API mocks.
	<br>With the mcks and different optimization techniques we managed to drop that number to 3 minutes, which is still a relevant wait.

	I have some ideas to improve that in the following projects and I will discuss that it in a future post.

* Performance

	We encountered some performance issues because of our UX guidelines, which made us add to many bindable controls visible on the screen at the same time.
	<br>We also encountered problems optimizing directives.

	I will talk about the solutions that we encountered in another post.

* IE8

	Do I really have to say something? :) Supporting old versions of IE is a pain.
	<br>This means not being able to migrate to newer versions of Angular and also dealing with weird CSS and Javascript problems.

* Phamton
* Unit tests
* Build process
* Event hell between directives

### I will think about in the next project
	Performance of isolated scopes in directives
	Ballance of unit x end to end tests
	Build


# NodeJS
### The good
	Memory leak assessment
	Schema validation
	Config strategy
	Code coverage
	Logging with logstash
	XML to JS
	JS to XML
	Request
	Bluebird promisses
	Shut down nodejs on error
	Middleware examples
	Configurations
	Defining routes
	Folder structure

### The bad
### I will think about in the next project

# Couchbase
	Couchbase API
	Setting up views / documents
### The good
### The bad
### I will think about in the next project


# Other

	Sharing data beetwen javascript apps
	Get a MAC


