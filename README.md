JavaScript-Practices
====================

A place to collectively work on establishing JavaScript best practices for the OnePortal project.

Code Conventions
----------------

[Coding style matters](http://coding.smashingmagazine.com/2012/10/25/why-coding-style-matters/). At Optus, our coding style is based on [the style documented by Douglas Crockford](http://javascript.crockford.com/code.html), however we have some exceptions.

1.  **<del>Do not use `$` (dollar sign) or `\` (backslash) in names.</del>**
    
    We use `$` at the beginning of some variable names to indicate that they are jQuery objects.
    
2.  **<del>Avoid lines longer than 80 characters.</del>**
    
    We aren’t writing code on tiny 640x480 screens anymore so we can accommodate slightly longer lines than 80 chars. We don’t have a hard limit, but be sensible. Anything longer than about 120 chars and you should think about breaking it up.
    
3.  **<del>Variables should be listed in alphabetical order.</del>**
    
    This is arbitrary and there is no good reason for enforcing this rule. Order variables logically, and feel free to separate logical groups of variables with an empty line.
    
On top of this, we also have some conventions of our own.

1.  **Variable and function names should be in `camelCase`.**

2.  **Do not use the `for (variable in object)` syntax for `for` loops.**
    
    Its behaviour is confusing and can lead to less than obvious bugs. Instead we should use generic iterators, such as the `$.each` function provided by jQuery.

3.  **Do not wrap all of your code in closures.**
    
    Using self-executing functions to wrap your code in a closure is unnecessary boilerplate code. As long as you are careful when adding variables to the global scope, then there is no reason to include them. And yes, care should be taken when adding global variables – if I see any unnecessary global vars in your code it will result in 45 mins in the naughty corner.

4.  **Do not write your code in strict mode.**
    
    Strict mode provides no benefits that will not be found by linting your code and also has no performance benefits.

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

We use [Jasmine](https://jasmine.github.io/) for writing tests and [Sinon](http://sinonjs.org/) for stubs and mocks.

Specs should be saved with the `.spec.js` extension.
