---
layout: post
title: Creating your first Angular 2 app
---

Hi all,

This post will help you get your first [Angular 2]() + [TypeScript]() "hello world on asteroids" out of the door.
Please have a look on this [post]() first if you are wondering why you should learn Angular 2 and TypeScript.

If you are wondering I am using [Visual Studio Code]() on a Mac. :)
Please make sure that you have [NodeJS]() installed.

I used [this tutorial](), build by the Angular team and [John Papa]() to create this little app.
[Here]() is the repository for the app that we are going to be discussing.

# Installing the app

To run our app we will need to install TypeScript and a package to host our app. It is super simple you just need to run two commands.

`npm install -g live-server`

Now you have a package to host you app and add a live reload feature. That means that whenever you change a file your browser will be automatically refreshed with the new content.

`npm install`

This will install Angular 2 and TypeScript which are the only dependencies specified in our package.json.

# Hosting and compiling the app... Wait... Compiling?

Yes! We will need to compile our app since it is written with TypeScript.
But to do it is quite simple, you just need to run this command:

`npm run tsc`

Then just host your app running:

`npm start`

Done! You should have your app running on the browser.
At this stage the app already have ES5 JavaScript running in the browser instead of TypeScript.

As you are probably aware the commands we just ran are alias to the commands defined in package.json file.
Those are not the focus of this post :)

# So... About the Angular 2 code!

### Components
What is a component

Old								New
App.js							Top level component
Directives						Component
Controller 						Component
Directive with a controller 	Component

```javascript
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

bootstrap(AppComponent);
```

Annotation
  Selector
  Template
  directives

decorator to create components
very similar to .net for example
it is probably going to be part of ES7

### Dependency Injection
new Dependency injections is just ES6 and Typescript
now we can reuse basic classes from the server for example

### Templating

### Wiring everything up
bootstrap
index

### TypeScript coolness
Change type
Autocomplete with documentation
Classes and consructor
Go to

### Debugging the code
Debug with typescript