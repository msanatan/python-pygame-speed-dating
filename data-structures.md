# Data Structures

We know how to use variables to store values. And so far our examples have been
pretty small and well contained. What if we need to store 1,000 sets of data...
are we really going to make 1,000 variables? We should never have to. Python 
and other programming languages caters for this and for other scenarios with a
variety of **data structures** - methods for storing data in a computer
in an organised fashion.

## List
Well, the name kind of gave it away. In Python we use lists to store an
ordered sequence of items.

```python
# A list of items are enclosed by square brackets
# Each item is separated by a comma
# And that's right, a variable can store a list just like it can for 
# strings, numbers or booleans
face = ['eyes', 'nose', 'ears', 'mouth']

# List of numbers
favourite_numbers = [3, 42, 69, 7]

# Yes, any kind of number
more_numbers = [4.5, 2, 10.823]

# Empty list
nothing = []

# No limitation, mix and match
random_variable = 24 / 3
random_list = ['hill', 12, 'c', random_variable]

# Lists can be stored inside, you guessed it, lists!
listception = ['bob', ['damian', 'junior', 'stephen', 3], 9, 'rita', [67]]
```

It's quite easy to make lists. It's also very easy to get an item from a list.
Recall that lists are an **ordered** sequence of items. To get an item from a 
list, we can use the item's index - the position of a list item.

```python
# Let's take the face variable from before
face = ['eyes', 'nose', 'ears', 'mouth']

# The position of a list starts from 0
# All we simply do is use the variable, put square brackets in front and then
# put the index inside of the square brackets
face[0] # First item, 'eyes'
face[1] # Second item, 'nose'
face[2] # Third item, 'ears'
face[3] # Fourth item, 'mouth'
```

As you've noticed, the last item is one less than the length of the list. Let's
say you didn't create the list, how would know it's length? Use the `len`
function

```python
len(face)       # 4
len([5,False])  # 2
len([])         # 0
```

Let's go back to more list indices

```python
favourite_numbers = [3, 42, 69, 7]
favourite_numbers[2] # Third item, 69
# Remember, the index starts at 0!

# How do we get 'stephen'?
# Simple, first get the list containing the Marleys - 2nd item of listception
# Then get the the 3rd of item of that list
listception = ['bob', ['damian', 'junior', 'stephen', 3], 9, 'rita', [67]]
listception[1][2]

# To get the last item use the last index.
# A list with 5 items has indices: 0, 1, 2, 3, 4
listception[4] # [67]
# To get the actual number you do the following
listception[4][0] # 67

# Have a little more fun with len before you go
len(listception) # 5 - ['bob', ['damian', 'junior', 'stephen', 3], 9, 'rita', [67]]
len(listception[1]) # 4 - ['damian', 'junior', 'stephen', 3]
```

### Lists and If Statements

### Exercises 1

## Tuples

### Exercises 2

## Dictionaries

### Exercises 3
