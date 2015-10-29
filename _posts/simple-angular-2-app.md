---
layout: post
title: Creating your first Angular 2 app
---

Hi all,

This post will help you get your first [Angular 2]() + [TypeScript]() "hello world on asteroids" out of the door.
Please have a look on this [post]() first if you are wondering why you should learn Angular 2 and TypeScript.
Also make sure that you have [NodeJS]() installed before continuing.

I used [this tutorial](), build by the Angular team and [John Papa](), to create this little app.
[Here]() is the repository for the app that we are going to investigate.

PS: I am using [Visual Studio Code]() on a Mac which works quite well. :)

# Installing the app (boring things first)

To run our app we will need to install TypeScript and a node package to host our app.
It is simpler than it sounds, you just need to run these two commands:

`npm install -g live-server`

[live-server]() will let you host you app and add a live reload feature (sweet).
That means that whenever you change a file your browser will be automatically refreshed with the new content.

`npm install`

This will install Angular 2 and TypeScript which are the only dependencies specified in our package.json.
If you don't know what a package.json is you will need to learn a little bit more about [NodeJS]() and specially [NPM]().
But don't stress too much, for the purpose of this post you can abstract those technologies :).

# Hosting and compiling the app... Wait... Compiling?

Yes! We will need to compile our app to convert TypeScript into [ES5]() (same old JavaScript) code, otherwise browsers will not understand what we are creating. :)
It is super simple to do it, just run this command:

`npm run tsc`

Then just host your app running:

`npm start`

Done! You should have your app running on the browser.
At this stage the app already have ES5 JavaScript running in the browser instead of TypeScript.

As you are probably aware the commands we just ran are alias to the commands defined in package.json file.
Again, this topic is not the focus of this post :)

# So... About the Angular 2 code!

### Components
Components are main building blocks from a Angular 2 app.
Instead of having a mix of directives, views, controllers and multiple scopes you just have a tree of components now.
It will be simpler having a look on a code:

```javascript
@Component({
    selector: 'little-component',
    template: `
        This is a nice little component :)
        <h1>{{title}}</h1>
        `
})
class LittleComponent {
    public title = 'Sweet!';
}
```

To define a component using Angular 2 we will need to creat a class (TypeScript) and decorate (TypeScript) with the @Component decorator.
Then our class will have our logic while the componnet decorator is going to define the Angular component.
The decorator content reminds me a lot of how we used to create a Angular 1 directive deffinition.

Just to help you out, here is a quick comparison of Angular 1 and 2 concepts:

Angular 1                       Angular 2
App.js							Top level component
Directives						Component
Controller and a vire 			Component
Directive with a controller 	Component

Much simpler, right?
This decorator sintax is probably going to be part of ES7.

Ok now lets have a look in the code from the repository, which is a component a little bit fancier:

```javascript
// Ignore this for now
import {bootstrap, Component, FORM_DIRECTIVES} from 'angular2/angular2';

class Hero {
  id: number;
  name: string;
}

@Component({
    selector: 'my-app',
    template: `
        <h1>{{title}}</h1>
        <h2>{{hero.name}} details!</h2>
        <div><label>id: </label>{{hero.id}}</div>
        <div>
            <label>name: </label>
            <input [(ng-model)]="hero.name" placeholder="name">
        </div>
        `,
    directives: [FORM_DIRECTIVES]
})
class AppComponent {
    public title = 'Tour of Heroes';
    public hero: Hero = {
        id: 1,
        name: 'Windstorm'
    };
}

// Ignore this for now
bootstrap(AppComponent);
```

Let's point out some interesting bits of this component:
* Selector: This is how you are going to 'activate' your componen in the html. In this case you can use <my-app> on the html.
* Template: Quite easy, just the HTML that is going to be inserted when this component is used. You can also specify a templateUrl.
* Directives: Kind of a dependency injection. You have to pass an array with all the other components that you are going to use.
    The FORM_DIRECTIVES is an array of common components used in forms (duh). You have to add it if you want to use two-way data binding for example.
* [(ng-model)]: This is how you create two-way data binding now.
* Typed language: Did you saw how we reused the Hero class? Try to construct it with the wrong data you will get a nice error :)

### Dependency Injection
As you probably realised, the first line from the example above is one of the new ways to use dependency injection ([SystemJS]()).
That makes Angular 2 much better than 1 in my opinion, to begin with we can reuse code much easier. The dream of reusing your models defined on the server is not that far away anymore.

```javascript
import {bootstrap, Component, FORM_DIRECTIVES} from 'angular2/angular2';
```

Another neat things is that with TypeScript you have autocomplete while typing the stuff inside the 'import { '.

![Autocomplete with TypeScript]()

### Templating

As you saw the way to create a two-way data binding changed a little bit.
The picture bellow shows how to bind to events and properties with Angular 2:

![Angular 2 binding example](https://raw.githubusercontent.com/rafaelaudy/rafaelaudy.github.io/master/images/posts/angular/angular-1-and-2-state/Angular-2-style.png)

### Wiring everything up
You might wonder where is the app.js where you used to configure your app and bootstrap your app.
That is all going to be done in the root component now. That is why this code is executed at the bottom of the file.
It is basically tellying Angular that this is the root component.

```javascript
bootstrap(AppComponent);
```

Now you can just go and use it on your index.html.

```html
<html>
  <head>
    <title>Angular 2 QuickStart</title>
    <script src="../node_modules/systemjs/dist/system.src.js"></script>
    <script src="../node_modules/angular2/bundles/angular2.dev.js"></script>
    <script>
      System.config({
        packages: {'app': {defaultExtension: 'js'}}
      });
      System.import('app/app');
    </script>
  </head>
  <body>
    <my-app>Loading...</my-app>
  </body>
</html>
```

### TypeScript coolness
Using TypeScript is not only going to enhance the JavaScript language, it is also going yo provide a lot of help during development.
In this small code sample you can try do things like:

* Change type
* Autocomplete with documentation
* Classes and consructor
* Go to

### Debugging the code
*Debug with typescript