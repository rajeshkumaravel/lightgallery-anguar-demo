# [jQuery lightGallery](https://github.com/sachinchoolur/lightGallery) demo with Angular


#### Step 1
Include jQuery in you project.

Take a look at the [StackOverflow answer](https://stackoverflow.com/questions/43934727/how-to-use-jquery-plugin-with-angular-4) for reference - 

#### Step 2
Install lightgallery package via npm

`npm install lightgallery`

Install required [plugin ](https://github.com/sachinchoolur/lightGallery#modules) (optional)

`npm install lg-zoom lg-share`


#### Step 3

Add lightgallery to the runtime global scope

 1) Add lightgallery.js and it's plugins path to the `scripts` field in the angular.json file
 
```
"scripts": [
  "node_modules/jquery/dist/jquery.min.js",
  "node_modules/lightgallery/dist/js/lightgallery.js",
  "node_modules/lg-zoom/dist/lg-zoom.js"
]
```

2) Add lightgallery.css path to the `styles` field in the angular.json file
```
"styles": [
  "node_modules/lightgallery/dist/css/lightgallery.css",
],
```

#### Step 4
Define typings for lightgallery.js

In `src/typings.d.ts` add the following line 

`declare var lightGallery: any;` 

#### Step 5

Invoke lightgallery

``` ts
ngOnInit() {
  ($('#lightgallery') as any).lightGallery();
}

```

-----------------------------

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 10.1.1.

## Development server

Run `ng serve` for a dev server. Navigate to `http://localhost:4200/`. The app will automatically reload if you change any of the source files.

## Code scaffolding

Run `ng generate component component-name` to generate a new component. You can also use `ng generate directive|pipe|service|class|guard|interface|enum|module`.

## Build

Run `ng build` to build the project. The build artifacts will be stored in the `dist/` directory. Use the `--prod` flag for a production build.

## Running unit tests

Run `ng test` to execute the unit tests via [Karma](https://karma-runner.github.io).

## Running end-to-end tests

Run `ng e2e` to execute the end-to-end tests via [Protractor](http://www.protractortest.org/).

## Further help

To get more help on the Angular CLI use `ng help` or go check out the [Angular CLI README](https://github.com/angular/angular-cli/blob/master/README.md).
