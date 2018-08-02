# Pyhton Intro

This branch will cover the Python Intro part of the workshop.

## What is Python
Python is an high-level object-oriented programming language.
The philosophy of Python can be seen in your Python interpreter if you run `import this`:

    >>> import this
    The Zen of Python, by Tim Peters

    Beautiful is better than ugly.
    Explicit is better than implicit.
    Simple is better than complex.
    Complex is better than complicated.
    Flat is better than nested.
    Sparse is better than dense.
    Readability counts.
    Special cases aren't special enough to break the rules.
    Although practicality beats purity.
    Errors should never pass silently.
    Unless explicitly silenced.
    In the face of ambiguity, refuse the temptation to guess.
    There should be one-- and preferably only one --obvious way to do it.
    Although that way may not be obvious at first unless you're Dutch.
    Now is better than never.
    Although never is often better than *right* now.
    If the implementation is hard to explain, it's a bad idea.
    If the implementation is easy to explain, it may be a good idea.
    Namespaces are one honking great idea -- let's do more of those!

## Workshop

### 1 - Documentation
Python 3 documentation can be found [here](https://docs.python.org/3/).
This is your best reference for when you're developing with Python.

As Python is a mature programming language with millions of users worldwide, a simple Google search will also help you when you're stuck.
StackOverflow is probably your best friend (after the docs).

In the following examples Python interpreter will be used, which can be started by writing `python` in the command line.

### 2 - Python Syntax and Indentation
#### 2.1 - Variables
Docs: https://docs.python.org/3/tutorial/introduction.html#

Note: Variable and function names should be written in `lower_case_with_underscores`.

Python is dynamically typed, which means that you don't have to declare what type each variable is.
So, lets imagine that you want to assign the value `10` to the variable `a`, you simply type:

    a = 10
    b = 5
    a = b * 2
    a = b + b
    b += b
    a = b # how much is a now?

If you want to assign a string or other data type:

    a = 'some string'           # you can use single quotes
    a = "some string"           # but you can also use double quotes
    a = 'let\'s dance'          # you can escape a quote with a backslash
    a = "let's dance"           # this works too
    a = ['string1', 'string2']  # a list of strings
    pizza = True                # a boolean - notice the capital 'T'
    broccoli = False            # another boolean - again, notice the capital 'F'


Notice that there is no `;` after the assignment. Python does not use semi-colons.

Also notice that an inline comment in Python starts with an `#`

### 2.2 - Control Flow

#### 2.2.1 - If, Elif, Else
Docs: https://docs.python.org/3/tutorial/controlflow.html#if-statements

In Python, control flow statements are defined similarly to the other languages:

    lunch = input("Insert today's lunch: ") # we ask the user for an input
    if lunch == 'pizza':                    # if lunch equals pizza
        print('Yey!')                       # a print
    elif lunch == 'francesinha':            # else if lunch equals francesinha
        print('Nice!')
    else:                                   # else (if lunch is anything else)
        print('Meh...')

Notice that we do not use brackets (`{}`) in Python. So how does the compiler knows which block of code belongs where?
By using *Indentation*.

Although Indentation should be used in all languages, in order to improve readability, in Python it is obligatory.
Four spaces should be used to indent code in Python. (Docs: https://docs.python.org/3/tutorial/controlflow.html#intermezzo-coding-style)

#### 2.2.2 - Cycles
Docs: https://docs.python.org/3/tutorial/controlflow.html#for-statements

Cycles, especially `for` cycles are easy to use in Python.
There are two ways of using a `for` cycle in Python.

The _traditional_ `for` cycle:

    for i in range(0,10):       # similar to C or Java -> for (i = 0; i < 10; i++)
        print(i)

This is the same as:

    for i in range(10):
        print (i)

The `range` function can take the following arguments:

    range(stop)                 # where we only define the stop
    range(start, stop, [step])  # where step is optional

An example using step:

    for i in range(0, 10, 2):   # prints only even numbers
        print(i)

Docs: https://docs.python.org/3/library/stdtypes.html#range

The `for in` cycle:

    for letter in 'word':       # prints every char in 'word'
        print(letter)

    fruits = ['banana', 'strawberry', 'pineapple']
    for fruit in fruits:        # prints each element of the list followed by its length
        print(fruit, len(fruit))



#### 2.2.3 - Functions
Docs: https://docs.python.org/3/tutorial/controlflow.html#defining-functions

In Python a function starts with the `keyword` `def`, which stands for _definition_:

    def main():
        pass # this does nothing

The `keyword` is followed by the function name, which in the above example is `main`.
Following the function name, arguments are passed to the function inside the parenthesis.

So if we want to create a function called `sum` which sums two given numbers:

    def sum(a, b):
        return a + b

To call a function:

    def main():
        a = int(input('Number a: '))
        b = int(input('Number b: '))
        print(sum(a, b))

    main()

#### 2.2.4 - Python Classes
Docs: https://docs.python.org/3/tutorial/classes.html

Creating a new class creates a new type of object, allowing new instances of that type to be made.
The simplest form of class definition looks like this:

    class ClassName:
        <statement-1>
        .
        .
        .
        <statement-N>

Note how `ClassName` is in `CamelCase`. Class names in Python should be written in `CamelCase`.

Class instantiation uses function notation. Just pretend that the class object is a parameterless function that returns a new instance of the class. For example (assuming the above class):

    x = MyClass()

 Many classes like to create objects with instances customized to a specific initial state. Therefore a class may define a special method named `__init__()`, like this:

    class User:
        def __init__(self, user_name, email):
            self.user_name = user_name
            self.email = email



### 3 - Running a Python program
The latest examples where shown using the Python interpreter.
But what if we want to save our program and call it later whenever we need?

We just need to create a file with the `.py` extension, such as `<my_file>.py`.
Inside the file we should have a `main` method:

    def main():
        # Your code goes in here

    if __name__ == '__main__':
        main()

`__ name__ == '__main__'` will make sure that the code/statements present inside this block will run only when we execute this file directly, instead if we import this as module in another python file then we can call the function defined in it and also the block whichever is present inside the `__ name__ == '__main__'` will not get executed.

More info in docs: https://docs.python.org/3/tutorial/modules.html

Finally, to run your program simple write `python <my_file>.py` on your command line.
