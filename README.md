# Description

This project is for Fandango 360 Web application that is built using Angular 8 Framwork

## App Structure

- **Auth**
    This section contains all the Authenication components which includes login & password modifications and also the setup for NgRx store for auth

- **Layout**
    This section contains all the Layout components which includes Hearder, Footer & Navigation

- **Model**
    This section contains all the Model classes used in the application.

- **Pages**
    This section contains the core part of the entire application which includes the following.
    - Account
    - Admin
    - Audience-create
    - Audience-insights
    - Audience-Manager
    - Audience-Spotlight
    - Home

- **Services**
    This section contains the services resposible for the dependency injections required for the app to call the backed api and other required services.

- **Shared**
    Components required commonly required throught the app are stored underthis section.

- **Store**
- The central store setup is kept under this section.


## Steps to Run the Application Locally

### Clone the repo

```shell
git clone https://code.mgo.com/scm/analytics/f360-web.git
cd f360-web
```

### Install npm packages

Install the `npm` packages described in the `package.json` and verify that it works:

```shell
npm install
npm start or ng serve
```

The `npm start` which in turn calls `ng serve` builds (compiles TypeScript and copies assets) the application into `dist/`, watches for changes to the source files, and deploys the application on port `4200`. 

**The app will automatically reload if you change any of the source files.**

You can Shut it down manually with `Ctrl-C`.

## Code scaffolding

Run `ng generate component component-name` to generate a new component. You can also use `ng generate directive|pipe|service|class|guard|interface|enum|module`.

## Build

Run `ng build` to build the project. The build artifacts will be stored in the `dist/` directory. Use the `-prod` flag for a production build.

## Running unit tests

Run `ng test` to execute the unit tests via [Karma](https://karma-runner.github.io). <br>
Run `ng test --code-coverage` to generate the a report containing the code coverage of the test cases. <br>
To check code coverage report goto application root directory and open /coverage/index.html 

## Running end-to-end tests

Run `ng e2e` to execute the end-to-end tests via [Protractor](http://www.protractortest.org/).

## Links
- [Fandango Web360 Web App](https://code.mgo.com/projects/ANALYTICS/repos/f360-web/browse "360 Web App")

