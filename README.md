# Fandango Web-360 Application

# Description

With Fandango 360, users would be able to leverage Fandango’s 1st and 3rd party data streams, along with our refined scoring algorithm, to create optimized audience segments to push into today’s popular ad channels (available channels: Facebook, Google, LiveRamp, AdSmart, Apple News, Redshift, Twitter and Snapchat). By providing comprehensive movie-goer data, users interested in creating marketing campaigns on upcoming or past movies, can be confident when creating segments with our standardized smart-score or through manual attribute building. Fandango 360 users will be excited to reach a more targeted audience, spending less and converting more on their ad campaigns. </br>

## Technologies

Project | Language
------------ | -------------
Web | Angular 8
Unit test |Karma & Jasmine 
API | NodeJS
Database |Postgres, Elasticsearch
Authetication | Congnito
Sequalize | ORM 

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
    Components required commonly required throught the app are stored under this section.

- **Store :**
    The central NgRx store setup is kept under this section.


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

## Prior to running unit tests:
In the below file comment the following lines
#### **`karma.conf.js`**

```javascript 
    browsers: ['ChromeHeadlessNoSandbox'],
    customLaunchers: {
      ChromeHeadlessNoSandbox: {
        base: 'ChromeHeadless',
        flags: ['--no-sandbox']
      }
    },
    singleRun: true
```
And uncomment out the following lines.

```javascript 
browsers: ['Chrome'],
singleRun: false
```
- ![#f03c15](https://via.placeholder.com/15/f03c15/000000?text=+) `#f03c15` Make sure these changes are unstaged/reverted and not pushed into the repository.

## Running unit tests for all components:

Run `ng test` to execute the unit tests via [Karma](https://karma-runner.github.io). <br>
Run `ng test --code-coverage` to generate the a report containing the code coverage of the test cases. <br>
To check code coverage report goto application root directory and open /coverage/index.html<br>

## Run test for a single component:
In `tsconfig.spec.json` add the Absolute path of the test file under ```"**/*.d.ts"``` <br>
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

## Git Commands

After cloning the project create a new branch via JIRA and then fire the below commands:

```shell
git pull
git checkout <your_new_branch_name>
```
After completing your changes fire the below:

```shell
git status
git add -p # to add/reject changes press y : n
git commit -m "F360A-<story_id> #comment web - <changes_done>"
git push
```

## Links
### Code MGO Repo
- [Fandango Web360 Web App Repo](https://code.mgo.com/projects/ANALYTICS/repos/f360-web/browse "360 Web App")
### Running environment
- [Fandango Web360 Web DEV](http://fd-bi-f360-ui-dpe.s3-website-us-west-2.amazonaws.com/ "360 Web DEV")
- [Fandango Web360 Web INT](https://int-360.fandango.com/ "360 Web INT")
- [Fandango Web360 Web PROD](https://360.fandango.com/auth/login "360 Web PROD")
### CI/CD
- [Jenkins Build Job](https://ci.mgo.com/view/F360/job/F360Web-Build-Master/ "Jenkins Build Job")
- [Jenkins Deploy Job](https://ci.mgo.com/view/F360/job/F360Web-Deploy-Project/ "Jenkins Deploy Job")
