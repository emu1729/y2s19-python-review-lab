## Y2 2018 Summer: Python Cipher Lab

Welcome to the Python Cipher lab! Please read all the instructions so you don't
get lost halfway through, but definitely feel free to ask for help if you
get stuck. Good luck, and have fun!

### Part 1: Basic functions

The stubs for these functions can be found in `part1.py`. You can test your functions by running `part1-test.py`.

1. Write a function to `hello_world`, which takes in no inputs
and prints `hello world`. 

2. Write a function `greet_by_name` which takes in a string, `name`,
and prints `hello <name>`

3. Write a function, `encode`, that takes in a number, `x` and computes
the product of `x` and 3953531.
This function shouldn't print anything, but should return an integer value.

4. Write a function, `decode`, which takes in the output from the previous function and
finds `x`. You may use the value 3953531 in this function.

### Part 2: Loops

The stubs for these functions can be found in `part2.py`.

1. First, update your function `encode`, to take in 2 numbers `x` and `y`, and compute their product.
This function should require `1 < y < 250` and `500 < x < 1,000`. If this isn't true, the function should print
`Invalid input: Outside range.`, and return None.

2. Update your encode function to guarantee that the inputs `x` and `y` are prime. If `x` is not prime,
then keep incrementing the value of `x` until it is prime; then, do the same process for `y`. If this
causes the new values of `x` and `y` to be out of the range, print `Invalid input: Outside range.`,
and return None.  
*Hint: Have we implemented any functions previously, which could be useful here?*

3. Write a function, `decode`, which takes in the output (the value of the product)
from your updated `encode` function and tries to compute values for `x` and `y`.
This function only takes in, as input,
the `coded_message`, which is output from `encode`. You may also use the ranges of possible values for `x` and `y` - that is, `1 < y < 250` and `500 < x < 1,000`.
Consider trying all possible values for `x` and `y`!
*Hint: The mod function might be useful here! The mod function can be used to calculate the remainder.
For instance, `500 % 6` returns the remainder when 500 is divided by 6.*

4. Test your `encode` and `decode` functions to
make sure they work. Note that the `encode` function changes your input to make sure that it's prime. Thus, if your original input was not prime, `decode(encode(x, y))`, might not return
the original values of `x` and `y`. So, in `encode`, add a print statement, to print the values of `x` and `y` after the incrementing is finished. These values, `x'` and `y'` should be returned when `decode(encode(x, y))` is run.
