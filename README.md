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
```

    3

```python
# Subtraction
2-1
```

    1

```python
# Multiplication
2*2
```

    4

```python
# Division
3/2
```

    1.5

```python
# Floor Division
7//4
```

    1

**Whoa! What just happened? Last time I checked, 7 divided by 4 equals 1.75 not 1!**

The reason we get this result is because we are using "_floor_" division. The // operator (two forward slashes) truncates the decimal without rounding, and returns an integer result.

**So what if we just want the remainder after division?**

```python
# Modulo
7%4
```

    3

4 goes into 7 once, with a remainder of 3. The % operator returns the remainder after division.

### Arithmetic continued

```python
# Powers
2**3
```

    8

```python
# Can also do roots this way
4**0.5
```

    2.0

```python
# Order of Operations followed in Python
2 + 10 * 10 + 3
```

    105

```python
# Can use parentheses to specify orders
(2+10) * (10+3)
```

    156

---

---

---

# Variable

## Rules for variable names

- names can not start with a number
- names can not contain spaces, use \_ intead
- names can not contain any of these symbols:

      :'",<>/?|\!@#%^&*~-+

- it's considered best practice ([PEP8](https://www.python.org/dev/peps/pep-0008/#function-and-variable-names)) that names are lowercase with underscores
- avoid using Python built-in keywords like `list` and `str`
- avoid using the single characters `l` (lowercase letter el), `O` (uppercase letter oh) and `I` (uppercase letter eye) as they can be confused with `1` and `0`

## Dynamic Typing

Python uses _dynamic typing_, meaning you can reassign variables to different data types. This makes Python very flexible in assigning data types; it differs from other languages that are _statically typed_.

```python
my_dogs = 2
```

```python
my_dogs
```

    2

```python
my_dogs = ['Sammy', 'Frankie']
```

```python
my_dogs
```

    ['Sammy', 'Frankie']

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

```python
a
```

    5

Here we assigned the integer object `5` to the variable name `a`.<br>Let's assign `a` to something else:

```python
a = 10
```

```python
a
```

    10

You can now use `a` in place of the number `10`:

```python
a + a
```

    20

## Reassigning Variables

Python lets you reassign variables with a reference to the same object.

```python
a = a + 10
```

```python
a
```

    20

There's actually a shortcut for this. Python lets you add, subtract, multiply and divide numbers with reassignment using `+=`, `-=`, `*=`, and `/=`.

```python
a += 10
```

```python
a
```

    30

```python
a *= 2
```

```python
a
```

    60

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
```

    int

```python
a = (1,2)
```

```python
type(a)
```

    tuple

## Simple Exercise

This shows how variables make calculations more readable and easier to follow.

```python
my_income = 100
tax_rate = 0.1
my_taxes = my_income * tax_rate
```

```python
my_taxes
```

    10.0

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
```

    'hello'

```python
# Entire phrase
'This is also a string'
```

    'This is also a string'

```python
# We can also use double quote
"String built with double quotes"
```

    'String built with double quotes'

```python
# Be careful with quotes!
' I'm using single quotes, but this will create an error'
```

      File "<ipython-input-4-da9a34b3dc31>", line 2
        ' I'm using single quotes, but this will create an error'
            ^
    SyntaxError: invalid syntax

The reason for the error above is because the single quote in <code>I'm</code> stopped the string. You can use combinations of double and single quotes to get the complete statement.

```python
"Now I'm ready to use the single quotes inside a string!"
```

    "Now I'm ready to use the single quotes inside a string!"

## Printing a String

Using terminal with just a string in a command will automatically output strings, but the correct way to display strings in your output is by using a print function.

```python
# We can simply declare a string
'Hello World'
```

    'Hello World'

We can use a print statement to print a string.

```python
print('Hello World 1')
print('Hello World 2')
print('Use \n to print a new line')
print('\n')
print('See what I mean?')
```

    Hello World 1
    Hello World 2
    Use
     to print a new line


    See what I mean?

## String Basics

We can also use a function called len() to check the length of a string!

```python
len('Hello World')
```

    11

Python's built-in len() function counts all of the characters in the string, including spaces and punctuation.

## String Indexing

We know strings are a sequence, which means Python can use indexes to call parts of the sequence. Let's learn how this works.

In Python, we use brackets <code>[]</code> after an object to call its index. We should also note that indexing starts at 0 for Python. Let's create a new object called <code>s</code> and then walk through a few examples of indexing.

```python
# Assign s as a string
s = 'Hello World'
```

```python
#Check
s
```

    'Hello World'

```python
# Print the object
print(s)
```

    Hello World

Let's start indexing!

```python
# Show first element (in this case a letter)
s[0]
```

    'H'

```python
s[1]
```

    'e'

```python
s[2]
```

    'l'

We can use a <code>:</code> to perform _slicing_ which grabs everything up to a designated point. For example:

```python
# Grab everything past the first term all the way to the length of s which is len(s)
s[1:]
```

    'ello World'

```python
# Note that there is no change to the original s
s
```

    'Hello World'

```python
# Grab everything UP TO the 3rd index
s[:3]
```

    'Hel'

Note the above slicing. Here we're telling Python to grab everything from 0 up to 3. It doesn't include the 3rd index. You'll notice this a lot in Python, where statements and are usually in the context of "up to, but not including".

```python
#Everything
s[:]
```

    'Hello World'

We can also use negative indexing to go backwards.

```python
# Last letter (one index behind 0 so it loops back around)
s[-1]
```

    'd'

```python
# Grab everything but the last letter
s[:-1]
```

    'Hello Worl'

We can also use index and slice notation to grab elements of a sequence by a specified step size (the default is 1). For instance we can use two colons in a row and then a number specifying the frequency to grab elements. For example:

```python
# Grab everything, but go in steps size of 1
s[::1]
```

    'Hello World'

```python
# Grab everything, but go in step sizes of 2
s[::2]
```

    'HloWrd'

```python
# We can use this to print a string backwards
s[::-1]
```

    'dlroW olleH'

## String Properties

It's important to note that strings have an important property known as _immutability_. This means that once a string is created, the elements within it can not be changed or replaced. For example:

```python
s
```

    'Hello World'

```python
# Let's try to change the first letter to 'x'
s[0] = 'x'
```

    ----> 2 s[0] = 'x'


    TypeError: 'str' object does not support item assignment

Notice how the error tells us directly what we can't do, change the item assignment!

Something we _can_ do is concatenate strings!

```python
s
```

    'Hello World'

```python
# Concatenate strings!
s + ' concatenate me!'
```

    'Hello World concatenate me!'

```python
# We can reassign s completely though!
s = s + ' concatenate me!'
```

```python
print(s)
```

    Hello World concatenate me!

```python
s
```

    'Hello World concatenate me!'

We can use the multiplication symbol to create repetition!

```python
letter = 'z'
```

```python
letter*10
```

    'zzzzzzzzzz'

## Basic Built-in String methods

Objects in Python usually have built-in methods. These methods are functions inside the object (we will learn about these in much more depth later) that can perform actions or commands on the object itself.

We call methods with a period and then the method name. Methods are in the form:

object.method(parameters)

Where parameters are extra arguments we can pass into the method. Don't worry if the details don't make 100% sense right now. Later on we will be creating our own objects and functions!

Here are some examples of built-in methods in strings:

```python
s
```

    'Hello World concatenate me!'

```python
# Upper Case a string
s.upper()
```

    'HELLO WORLD CONCATENATE ME!'

```python
# Lower case
s.lower()
```

    'hello world concatenate me!'

```python
# Split a string by blank space (this is the default)
s.split()
```

    ['Hello', 'World', 'concatenate', 'me!']

```python
# Split by a specific element (doesn't include the element that was split on)
s.split('W')
```

    ['Hello ', 'orld concatenate me!']

There are many more methods than the ones covered here. Visit the Advanced String section to find out more!

## Print Formatting

We can use the .format() method to add formatted objects to printed string statements.

The easiest way to show this is through an example:

```python
'Insert another string with curly brackets: {}'.format('The inserted string')
```

    'Insert another string with curly brackets: The inserted string'

We will revisit this string formatting topic in later sections when we are building our projects!

---

---

---

# String Formatting

String formatting lets you inject items into a string rather than trying to chain items together using commas or string concatenation. As a quick comparison, consider:

    player = 'Thomas'
    points = 33

    'Last night, '+player+' scored '+str(points)+' points.'  # concatenation

    f'Last night, {player} scored {points} points.'          # string formatting

There are three ways to perform string formatting.

- The oldest method involves placeholders using the modulo `%` character.
- An improved technique uses the `.format()` string method.
- The newest method, introduced with Python 3.6, uses formatted string literals, called _f-strings_.

Since you will likely encounter all three versions in someone else's code, we describe each of them here.

## Formatting with placeholders

You can use <code>%s</code> to inject strings into your print statements. The modulo `%` is referred to as a "string formatting operator".

```python
print("I'm going to inject %s here." %'something')
```

    I'm going to inject something here.

You can pass multiple items by placing them inside a tuple after the `%` operator.

```python
print("I'm going to inject %s text here, and %s text here." %('some','more'))
```

    I'm going to inject some text here, and more text here.

You can also pass variable names:

```python
x, y = 'some', 'more'
print("I'm going to inject %s text here, and %s text here."%(x,y))
```

    I'm going to inject some text here, and more text here.

### Format conversion methods.

It should be noted that two methods <code>%s</code> and <code>%r</code> convert any python object to a string using two separate methods: `str()` and `repr()`. We will learn more about these functions later on in the course, but you should note that `%r` and `repr()` deliver the _string representation_ of the object, including quotation marks and any escape characters.

```python
print('He said his name was %s.' %'Fred')
print('He said his name was %r.' %'Fred')
```

    He said his name was Fred.
    He said his name was 'Fred'.

As another example, `\t` inserts a tab into a string.

```python
print('I once caught a fish %s.' %'this \tbig')
print('I once caught a fish %r.' %'this \tbig')
```

    I once caught a fish this 	big.
    I once caught a fish 'this \tbig'.

The `%s` operator converts whatever it sees into a string, including integers and floats. The `%d` operator converts numbers to integers first, without rounding. Note the difference below:

```python
print('I wrote %s programs today.' %3.75)
print('I wrote %d programs today.' %3.75)
```

    I wrote 3.75 programs today.
    I wrote 3 programs today.

### Padding and Precision of Floating Point Numbers

Floating point numbers use the format <code>%5.2f</code>. Here, <code>5</code> would be the minimum number of characters the string should contain; these may be padded with whitespace if the entire number does not have this many digits. Next to this, <code>.2f</code> stands for how many numbers to show past the decimal point. Let's see some examples:

```python
print('Floating point numbers: %5.2f' %(13.144))
```

    Floating point numbers: 13.14

```python
print('Floating point numbers: %1.0f' %(13.144))
```

    Floating point numbers: 13

```python
print('Floating point numbers: %1.5f' %(13.144))
```

    Floating point numbers: 13.14400

```python
print('Floating point numbers: %10.2f' %(13.144))
```

    Floating point numbers:      13.14

```python
print('Floating point numbers: %25.2f' %(13.144))
```

    Floating point numbers:                     13.14

For more information on string formatting with placeholders visit https://docs.python.org/3/library/stdtypes.html#old-string-formatting

### Multiple Formatting

Nothing prohibits using more than one conversion tool in the same print statement:

```python
print('First: %s, Second: %5.2f, Third: %r' %('hi!',3.1415,'bye!'))
```

    First: hi!, Second:  3.14, Third: 'bye!'

## Formatting with the `.format()` method

A better way to format objects into your strings for print statements is with the string `.format()` method. The syntax is:

    'String here {} then also {}'.format('something1','something2')

For example:

```python
print('This is a string with an {}'.format('insert'))
```

    This is a string with an insert

### The .format() method has several advantages over the %s placeholder method:

#### 1. Inserted objects can be called by index position:

```python
print('The {2} {1} {0}'.format('fox','brown','quick'))
```

    The quick brown fox

#### 2. Inserted objects can be assigned keywords:

```python
print('First Object: {a}, Second Object: {b}, Third Object: {c}'.format(a=1,b='Two',c=12.3))
```

    First Object: 1, Second Object: Two, Third Object: 12.3

#### 3. Inserted objects can be reused, avoiding duplication:

```python
print('A %s saved is a %s earned.' %('penny','penny'))
# vs.
print('A {p} saved is a {p} earned.'.format(p='penny'))
```

    A penny saved is a penny earned.
    A penny saved is a penny earned.

### Alignment, padding and precision with `.format()`

Within the curly braces you can assign field lengths, left/right alignments, rounding parameters and more

```python
print('{0:8} | {1:9}'.format('Fruit', 'Quantity'))
print('{0:8} | {1:9}'.format('Apples', 3.))
print('{0:8} | {1:9}'.format('Oranges', 10))
```

    Fruit    | Quantity
    Apples   |       3.0
    Oranges  |        10

By default, `.format()` aligns text to the left, numbers to the right. You can pass an optional `<`,`^`, or `>` to set a left, center or right alignment:

```python
print('{0:<8} | {1:^8} | {2:>8}'.format('Left','Center','Right'))
print('{0:<8} | {1:^8} | {2:>8}'.format(11,22,33))
```

    Left     |  Center  |    Right
    11       |    22    |       33

You can precede the aligment operator with a padding character

```python
print('{0:=<8} | {1:-^8} | {2:.>8}'.format('Left','Center','Right'))
print('{0:=<8} | {1:-^8} | {2:.>8}'.format(11,22,33))
```

    Left==== | -Center- | ...Right
    11====== | ---22--- | ......33

Field widths and float precision are handled in a way similar to placeholders. The following two print statements are equivalent:

```python
print('This is my ten-character, two-decimal number:%10.2f' %13.579)
print('This is my ten-character, two-decimal number:{0:10.2f}'.format(13.579))
```

    This is my ten-character, two-decimal number:     13.58
    This is my ten-character, two-decimal number:     13.58

Note that there are 5 spaces following the colon, and 5 characters taken up by 13.58, for a total of ten characters.

For more information on the string `.format()` method visit https://docs.python.org/3/library/string.html#formatstrings

## Formatted String Literals (f-strings)

Introduced in Python 3.6, f-strings offer several benefits over the older `.format()` string method described above. For one, you can bring outside variables immediately into to the string rather than pass them as arguments through `.format(var)`.

```python
name = 'Fred'

print(f"He said his name is {name}.")
```

    He said his name is Fred.

Pass `!r` to get the string representation:

```python
print(f"He said his name is {name!r}")
```

    He said his name is 'Fred'

#### Float formatting follows `"result: {value:{width}.{precision}}"`

Where with the `.format()` method you might see `{value:10.4f}`, with f-strings this can become `{value:{10}.{6}}`

```python
num = 23.45678
print("My 10 character, four decimal number is:{0:10.4f}".format(num))
print(f"My 10 character, four decimal number is:{num:{10}.{6}}")
```

    My 10 character, four decimal number is:   23.4568
    My 10 character, four decimal number is:   23.4568

Note that with f-strings, _precision_ refers to the total number of digits, not just those following the decimal. This fits more closely with scientific notation and statistical analysis. Unfortunately, f-strings do not pad to the right of the decimal, even if precision allows it:

```python
num = 23.45
print("My 10 character, four decimal number is:{0:10.4f}".format(num))
print(f"My 10 character, four decimal number is:{num:{10}.{6}}")
```

    My 10 character, four decimal number is:   23.4500
    My 10 character, four decimal number is:     23.45

If this becomes important, you can always use `.format()` method syntax inside an f-string:

```python
num = 23.45
print("My 10 character, four decimal number is:{0:10.4f}".format(num))
print(f"My 10 character, four decimal number is:{num:10.4f}")
```

    My 10 character, four decimal number is:   23.4500
    My 10 character, four decimal number is:   23.4500

For more info on formatted string literals visit https://docs.python.org/3/reference/lexical_analysis.html#f-strings

That is the basics of string formatting!

---

---

---

# Lists

Earlier when discussing strings we introduced the concept of a _sequence_ in Python. Lists can be thought of the most general version of a _sequence_ in Python. Unlike strings, they are mutable, meaning the elements inside a list can be changed!

In this section we will learn about:

    1.) Creating lists
    2.) Indexing and Slicing Lists
    3.) Basic List Methods
    4.) Nesting Lists
    5.) Introduction to List Comprehensions

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
```

    4

### Indexing and Slicing

Indexing and slicing work just like in strings. Let's make a new list to remind ourselves of how this works:

```python
my_list = ['one','two','three',4,5]
```

```python
# Grab element at index 0
my_list[0]
```

    'one'

```python
# Grab index 1 and everything past it
my_list[1:]
```

    ['two', 'three', 4, 5]

```python
# Grab everything UP TO index 3
my_list[:3]
```

    ['one', 'two', 'three']

We can also use + to concatenate lists, just like we did for strings.

```python
my_list + ['new item']
```

    ['one', 'two', 'three', 4, 5, 'new item']

Note: This doesn't actually change the original list!

```python
my_list
```

    ['one', 'two', 'three', 4, 5]

You would have to reassign the list to make the change permanent.

```python
# Reassign
my_list = my_list + ['add new item permanently']
```

```python
my_list
```

    ['one', 'two', 'three', 4, 5, 'add new item permanently']

We can also use the \* for a duplication method similar to strings:

```python
# Make the list double
my_list * 2
```

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

```python
# Again doubling not permanent
my_list
```

    ['one', 'two', 'three', 4, 5, 'add new item permanently']

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
```

```python
# Show
list1
```

    [1, 2, 3, 'append me!']

Use **pop** to "pop off" an item from the list. By default pop takes off the last index, but you can also specify which index to pop off. Let's see an example:

```python
# Pop off the 0 indexed item
list1.pop(0)
```

    1

```python
# Show
list1
```

    [2, 3, 'append me!']

```python
# Assign the popped element, remember default popped index is -1
popped_item = list1.pop()
```

```python
popped_item
```

    'append me!'

```python
# Show remaining list
list1
```

    [2, 3]

It should also be noted that lists indexing will return an error if there is no element at that index. For example:

```python
list1[100]
```

    ---------------------------------------------------------------------------

    IndexError                                Traceback (most recent call last)

    <ipython-input-22-af6d2015fa1f> in <module>()
    ----> 1 list1[100]


    IndexError: list index out of range

We can use the **sort** method and the **reverse** methods to also effect your lists:

```python
new_list = ['a','e','x','b','c']
```

```python
#Show
new_list
```

    ['a', 'e', 'x', 'b', 'c']

```python
# Use reverse to reverse order (this is permanent!)
new_list.reverse()
```

```python
new_list
```

    ['c', 'b', 'x', 'e', 'a']

```python
# Use sort to sort the list (in this case alphabetical order, but for numbers it will go ascending)
new_list.sort()
```

```python
new_list
```

    ['a', 'b', 'c', 'e', 'x']

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
```

```python
# Show
matrix
```

    [[1, 2, 3], [4, 5, 6], [7, 8, 9]]

We can again use indexing to grab elements, but now there are two levels for the index. The items in the matrix object, and then the items inside that list!

```python
# Grab first item in matrix object
matrix[0]
```

    [1, 2, 3]

```python
# Grab first item of the first item in the matrix object
matrix[0][0]
```

    1

# List Comprehensions

Python has an advanced feature called list comprehensions. They allow for quick construction of lists. To fully understand list comprehensions we need to understand for loops. So don't worry if you don't completely understand this section, and feel free to just skip it since we will return to this topic later.

But in case you want to know now, here are a few examples!

```python
# Build a list comprehension by deconstructing a for loop within a []
first_col = [row[0] for row in matrix]
```

```python
first_col
```

    [1, 4, 7]

We used a list comprehension here to grab the first element of every row in the matrix object. We will cover this in much more detail later on!

For more advanced methods and features of lists in Python, check out the Advanced Lists section later on in this course!

---

---

---

# Dictionaries

We've been learning about _sequences_ in Python but now we're going to switch gears and learn about _mappings_ in Python. If you're familiar with other languages you can think of these Dictionaries as hash tables.

This section will serve as a brief introduction to dictionaries and consist of:

    1.) Constructing a Dictionary
    2.) Accessing objects from a dictionary
    3.) Nesting Dictionaries
    4.) Basic Dictionary Methods

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
```

    'value2'

Its important to note that dictionaries are very flexible in the data types they can hold. For example:

```python
my_dict = {'key1':123,'key2':[12,23,33],'key3':['item0','item1','item2']}
```

```python
# Let's call items from the dictionary
my_dict['key3']
```

    ['item0', 'item1', 'item2']

```python
# Can call an index on that value
my_dict['key3'][0]
```

    'item0'

```python
# Can then even call methods on that value
my_dict['key3'][0].upper()
```

    'ITEM0'

We can affect the values of a key as well. For instance:

```python
my_dict['key1']
```

    123

```python
# Subtract 123 from the value
my_dict['key1'] = my_dict['key1'] - 123
```

```python
#Check
my_dict['key1']
```

    0

A quick note, Python has a built-in method of doing a self subtraction or addition (or multiplication or division). We could have also used += or -= for the above statement. For example:

```python
# Set the object equal to itself minus 123
my_dict['key1'] -= 123
my_dict['key1']
```

    -123

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
```

    {'animal': 'Dog', 'answer': 42}

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
```

    'value'

## A few Dictionary Methods

There are a few methods we can call on a dictionary. Let's get a quick introduction to a few of them:

```python
# Create a typical dictionary
d = {'key1':1,'key2':2,'key3':3}
```

```python
# Method to return a list of all keys
d.keys()
```

    dict_keys(['key1', 'key2', 'key3'])

```python
# Method to grab all values
d.values()
```

    dict_values([1, 2, 3])

```python
# Method to return tuples of all items  (we'll learn about tuples soon)
d.items()
```

    dict_items([('key1', 1), ('key2', 2), ('key3', 3)])

Hopefully you now have a good basic understanding how to construct dictionaries. There's a lot more to go into here, but we will revisit dictionaries at later time. After this section all you need to know is how to create a dictionary and how to retrieve values from it.

---

---

---

# Tuples

In Python tuples are very similar to lists, however, unlike lists they are _immutable_ meaning they can not be changed. You would use tuples to present things that shouldn't be changed, such as days of the week, or dates on a calendar.

In this section, we will get a brief overview of the following:

    1.) Constructing Tuples
    2.) Basic Tuple Methods
    3.) Immutability
    4.) When to Use Tuples

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
```

    3

```python
# Can also mix object types
t = ('one',2)

# Show
t
```

    ('one', 2)

```python
# Use indexing just like we did in lists
t[0]
```

    'one'

```python
# Slicing just like a list
t[-1]
```

    2

## Basic Tuple Methods

Tuples have built-in methods, but not as many as lists do. Let's look at two of them:

```python
# Use .index to enter a value and return the index
t.index('one')
```

    0

```python
# Use .count to count the number of times a value appears
t.count('one')
```

    1

## Immutability

It can't be stressed enough that tuples are immutable. To drive that point home:

```python
t[0]= 'change'
```

    ----> 1 t[0]= 'change'


    TypeError: 'tuple' object does not support item assignment

Because of this immutability, tuples can't grow. Once a tuple is made we can not add to it.

```python
t.append('nope')
```

    ---------------------------------------------------------------------------

    AttributeError                            Traceback (most recent call last)

    <ipython-input-9-b75f5b09ac19> in <module>()
    ----> 1 t.append('nope')


    AttributeError: 'tuple' object has no attribute 'append'

## When to use Tuples

You may be wondering, "Why bother using tuples when they have fewer available methods?" To be honest, tuples are not used as often as lists in programming, but are used when immutability is necessary. If in your program you are passing around an object and need to make sure it does not get changed, then a tuple becomes your solution. It provides a convenient source of data integrity.

You should now be able to create and use tuples in your programming as well as have an understanding of their immutability.

Up next Files!

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
```

    {1}

Note the curly brackets. This does not indicate a dictionary! Although you can draw analogies as a set being a dictionary with only keys.

We know that a set has only unique entries. So what happens when we try to add something that is already in a set?

```python
# Add a different element
x.add(2)
```

```python
#Show
x
```

    {1, 2}

```python
# Try to add the same element
x.add(1)
```

```python
#Show
x
```

    {1, 2}

Notice how it won't place another 1 there. That's because a set is only concerned with unique elements! We can cast a list with multiple repeat elements to a set to get the unique elements. For example:

```python
# Create a list with repeats
list1 = [1,1,2,2,3,4,5,6,1,1]
```

```python
# Cast as set to get unique values
set(list1)
```

    {1, 2, 3, 4, 5, 6}

## Booleans

Python comes with Booleans (with predefined True and False displays that are basically just the integers 1 and 0). It also has a placeholder object called None. Let's walk through a few quick examples of Booleans (we will dive deeper into them later in this course).

```python
# Set object to be a boolean
a = True
```

```python
#Show
a
```

    True

We can also use comparison operators to create booleans. We will go over all the comparison operators later on in the course.

```python
# Output is boolean
1 > 2
```

    False

We can use None as a placeholder for an object that we don't want to reassign yet:

```python
# None placeholder
b = None
```

```python
# Show
print(b)
```

    None

Thats it! You should now have a basic understanding of Python objects and data structure types. Next, go ahead and do the assessment test!

---

---

---

# Files

Python uses file objects to interact with external files on your computer. These file objects can be any sort of file you have on your computer, whether it be an audio file, a text file, emails, Excel documents, etc. Note: You will probably need to install certain libraries or modules to interact with those various file types, but they are easily available. (We will cover downloading modules later on in the course).

Python has a built-in open function that allows us to open and play with basic file types. First we will need a file though. We're going to use some IPython magic to create a text file!

## IPython Writing a File

#### This function is specific to jupyter notebooks! Alternatively, quickly create a simple .txt file with sublime text editor.

```python
%%writefile test.txt
Hello, this is a quick test file.
```

    Overwriting test.txt

## Python Opening a file

Let's being by opening the file test.txt that is located in the same directory as this notebook. For now we will work with files located in the same directory as the notebook or .py script you are using.

It is very easy to get an error on this step:

```python
myfile = open('whoops.txt')
```

    ---------------------------------------------------------------------------

    FileNotFoundError                         Traceback (most recent call last)

    <ipython-input-1-dafe28ee473f> in <module>()
    ----> 1 myfile = open('whoops.txt')


    FileNotFoundError: [Errno 2] No such file or directory: 'whoops.txt'

To avoid this error,make sure your .txt file is saved in the same location as your notebook, to check your notebook location, use **pwd**:

```python
pwd
```

    'C:\\Users\\Marcial\\Pierian-Data-Courses\\Complete-Python-3-Bootcamp\\00-Python Object and Data Structure Basics'

**Alternatively, to grab files from any location on your computer, simply pass in the entire file path. **

For Windows you need to use double \ so python doesn't treat the second \ as an escape character, a file path is in the form:

    myfile = open("C:\\Users\\YourUserName\\Home\\Folder\\myfile.txt")

For MacOS and Linux you use slashes in the opposite direction:

    myfile = open("/Users/YouUserName/Folder/myfile.txt")

```python
# Open the text.txt we made earlier
my_file = open('test.txt')
```

```python
# We can now read the file
my_file.read()
```

    'Hello, this is a quick test file.'

```python
# But what happens if we try to read it again?
my_file.read()
```

    ''

This happens because you can imagine the reading "cursor" is at the end of the file after having read it. So there is nothing left to read. We can reset the "cursor" like this:

```python
# Seek to the start of file (index 0)
my_file.seek(0)
```

    0

```python
# Now read again
my_file.read()
```

    'Hello, this is a quick test file.'

You can read a file line by line using the readlines method. Use caution with large files, since everything will be held in memory. We will learn how to iterate over large files later in the course.

```python
# Readlines returns a list of the lines in the file
my_file.seek(0)
my_file.readlines()
```

    ['Hello, this is a quick test file.']

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
```

    18

```python
# Read the file
my_file.seek(0)
my_file.read()
```

    'This is a new line'

```python
my_file.close()  # always do this when you're done with a file
```

## Appending to a File

Passing the argument `'a'` opens the file and puts the pointer at the end, so anything written is appended. Like `'w+'`, `'a+'` lets us read and write to a file. If the file does not exist, one will be created.

```python
my_file = open('test.txt','a+')
my_file.write('\nThis is text being appended to test.txt')
my_file.write('\nAnd another line here.')
```

    23

```python
my_file.seek(0)
print(my_file.read())
```

    This is a new line
    This is text being appended to test.txt
    And another line here.

```python
my_file.close()
```

### Appending with `%%writefile`

We can do the same thing using IPython cell magic:

```python
%%writefile -a test.txt

This is text being appended to test.txt
And another line here.
```

    Appending to test.txt

Add a blank space if you want the first line to begin on its own line, as Jupyter won't recognize escape sequences like `\n`

## Iterating through a File

Lets get a quick preview of a for loop by iterating over a text file. First let's make a new text file with some IPython Magic:

```python
%%writefile test.txt
First Line
Second Line
```

    Overwriting test.txt

Now we can use a little bit of flow to tell the program to for through every line of the file and do something:

```python
for line in open('test.txt'):
    print(line)
```

    First Line

    Second Line

Don't worry about fully understanding this yet, for loops are coming up soon. But we'll break down what we did above. We said that for every line in this text file, go ahead and print that line. It's important to note a few things here:

1. We could have called the "line" object anything (see example below).
2. By not calling `.read()` on the file, the whole text file was not stored in memory.
3. Notice the indent on the second line for print. This whitespace is required in Python.

```python
# Pertaining to the first point above
for asdf in open('test.txt'):
    print(asdf)
```

    First Line

    Second Line

We'll learn a lot more about this later, but up next: Sets and Booleans!

---

---

---

## Test your knowledge

** Answer the following questions **

Write a brief description of all the following Object Types and Data Structures we've learned about:

## Numbers

Write an equation that uses multiplication, division, an exponent, addition, and subtraction that is equal to 100.25.

Hint: This is just to test your memory of the basic arithmetic commands, work backwards from 100.25

```python
# Your answer is probably different
(60 + (10 ** 2) / 4 * 7) - 134.75
```

    100.25

Answer these 3 questions without typing code. Then type code to check your answer.

    What is the value of the expression 4 * (6 + 5)

    What is the value of the expression 4 * 6 + 5

    What is the value of the expression 4 + 6 * 5

```python
4 * (6 + 5)
```

    44

```python
4 * 6 + 5
```

    29

```python
4 + 6 * 5
```

    34

What is the _type_ of the result of the expression 3 + 1.5 + 4?

**Answer: Floating Point Number**

What would you use to find a number’s square root, as well as its square?

```python
# Square root:
100 ** 0.5
```

    10.0

```python
# Square:
10 ** 2
```

    100

## Strings

Given the string 'hello' give an index command that returns 'e'. Enter your code in the cell below:

```python
s = 'hello'
# Print out 'e' using indexing

s[1]
```

    'e'

Reverse the string 'hello' using slicing:

```python
s ='hello'
# Reverse the string using slicing

s[::-1]
```

    'olleh'

Given the string 'hello', give two methods of producing the letter 'o' using indexing.

```python
s ='hello'
# Print out the 'o'

# Method 1:

s[-1]
```

    'o'

```python
# Method 2:

s[4]
```

    'o'

## Lists

Build this list [0,0,0] two separate ways.

```python
# Method 1:
[0]*3
```

    [0, 0, 0]

```python
# Method 2:
list2 = [0,0,0]
list2
```

    [0, 0, 0]

Reassign 'hello' in this nested list to say 'goodbye' instead:

```python
list3 = [1,2,[3,4,'hello']]
```

```python
list3[2][2] = 'goodbye'
```

```python
list3
```

    [1, 2, [3, 4, 'goodbye']]

Sort the list below:

```python
list4 = [5,3,4,6,1]
```

```python
# Method 1:
sorted(list4)
```

    [1, 3, 4, 5, 6]

```python
# Method 2:
list4.sort()
list4
```

    [1, 3, 4, 5, 6]

## Dictionaries

Using keys and indexing, grab the 'hello' from the following dictionaries:

```python
d = {'simple_key':'hello'}
# Grab 'hello'

d['simple_key']
```

    'hello'

```python
d = {'k1':{'k2':'hello'}}
# Grab 'hello'

d['k1']['k2']
```

    'hello'

```python
# Getting a little tricker
d = {'k1':[{'nest_key':['this is deep',['hello']]}]}
```

```python
# This was harder than I expected...
d['k1'][0]['nest_key'][1][0]
```

    'hello'

```python
# This will be hard and annoying!
d = {'k1':[1,2,{'k2':['this is tricky',{'tough':[1,2,['hello']]}]}]}
```

```python
# Phew!
d['k1'][2]['k2'][1]['tough'][2][0]
```

    'hello'

Can you sort a dictionary? Why or why not?

**Answer: No! Because normal dictionaries are _mappings_ not a sequence. **

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
```

    {1, 2, 3, 4, 11, 22, 33}

## Booleans

For the following quiz questions, we will get a preview of comparison operators. In the table below, a=3 and b=4.

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
<td> (a != b) is true.</td>
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

What will be the resulting Boolean of the following pieces of code (answer fist then check by typing it in!)

```python
# Answer before running cell
2 > 3
```

    False

```python
# Answer before running cell
3 <= 2
```

    False

```python
# Answer before running cell
3 == 2.0
```

    False

```python
# Answer before running cell
3.0 == 3
```

    True

```python
# Answer before running cell
4**0.5 != 2
```

    False

Final Question: What is the boolean output of the cell block below?

```python
# two nested lists
l_one = [1,2,[3,4]]
l_two = [1,2,{'k1':4}]

# True or False?
l_one[2][0] >= l_two[2]['k1']
```

    False

---

---

---
