# Angular CLI with Library support (1.2.7)

This project was generated with [Angular CLI](https://github.com/angular/angular-cli). It is an extended version of a new app generated with ng new. It adds Library support for multiple apps in a mono-repo.

This starter is a result of many workarounds in order to make angular-cli work with a shared library of components/services/modules etc.

Currently supports: 

* Serving multiple apps at the same time
* Production build of multiple apps (with AOT)
* Shared Library of components/modules ( can be shared between each app with `@shared/` )
* Shared assets folder and polyfills. ( can be shared between each app )
* Shared SCSS. ( can be shared between each app )
* lazy loading of Shared modules
* Unit tests for each app
* E2E tests for each app
* Custom commands to make your life easier
* and everything else you would normally be able to do with an app generated with ng new. 

Feel free to create an issue for a request or to fix something. 

Star and support this project if you like it, to help it stay alive and maybe even be added as a boilerplate/starter to angular-cli (e.x. ng new app-name --template library).

## Versioning

Versioning of this project will follow the same with Angular-cli. There will be a separate branch that will be working for each version (starting with 1.2.7)

## Current Example

In the example of this repo there are two apps (app1 and app2):
* Each app is declared in angular-cli.json
* Each app has its own tsconfig file. 
* Each app can use the shared Library of components/providers/modules/assets and whatever else you want. In this example they share the `AngularCLIModule` module which is lazy loaded as a component of the default view/route.


## Commands

#### Development server

* Run `npm run app1` to serve app1 (runs `ng serve --app app1 --port 4200`)
* Run `npm run app2` to serve app2 etc. (runs `ng serve --app app2 --port 4201`) 

Names can change if you want (package.json). You can have multiple apps running in your browser as each app is launched on a different port. Navigate to `http://localhost:4200/` or `http://localhost:4201/` for example. Each app will automatically reload if you change any of the source files (if you edit your shared library both apps will reload if they are using it).

#### Build

* Run `npm run app1:build` to build app1. (runs `ng build --app app1 --prod`) 
* Run `npm run app2:build` to build app2 etc. (runs `ng build --app app2 --prod`) 

The build artifacts will be stored in the `dist/app1` or `dist/app2` directory. All builds are for production ( --prod ).

#### Code scaffolding

Run `ng generate component component-name` to generate a new component. To add a component to app1 specify app.module as in the following example: `ng g component default --module ../app.module.ts`. You can also use `ng generate directive|pipe|service|class|guard|interface|enum|module`.

#### Running unit tests

* Run `npm run app1:test` to run *.spec.ts tests in app1 folder. (runs `ng test --app app1`)  
* Run `npm run app2:test` to run *.spec.ts tests in app2 folder. (runs `ng test --app app2`)

#### Running end-to-end tests

* Run `npm run app1:e2e` to run e2e tests from e2e/app1 folder. (runs `ng e2e --app app1`)  
* Run `npm run app2:e2e` to run e2e tests from e2e/app2 folder. (runs `ng e2e --app app2`)

#### Further help

To get more help on the Angular CLI use `ng help` or go check out the [Angular CLI README](https://github.com/angular/angular-cli/blob/master/README.md).
