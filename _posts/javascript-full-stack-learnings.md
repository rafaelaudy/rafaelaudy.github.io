---
layout: post
title: AngularJS, NodeJS and Couchbase - Personal Retrospective and Learnings
---

Since I have been working for almost a year in a big project built with AngularJS, NodeJS and Couchbase
I thought it would be a good idea to review and write about all the cool things I learned and the pitfals
that we encoutered in the process of making an application that will be globally availlable.

If you don't agree with one of the topics please write in the comments, I would love the feedback! :)

### AngularJS
### The good

	IE8 Support
		Version of AngularJS
		Shims

	Tests
		End to end tests
		Wait
		Mocking tests
		Test coverage

	SASS

	AngularJS
		Default resolve, calling just once
		Localization
		Folder structure
		Directives
			Text countdown
			Multi select datepicker
			Date picker
		Validation
			Scroll
			Summary
			Setting style after save
		Modals
		Controller as and John Papa's style guide
		View model to DTO and vice versa
		Factories

	Dev process
		run app in dev and dist
		Watch / host
		Reising variables grunt
		Feature switch
		Dividing the Grunt project
		Integration with IIS MVC
		Static analysis
		Deploy & minifying strategy
			Concatenating directives
			Adding versions to minifyed files
			Copying files
			Concatenatig files and changing the UI
			Verifying if it need to be done


### The bad
	Time to run the tests
	Performance
	IE8
	Phamton
	Unit tests
	Build process
	Event hell between directives

### I will think about in the next project
	Performance of isolated scopes in directives
	Ballance of unit x end to end tests
	Build


### NodeJS
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

### Couchbase
	Couchbase API
	Setting up views / documents
### The good
### The bad
### I will think about in the next project


### Other

	Sharing data beetwen javascript apps



