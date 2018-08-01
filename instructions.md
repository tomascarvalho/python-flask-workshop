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

### 2 - Python Syntax and Indentation
#### 2.1 - Variables
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

### 2.2 - Conditional Statements
