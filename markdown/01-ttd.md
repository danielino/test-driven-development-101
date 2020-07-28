# Test Driven Development 101



---


## Goal

  - Understand the rationale of TDD

---

# Test Driven Development

1- define and clarify one user requirement
2- write down some examples with the inputs and the expected outputs
3- write the code testing for the expected behavior
4- implement the code

----

## TDD in practice

You need to implement a function that finds the maximum number in a list.

The first step is to *gather examples*.

```python

my_input = [1,5,3,0,9]
expected_output = 9
```

---- 

Then I write my function, which just throws an exception

```python
def maximum(l: list):
    raise NotImplementedError("Write me") 
```

----

Finally I write the test

```python
def test_maximum(my_input, expected_output):
    assert maximum(my_input) == expected_output

# and run it

test_maximum(my_input, expected_output)
```

Now I just have to start coding until the test works.

----

## Advantages

- your code will be covered by tests in time
- newcomers can develop without fear of breaking things
- refactors will be safer
- code usability and reusability
- less time spent in debugging
- bugs are isolated easily

=> Faster development

----

## Advantages

Writing tests helps the developer to *think* about how using the function
and being in the shoes of the function user.

This improves design significantly!

---

# What to test

So the question: should I write unit test for every function/method?

While you should write unit test for relevant functionalities (eg. public methods, ...)
you should focus on *code coverage* instead.

Code coverage is a measure in percentage used to describe the degree to which the source code of a program is executed when a particular test suite runs; 

----

## Code coverage

A code coverage of 75% means that your testsuite executes 75% of the project's code.
An acceptable code coverage starts at 88-90%

Using a code-coverage tool you can ensure that even if you don't wrote unittest for all functions, that test is still stressed.
Moreover you can use those tools to identify the uncovered parts, so that you can add more test cases or discover "dead" code parts.


