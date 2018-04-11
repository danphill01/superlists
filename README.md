
# Useful TDD Concepts

**User Story**

    A description of how the application will work from the point of view of the user. Used to structure a functional test.
**Expected failure**

    When a test fails in the way that we expected it to.

# Useful Commands and Concepts

**Running the Django dev server**

    python manage.py runserver
**Running the functional tests**

    python manage.py test functional_tests
**Running the unit tests**

    python manage.py test lists


# The unit-test/code cycle

1. Run the unit tests in the terminal.

2. Make a minimal code change in the editor.

3. Repeat!


# Useful TDD Concepts

**Regression**

    When new code breaks some aspect of the application which used to work.
**Unexpected failure**

    When a test fails in a way we weren’t expecting. This either means that we’ve made a mistake in our tests, or that the tests have helped us find a regression, and we need to fix something in our code.
**Red/Green/Refactor**

    Another way of describing the TDD process. Write a test and see it fail (Red), write some code to get it to pass (Green), then Refactor to improve the implementation.
**Triangulation**

    Adding a test case with a new specific example for some existing code, to justify generalising the implementation (which may be a "cheat" until that point).
**Three strikes and refactor**

    A rule of thumb for when to remove duplication from code. When two pieces of code look very similar, it often pays to wait until you see a third use case, so that you’re more sure about what part of the code really is the common, re-usable part to refactor out.
**The scratchpad to-do list**

    A place to write down things that occur to us as we’re coding, so that we can finish up what we’re doing and come back to them later.

# Testing "Best Practices" Applied in this Chapter

**Ensuring test isolation and managing global state

    Different tests shouldn’t affect one another. This means we need to reset any permanent state at the end of each test. Django’s test runner helps us do this by creating a test database, which it wipes clean in between each test. (See also [chapter_purist_unit_tests].)
Avoid "voodoo" sleeps

    Whenever we need to wait for something to load, it’s always tempting to throw in a quick-and-dirty time.sleep. But the problem is that the length of time we wait is always a bit of a shot in the dark, either too short and vulnerable to spurious failures, or too long and it’ll slow down our test runs. Prefer a retry loop that polls our app and moves on as soon as possible.
Don’t rely on Selenium’s implicit waits

    Selenium does theoretically do some "implicit" waits, but the implementation varies between browsers, and at the time of writing was highly unreliable in the Selenium 3 Firefox driver. "Explicit is better than implict", as the Zen of Python says, so prefer explicit waits.

