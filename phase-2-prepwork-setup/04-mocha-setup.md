# Mocha Setup

As a developer, testing your code before it reaches any sort of live
environment is critical to ensuring that problems don't occur for end users.

Unit tests are tests designed to test the smallest piece of code that can be
logically isolated. This usually includes any functions, methods, and properties
that you write to ensure that they behave in the way you intended.

For now, you will not have to write your own tests, but you will have to run the
tests written for you.

In this reading, you will learn to:

- Install Mocha
- Run Mocha/Chai tests
- Read tests to understand requirements for tasks and assignments

## Testing Frameworks - Mocha and Chai

In JavaScript, one of the most popular unit testing libraries is [Mocha]. It
provides a plethora of tools to test your code. Writing tests is straightforward
as the syntax reads as plain English. Tests are written by **asserting** that
a certain condition is met. For example, a simple test describing the
`.indexOf()` method of Arrays could look like this:

```js
// Example from Mocha's documentation:
const assert = require('assert');
describe('Array', function() {
  describe('#indexOf()', function() {
    it('should return -1 when the value is not present', function() {
      assert.equal([1, 2, 3].indexOf(4), -1);
    });
  });
});
```

Note the `it()` function, which describes what the test should test for (in this
case that `.indexOf()` should return -1 when the specified value isn't in the
input Array). Also note the `assert` statement underneath that is checking to
see if the return of the first argument of the `.equals()` method is equal to
the second argument.

[Chai] is an assertion library that can be used in conjunction with Mocha to
write more detailed, fully-fledged tests that make use of other assertion
statements (e.g. `should` and `expect` instead of `assert`). These statements
do more or less the same things, but support other chained methods like
`assert`'s `.equal()`.

## Installing Mocha

To install Mocha, you will use the `npm` command.

> NOTE: DO NOT confuse `npm` with `nvm`. They are different tools. `nvm`
> controls the version of Node.JS you have installed, while `npm` is responsible
> for installing Node Packages which are third party pieces of software written
> in JavaScript.

To install mocha, enter the following command into your Mac or Windows terminal:

```shell
npm install -g mocha
```

The `-g` is called a flag. This changes the behavior of the install command.

In this case it means `global`.  By default, `npm` will install files into your
project directory.  We want mocha to be installed for all projects, so we
specify `-g`.

You can verify mocha works by typing

`mocha --version`

If it prints out a version number, pay yourself on the back, you have
successfully installed Node.JS and Mocha!

## Running Tests

Running a Mocha test is very straightforward. In problem sets provided to you,
the test files will likely be located in one place with the starter files.

First, navigate to the directory where the starter exists. This is typically
where the `package.json` file exists which contains metadata for the repository
and includes the packages/libraries that need to be installed to run the code
properly, including Mocha and Chai. For example, the file structure for the
repository structure may look like this:

```plaintext
testing-demo
  └──  package.json
  └──  problems
        └── problem-one.js
        └── problem-two.js
  └──  test
        └── problem-one-spec.js
        └── problem-two-spec.js
```

Simply run the following line in the terminal after navigating to the
`testing-demo` directory:

```shell
npm install
```

This should install all the dependencies for the code to run, including Mocha
and Chai. Afterwards, run the following command to execute the tests:

```shell
mocha
```

The results of the tests should be printed below, detailing which tests ran,
which tests passed (denoted by checkmarks), how many tests passed, and how long
the tests took to run.

```shell
  Problem One
    ✔ should <some assertion>
    ✔ should <some other assertion>

  2 passing (5ms)
```

## What you learned

In this reading, you learned what unit tests are, why they are important, how
to read them, and how to run them.

[Mocha]: https://mochajs.org/
[Chai]: https://www.chaijs.com/

