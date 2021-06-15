# Fandango Web-360 Application

# Description

With Fandango 360, users would be able to leverage Fandango’s 1st and 3rd party data streams, along with our refined scoring algorithm, to create optimized audience segments to push into today’s popular ad channels (available channels: Facebook, Google, Twitter, Snapchat).
By providing comprehensive movie-goer data, users interested in creating marketing campaigns on upcoming or past movies, can be confident when creating segments with our standardized smart-score or through manual attribute building. Fandango 360 users will be excited to reach a more targeted audience, spending less and converting more on their ad campaigns. </br>
### Product Vision
With our MVP release, initially we would like to have movie studios onboarded and using the Fandango 360 as an integral part of their ad marketing campaigns targeting. They would be empowered to quickly create and manage their audiences.
Ultimately, we would like any potential client, interested in creating a target audience for a movie, to be able to use Fandango 360 to not only create accurate segments but also use it as an insights tool to discover more about their audience’s behaviors.

## Technologies

Project | Language
------------ | -------------
Web | Angular 8
Unit test |Karma & Jasmine 
API | NodeJS
Database |Postgres

## App Structure

- **Auth :**
    This section contains all the Authenication components which includes login & password modifications and also the setup for NgRx store for auth

- **Layout :**
    This section contains all the Layout components which includes Hearder, Footer & Navigation

- **Model :**
    This section contains all the Model classes used in the application.

- **Pages :**
    This section contains the core part of the entire application which includes the following.
    - Account
    - Admin
    - Audience-create
    - Audience-insights
    - Audience-Manager
    - Audience-Spotlight
    - Home

- **Services :**
    This section contains the services resposible for the dependency injections required for the app to call the backed api and other required services.

- **Shared :**
    Components required commonly required throught the app are stored underthis section.

- **Store :**
    The central store setup is kept under this section.


## Running the Application Locally

### Prerequisite for running the application
 - Make sure node js is installed by running `node -v` in your bash terminal
 - Fire this command to install angular CLI `npm install -g @angular/cli`

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
ng serve --open  # to automatically open your default browser
```

The `npm start` which in turn calls `ng serve` builds (compiles TypeScript and copies assets) the application into `dist/`, watches for changes to the source files, and deploys the application on port `4200`. 

**The app will automatically reload if you change any of the source files.**

You can Shut it down manually with `Ctrl-C`.

## Code scaffolding

Run `ng generate component component-name` to generate a new component. You can also use `ng generate directive|pipe|service|class|guard|interface|enum|module`.

## Build

Run `ng build` to build the project. The build artifacts will be stored in the `dist/` directory. Use the `-prod` flag for a production build.

<b> Make sure to Run </b> `ng build --prod --aot` before pushing your changes.

## Running unit tests for all components:

Run `ng test` to execute the unit tests via [Karma](https://karma-runner.github.io). <br>
Run `ng test --code-coverage` to generate the a report containing the code coverage of the test cases. <br>
To check code coverage report goto application root directory and open /coverage/index.html<br>

## Run test for a single component:
In `tsconfig.spec.json` add the Absolute path of the test file under ```__"**/*.d.ts"__  ``` <br>
Example: 
```json
"src/app/pages/admin/admin-menu/admin-menu.component.spec.ts"
```
In `test.ts` comment out ```const context = require.context('./', true, /\.spec\.ts$/);``` and add the path to yout spec file <br>
Example: 
```javascript
const context = require.context('app/pages/admin/admin-menu', true, /admin-menu.component\.spec\.ts$/);
```
## Running end-to-end tests

Run `ng e2e` to execute the end-to-end tests via [Protractor](http://www.protractortest.org/).

## Links
- [Fandango Web360 Web App Repo](https://code.mgo.com/projects/ANALYTICS/repos/f360-web/browse "360 Web App")
- [Fandango Web360 Web DEV](http://fd-bi-f360-ui-dpe.s3-website-us-west-2.amazonaws.com/ "360 Web DEV")
- [Fandango Web360 Web INT](https://int-360.fandango.com/ "360 Web INT")
- [Fandango Web360 Web PROD](https://360.fandango.com/auth/login "360 Web PROD")
- [Jenkins](http://10.13.33.48/ "Jinkins")


