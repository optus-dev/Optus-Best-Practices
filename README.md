JavaScript-Practices
====================

A place to collectively work on establishing JavaScript best practices for the OnePortal project.

Code Conventions
----------------

[Coding style matters](http://coding.smashingmagazine.com/2012/10/25/why-coding-style-matters/). At Optus, we follow the style [documented by Douglas Crockford](http://javascript.crockford.com/code.html).

Folder Structure
----------------

*   external
*   app
    *   functions
    *   behaviours
*   tests
    *   functions
    *   behaviours
*   release

Testing
-------

All JS should be developed using TDD. A high level of test coverage with suitable assertions is expected.

We use [Jasmine](http://pivotal.github.com/jasmine/) for writing tests and [Sinon](http://sinonjs.org/) for stubs and mocks.

Specs should be saved with the `.spec.js` extension.