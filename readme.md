Exercise 02: Math and functions
=======

Introduction
--------
We're taught mathematical notation using 'infix' notation, that is, the operator goes between the numbers:

    eg: In '3 + 2', the operator, '+', goes between the operands, 3 and 2.

An alternate notation for math is called 'prefix'. As you might have guessed, in prefix notation, the operator goes in front of the operands:

    eg: In prefix notation, the same statement would be written '+ 3 2'

Some advantages of prefix notation include the ability to have an arbitrary number of operands.

    eg: '+ 3 2 1 4 5 6 7' will add up all the numbers.

In this exercise, we will build a basic prefix calculator together. We will provide half of the program, and you will code the other half. We will use this idea to explore the concept of an 'interface'.

In common English, an interface is defined as a surface that is a common boundary between two different things. In computing, the idea is very similar. An interface is the common 'surface' between two pieces of code, and is defined by an agreed-upon set of 'function signatures'.

A function signature is a way of describing a function without going into the details of how it operates. For example, consider the following function:

    def square(x):
        return x * x

If we were to describe this function, we might say "the function named 'square' accepts a single number as an input, and returns a number as output (presumably the square of the input)." This phrase is the function signature. It includes the function name, the number (and type) of inputs, and the type of the output. We can also include a rough description of what the function is _supposed_ to do. More succinctly, we can say:

    square(int) -> int
    Returns the square of the input integer.


Note that it says nothing about how the output integer is produced, nor does it say anything about the correctness of the output. It also doesn't say anything about what arguments to a function should be named.

Why is this useful? Well, when two or more programmers collaborate on a project, it is rare that they can work completely independently of each other. At some point, I will rely on code that you have written, or more likely, you will write in the future. If I waited until you wrote your code, that would delay the project significantly. Instead, we would agree upon an interface, a series of method signatures that my code would use to interact with yours. I would write my code _assuming_ at some point, you will fill in those method signatures with the correct implementation eventually.

One way of thinking about it is like after-market parts for cars. As long as the screws and holes are in the right positions at the right sizes, the pieces can be bolted together even though they come from different manufacturers.


Resources:

    * http://learnpythonthehardway.org/book/ex3.html
    * http://learnpythonthehardway.org/book/ex18.html
    * http://learnpythonthehardway.org/book/ex19.html
    * http://learnpythonthehardway.org/book/ex21.html
    * http://www.learnpython.org/Variables_and_Types
    * http://www.learnpython.org/Functions

Concepts required:
    * functions
    * arithmetic
    * return values


Description
-------
We have provided a program, calculator.pyc that implements a basic prefix calculator. A pyc is a special python file. You can still run the program, but you can't view the original source of the program. Run it with the following command from your shell:

    python calculator.pyc

The calculator lets a user add, subtract, multiply, divide, square a number, cube a number, and find the square root.

Calculator uses the following interface:

    In the file arithmetic.py, these function signatures are required

    add(int, int) -> int
    Returns the sum of the two input integers
    
    subtract(int, int) -> int
    Returns the second number subtracted from the first

    multiply(int, int) -> int
    Multiplies the two inputs together

    divide(int, int) -> float
    Divides the first input by the second, returning a floating point

    square(int) -> int
    Returns the square of the input

    cube(int) -> int
    Returns the cube of the input

    power(int, int) -> int
    Raises the first integer to the power of the second integer and returns the value.

    mod(int, int) -> int
    Returns the remainder when the first integer is divided by the second integer.


A sample session of the calculator looks like this:
    Meringue:math chriszf$ python calculator.pyc
    > + 1 2
    3
    > - 10 5
    5
    > * 2 3
    6
    > / 6 2
    3.000000
    > square 2
    4
    > cube 3
    27
    > pow 2 5
    32
    > mod 10 3
    1
    > q
    Meringue:math chriszf$ 

We have provided a sample arithmetic.py with a function that matches the signature for 'add', although it returns an incorrect value. Your job is to make it return the correct value, then provide the remaining interface.

Try running the program first to understand where and how it fails. Read the error messages, and try to fix it by addressing one error at a time.
