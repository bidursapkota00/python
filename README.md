# Python Complete Course

![Bidur Sapkota](https://www.bidursapkota.com.np/images/gravatar.webp "Bidur Sapkota - Developer")&nbsp;[Bidur Sapkota](https://www.bidursapkota.com.np/)

![Python Complete Course by Bidur Sapkota](/images/12-python-post-1200.webp "Python Complete Course – Blog by Bidur Sapkota")

## Table of Contents

1. [Numbers and more in Python!](#numbers-and-more-in-python)
2. [Variable](#variable)
3. [Strings](#strings)
4. [String Formatting](#string-formatting)
5. [Lists](#lists)
6. [Dictionaries](#dictionaries)
7. [Tuples](#tuples)
8. [Set and Booleans](#set-and-booleans)
9. [Files](#files)
10. [Test your knowledge](#test-your-knowledge)

# Numbers and more in Python!

## Types of numbers

Python has various "types" of numbers (numeric literals). We'll mainly focus on integers and floating point numbers.

Integers are just whole numbers, positive or negative. For example: 2 and -2 are examples of integers.

Floating point numbers in Python are notable because they have a decimal point in them, or use an exponential (e) to define the number. For example 2.0 and -2.1 are examples of floating point numbers. 4E2 (4 times 10 to the power of 2) is also an example of a floating point number in Python.

Throughout this course we will be mainly working with integers or simple float number types.

Here is a table of the two main types we will spend most of our time working with some examples:

<table>
<tr>
    <th>Examples</th> 
    <th>Number "Type"</th>
</tr>

<tr>
    <td>1,2,-5,1000</td>
    <td>Integers</td> 
</tr>

<tr>
    <td>1.2,-0.5,2e2,3E2</td> 
    <td>Floating-point numbers</td> 
</tr>
 </table>

Now let's start with some basic arithmetic.

### Basic Arithmetic

```python
# Addition
2+1
# 3
```

```python
# Subtraction
2-1
# 1
```

```python
# Multiplication
2*2
# 4
```

```python
# Division
3/2
# 1.5
```

```python
# Floor Division
7//4
# 1
```

**Whoa! What just happened? Last time I checked, 7 divided by 4 equals 1.75 not 1!**

The reason we get this result is because we are using "_floor_" division. The // operator (two forward slashes) truncates the decimal without rounding, and returns an integer result.

**So what if we just want the remainder after division?**

```python
# Modulo
7%4
# 3
```

4 goes into 7 once, with a remainder of 3. The % operator returns the remainder after division.

### Arithmetic continued

```python
# Powers
2**3
# 8
```

```python
# Can also do roots this way
4**0.5
# 2.0
```

```python
# Order of Operations followed in Python
2 + 10 * 10 + 3
# 105
```

```python
# Can use parentheses to specify orders
(2+10) * (10+3)
# 156
```

---

---

---

# Variable

## Rules for variable names

- names can not start with a number
- names can not contain spaces, use \_ intead
- names can not contain any of these symbols: `:'",<>/?|\!@#%^&*~-+`
- it's considered best practice ([PEP8](https://www.python.org/dev/peps/pep-0008/#function-and-variable-names)) that names are lowercase with underscores
- avoid using Python built-in keywords like `list` and `str`
- avoid using the single characters `l` (lowercase letter el), `O` (uppercase letter oh) and `I` (uppercase letter eye) as they can be confused with `1` and `0`

## Dynamic Typing

Python uses _dynamic typing_, meaning you can reassign variables to different data types. This makes Python very flexible in assigning data types; it differs from other languages that are _statically typed_.

```python
my_dogs = 2
my_dogs = ['Sammy', 'Frankie']
```

### Pros and Cons of Dynamic Typing

#### Pros of Dynamic Typing

- very easy to work with
- faster development time

#### Cons of Dynamic Typing

- may result in unexpected bugs!
- you need to be aware of `type()`

## Assigning Variables

Variable assignment follows `name = object`, where a single equals sign `=` is an _assignment operator_

```python
a = 5
```

Here we assigned the integer object `5` to the variable name `a`.<br>Let's assign `a` to something else:

```python
a = 10
```

You can now use `a` in place of the number `10`:

```python
a + a
# 20
```

## Reassigning Variables

Python lets you reassign variables with a reference to the same object.

```python
a = a + 10
# 20
```

There's actually a shortcut for this. Python lets you add, subtract, multiply and divide numbers with reassignment using `+=`, `-=`, `*=`, and `/=`.

```python
a += 10
# 30
```

```python
a *= 2
# 60
```

## Determining variable type with `type()`

You can check what type of object is assigned to a variable using Python's built-in `type()` function. Common data types include:

- **int** (for integer)
- **float**
- **str** (for string)
- **list**
- **tuple**
- **dict** (for dictionary)
- **set**
- **bool** (for Boolean True/False)

```python
type(a)
# int

a = (1,2)
type(a)
# tuple
```

## Simple Exercise

This shows how variables make calculations more readable and easier to follow.

```python
my_income = 100
tax_rate = 0.1
my_taxes = my_income * tax_rate
my_taxes
# 10.0
```

---

---

---

# Strings

Strings are used in Python to record text information, such as names. Strings in Python are actually a _sequence_, which basically means Python keeps track of every element in the string as a sequence. For example, Python understands the string "hello' to be a sequence of letters in a specific order. This means we will be able to use indexing to grab particular letters (like the first letter, or the last letter).

This idea of a sequence is an important one in Python and we will touch upon it later on in the future.

## Creating a String

To create a string in Python you need to use either single quotes or double quotes. For example:

```python
# Single word
'hello'
# 'hello'
```

```python
# Entire phrase
'This is also a string'
# 'This is also a string'
```

```python
# We can also use double quote
"String built with double quotes"
# 'String built with double quotes'
```

```python
# Be careful with quotes!
' I'm using single quotes, but this will create an error'
```

**Output:**

```text
line 2
    ' I'm using single quotes, but this will create an error'
        ^
SyntaxError: invalid syntax
```

The reason for the error above is because the single quote in <code>I'm</code> stopped the string. You can use combinations of double and single quotes to get the complete statement.

```python
"Now I'm ready to use the single quotes inside a string!"
# "Now I'm ready to use the single quotes inside a string!"
```

## Printing a String

Using terminal with just a string in a command will automatically output strings, but the correct way to display strings in your output is by using a print function.

```python
# We can simply declare a string
'Hello World'
# 'Hello World'
```

We can use a print statement to print a string.

```python
print('Hello World 1')
print('Hello World 2')
print('Use \n to print a new line')
print('\n')
print('See what I mean?')
```

**Output:**

```text
Hello World 1
Hello World 2
Use
 to print a new line


See what I mean?
```

## String Basics

We can also use a function called len() to check the length of a string!

```python
len('Hello World')
# 11
```

Python's built-in len() function counts all of the characters in the string, including spaces and punctuation.

## String Indexing

We know strings are a sequence, which means Python can use indexes to call parts of the sequence. Let's learn how this works.

In Python, we use brackets <code>[]</code> after an object to call its index. We should also note that indexing starts at 0 for Python. Let's create a new object called <code>s</code> and then walk through a few examples of indexing.

```python
# Assign s as a string
s = 'Hello World'
```

Let's start indexing!

```python
# Show first element (in this case a letter)
s[0]
# 'H'

s[1]
# 'e'

s[2]
# 'l'
```

We can use a <code>:</code> to perform _slicing_ which grabs everything up to a designated point. For example:

```python
# Grab everything past the first term all the way to the length of s which is len(s)
s[1:]
# 'ello World'
```

```python
# Note that there is no change to the original s
s
# 'Hello World'
```

```python
# Grab everything UP TO the 3rd index
s[:3]
# 'Hel'
```

Note the above slicing. Here we're telling Python to grab everything from 0 up to 3. It doesn't include the 3rd index. You'll notice this a lot in Python, where statements and are usually in the context of "up to, but not including".

```python
#Everything
s[:]
# 'Hello World'
```

We can also use negative indexing to go backwards.

```python
# Last letter (one index behind 0 so it loops back around)
s[-1]
# 'd'
```

```python
# Grab everything but the last letter
s[:-1]
# 'Hello Worl'
```

We can also use index and slice notation to grab elements of a sequence by a specified step size (the default is 1). For instance we can use two colons in a row and then a number specifying the frequency to grab elements. For example:

```python
# Grab everything, but go in steps size of 1
s[::1]
# 'Hello World'
```

```python
# Grab everything, but go in step sizes of 2
s[::2]
# 'HloWrd'
```

```python
# We can use this to print a string backwards
s[::-1]
# 'dlroW olleH'
```

## String Properties

It's important to note that strings have an important property known as _immutability_. This means that once a string is created, the elements within it can not be changed or replaced. For example:

```python
# Let's try to change the first letter to 'x'
s[0] = 'x'
```

**Output:**

```text
----> 2 s[0] = 'x'

TypeError: 'str' object does not support item assignment
```

Notice how the error tells us directly what we can't do, change the item assignment!

Something we _can_ do is concatenate strings!

```python
# Concatenate strings!
s + ' concatenate me!'
# 'Hello World concatenate me!'
```

```python
# We can reassign s completely though!
s = s + ' concatenate me!'
print(s)
# Hello World concatenate me!
```

We can use the multiplication symbol to create repetition!

```python
letter = 'z'
```

```python
letter*10
# 'zzzzzzzzzz'
```

## Basic Built-in String methods

Objects in Python usually have built-in methods. These methods are functions inside the object (we will learn about these in much more depth later) that can perform actions or commands on the object itself.

We call methods with a period and then the method name. Methods are in the form:

object.method(parameters)

Where parameters are extra arguments we can pass into the method. Don't worry if the details don't make 100% sense right now. Later on we will be creating our own objects and functions!

Here are some examples of built-in methods in strings:

```python
# Upper Case a string
s.upper()
# 'HELLO WORLD CONCATENATE ME!'
```

```python
# Lower case
s.lower()
# 'hello world concatenate me!'
```

```python
# Split a string by blank space (this is the default)
s.split()
# ['Hello', 'World', 'concatenate', 'me!']
```

```python
# Split by a specific element (doesn't include the element that was split on)
s.split('W')
# ['Hello ', 'orld concatenate me!']
```

There are many more methods than the ones covered here. Visit the Advanced String section to find out more!

## Print Formatting

We can use the .format() method to add formatted objects to printed string statements.

The easiest way to show this is through an example:

```python
'Insert another string with curly brackets: {}'.format('The inserted string')
# 'Insert another string with curly brackets: The inserted string'
```

---

---

---

# String Formatting

String formatting lets you inject items into a string rather than trying to chain items together using commas or string concatenation. As a quick comparison, consider:

```python
player = 'Thomas'
points = 33

'Last night, '+player+' scored '+str(points)+' points.'  # concatenation

f'Last night, {player} scored {points} points.'          # string formatting
```

There are three ways to perform string formatting.

- The oldest method involves placeholders using the modulo `%` character.
- An improved technique uses the `.format()` string method.
- The newest method, introduced with Python 3.6, uses formatted string literals, called _f-strings_.

Since you will likely encounter all three versions in someone else's code, we describe each of them here.

## Formatting with placeholders

You can use <code>%s</code> to inject strings into your print statements. The modulo `%` is referred to as a "string formatting operator".

```python
print("I'm going to inject %s here." %'something')
# I'm going to inject something here.
```

You can pass multiple items by placing them inside a tuple after the `%` operator.

```python
print("I'm going to inject %s text here, and %s text here." %('some','more'))
# I'm going to inject some text here, and more text here.
```

You can also pass variable names:

```python
x, y = 'some', 'more'
print("I'm going to inject %s text here, and %s text here."%(x,y))
# I'm going to inject some text here, and more text here.
```

### Format conversion methods.

It should be noted that two methods <code>%s</code> and <code>%r</code> convert any python object to a string using two separate methods: `str()` and `repr()`. We will learn more about these functions later on in the course, but you should note that `%r` and `repr()` deliver the _string representation_ of the object, including quotation marks and any escape characters.

```python
print('He said his name was %s.' %'Fred')
# He said his name was Fred.
print('He said his name was %r.' %'Fred')
# He said his name was 'Fred'.
```

As another example, `\t` inserts a tab into a string.

```python
print('I once caught a fish %s.' %'this \tbig')
# I once caught a fish this 	big.
print('I once caught a fish %r.' %'this \tbig')
# I once caught a fish 'this \tbig'.
```

The `%s` operator converts whatever it sees into a string, including integers and floats. The `%d` operator converts numbers to integers first, without rounding. Note the difference below:

```python
print('I wrote %s programs today.' %3.75)
# I wrote 3.75 programs today.
print('I wrote %d programs today.' %3.75)
# I wrote 3 programs today.
```

### Padding and Precision of Floating Point Numbers

Floating point numbers use the format <code>%5.2f</code>. Here, <code>5</code> would be the minimum number of characters the string should contain; these may be padded with whitespace if the entire number does not have this many digits. Next to this, <code>.2f</code> stands for how many numbers to show past the decimal point. Let's see some examples:

```python
print('Floating point numbers: %5.2f' %(13.144))
# Floating point numbers: 13.14
print('Floating point numbers: %1.0f' %(13.144))
# Floating point numbers: 13
print('Floating point numbers: %1.5f' %(13.144))
# Floating point numbers: 13.14400
print('Floating point numbers: %10.2f' %(13.144))
# Floating point numbers:      13.14
print('Floating point numbers: %25.2f' %(13.144))
# Floating point numbers:                     13.14
```

For more information on string formatting with placeholders visit `https://docs.python.org/3/library/stdtypes.html#old-string-formatting`

### Multiple Formatting

Nothing prohibits using more than one conversion tool in the same print statement:

```python
print('First: %s, Second: %5.2f, Third: %r' %('hi!',3.1415,'bye!'))
# First: hi!, Second:  3.14, Third: 'bye!'
```

## Formatting with the `.format()` method

A better way to format objects into your strings for print statements is with the string `.format()` method. The syntax is:

```python
'String here {} then also {}'.format('something1','something2')
```

For example:

```python
print('This is a string with an {}'.format('insert'))
# This is a string with an insert
```

### The .format() method has several advantages over the %s placeholder method:

#### 1. Inserted objects can be called by index position:

```python
print('The {2} {1} {0}'.format('fox','brown','quick'))
# The quick brown fox
```

#### 2. Inserted objects can be assigned keywords:

```python
print('First Object: {a}, Second Object: {b}, Third Object: {c}'.format(a=1,b='Two',c=12.3))
# First Object: 1, Second Object: Two, Third Object: 12.3
```

#### 3. Inserted objects can be reused, avoiding duplication:

```python
print('A %s saved is a %s earned.' %('penny','penny'))
# A penny saved is a penny earned.

# vs.

print('A {p} saved is a {p} earned.'.format(p='penny'))
# A penny saved is a penny earned.
```

### Alignment, padding and precision with `.format()`

Within the curly braces you can assign field lengths, left/right alignments, rounding parameters and more

```python
print('{0:8} | {1:9}'.format('Fruit', 'Quantity'))
print('{0:8} | {1:9}'.format('Apples', 3.))
print('{0:8} | {1:9}'.format('Oranges', 10))
```

**Output:**

```text
Fruit    | Quantity
Apples   |       3.0
Oranges  |        10
```

By default, `.format()` aligns text to the left, numbers to the right. You can pass an optional `<`,`^`, or `>` to set a left, center or right alignment:

```python
print('{0:<8} | {1:^8} | {2:>8}'.format('Left','Center','Right'))
print('{0:<8} | {1:^8} | {2:>8}'.format(11,22,33))
```

**Output:**

```text
Left     |  Center  |    Right
11       |    22    |       33
```

You can precede the aligment operator with a padding character

```python
print('{0:=<8} | {1:-^8} | {2:.>8}'.format('Left','Center','Right'))
print('{0:=<8} | {1:-^8} | {2:.>8}'.format(11,22,33))
```

**Output:**

```text
Left==== | -Center- | ...Right
11====== | ---22--- | ......33
```

Field widths and float precision are handled in a way similar to placeholders. The following two print statements are equivalent:

```python
print('This is my ten-character, two-decimal number:%10.2f' %13.579)
# This is my ten-character, two-decimal number:     13.58
print('This is my ten-character, two-decimal number:{0:10.2f}'.format(13.579))
# This is my ten-character, two-decimal number:     13.58
```

Note that there are 5 spaces following the colon, and 5 characters taken up by 13.58, for a total of ten characters.

For more information on the string `.format()` method visit `https://docs.python.org/3/library/string.html#formatstrings`

## Formatted String Literals (f-strings)

Introduced in Python 3.6, f-strings offer several benefits over the older `.format()` string method described above. For one, you can bring outside variables immediately into to the string rather than pass them as arguments through `.format(var)`.

```python
name = 'Fred'

print(f"He said his name is {name}.")
# He said his name is Fred.
```

Pass `!r` to get the string representation:

```python
print(f"He said his name is {name!r}")
# He said his name is 'Fred'
```

#### Float formatting follows `"result: {value:{width}.{precision}}"`

Where with the `.format()` method you might see `{value:10.4f}`, with f-strings this can become `{value:{10}.{6}}`

```python
num = 23.45678
print("My 10 character, four decimal number is:{0:10.4f}".format(num))
# My 10 character, four decimal number is:   23.4568
print(f"My 10 character, four decimal number is:{num:{10}.{6}}")
# My 10 character, four decimal number is:   23.4568
```

Note that with f-strings, _precision_ refers to the total number of digits, not just those following the decimal. This fits more closely with scientific notation and statistical analysis. Unfortunately, f-strings do not pad to the right of the decimal, even if precision allows it:

```python
num = 23.45
print("My 10 character, four decimal number is:{0:10.4f}".format(num))
# My 10 character, four decimal number is:   23.4500
print(f"My 10 character, four decimal number is:{num:{10}.{6}}")
# My 10 character, four decimal number is:     23.45
```

If this becomes important, you can always use `.format()` method syntax inside an f-string:

```python
num = 23.45
print("My 10 character, four decimal number is:{0:10.4f}".format(num))
# My 10 character, four decimal number is:   23.4500
print(f"My 10 character, four decimal number is:{num:10.4f}")
# My 10 character, four decimal number is:   23.4500
```

For more info on formatted string literals visit `https://docs.python.org/3/reference/lexical_analysis.html#f-strings`

That is the basics of string formatting!

---

---

---

# Lists

Earlier when discussing strings we introduced the concept of a _sequence_ in Python. Lists can be thought of the most general version of a _sequence_ in Python. Unlike strings, they are mutable, meaning the elements inside a list can be changed!

Lists are constructed with brackets [] and commas separating every element in the list.

Let's go ahead and see how we can construct lists!

```python
# Assign a list to an variable named my_list
my_list = [1,2,3]
```

We just created a list of integers, but lists can actually hold different object types. For example:

```python
my_list = ['A string',23,100.232,'o']
```

Just like strings, the len() function will tell you how many items are in the sequence of the list.

```python
len(my_list)
# 4
```

### Indexing and Slicing

Indexing and slicing work just like in strings. Let's make a new list to remind ourselves of how this works:

```python
my_list = ['one','two','three',4,5]
```

```python
# Grab element at index 0
my_list[0]
# 'one'
```

```python
# Grab index 1 and everything past it
my_list[1:]
# ['two', 'three', 4, 5]
```

```python
# Grab everything UP TO index 3
my_list[:3]
# ['one', 'two', 'three']
```

We can also use + to concatenate lists, just like we did for strings.

```python
my_list + ['new item']
# ['one', 'two', 'three', 4, 5, 'new item']
```

Note: This doesn't actually change the original list!

```python
my_list
# ['one', 'two', 'three', 4, 5]
```

You would have to reassign the list to make the change permanent.

```python
# Reassign
my_list = my_list + ['add new item permanently']
# ['one', 'two', 'three', 4, 5, 'add new item permanently']
```

We can also use the \* for a duplication method similar to strings:

```python
# Make the list double
my_list * 2
```

**Output:**

```python
    ['one',
     'two',
     'three',
     4,
     5,
     'add new item permanently',
     'one',
     'two',
     'three',
     4,
     5,
     'add new item permanently']
```

```python
# Again doubling not permanent
my_list
# ['one', 'two', 'three', 4, 5, 'add new item permanently']
```

## Basic List Methods

If you are familiar with another programming language, you might start to draw parallels between arrays in another language and lists in Python. Lists in Python however, tend to be more flexible than arrays in other languages for a two good reasons: they have no fixed size (meaning we don't have to specify how big a list will be), and they have no fixed type constraint (like we've seen above).

Let's go ahead and explore some more special methods for lists:

```python
# Create a new list
list1 = [1,2,3]
```

Use the **append** method to permanently add an item to the end of a list:

```python
# Append
list1.append('append me!')
# [1, 2, 3, 'append me!']
```

Use the **insert** method to permanently add an item at any position of a list:

```python
# Insert 34 at index = 1
list1.insert(1, 34)
# [1, 34, 2, 3, 'append me!']
```

Use **pop** to "pop off" an item from the list. By default pop takes off the last index, but you can also specify which index to pop off. Let's see an example:

```python
# Pop off the 0 indexed item
list1.pop(0)
# 1
```

```python
# Show
list1
# [2, 3, 'append me!']
```

```python
# Assign the popped element, remember default popped index is -1
popped_item = list1.pop()
# 'append me!'
```

```python
# Show remaining list
list1
# [2, 3]
```

It should also be noted that lists indexing will return an error if there is no element at that index. For example:

```python
list1[100]
```

**Output:**

```text
---------------------------------------------------------------------------

IndexError                            Traceback (most recent call last)

----> 1 list1[100]


IndexError: list index out of range
```

We can use the **sort** method and the **reverse** methods to also effect your lists:

```python
new_list = ['a','e','x','b','c']
```

```python
# Use reverse to reverse order (this is permanent!)
new_list.reverse()
# ['c', 'b', 'x', 'e', 'a']  // permanent
```

```python
# Use sort to sort the list (in this case alphabetical order, but for numbers it will go ascending)
new_list.sort()
# ['a', 'b', 'c', 'e', 'x']  // permanent
```

```python
# Sort in descending order
new_list.sort(reverse=True)
# ['x', 'e', 'c', 'b', 'a']  // permanent
```

## Nesting Lists

A great feature of of Python data structures is that they support _nesting_. This means we can have data structures within data structures. For example: A list inside a list.

Let's see how this works!

```python
# Let's make three lists
lst_1=[1,2,3]
lst_2=[4,5,6]
lst_3=[7,8,9]

# Make a list of lists to form a matrix
matrix = [lst_1,lst_2,lst_3]
# [[1, 2, 3], [4, 5, 6], [7, 8, 9]]
```

We can again use indexing to grab elements, but now there are two levels for the index. The items in the matrix object, and then the items inside that list!

```python
# Grab first item in matrix object
matrix[0]
# [1, 2, 3]
```

```python
# Grab first item of the first item in the matrix object
matrix[0][0]
# 1
```

# List Comprehensions

Python has an advanced feature called list comprehensions. They allow for quick construction of lists. To fully understand list comprehensions we need to understand for loops. So don't worry if you don't completely understand this section, and feel free to just skip it since we will return to this topic later.

But in case you want to know now, here are a few examples!

```python
# Build a list comprehension by deconstructing a for loop within a []
first_col = [row[0] for row in matrix]
# [1, 4, 7]
```

---

---

---

# Dictionaries

We've been learning about _sequences_ in Python but now we're going to switch gears and learn about _mappings_ in Python. If you're familiar with other languages you can think of these Dictionaries as hash tables.

So what are mappings? Mappings are a collection of objects that are stored by a _key_, unlike a sequence that stored objects by their relative position. This is an important distinction, since mappings won't retain order since they have objects defined by a key.

A Python dictionary consists of a key and then an associated value. That value can be almost any Python object.

## Constructing a Dictionary

Let's see how we can construct dictionaries to get a better understanding of how they work!

```python
# Make a dictionary with {} and : to signify a key and a value
my_dict = {'key1':'value1','key2':'value2'}
```

```python
# Call values by their key
my_dict['key2']
# 'value2'
```

Its important to note that dictionaries are very flexible in the data types they can hold. For example:

```python
my_dict = {'key1':123,'key2':[12,23,33],'key3':['item0','item1','item2']}
```

```python
# Let's call items from the dictionary
my_dict['key3']
# ['item0', 'item1', 'item2']
```

```python
# Can call an index on that value
my_dict['key3'][0]
# 'item0'
```

```python
# Can then even call methods on that value
my_dict['key3'][0].upper()
# 'ITEM0'
```

We can affect the values of a key as well. For instance:

```python
my_dict['key1']
# 123
```

```python
# Subtract 123 from the value
my_dict['key1'] = my_dict['key1'] - 123
```

```python
#Check
my_dict['key1']
# 0
```

A quick note, Python has a built-in method of doing a self subtraction or addition (or multiplication or division). We could have also used += or -= for the above statement. For example:

```python
# Set the object equal to itself minus 123
my_dict['key1'] -= 123
my_dict['key1']
# -123
```

We can also create keys by assignment. For instance if we started off with an empty dictionary, we could continually add to it:

```python
# Create a new dictionary
d = {}
```

```python
# Create a new key through assignment
d['animal'] = 'Dog'
```

```python
# Can do this with any object
d['answer'] = 42
```

```python
#Show
d
# {'animal': 'Dog', 'answer': 42}
```

## Nesting with Dictionaries

Hopefully you're starting to see how powerful Python is with its flexibility of nesting objects and calling methods on them. Let's see a dictionary nested inside a dictionary:

```python
# Dictionary nested inside a dictionary nested inside a dictionary
d = {'key1':{'nestkey':{'subnestkey':'value'}}}
```

Wow! That's a quite the inception of dictionaries! Let's see how we can grab that value:

```python
# Keep calling the keys
d['key1']['nestkey']['subnestkey']
# 'value'
```

## A few Dictionary Methods

There are a few methods we can call on a dictionary. Let's get a quick introduction to a few of them:

```python
# Create a typical dictionary
d = {'key1':1,'key2':2,'key3':3}
```

```python
# Method to return a list of all keys
d.keys()
# dict_keys(['key1', 'key2', 'key3'])
```

```python
# Method to grab all values
d.values()
# dict_values([1, 2, 3])
```

```python
# Method to return tuples of all items  (we'll learn about tuples soon)
d.items()
# dict_items([('key1', 1), ('key2', 2), ('key3', 3)])
```

---

---

---

# Tuples

In Python tuples are very similar to lists, however, unlike lists they are _immutable_ meaning they can not be changed. You would use tuples to present things that shouldn't be changed, such as days of the week, or dates on a calendar.

You'll have an intuition of how to use tuples based on what you've learned about lists. We can treat them very similarly with the major distinction being that tuples are immutable.

## Constructing Tuples

The construction of a tuples use () with elements separated by commas. For example:

```python
# Create a tuple
t = (1,2,3)
```

```python
# Check len just like a list
len(t)
# 3
```

```python
# Can also mix object types
t = ('one',2)

# Show
t
# ('one', 2)
```

```python
# Use indexing just like we did in lists
t[0]
# 'one'
```

```python
# Slicing just like a list
t[-1]
# 2
```

## Basic Tuple Methods

Tuples have built-in methods, but not as many as lists do. Let's look at two of them:

```python
# Use .index to enter a value and return the index
t.index('one')
# 0
```

```python
# Use .count to count the number of times a value appears
t.count('one')
# 1
```

## Immutability

It can't be stressed enough that tuples are immutable. To drive that point home:

```python
t[0]= 'change'
```

**Output:**

```text
----> 1 t[0]= 'change'

TypeError: 'tuple' object does not support item assignment
```

Because of this immutability, tuples can't grow. Once a tuple is made we can not add to it.

```python
t.append('nope')
```

**Output:**

```text
---------------------------------------------------------------------------

AttributeError                            Traceback (most recent call last)

----> 1 t.append('nope')

AttributeError: 'tuple' object has no attribute 'append'
```

## When to use Tuples

You may be wondering, "Why bother using tuples when they have fewer available methods?" To be honest, tuples are not used as often as lists in programming, but are used when immutability is necessary. If in your program you are passing around an object and need to make sure it does not get changed, then a tuple becomes your solution. It provides a convenient source of data integrity.

---

---

---

# Set and Booleans

There are two other object types in Python that we should quickly cover: Sets and Booleans.

## Sets

Sets are an unordered collection of _unique_ elements. We can construct them by using the set() function. Let's go ahead and make a set to see how it works

```python
x = set()
```

```python
# We add to sets with the add() method
x.add(1)
```

```python
#Show
x
# {1}
```

Note the curly brackets. This does not indicate a dictionary! Although you can draw analogies as a set being a dictionary with only keys.

We know that a set has only unique entries. So what happens when we try to add something that is already in a set?

```python
# Add a different element
x.add(2)
```

```python
#Show
x
# {1, 2}
```

```python
# Try to add the same element
x.add(1)
```

```python
#Show
x
# {1, 2}
```

Notice how it won't place another 1 there. That's because a set is only concerned with unique elements! We can cast a list with multiple repeat elements to a set to get the unique elements. For example:

```python
# Create a list with repeats
list1 = [1,1,2,2,3,4,5,6,1,1]
```

```python
# Cast as set to get unique values
set(list1)
# {1, 2, 3, 4, 5, 6}
```

## Booleans

Python comes with Booleans (with predefined True and False displays that are basically just the integers 1 and 0). It also has a placeholder object called None. Let's walk through a few quick examples of Booleans (we will dive deeper into them later in this course).

```python
# Set object to be a boolean
a = True
```

```python
#Show
a
# True
```

We can also use comparison operators to create booleans. We will go over all the comparison operators later on in the course.

```python
# Output is boolean
1 > 2
# False
```

We can use None as a placeholder for an object that we don't want to reassign yet:

```python
# None placeholder
b = None
```

```python
# Show
print(b)
# None
```

---

---

---

# Files

Python uses file objects to interact with external files on your computer. These file objects can be any sort of file you have on your computer, whether it be an audio file, a text file, emails, Excel documents, etc. Note: You will probably need to install certain libraries or modules to interact with those various file types, but they are easily available. (We will cover downloading modules later on in the course).

Python has a built-in open function that allows us to open and play with basic file types. First we will need a file though. We're going to use some IPython magic to create a text file!

**Quickly create a simple `test.txt` file with vscode text editor.**

**Create test.txt file**

```text
Hello, this is a quick test file.
```

## Python Opening a file

Let's begin by opening the file test.txt that is located in the same directory as opened folder in vscode.

It is very easy to get an error on this step:

```python
myfile = open('whoops.txt')
```

**Output:**

```text
---------------------------------------------------------------------------

FileNotFoundError                         Traceback (most recent call last)

----> 1 myfile = open('whoops.txt')


FileNotFoundError: [Errno 2] No such file or directory: 'whoops.txt'
```

To avoid this error,make sure your .txt file is saved in the same location, to check your location, use **pwd** or **echo %cd%**:

```bash
pwd

# 'C:\\Users\\b2r\\Python\\Object'
```

Alternatively, to grab files from any location on your computer, simply pass in the entire file path.

For Windows you need to use double \ so python doesn't treat the second \ as an escape character, a file path is in the form:

```py
myfile = open("C:\\Users\\YourUserName\\Home\\Folder\\myfile.txt")
```

For MacOS and Linux you use slashes in the opposite direction:

```py
myfile = open("/Users/YouUserName/Folder/myfile.txt")
```

```python
# Open the test.txt we made earlier
my_file = open('test.txt')
```

```python
# We can now read the file
my_file.read()
# 'Hello, this is a quick test file.'
```

```python
# But what happens if we try to read it again?
my_file.read()
# ''
```

This happens because you can imagine the reading "cursor" is at the end of the file after having read it. So there is nothing left to read. We can reset the "cursor" like this:

```python
# Seek to the start of file (index 0)
my_file.seek(0)
# Now read again
my_file.read()
# 'Hello, this is a quick test file.'
```

You can read a file line by line using the readlines method. Use caution with large files, since everything will be held in memory. We will learn how to iterate over large files later in the course.

```python
# Readlines returns a list of the lines in the file
my_file.seek(0)
my_file.readlines()
# ['Hello, this is a quick test file.']
```

When you have finished using a file, it is always good practice to close it.

```python
my_file.close()
```

## Writing to a File

By default, the `open()` function will only allow us to read the file. We need to pass the argument `'w'` to write over the file. For example:

```python
# Add a second argument to the function, 'w' which stands for write.
# Passing 'w+' lets us read and write to the file

my_file = open('test.txt','w+')
```

### <strong><font color='red'>Use caution!</font></strong>

Opening a file with `'w'` or `'w+'` truncates the original, meaning that anything that was in the original file **is deleted**!

```python
# Write to the file
my_file.write('This is a new line')
# 18
```

```python
# Read the file
my_file.seek(0)
my_file.read()
# 'This is a new line'
```

```python
my_file.close()  # always do this when you're done with a file
```

## Appending to a File

Passing the argument `'a'` opens the file and puts the pointer at the end, so anything written is appended. Like `'w+'`, `'a+'` lets us read and write to a file. If the file does not exist, one will be created.

```python
my_file = open('test.txt','a+')
my_file.write('\nThis is text being appended to test.txt')
my_file.write('\nAnd another line here.')
# 23
```

```python
my_file.seek(0)
print(my_file.read())
```

**Output:**

```text
This is a new line
This is text being appended to test.txt
And another line here.
```

```python
my_file.close()
```

## Iterating through a File

Lets get a quick preview of a for loop by iterating over a text file.

Now we can use a little bit of flow to tell the program to for through every line of the file and do something:

```python
for line in open('test.txt'):
    print(line)
```

```text
This is a new line
This is text being appended to test.txt
And another line here.
```

Don't worry about fully understanding this yet, for loops are coming up soon. But we'll break down what we did above. We said that for every line in this text file, go ahead and print that line. It's important to note a few things here:

1. We could have called the "line" object anything (see example below).
2. By not calling `.read()` on the file, the whole text file was not stored in memory.
3. Notice the indent on the second line for print. This whitespace is required in Python.

```python
# Pertaining to the first point above
for asdf in open('test.txt'):
    print(asdf)
```

---

---

---

## Test your knowledge

**Answer the following questions**

Write a brief description of all the following Object Types and Data Structures we've learned about:

## Numbers

Write an equation that uses multiplication, division, an exponent, addition, and subtraction that is equal to 100.25.

Hint: This is just to test your memory of the basic arithmetic commands, work backwards from 100.25

```python
# Your answer is probably different
(60 + (10 ** 2) / 4 * 7) - 134.75
# 100.25
```

Answer these 3 questions without typing code. Then type code to check your answer.

```text
What is the value of the expression 4 * (6 + 5)
What is the value of the expression 4 * 6 + 5
What is the value of the expression 4 + 6 * 5
```

```python
4 * (6 + 5)
# 44
```

```python
4 * 6 + 5
# 29
```

```python
4 + 6 * 5
# 34
```

What is the _type_ of the result of the expression 3 + 1.5 + 4?

**Answer: Floating Point Number**

What would you use to find a number’s square root, as well as its square?

```python
# Square root:
100 ** 0.5
# 10.0
```

```python
# Square:
10 ** 2
# 100
```

## Strings

Given the string 'hello' give an index command that returns 'e'. Enter your code in the cell below:

```python
s = 'hello'
# Print out 'e' using indexing

s[1]
# 'e'
```

Reverse the string 'hello' using slicing:

```python
s ='hello'
# Reverse the string using slicing

s[::-1]
# 'olleh'
```

Given the string 'hello', give two methods of producing the letter 'o' using indexing.

```python
s ='hello'
# Print out the 'o'

# Method 1:

s[-1]
# 'o'
```

```python
# Method 2:

s[4]
# 'o'
```

## Lists

Build this list [0,0,0] two separate ways.

```python
# Method 1:
[0]*3
# [0, 0, 0]
```

```python
# Method 2:
list2 = [0,0,0]
list2
# [0, 0, 0]
```

Reassign 'hello' in this nested list to say 'goodbye' instead:

```python
list3 = [1,2,[3,4,'hello']]
```

```python
list3[2][2] = 'goodbye'
```

```python
list3
# [1, 2, [3, 4, 'goodbye']]
```

Sort the list below:

```python
list4 = [5,3,4,6,1]
```

```python
# Method 1:
sorted(list4)
# [1, 3, 4, 5, 6]
```

```python
# Method 2:
list4.sort()
list4
# [1, 3, 4, 5, 6]
```

## Dictionaries

Using keys and indexing, grab the 'hello' from the following dictionaries:

```python
d = {'simple_key':'hello'}
# Grab 'hello'

d['simple_key']
# 'hello'
```

```python
d = {'k1':{'k2':'hello'}}
# Grab 'hello'

d['k1']['k2']
# 'hello'
```

```python
# Getting a little tricker
d = {'k1':[{'nest_key':['this is deep',['hello']]}]}
```

```python
# This was harder than I expected...
d['k1'][0]['nest_key'][1][0]
# 'hello'
```

```python
# This will be hard and annoying!
d = {'k1':[1,2,{'k2':['this is tricky',{'tough':[1,2,['hello']]}]}]}
```

```python
# Phew!
d['k1'][2]['k2'][1]['tough'][2][0]
# 'hello'
```

Can you sort a dictionary? Why or why not?

**Answer: No! Because normal dictionaries are _mappings_ not a sequence.**

## Tuples

What is the major difference between tuples and lists?

**Tuples are immutable!**

How do you create a tuple?

```python
t = (1,2,3)
```

## Sets

What is unique about a set?

**Answer: They don't allow for duplicate items!**

Use a set to find the unique values of the list below:

```python
list5 = [1,2,2,33,4,4,11,22,3,3,2]
```

```python
set(list5)
# {1, 2, 3, 4, 11, 22, 33}
```

## Booleans

For the following quiz questions, we will get a preview of comparison operators. In the table below, a=3 and b=4.

<table class="table table-bordered">
  <tr>
    <th style="width: 10%">Operator</th>
    <th style="width: 45%">Description</th>
    <th>Example</th>
  </tr>
  <tr>
    <td>==</td>
    <td>
      If the values of two operands are equal, then the condition becomes true.
    </td>
    <td>(a == b) is not true.</td>
  </tr>
  <tr>
    <td>!=</td>
    <td>
      If values of two operands are not equal, then condition becomes true.
    </td>
    <td>(a != b) is true.</td>
  </tr>
  <tr>
    <td>&gt;</td>
    <td>
      If the value of left operand is greater than the value of right operand,
      then condition becomes true.
    </td>
    <td>(a &gt; b) is not true.</td>
  </tr>
  <tr>
    <td>&lt;</td>
    <td>
      If the value of left operand is less than the value of right operand, then
      condition becomes true.
    </td>
    <td>(a &lt; b) is true.</td>
  </tr>
  <tr>
    <td>&gt;=</td>
    <td>
      If the value of left operand is greater than or equal to the value of
      right operand, then condition becomes true.
    </td>
    <td>(a &gt;= b) is not true.</td>
  </tr>
  <tr>
    <td>&lt;=</td>
    <td>
      If the value of left operand is less than or equal to the value of right
      operand, then condition becomes true.
    </td>
    <td>(a &lt;= b) is true.</td>
  </tr>
</table>

What will be the resulting Boolean of the following pieces of code (answer fist then check by typing it in!)

```python
2 > 3
# False
```

```python
3 <= 2
# False
```

```python
3 == 2.0
# False
```

```python
3.0 == 3
# True
```

```python
4**0.5 != 2
# False
```

Final Question: What is the boolean output of the cell block below?

```python
# two nested lists
l_one = [1,2,[3,4]]
l_two = [1,2,{'k1':4}]

# True or False?
l_one[2][0] >= l_two[2]['k1']
# False
```

---

---

---

# Comparison Operators

In this lecture we will be learning about Comparison Operators in Python. These operators will allow us to compare variables and output a Boolean value (True or False).

If you have any sort of background in Math, these operators should be very straight forward.

First we'll present a table of the comparison operators and then work through some examples:

<h2> Table of Comparison Operators </h2><p>  In the table below, a=3 and b=4.</p>

<table class="table table-bordered">
<tr>
<th style="width:10%">Operator</th><th style="width:45%">Description</th><th>Example</th>
</tr>
<tr>
<td>==</td>
<td>If the values of two operands are equal, then the condition becomes true.</td>
<td> (a == b) is not true.</td>
</tr>
<tr>
<td>!=</td>
<td>If values of two operands are not equal, then condition becomes true.</td>
<td>(a != b) is true</td>
</tr>
<tr>
<td>&gt;</td>
<td>If the value of left operand is greater than the value of right operand, then condition becomes true.</td>
<td> (a &gt; b) is not true.</td>
</tr>
<tr>
<td>&lt;</td>
<td>If the value of left operand is less than the value of right operand, then condition becomes true.</td>
<td> (a &lt; b) is true.</td>
</tr>
<tr>
<td>&gt;=</td>
<td>If the value of left operand is greater than or equal to the value of right operand, then condition becomes true.</td>
<td> (a &gt;= b) is not true. </td>
</tr>
<tr>
<td>&lt;=</td>
<td>If the value of left operand is less than or equal to the value of right operand, then condition becomes true.</td>
<td> (a &lt;= b) is true. </td>
</tr>
</table>

Let's now work through quick examples of each of these.

#### Equal

```python
2 == 2
```

    True

```python
1 == 0
```

    False

Note that <code>==</code> is a <em>comparison</em> operator, while <code>=</code> is an <em>assignment</em> operator.

#### Not Equal

```python
2 != 1
```

    True

```python
2 != 2
```

    False

#### Greater Than

```python
2 > 1
```

    True

```python
2 > 4
```

    False

#### Less Than

```python
2 < 4
```

    True

```python
2 < 1
```

    False

#### Greater Than or Equal to

```python
2 >= 2
```

    True

```python
2 >= 1
```

    True

#### Less than or Equal to

```python
2 <= 2
```

    True

```python
2 <= 4
```

    True

**Great! Go over each comparison operator to make sure you understand what each one is saying. But hopefully this was straightforward for you.**

Next we will cover chained comparison operators

---

---

---

# Chained Comparison Operators

An interesting feature of Python is the ability to _chain_ multiple comparisons to perform a more complex test. You can use these chained comparisons as shorthand for larger Boolean Expressions.

In this lecture we will learn how to chain comparison operators and we will also introduce two other important statements in Python: **and** and **or**.

Let's look at a few examples of using chains:

```python
1 < 2 < 3
```

    True

The above statement checks if 1 was less than 2 **and** if 2 was less than 3. We could have written this using an **and** statement in Python:

```python
1<2 and 2<3
```

    True

The **and** is used to make sure two checks have to be true in order for the total check to be true. Let's see another example:

```python
1 < 3 > 2
```

    True

The above checks if 3 is larger than both of the other numbers, so you could use **and** to rewrite it as:

```python
1<3 and 3>2
```

    True

It's important to note that Python is checking both instances of the comparisons. We can also use **or** to write comparisons in Python. For example:

```python
1==2 or 2<3
```

    True

Note how it was true; this is because with the **or** operator, we only need one _or_ the other to be true. Let's see one more example to drive this home:

```python
1==1 or 100==1
```

    True

Great! For an overview of this quick lesson: You should have a comfortable understanding of using **and** and **or** statements as well as reading chained comparison code.

Go ahead and go to the quiz for this section to check your understanding!

# Introduction to Python Statements

In this lecture we will be doing a quick overview of Python Statements. This lecture will emphasize differences between Python and other languages such as C++.

There are two reasons we take this approach for learning the context of Python Statements:

    1.) If you are coming from a different language this will rapidly accelerate your understanding of Python.
    2.) Learning about statements will allow you to be able to read other languages more easily in the future.

## Python vs Other Languages

Let's create a simple statement that says:
"If a is greater than b, assign 2 to a and 4 to b"

Take a look at these two if statements (we will learn about building out if statements soon).

**Version 1 (Other Languages)**

    if (a>b){
        a = 2;
        b = 4;
    }

**Version 2 (Python)**

    if a>b:
        a = 2
        b = 4

You'll notice that Python is less cluttered and much more readable than the first version. How does Python manage this?

Let's walk through the main differences:

Python gets rid of () and {} by incorporating two main factors: a _colon_ and _whitespace_. The statement is ended with a colon, and whitespace is used (indentation) to describe what takes place in case of the statement.

Another major difference is the lack of semicolons in Python. Semicolons are used to denote statement endings in many other languages, but in Python, the end of a line is the same as the end of a statement.

Lastly, to end this brief overview of differences, let's take a closer look at indentation syntax in Python vs other languages:

## Indentation

Here is some pseudo-code to indicate the use of whitespace and indentation in Python:

**Other Languages**

    if (x)
        if(y)
            code-statement;
    else
        another-code-statement;

**Python**

    if x:
        if y:
            code-statement
    else:
        another-code-statement

Note how Python is so heavily driven by code indentation and whitespace. This means that code readability is a core part of the design of the Python language.

Now let's start diving deeper by coding these sort of statements in Python!

## Time to code!

# if, elif, else Statements

<code>if</code> Statements in Python allows us to tell the computer to perform alternative actions based on a certain set of results.

Verbally, we can imagine we are telling the computer:

"Hey if this case happens, perform some action"

We can then expand the idea further with <code>elif</code> and <code>else</code> statements, which allow us to tell the computer:

"Hey if this case happens, perform some action. Else, if another case happens, perform some other action. Else, if _none_ of the above cases happened, perform this action."

Let's go ahead and look at the syntax format for <code>if</code> statements to get a better idea of this:

    if case1:
        perform action1
    elif case2:
        perform action2
    else:
        perform action3

## First Example

Let's see a quick example of this:

```python
if True:
    print('It was true!')
```

    It was true!

Let's add in some else logic:

```python
x = False

if x:
    print('x was True!')
else:
    print('I will be printed in any case where x is not true')
```

    I will be printed in any case where x is not true

### Multiple Branches

Let's get a fuller picture of how far <code>if</code>, <code>elif</code>, and <code>else</code> can take us!

We write this out in a nested structure. Take note of how the <code>if</code>, <code>elif</code>, and <code>else</code> line up in the code. This can help you see what <code>if</code> is related to what <code>elif</code> or <code>else</code> statements.

We'll reintroduce a comparison syntax for Python.

```python
loc = 'Bank'

if loc == 'Auto Shop':
    print('Welcome to the Auto Shop!')
elif loc == 'Bank':
    print('Welcome to the bank!')
else:
    print('Where are you?')
```

    Welcome to the bank!

Note how the nested <code>if</code> statements are each checked until a True boolean causes the nested code below it to run. You should also note that you can put in as many <code>elif</code> statements as you want before you close off with an <code>else</code>.

Let's create two more simple examples for the <code>if</code>, <code>elif</code>, and <code>else</code> statements:

```python
person = 'Sammy'

if person == 'Sammy':
    print('Welcome Sammy!')
else:
    print("Welcome, what's your name?")
```

    Welcome Sammy!

```python
person = 'George'

if person == 'Sammy':
    print('Welcome Sammy!')
elif person =='George':
    print('Welcome George!')
else:
    print("Welcome, what's your name?")
```

    Welcome George!

## Indentation

It is important to keep a good understanding of how indentation works in Python to maintain the structure and order of your code. We will touch on this topic again when we start building out functions!

# for Loops

A <code>for</code> loop acts as an iterator in Python; it goes through items that are in a _sequence_ or any other iterable item. Objects that we've learned about that we can iterate over include strings, lists, tuples, and even built-in iterables for dictionaries, such as keys or values.

We've already seen the <code>for</code> statement a little bit in past lectures but now let's formalize our understanding.

Here's the general format for a <code>for</code> loop in Python:

    for item in object:
        statements to do stuff

The variable name used for the item is completely up to the coder, so use your best judgment for choosing a name that makes sense and you will be able to understand when revisiting your code. This item name can then be referenced inside your loop, for example if you wanted to use <code>if</code> statements to perform checks.

Let's go ahead and work through several example of <code>for</code> loops using a variety of data object types. We'll start simple and build more complexity later on.

## Example 1

Iterating through a list

```python
# We'll learn how to automate this sort of list in the next lecture
list1 = [1,2,3,4,5,6,7,8,9,10]
```

```python
for num in list1:
    print(num)
```

    1
    2
    3
    4
    5
    6
    7
    8
    9
    10

Great! Hopefully this makes sense. Now let's add an <code>if</code> statement to check for even numbers. We'll first introduce a new concept here--the modulo.

### Modulo

The modulo allows us to get the remainder in a division and uses the % symbol. For example:

```python
17 % 5
```

    2

This makes sense since 17 divided by 5 is 3 remainder 2. Let's see a few more quick examples:

```python
# 3 Remainder 1
10 % 3
```

    1

```python
# 2 Remainder 4
18 % 7
```

    4

```python
# 2 no remainder
4 % 2
```

    0

Notice that if a number is fully divisible with no remainder, the result of the modulo call is 0. We can use this to test for even numbers, since if a number modulo 2 is equal to 0, that means it is an even number!

Back to the <code>for</code> loops!

## Example 2

Let's print only the even numbers from that list!

```python
for num in list1:
    if num % 2 == 0:
        print(num)
```

    2
    4
    6
    8
    10

We could have also put an <code>else</code> statement in there:

```python
for num in list1:
    if num % 2 == 0:
        print(num)
    else:
        print('Odd number')
```

    Odd number
    2
    Odd number
    4
    Odd number
    6
    Odd number
    8
    Odd number
    10

## Example 3

Another common idea during a <code>for</code> loop is keeping some sort of running tally during multiple loops. For example, let's create a <code>for</code> loop that sums up the list:

```python
# Start sum at zero
list_sum = 0

for num in list1:
    list_sum = list_sum + num

print(list_sum)
```

    55

Great! Read over the above cell and make sure you understand fully what is going on. Also we could have implemented a <code>+=</code> to perform the addition towards the sum. For example:

```python
# Start sum at zero
list_sum = 0

for num in list1:
    list_sum += num

print(list_sum)
```

    55

## Example 4

We've used <code>for</code> loops with lists, how about with strings? Remember strings are a sequence so when we iterate through them we will be accessing each item in that string.

```python
for letter in 'This is a string.':
    print(letter)
```

    T
    h
    i
    s

    i
    s

    a

    s
    t
    r
    i
    n
    g
    .

## Example 5

Let's now look at how a <code>for</code> loop can be used with a tuple:

```python
tup = (1,2,3,4,5)

for t in tup:
    print(t)
```

    1
    2
    3
    4
    5

## Example 6

Tuples have a special quality when it comes to <code>for</code> loops. If you are iterating through a sequence that contains tuples, the item can actually be the tuple itself, this is an example of _tuple unpacking_. During the <code>for</code> loop we will be unpacking the tuple inside of a sequence and we can access the individual items inside that tuple!

```python
list2 = [(2,4),(6,8),(10,12)]
```

```python
for tup in list2:
    print(tup)
```

    (2, 4)
    (6, 8)
    (10, 12)

```python
# Now with unpacking!
for (t1,t2) in list2:
    print(t1)
```

    2
    6
    10

Cool! With tuples in a sequence we can access the items inside of them through unpacking! The reason this is important is because many objects will deliver their iterables through tuples. Let's start exploring iterating through Dictionaries to explore this further!

## Example 7

```python
d = {'k1':1,'k2':2,'k3':3}
```

```python
for item in d:
    print(item)
```

    k1
    k2
    k3

Notice how this produces only the keys. So how can we get the values? Or both the keys and the values?

We're going to introduce three new Dictionary methods: **.keys()**, **.values()** and **.items()**

In Python each of these methods return a _dictionary view object_. It supports operations like membership test and iteration, but its contents are not independent of the original dictionary – it is only a view. Let's see it in action:

```python
# Create a dictionary view object
d.items()
```

    dict_items([('k1', 1), ('k2', 2), ('k3', 3)])

Since the .items() method supports iteration, we can perform _dictionary unpacking_ to separate keys and values just as we did in the previous examples.

```python
# Dictionary unpacking
for k,v in d.items():
    print(k)
    print(v)
```

    k1
    1
    k2
    2
    k3
    3

If you want to obtain a true list of keys, values, or key/value tuples, you can _cast_ the view as a list:

```python
list(d.keys())
```

    ['k1', 'k2', 'k3']

Remember that dictionaries are unordered, and that keys and values come back in arbitrary order. You can obtain a sorted list using sorted():

```python
sorted(d.values())
```

    [1, 2, 3]

## Conclusion

We've learned how to use for loops to iterate through tuples, lists, strings, and dictionaries. It will be an important tool for us, so make sure you know it well and understood the above examples.

[More resources](http://www.tutorialspoint.com/python/python_for_loop.htm)

# while Loops

The <code>while</code> statement in Python is one of most general ways to perform iteration. A <code>while</code> statement will repeatedly execute a single statement or group of statements as long as the condition is true. The reason it is called a 'loop' is because the code statements are looped through over and over again until the condition is no longer met.

The general format of a while loop is:

    while test:
        code statements
    else:
        final code statements

Let’s look at a few simple <code>while</code> loops in action.

```python
x = 0

while x < 10:
    print('x is currently: ',x)
    print(' x is still less than 10, adding 1 to x')
    x+=1
```

    x is currently:  0
     x is still less than 10, adding 1 to x
    x is currently:  1
     x is still less than 10, adding 1 to x
    x is currently:  2
     x is still less than 10, adding 1 to x
    x is currently:  3
     x is still less than 10, adding 1 to x
    x is currently:  4
     x is still less than 10, adding 1 to x
    x is currently:  5
     x is still less than 10, adding 1 to x
    x is currently:  6
     x is still less than 10, adding 1 to x
    x is currently:  7
     x is still less than 10, adding 1 to x
    x is currently:  8
     x is still less than 10, adding 1 to x
    x is currently:  9
     x is still less than 10, adding 1 to x

Notice how many times the print statements occurred and how the <code>while</code> loop kept going until the True condition was met, which occurred once x==10. It's important to note that once this occurred the code stopped. Let's see how we could add an <code>else</code> statement:

```python
x = 0

while x < 10:
    print('x is currently: ',x)
    print(' x is still less than 10, adding 1 to x')
    x+=1

else:
    print('All Done!')
```

    x is currently:  0
     x is still less than 10, adding 1 to x
    x is currently:  1
     x is still less than 10, adding 1 to x
    x is currently:  2
     x is still less than 10, adding 1 to x
    x is currently:  3
     x is still less than 10, adding 1 to x
    x is currently:  4
     x is still less than 10, adding 1 to x
    x is currently:  5
     x is still less than 10, adding 1 to x
    x is currently:  6
     x is still less than 10, adding 1 to x
    x is currently:  7
     x is still less than 10, adding 1 to x
    x is currently:  8
     x is still less than 10, adding 1 to x
    x is currently:  9
     x is still less than 10, adding 1 to x
    All Done!

# break, continue, pass

We can use <code>break</code>, <code>continue</code>, and <code>pass</code> statements in our loops to add additional functionality for various cases. The three statements are defined by:

    break: Breaks out of the current closest enclosing loop.
    continue: Goes to the top of the closest enclosing loop.
    pass: Does nothing at all.

Thinking about <code>break</code> and <code>continue</code> statements, the general format of the <code>while</code> loop looks like this:

    while test:
        code statement
        if test:
            break
        if test:
            continue
    else:

<code>break</code> and <code>continue</code> statements can appear anywhere inside the loop’s body, but we will usually put them further nested in conjunction with an <code>if</code> statement to perform an action based on some condition.

Let's go ahead and look at some examples!

```python
x = 0

while x < 10:
    print('x is currently: ',x)
    print(' x is still less than 10, adding 1 to x')
    x+=1
    if x==3:
        print('x==3')
    else:
        print('continuing...')
        continue
```

    x is currently:  0
     x is still less than 10, adding 1 to x
    continuing...
    x is currently:  1
     x is still less than 10, adding 1 to x
    continuing...
    x is currently:  2
     x is still less than 10, adding 1 to x
    x==3
    x is currently:  3
     x is still less than 10, adding 1 to x
    continuing...
    x is currently:  4
     x is still less than 10, adding 1 to x
    continuing...
    x is currently:  5
     x is still less than 10, adding 1 to x
    continuing...
    x is currently:  6
     x is still less than 10, adding 1 to x
    continuing...
    x is currently:  7
     x is still less than 10, adding 1 to x
    continuing...
    x is currently:  8
     x is still less than 10, adding 1 to x
    continuing...
    x is currently:  9
     x is still less than 10, adding 1 to x
    continuing...

Note how we have a printed statement when x==3, and a continue being printed out as we continue through the outer while loop. Let's put in a break once x ==3 and see if the result makes sense:

```python
x = 0

while x < 10:
    print('x is currently: ',x)
    print(' x is still less than 10, adding 1 to x')
    x+=1
    if x==3:
        print('Breaking because x==3')
        break
    else:
        print('continuing...')
        continue
```

    x is currently:  0
     x is still less than 10, adding 1 to x
    continuing...
    x is currently:  1
     x is still less than 10, adding 1 to x
    continuing...
    x is currently:  2
     x is still less than 10, adding 1 to x
    Breaking because x==3

Note how the other <code>else</code> statement wasn't reached and continuing was never printed!

After these brief but simple examples, you should feel comfortable using <code>while</code> statements in your code.

**A word of caution however! It is possible to create an infinitely running loop with <code>while</code> statements. For example:**

```python
# DO NOT RUN THIS CODE!!!!
while True:
    print("I'm stuck in an infinite loop!")
```

A quick note: If you _did_ run the above cell, click on the Kernel menu above to restart the kernel!

# Useful Operators

There are a few built-in functions and "operators" in Python that don't fit well into any category, so we will go over them in this lecture, let's begin!

## range

The range function allows you to quickly _generate_ a list of integers, this comes in handy a lot, so take note of how to use it! There are 3 parameters you can pass, a start, a stop, and a step size. Let's see some examples:

```python
range(0,11)
```

    range(0, 11)

Note that this is a **generator** function, so to actually get a list out of it, we need to cast it to a list with **list()**. What is a generator? Its a special type of function that will generate information and not need to save it to memory. We haven't talked about functions or generators yet, so just keep this in your notes for now, we will discuss this in much more detail in later on in your training!

```python
# Notice how 11 is not included, up to but not including 11, just like slice notation!
list(range(0,11))
```

    [0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10]

```python
list(range(0,12))
```

    [0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11]

```python
# Third parameter is step size!
# step size just means how big of a jump/leap/step you
# take from the starting number to get to the next number.

list(range(0,11,2))
```

    [0, 2, 4, 6, 8, 10]

```python
list(range(0,101,10))
```

    [0, 10, 20, 30, 40, 50, 60, 70, 80, 90, 100]

## enumerate

enumerate is a very useful function to use with for loops. Let's imagine the following situation:

```python
index_count = 0

for letter in 'abcde':
    print("At index {} the letter is {}".format(index_count,letter))
    index_count += 1
```

    At index 0 the letter is a
    At index 1 the letter is b
    At index 2 the letter is c
    At index 3 the letter is d
    At index 4 the letter is e

Keeping track of how many loops you've gone through is so common, that enumerate was created so you don't need to worry about creating and updating this index_count or loop_count variable

```python
# Notice the tuple unpacking!

for i,letter in enumerate('abcde'):
    print("At index {} the letter is {}".format(i,letter))
```

    At index 0 the letter is a
    At index 1 the letter is b
    At index 2 the letter is c
    At index 3 the letter is d
    At index 4 the letter is e

## zip

Notice the format enumerate actually returns, let's take a look by transforming it to a list()

```python
list(enumerate('abcde'))
```

    [(0, 'a'), (1, 'b'), (2, 'c'), (3, 'd'), (4, 'e')]

It was a list of tuples, meaning we could use tuple unpacking during our for loop. This data structure is actually very common in Python , especially when working with outside libraries. You can use the **zip()** function to quickly create a list of tuples by "zipping" up together two lists.

```python
mylist1 = [1,2,3,4,5]
mylist2 = ['a','b','c','d','e']
```

```python
# This one is also a generator! We will explain this later, but for now let's transform it to a list
zip(mylist1,mylist2)
```

    <zip at 0x1d205086f08>

```python
list(zip(mylist1,mylist2))
```

    [(1, 'a'), (2, 'b'), (3, 'c'), (4, 'd'), (5, 'e')]

To use the generator, we could just use a for loop

```python
for item1, item2 in zip(mylist1,mylist2):
    print('For this tuple, first item was {} and second item was {}'.format(item1,item2))
```

    For this tuple, first item was 1 and second item was a
    For this tuple, first item was 2 and second item was b
    For this tuple, first item was 3 and second item was c
    For this tuple, first item was 4 and second item was d
    For this tuple, first item was 5 and second item was e

## in operator

We've already seen the **in** keyword during the for loop, but we can also use it to quickly check if an object is in a list

```python
'x' in ['x','y','z']
```

    True

```python
'x' in [1,2,3]
```

    False

## not in

We can combine **in** with a **not** operator, to check if some object or variable is not present in a list.

```python
'x' not in ['x','y','z']
```

    False

```python
'x' not in [1,2,3]
```

    True

## min and max

Quickly check the minimum or maximum of a list with these functions.

```python
mylist = [10,20,30,40,100]
```

```python
min(mylist)
```

    10

```python
max(mylist)
```

    100

## random

Python comes with a built in random library. There are a lot of functions included in this random library, so we will only show you two useful functions for now.

```python
from random import shuffle
```

```python
# This shuffles the list "in-place" meaning it won't return
# anything, instead it will effect the list passed
shuffle(mylist)
```

```python
mylist
```

    [40, 10, 100, 30, 20]

```python
from random import randint
```

```python
# Return random integer in range [a, b], including both end points.
randint(0,100)
```

    25

```python
# Return random integer in range [a, b], including both end points.
randint(0,100)
```

    91

## input

```python
input('Enter Something into this box: ')
```

    Enter Something into this box: great job!





    'great job!'

# List Comprehensions

In addition to sequence operations and list methods, Python includes a more advanced operation called a list comprehension.

List comprehensions allow us to build out lists using a different notation. You can think of it as essentially a one line <code>for</code> loop built inside of brackets. For a simple example:

## Example 1

```python
# Grab every letter in string
lst = [x for x in 'word']
```

```python
# Check
lst
```

    ['w', 'o', 'r', 'd']

This is the basic idea of a list comprehension. If you're familiar with mathematical notation this format should feel familiar for example: x^2 : x in { 0,1,2...10 }

Let's see a few more examples of list comprehensions in Python:

## Example 2

```python
# Square numbers in range and turn into list
lst = [x**2 for x in range(0,11)]
```

```python
lst
```

    [0, 1, 4, 9, 16, 25, 36, 49, 64, 81, 100]

## Example 3

Let's see how to add in <code>if</code> statements:

```python
# Check for even numbers in a range
lst = [x for x in range(11) if x % 2 == 0]
```

```python
lst
```

    [0, 2, 4, 6, 8, 10]

## Example 4

Can also do more complicated arithmetic:

```python
# Convert Celsius to Fahrenheit
celsius = [0,10,20.1,34.5]

fahrenheit = [((9/5)*temp + 32) for temp in celsius ]

fahrenheit
```

    [32.0, 50.0, 68.18, 94.1]

## Example 5

We can also perform nested list comprehensions, for example:

```python
lst = [ x**2 for x in [x**2 for x in range(11)]]
lst
```

    [0, 1, 16, 81, 256, 625, 1296, 2401, 4096, 6561, 10000]

Later on in the course we will learn about generator comprehensions. After this lecture you should feel comfortable reading and writing basic list comprehensions.

# Statements Assessment Solutions

---

**Use <code>for</code>, .split(), and <code>if</code> to create a Statement that will print out words that start with 's':**

```python
st = 'Print only the words that start with s in this sentence'
```

```python
for word in st.split():
    if word[0] == 's':
        print(word)
```

    start
    s
    sentence

---

**Use range() to print all the even numbers from 0 to 10.**

```python
list(range(0,11,2))
```

    [0, 2, 4, 6, 8, 10]

---

**Use List comprehension to create a list of all numbers between 1 and 50 that are divisible by 3.**

```python
[x for x in range(1,51) if x%3 == 0]
```

    [3, 6, 9, 12, 15, 18, 21, 24, 27, 30, 33, 36, 39, 42, 45, 48]

---

**Go through the string below and if the length of a word is even print "even!"**

```python
st = 'Print every word in this sentence that has an even number of letters'
```

```python
for word in st.split():
    if len(word)%2 == 0:
        print(word+" <-- has an even length!")
```

    word <-- has an even length!
    in <-- has an even length!
    this <-- has an even length!
    sentence <-- has an even length!
    that <-- has an even length!
    an <-- has an even length!
    even <-- has an even length!
    number <-- has an even length!
    of <-- has an even length!

---

**Write a program that prints the integers from 1 to 100. But for multiples of three print "Fizz" instead of the number, and for the multiples of five print "Buzz". For numbers which are multiples of both three and five print "FizzBuzz".**

```python
for num in range(1,101):
    if num % 3 == 0 and num % 5 == 0:
        print("FizzBuzz")
    elif num % 3 == 0:
        print("Fizz")
    elif num % 5 == 0:
        print("Buzz")
    else:
        print(num)
```

---

**Use a List Comprehension to create a list of the first letters of every word in the string below:**

```python
st = 'Create a list of the first letters of every word in this string'
```

```python
[word[0] for word in st.split()]
```

    ['C', 'a', 'l', 'o', 't', 'f', 'l', 'o', 'e', 'w', 'i', 't', 's']

### Great Job!

# Guessing Game Challenge - Solution

Let's use `while` loops to create a guessing game.

The Challenge:

Write a program that picks a random integer from 1 to 100, and has players guess the number. The rules are:

1. If a player's guess is less than 1 or greater than 100, say "OUT OF BOUNDS"
2. On a player's first turn, if their guess is

- within 10 of the number, return "WARM!"
- further than 10 away from the number, return "COLD!"

3. On all subsequent turns, if a guess is

- closer to the number than the previous guess return "WARMER!"
- farther from the number than the previous guess, return "COLDER!"

4. When the player's guess equals the number, tell them they've guessed correctly _and_ how many guesses it took!

#### First, pick a random integer from 1 to 100 using the random module and assign it to a variable

Note: `random.randint(a,b)` returns a random integer in range `[a, b]`, including both end points.

```python
import random

num = random.randint(1,100)
```

#### Next, print an introduction to the game and explain the rules

```python
print("WELCOME TO GUESS ME!")
print("I'm thinking of a number between 1 and 100")
print("If your guess is more than 10 away from my number, I'll tell you you're COLD")
print("If your guess is within 10 of my number, I'll tell you you're WARM")
print("If your guess is farther than your most recent guess, I'll say you're getting COLDER")
print("If your guess is closer than your most recent guess, I'll say you're getting WARMER")
print("LET'S PLAY!")
```

    WELCOME TO GUESS ME!
    I'm thinking of a number between 1 and 100
    If your guess is more than 10 away from my number, I'll tell you you're COLD
    If your guess is within 10 of my number, I'll tell you you're WARM
    If your guess is farther than your most recent guess, I'll say you're getting COLDER
    If your guess is closer than your most recent guess, I'll say you're getting WARMER
    LET'S PLAY!

#### Create a list to store guesses

Hint: zero is a good placeholder value. It's useful because it evaluates to "False"

```python
guesses = [0]
```

#### Write a `while` loop that asks for a valid guess. Test it a few times to make sure it works.

```python
while True:

    guess = int(input("I'm thinking of a number between 1 and 100.\n  What is your guess? "))

    if guess < 1 or guess > 100:
        print('OUT OF BOUNDS! Please try again: ')
        continue

    break
```

    I'm thinking of a number between 1 and 100.
      What is your guess? 500
    OUT OF BOUNDS! Please try again:
    I'm thinking of a number between 1 and 100.
      What is your guess? 50

#### Write a `while` loop that compares the player's guess to our number. If the player guesses correctly, break from the loop. Otherwise, tell the player if they're warmer or colder, and continue asking for guesses.

Some hints:

- it may help to sketch out all possible combinations on paper first!
- you can use the `abs()` function to find the positive difference between two numbers
- if you append all new guesses to the list, then the previous guess is given as `guesses[-2]`

```python
while True:

    # we can copy the code from above to take an input
    guess = int(input("I'm thinking of a number between 1 and 100.\n  What is your guess? "))

    if guess < 1 or guess > 100:
        print('OUT OF BOUNDS! Please try again: ')
        continue

    # here we compare the player's guess to our number
    if guess == num:
        print(f'CONGRATULATIONS, YOU GUESSED IT IN ONLY {len(guesses)} GUESSES!!')
        break

    # if guess is incorrect, add guess to the list
    guesses.append(guess)

    # when testing the first guess, guesses[-2]==0, which evaluates to False
    # and brings us down to the second section

    if guesses[-2]:
        if abs(num-guess) < abs(num-guesses[-2]):
            print('WARMER!')
        else:
            print('COLDER!')

    else:
        if abs(num-guess) <= 10:
            print('WARM!')
        else:
            print('COLD!')
```

    I'm thinking of a number between 1 and 100.
      What is your guess? 50
    COLD!
    I'm thinking of a number between 1 and 100.
      What is your guess? 75
    WARMER!
    I'm thinking of a number between 1 and 100.
      What is your guess? 85
    WARMER!
    I'm thinking of a number between 1 and 100.
      What is your guess? 92
    COLDER!
    I'm thinking of a number between 1 and 100.
      What is your guess? 80
    WARMER!
    I'm thinking of a number between 1 and 100.
      What is your guess? 78
    COLDER!
    I'm thinking of a number between 1 and 100.
      What is your guess? 82
    WARMER!
    I'm thinking of a number between 1 and 100.
      What is your guess? 83
    COLDER!
    I'm thinking of a number between 1 and 100.
      What is your guess? 81
    CONGRATULATIONS, YOU GUESSED IT IN ONLY 9 GUESSES!!

That's it! You've just programmed your first game!

In the next section we'll learn how to turn some of these repetitive actions into _functions_ that can be called whenever we need them.

### Good Job!

# Methods

We've already seen a few example of methods when learning about Object and Data Structure Types in Python. Methods are essentially functions built into objects. Later on in the course we will learn about how to create our own objects and methods using Object Oriented Programming (OOP) and classes.

Methods perform specific actions on an object and can also take arguments, just like a function. This lecture will serve as just a brief introduction to methods and get you thinking about overall design methods that we will touch back upon when we reach OOP in the course.

Methods are in the form:

    object.method(arg1,arg2,etc...)

You'll later see that we can think of methods as having an argument 'self' referring to the object itself. You can't see this argument but we will be using it later on in the course during the OOP lectures.

Let's take a quick look at what an example of the various methods a list has:

```python
# Create a simple list
lst = [1,2,3,4,5]
```

Fortunately, with iPython and the Jupyter Notebook we can quickly see all the possible methods using the tab key. The methods for a list are:

- append
- count
- extend
- insert
- pop
- remove
- reverse
- sort

Let's try out a few of them:

append() allows us to add elements to the end of a list:

```python
lst.append(6)
```

```python
lst
```

    [1, 2, 3, 4, 5, 6]

Great! Now how about count()? The count() method will count the number of occurrences of an element in a list.

```python
# Check how many times 2 shows up in the list
lst.count(2)
```

    1

You can always use Shift+Tab in the Jupyter Notebook to get more help about the method. In general Python you can use the help() function:

```python
help(lst.count)
```

    Help on built-in function count:

    count(...) method of builtins.list instance
        L.count(value) -> integer -- return number of occurrences of value

Feel free to play around with the rest of the methods for a list. Later on in this section your quiz will involve using help and Google searching for methods of different types of objects!

Great! By this lecture you should feel comfortable calling methods of objects in Python!

---

# Functions

## Introduction to Functions

This lecture will consist of explaining what a function is in Python and how to create one. Functions will be one of our main building blocks when we construct larger and larger amounts of code to solve problems.

### What is a function?

Formally, a function is a useful device that groups together a set of statements so they can be run more than once. They can also let us specify parameters that can serve as inputs to the functions.

On a more fundamental level, functions allow us to not have to repeatedly write the same code again and again. If you remember back to the lessons on strings and lists, remember that we used a function len() to get the length of a string. Since checking the length of a sequence is a common task you would want to write a function that can do this repeatedly at command.

Functions will be one of most basic levels of reusing code in Python, and it will also allow us to start thinking of program design (we will dive much deeper into the ideas of design when we learn about Object Oriented Programming).

### Why even use functions?

Put simply, you should use functions when you plan on using a block of code multiple times. The function will allow you to call the same block of code without having to write it multiple times. This in turn will allow you to create more complex Python scripts. To really understand this though, we should actually write our own functions!

## Function Topics

- def keyword
- simple example of a function
- calling a function with ()
- accepting parameters
- print versus return
- adding in logic inside a function
- multiple returns inside a function
- adding in loops inside a function
- tuple unpacking
- interactions between functions

### def keyword

Let's see how to build out a function's syntax in Python. It has the following form:

```python
def name_of_function(arg1,arg2):
    '''
    This is where the function's Document String (docstring) goes.
    When you call help() on your function it will be printed out.
    '''
    # Do stuff here
    # Return desired result
```

We begin with <code>def</code> then a space followed by the name of the function. Try to keep names relevant, for example len() is a good name for a length() function. Also be careful with names, you wouldn't want to call a function the same name as a [built-in function in Python](https://docs.python.org/3/library/functions.html) (such as len).

Next come a pair of parentheses with a number of arguments separated by a comma. These arguments are the inputs for your function. You'll be able to use these inputs in your function and reference them. After this you put a colon.

Now here is the important step, you must indent to begin the code inside your function correctly. Python makes use of _whitespace_ to organize code. Lots of other programing languages do not do this, so keep that in mind.

Next you'll see the docstring, this is where you write a basic description of the function. Using Jupyter and Jupyter Notebooks, you'll be able to read these docstrings by pressing Shift+Tab after a function name. Docstrings are not necessary for simple functions, but it's good practice to put them in so you or other people can easily understand the code you write.

After all this you begin writing the code you wish to execute.

The best way to learn functions is by going through examples. So let's try to go through examples that relate back to the various objects and data structures we learned about before.

### Simple example of a function

```python
def say_hello():
    print('hello')
```

### Calling a function with ()

Call the function:

```python
say_hello()
```

    hello

If you forget the parenthesis (), it will simply display the fact that say_hello is a function. Later on we will learn we can actually pass in functions into other functions! But for now, simply remember to call functions with ().

```python
say_hello
```

    <function __main__.say_hello>

### Accepting parameters (arguments)

Let's write a function that greets people with their name.

```python
def greeting(name):
    print(f'Hello {name}')
```

```python
greeting('Jose')
```

    Hello Jose

## Using return

So far we've only seen print() used, but if we actually want to save the resulting variable we need to use the **return** keyword.

Let's see some example that use a <code>return</code> statement. <code>return</code> allows a function to _return_ a result that can then be stored as a variable, or used in whatever manner a user wants.

### Example: Addition function

```python
def add_num(num1,num2):
    return num1+num2
```

```python
add_num(4,5)
```

    9

```python
# Can also save as variable due to return
result = add_num(4,5)
```

```python
print(result)
```

    9

What happens if we input two strings?

```python
add_num('one','two')
```

    'onetwo'

## Very Common Question: "What is the difference between _return_ and _print_?"

**The return keyword allows you to actually save the result of the output of a function as a variable. The print() function simply displays the output to you, but doesn't save it for future use. Let's explore this in more detail**

```python
def print_result(a,b):
    print(a+b)
```

```python
def return_result(a,b):
    return a+b
```

```python
print_result(10,5)
```

    15

```python
# You won't see any output if you run this in a .py script
return_result(10,5)
```

    15

**But what happens if we actually want to save this result for later use?**

```python
my_result = print_result(20,20)
```

    40

```python
my_result
```

```python
type(my_result)
```

    NoneType

**Be careful! Notice how print_result() doesn't let you actually save the result to a variable! It only prints it out, with print() returning None for the assignment!**

```python
my_result = return_result(20,20)
```

```python
my_result
```

    40

```python
my_result + my_result
```

    80

# Adding Logic to Internal Function Operations

So far we know quite a bit about constructing logical statements with Python, such as if/else/elif statements, for and while loops, checking if an item is **in** a list or **not in** a list (Useful Operators Lecture). Let's now see how we can perform these operations within a function.

### Check if a number is even

**Recall the mod operator % which returns the remainder after division, if a number is even then mod 2 (% 2) should be == to zero.**

```python
2 % 2
```

    0

```python
20 % 2
```

    0

```python
21 % 2
```

    1

```python
20 % 2 == 0
```

    True

```python
21 % 2 == 0
```

    False

** Let's use this to construct a function. Notice how we simply return the boolean check.**

```python
def even_check(number):
    return number % 2 == 0
```

```python
even_check(20)
```

    True

```python
even_check(21)
```

    False

### Check if any number in a list is even

Let's return a boolean indicating if **any** number in a list is even. Notice here how **return** breaks out of the loop and exits the function

```python
def check_even_list(num_list):
    # Go through each number
    for number in num_list:
        # Once we get a "hit" on an even number, we return True
        if number % 2 == 0:
            return True
        # Otherwise we don't do anything
        else:
            pass
```

** Is this enough? NO! We're not returning anything if they are all odds!**

```python
check_even_list([1,2,3])
```

    True

```python
check_even_list([1,1,1])
```

** VERY COMMON MISTAKE!! LET'S SEE A COMMON LOGIC ERROR, NOTE THIS IS WRONG!!!**

```python
def check_even_list(num_list):
    # Go through each number
    for number in num_list:
        # Once we get a "hit" on an even number, we return True
        if number % 2 == 0:
            return True
        # This is WRONG! This returns False at the very first odd number!
        # It doesn't end up checking the other numbers in the list!
        else:
            return False
```

```python
# UH OH! It is returning False after hitting the first 1
check_even_list([1,2,3])
```

    False

** Correct Approach: We need to initiate a return False AFTER running through the entire loop**

```python
def check_even_list(num_list):
    # Go through each number
    for number in num_list:
        # Once we get a "hit" on an even number, we return True
        if number % 2 == 0:
            return True
        # Don't do anything if its not even
        else:
            pass
    # Notice the indentation! This ensures we run through the entire for loop
    return False
```

```python
check_even_list([1,2,3])
```

    True

```python
check_even_list([1,3,5])
```

    False

### Return all even numbers in a list

Let's add more complexity, we now will return all the even numbers in a list, otherwise return an empty list.

```python
def check_even_list(num_list):

    even_numbers = []

    # Go through each number
    for number in num_list:
        # Once we get a "hit" on an even number, we append the even number
        if number % 2 == 0:
            even_numbers.append(number)
        # Don't do anything if its not even
        else:
            pass
    # Notice the indentation! This ensures we run through the entire for loop
    return even_numbers
```

```python
check_even_list([1,2,3,4,5,6])
```

    [2, 4, 6]

```python
check_even_list([1,3,5])
```

    []

## Returning Tuples for Unpacking

** Recall we can loop through a list of tuples and "unpack" the values within them**

```python
stock_prices = [('AAPL',200),('GOOG',300),('MSFT',400)]
```

```python
for item in stock_prices:
    print(item)
```

    ('AAPL', 200)
    ('GOOG', 300)
    ('MSFT', 400)

```python
for stock,price in stock_prices:
    print(stock)
```

    AAPL
    GOOG
    MSFT

```python
for stock,price in stock_prices:
    print(price)
```

    200
    300
    400

**Similarly, functions often return tuples, to easily return multiple results for later use.**

Let's imagine the following list:

```python
work_hours = [('Abby',100),('Billy',400),('Cassie',800)]
```

The employee of the month function will return both the name and number of hours worked for the top performer (judged by number of hours worked).

```python
def employee_check(work_hours):

    # Set some max value to intially beat, like zero hours
    current_max = 0
    # Set some empty value before the loop
    employee_of_month = ''

    for employee,hours in work_hours:
        if hours > current_max:
            current_max = hours
            employee_of_month = employee
        else:
            pass

    # Notice the indentation here
    return (employee_of_month,current_max)
```

```python
employee_check(work_hours)
```

    ('Cassie', 800)

## Interactions between functions

Functions often use results from other functions, let's see a simple example through a guessing game. There will be 3 positions in the list, one of which is an 'O', a function will shuffle the list, another will take a player's guess, and finally another will check to see if it is correct. This is based on the classic carnival game of guessing which cup a red ball is under.

**How to shuffle a list in Python**

```python
example = [1,2,3,4,5]
```

```python
from random import shuffle
```

```python
# Note shuffle is in-place
shuffle(example)
```

```python
example
```

    [3, 1, 4, 5, 2]

**OK, let's create our simple game**

```python
mylist = [' ','O',' ']
```

```python
def shuffle_list(mylist):
    # Take in list, and returned shuffle versioned
    shuffle(mylist)

    return mylist
```

```python
mylist
```

    [' ', 'O', ' ']

```python
shuffle_list(mylist)
```

    [' ', ' ', 'O']

```python
def player_guess():

    guess = ''

    while guess not in ['0','1','2']:

        # Recall input() returns a string
        guess = input("Pick a number: 0, 1, or 2:  ")

    return int(guess)
```

```python
player_guess()
```

    Pick a number: 0, 1, or 2:  1





    1

Now we will check the user's guess. Notice we only print here, since we have no need to save a user's guess or the shuffled list.

```python
def check_guess(mylist,guess):
    if mylist[guess] == 'O':
        print('Correct Guess!')
    else:
        print('Wrong! Better luck next time')
        print(mylist)
```

Now we create a little setup logic to run all the functions. Notice how they interact with each other!

```python
# Initial List
mylist = [' ','O',' ']

# Shuffle It
mixedup_list = shuffle_list(mylist)

# Get User's Guess
guess = player_guess()

# Check User's Guess
#------------------------
# Notice how this function takes in the input
# based on the output of other functions!
check_guess(mixedup_list,guess)
```

    Pick a number: 0, 1, or 2:  1
    Wrong! Better luck next time
    [' ', ' ', 'O']

Great! You should now have a basic understanding of creating your own functions to save yourself from repeatedly writing code!
