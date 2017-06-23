# python-refresh
Quick crash course over basic Python 3 language features in preparation for
ClickToStart's Programming course. You should take some time and go over the 
official Python tutorial https://docs.python.org/3/tutorial/, this is just to
quickly go through core features you should be familiar with. These notes were
greatly inspired by [University of Edinburgh Informatics lab
notes](http://www.inf.ed.ac.uk/teaching/courses/inf2a/tutorials/2016_inf2a_P01_exercises.pdf).

The code we are writing here would work on all of Python 3 versions (and the 
vast majority on Python 2 as well) But you should use version 3.6 as it's the 
latest and greatest at the time of writing.

# Interpreted or Compiled?
Python is a programming language, a formal language specification designed to 
give instructions to a computer. The Python language has many implementations: 
* CPython: the reference implementation for Python, and the one you probably
installed from the main website. CPython is an interpreter, but it first
compiles the Python source code to an intermediary byte code. The byte code is
what's interpreted.
* PyPy: a Python interpreter built with Python itself (a subset of Python to be
technical). It does [Just-in-Time
Compilation](https://en.wikipedia.org/wiki/Just-in-time_compilation) and is 
known to be quicker than CPython in many cases.
* Jython: Python which runs on the JVM
* IronPython: Python which runs on .NET framework and Mono

# Mind Your Space
Whitespace is important in Python. If you come from a language background with
brackets and the like, welcome to The Light! Indentation determines scope. For
indentation we'll be use 4 spaces as guided by
[PEP-8](https://www.python.org/dev/peps/pep-0008/).

# Numbers
The usual operators you've seen in Java/C/etc are all here as well:
+, -, *, /, %. Run Python on your shell `python3` and type the following:

```python    
5 + 3 # = 8
2 * 8 # = 16
3 / 2 # = 1.5
10 - 9 # = 1
13 % 3 # = 1

# You also figured that comments begin with # and go till the end of the line
# Note the division in of 3/2 returns 1.5. If you used Python 2 that division
# would return 1 as the numbers weren't explicitly floats. No need to worry 
# about that in version 3 :)

# To get that division that also floors the result do like the following
3 // 2 # = 1

# In Python, exponents use **
2**5 # = 32
```

# Strings
Strings can be represented with either single or double quotes


```python
'hi there'
"doing ok"
'what a horrible, invalid string!" # This wouldn't work
# The important thing is to be consistent. Pick one and keep up with it!

# You can concatenate strings with the plus sign
'hello ' + 'world' # hello world

# You can also repeat a string with the multiply sign
'Nana ' * 4 + 'Batman!'
```

Some strings are really long. Actually, it's common Python convention to put a 
long string immediately after the first line of a module, function, class or
method definition. Long strings are used as docstring

```python
'''
Roses are red
Violets are blue
Doubles with mango is sweet
But not as good as you
'''
# Do not recite the above lines to someone else please...
"""
Docstrings normally use double quotes.
We'll maintain that convention for this course
"""
```

# Booleans
Python has two boolean values: True and False. Booleans inherit from integers,
so you can add and multiply them like numbers. True is 1 and False is 0

```python
True + True # = 2
True * 7 # = 7
False - 5 # 0
```

## Conditions
Well Booleans aren't fun for additions and other mathematical operators. We use
them to test for truthfullness. Or truthiness. Truth. We can write expressions
which evaluate to True or False:

```python
True and True # = True, using and is much easier than && right?
True or False # = True, more English words please
not True # = False
```

We can do comparisons on other Data Types as well

```python
8 == 2 * 4 # = True, == test equality, strings can be tested as well
'hi' == "  hi\t".strip() # strip function removes whitespace characters

2**7 != 64 # = True, test inequality

# Greater than or less than
4 > 2
19 < 19.5

# Greater/less than or equal to
23 >= 23
-42 <= -37

# Python also has "is". People use it interchangeably with == but that's not
# entirely correct. The is keyword checks if the two things being compared 
# points to the same object. == checks if two values being referenced have the
# same value
1000 is 10**3 # False
1000  == 10**3 # True
# Python caches small numerical and string objects, so is can work for some
# values. Be wary as many a bad bugs can arise as a result
```
In addition to the docs, you can read this about is:
https://stackoverflow.com/questions/132988/is-there-a-difference-between-and-is-in-python

# Lists
Lists are awesome containers for storing a variety of objects

```python
things_guaranteed_in_life = ['death', 'taxes', 'a new fifa game every year']

# You can add an item to a list by the append method
things_guaranteed_in_life.append('another transformers movie')

# You can extend the list with another list via plus
things_guaranteed_in_life + ['call of duty']
# Note that the above doesn't change the list contents, if you want it saved
# then you'll have to assign a variable to that value
things_guaranteed_in_life = things_guaranteed_in_life + ['call of duty']
# Or for brevity's sake
things_guaranteed_in_life += ['call of duty']

# Lists can have multiple data types stored in it
random_list_of_things = [88.9, 'the meaning of life', 42, False]
```

You can access individual elements by a list as follows:
```python
things_guaranteed_in_life[0] # 'death'
things_guaranteed_in_life[3] # 'another transformers movie'

# You can use negative indices to access elements from the right of the list
things_guaranteed_in_life[-1] # 'call of duty'
things_guaranteed_in_life[-3] # 'a new fifa game every year'
```

## Fun with Indices

# Tuples

# Dictionaries

# If-Elif-Else

# For loop

# While loop

# List Comprehensions

# Lambda, Map and Filter

# Functions

# Classes and Objects
