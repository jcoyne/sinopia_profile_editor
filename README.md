[![CircleCI](https://circleci.com/gh/LD4P/sinopia_profile_editor.svg?style=svg)](https://circleci.com/gh/LD4P/sinopia_profile_editor)
[![Coverage Status](https://coveralls.io/repos/github/LD4P/sinopia_profile_editor/badge.svg)](https://coveralls.io/github/LD4P/sinopia_profile_editor)

# LD4P's BIBFRAME Profile Editor

## Overview
From lcnetdev description:  "The BIBFRAME Profile Editor was designed to work on the widest range of machines possible. As such, most of the business logic is implemented client-side in JavaScript. This code can run in Chrome, FireFox, IE 8+, and Safari. The AngularJS framework used is the latest in client-side MVC architecture, and provides a clear model for structuring and organizing code. Every effort has been made to follow this structure and document the code, making future modifications as easy as possible.
All of the JavaScript code comes with comments explaining what each bit does. Documentation tools were used to generate documentation for this part of the application automatically. This documentation is available in /source/documentation/jsdoc/. It is also viewable from the web interface at /documentation/jsdoc/. The Editor also contains a help link containing a FAQ section."

# Sinopia Profile Editor
Technical documentation specific to the Sinopia Profile Editor
[wiki](https://github.com/LD4P/sinopia_profile_editor/wiki/Sinopia-Profile-Editor) follows.

## Installation Prerequisites (before using docker image)

### Prerequisites
1.  node.js

### Installation Instructions
1.  install node.js
2.  Run `npm init`, and follow the instructions that appear.
3.  Get latest npm: `npm install -g npm@latest`
4.  Run `npm install`. This installs everything needed for the build to run successfully.
5.  Run `grunt` to build the code and jsdocs and ngdocs.

## Running the code

Follow installation instructions, then run `node server.js` or `npm start`.  This will start up the profile editor at http://localhost:8000

## Developers

The javascript code uses the AngularJS framework https://angular.io/.  It uses grunt as a build tool.

### grunt-dev

To build the code without running jsdocs or ngdocs, `npm run grunt-dev`

### Check for some errors / style guide

`npm run eslint`

### test

Tests are written in jest, also utilizing puppeteer for end-to-end tests.  To run them `npm test`.

#### test coverage
To get coverage data, `npm run test-cov`.  Use a web browser to open `coverage/lcov-report/index.html`.  There is a project view and also a view of each file.

### static analysis

We use plato (actually es6-plato) to get static analysis info such as code complexity, etc.  `npm run analysis` will create a folder static-analysis; use a web browser to open `static-analysis/index.html`.  There is a project view and also a view of each file.

### continuous integration

We use circleci.  The steps are in `.circleci/config.yml`.  See https://circleci.com/gh/Ld4p/sinopia_profile_editor.  

In the "artifacts" tab of a particular build, you can look at code coverage (`coverage/lcov-report/index.html`) and at static analysis output (`static-analysis/index.html`).


# lcnetdev info below

## Data References

Profiles, templates, properties, vocabularies, and ontologies are all stored in the "config" database in Verso.

## Acknowledgements

Thank you [IndexData](http://indexdata.com/) for your assistance on the latest build!

Contributors:
* [Kirk Hess](https://github.com/kirkhess)
* [Charles Ledvina](https://github.com/cledvina)
* [Wayne Schneider](https://github.com/wafschneider)

## License

As a work of the United States government, this project is in the public domain within the United States.

Additionally, we waive copyright and related rights in the work worldwide through the CC0 1.0 Universal public domain dedication.
