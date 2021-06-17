# OfficeAddIn

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 11.0.6.

## Description
The project intends to build an office.js addin template using angular, for microsoft excel 365. 

## Set up.
The projects initial code base was generated as a simple, new angular project.

*Important* It's important to note the microsoft REQUIRES that office.js addins have two items:
1. they reference the most recent CDN in a script tag in the <head> tag of the page. 

`<head>
    ...
    <script src="https://appsforoffice.microsoft.com/lib/1/hosted/office.js" type="text/javascript"></script>
</head>`

Thus, this was added to the root directory index.html page.

1. they initialize the office add-in using either `Office.onReady()` or `Office.Initialize`. Other js framework initialize functions should be placed inside this.



More info on intializing the add-in can be found here `https://docs.microsoft.com/en-us/office/dev/add-ins/develop/initialize-add-in`;



From there, the package.json files were modified to include required dependencies needed to build the microsoft excel 365 add in.

Then, a normal taskpane addin manifest.xml file was added to the project root folder. This file came from a project folder built using the yo generator. More information on the manifest.xml file can be found here `https://docs.microsoft.com/en-us/office/dev/add-ins/develop/add-in-manifests?tabs=tabid-1`

To transpile the add in, a webpack config file was added to the root. This webpack config file was also sourced from the example excel addin from Microsoft using the yo generator.

## Summary
Excel add-ins using office.js, are set up based on a manifest.xml file. This file describes how the add in should be set up. Currently (June 2021), there are two types of excel office.js addins, content addins and taskpane addins.

The content addin opens a webpane object that can be placed in an excel worksheet.

The taskpane addin opens a sidebar taskpane which displays web content. 

At June 2021, I don't believe there's an option to have both a content add in and a taskpane add in.


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

To get more help on the Angular CLI use `ng help` or go check out the [Angular CLI Overview and Command Reference](https://angular.io/cli) page.
