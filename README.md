# snyk-report

This module was created to allow for snyk.io integration into CI workflow.

It is a WIP. Long term goals are to allow failure of build depending on rulesets, which will be dependent upon various factors, such as..

* Date of oldest vulnerability
* Count of high / medium / low vulnerabilities

## Getting Started

This module can be installed with `npm`.

    npm install snyk-report --save-dev

An example script has been included, which demonstrates `snyk-report` being run against either a directory pointed to by the `REPO_DIR` environment variable, or the current directory if it is not defined.

    'use strict';

    var report = require('./lib/report');

    var targetDir = process.env.REPO_DIR || __dirname;
    report(targetDir, function(err, output) {
      if (err) throw new Error(err);
      console.log(output);
    });


## Running the tests

Tests are a WIP - but will be included.

## Linting

Linting for the project can be run with the following command.

    npm run lint