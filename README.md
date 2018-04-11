
# Useful TDD Concepts

**User Story**

    A description of how the application will work from the point of view of the user. Used to structure a functional test.
**Expected failure**

    When a test fails in the way that we expected it to.

# Useful Commands and Concepts

**Running the Django dev server**

    python manage.py runserver
**Running the functional tests**

    python functional_tests.py
**Running the unit tests**

    python manage.py test
**The unit-test/code cycle**

1. Run the unit tests in the terminal.

2. Make a minimal code change in the editor.

3. Repeat!


Useful TDD Concepts

Regression

    When new code breaks some aspect of the application which used to work.
Unexpected failure

    When a test fails in a way we weren’t expecting. This either means that we’ve made a mistake in our tests, or that the tests have helped us find a regression, and we need to fix something in our code.
Red/Green/Refactor

    Another way of describing the TDD process. Write a test and see it fail (Red), write some code to get it to pass (Green), then Refactor to improve the implementation.
Triangulation

    Adding a test case with a new specific example for some existing code, to justify generalising the implementation (which may be a "cheat" until that point).
Three strikes and refactor

    A rule of thumb for when to remove duplication from code. When two pieces of code look very similar, it often pays to wait until you see a third use case, so that you’re more sure about what part of the code really is the common, re-usable part to refactor out.
The scratchpad to-do list

    A place to write down things that occur to us as we’re coding, so that we can finish up what we’re doing and come back to them later.

