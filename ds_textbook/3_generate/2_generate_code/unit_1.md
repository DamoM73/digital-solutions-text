# Unit 1: Generate Code

In this section we will look at how we create code. We will look at  basic coding features and the types of operations. 

---
## Basic Features of Programming
Programs are created using six basic features. The skill of a programmer is knowing when and how to use these features.

### Variables
Variables are the names you give to computer memory locations which are used to store values in a computer program. Variables can store data of different types, and different types can do different things. In programming languages, there are two different type systems:

- **dynamic:** type checking only occurs as the code runs, and the type of a variable is allowed to change over its lifetime.
- **static:** type checks are performed without running the program. In most statically typed languages this is done as your program is compiled. The type of a variable is not allowed to change over its lifetime.

Python is a dynamically typed language. 

The Python data types that we will be using are:

- **Strings:** 
    - strings are sequences of character data
    - the string type in Python is called `str`
    - string literals may be delimited using either single or double quotes
- **Integers:**
    - integers are whole numbers
    - the integer type in Python is called `int`
    - there is effectively no limit to how long an integer value can be, but it is constrained by the amount of memory your system has.
- **Floating-Point Numbers:**
    - float values are numbers specified with a decimal point
    - the `float` type in Python designates a floating-point number
    - optionally, the character e or E followed by a positive or negative integer may be appended to specify scientific notation
- **Boolean Type:**
    - objects of Boolean type may have one of two values, `True` or `False`
    - the Boolean type in Python is called `bool`
    - a value that is true in Boolean context is sometimes said to be "truthy" and one that is false in Boolean context is said to be "falsy"
    - the "truthiness" of an object of Boolean type is self-evident: Boolean objects that are equal to `True` are truthy (true), and those equal to `False` are falsy (false)

### Control Structures
Flow of control through any given function is implemented with three basic types of control structures:

- **Sequential:** default mode. Sequential execution of code statements one line after another (like following a recipe)
- **Selection:** used for decisions, branching (choosing between 2 or more alternative paths). 
- **Repetition:** - used for looping, i.e. repeating a piece of code multiple times in a row.

### Data Structures
> Data structures are used to store data in an organized form. No matter what problem are you solving, in one way or another you have to deal with data — whether it's an employee's salary, stock prices, a grocery list, or even a simple telephone directory. {cite}`ulhaq_2018_the`

Based on different scenarios, data will need to be stored in a specific format. 

In Python we will deal with four data structures:
- lists
- tuples
- sets
- dictionaries

#### Lists
A list is defined as an ordered collection of items, and it is one of the essential data structures when using Python. The term "ordered collections" means that each item in a list comes with an order that uniquely identifies them. When creating a list, all the items in the list should be put in square brackets `[` `]` and separated by commas to let Python know that a list has been created.

Here's an example of a list of size 4 `[1,2,3,4]`.

Each data element is assigned a positive numerical value called the Index, which corresponds to the position of that item in the array. The starting index of the list is 0.

Lists can be nested, which means that it can contain any type of object, including other lists.
 
Lists are mutable, which means they can be altered even after being created. A user can search, add, shift, move, and delete elements from a list at their own will. 

When replacing elements in a list, the number of elements added does not need to be equal to the number of elements in the list, and Python will adjust the list as needed. Mutability also enables the user to input additional elements into the list without making any replacements.

#### Tuples
A tuple is an ordered collection of objects. Unlike lists, tuples come with limited functionality.

The primary differing characteristic between lists and tuples is mutability. Lists are mutable, whereas tuples are immutable. Tuples cannot be modified, added, or deleted once they've been created. Lists are defined by using parentheses `(` `)` to enclose the elements, which are separated by commas.

Here's an example of a tuple of size 4 `(1,2,3,4)`.

When writing a tuple with only a single element, the coder must use a comma after the item, for example `(1,)`.

Reasons for using tuples instead of list:
- when the developer does not want the data to be modified 
- when speed is important as tuples use less memory, and they make program execution faster than using lists.

#### Sets
A set is defined as a unique collection of unique elements that do not follow a specific order. 

Sets are used when the existence of an object in a collection of objects is more important than the number of times it appears or the order of the objects. 

Unlike tuples, sets are mutable – they can be modified, added, replaced, or removed. They are defined by using curly brackets `{` `}` to enclose the elements, which are separated by commas.

Here's an example of a set of size 4 `{1,2,3,4}`.

One of the ways that sets are used is when checking whether or not some elements are contained in a set or not. 

#### Dictionaries
Dictionaries in Python is an ordered collection of key-value pairs. Each key-value pair maps the key to its associated value. 

Dictionaries are mutable – they can be modified, added, replaced, or removed. They are defined by using curly brackets `{` `}` to enclose the elements, with a colon `:` separating a key and its value, and each key-pair separated by commas.

Here's an example of a dictionary of size 4 `{"Doh":"Doherty","Dun":"Dunlop","Fly":"Flynn","Nic":"Nichols"}`.

Dictionaries should be used when the data has a unique reference that can be associated with the value.

### Syntax
The syntax of a computer language is the set of rules that defines the combinations of symbols that are considered to be correctly structured statements or expressions in that language. This applies both to programming languages, where the document represents source code, and to markup languages, where the document represents data.

### Libraries
A software library refers to a collection of files, programs, routines, scripts, or functions referenced in the programming code. Python comes with a standard library which provides basic functionality. Python allows you to install additional libraries, as well as create your own.

### Classes
Classes and object are basic building blocks in object-oriented programming languages. A class is written by a programmer in a defined structure to create an object in an object-oriented programming language. It defines a set of properties and methods that are common to all objects of one type.

For example, a class could be a car, which could have a colour field, four tire fields, and a drive method. 

Another related class could be a truck, which would have similar fields, but not be exactly the same as a car. Both a car and a truck could be a kind of a third class which could be called a vehicle class. In this way, the programmer could create the parts of the program that are the same for both the car and the truck in programming the vehicle class, yet the programmer would be free to program how a car is different from a truck without duplicating all of the programming.

Although there is only one class called "car", there could be many objects that are created from the class called "car". And, although there is only one class that is called "truck", many objects of type truck could be created from this class. The class, vehicle, is actually general and there would probably not be any objects that were only of the class "vehicle". 

Inside of classes are two kinds of things: 
- **methods:** can store the code for doing actions; in this example you could have a drive method and a brake method, and maybe a turnRight and turnLeft method. 
- **attributes:** store data; you could have a colour field, a speed field and a size field. 

You can call methods by first making an object of the Car or Truck class, and call it for example `ferrari`, and doing `ferrari.methodName()`. In this case, if we wanted to make the vehicle move, we could do `ferrari.drive(distance)`.

### Scope: Local and Global Variables
In programming, the scope of a name defines the area of a program in which you can unambiguously access that name, such as variables, functions, objects, and so on. A name will only be visible to and accessible by the code in its scope. Several programming languages take advantage of scope for avoiding name collisions and unpredictable behaviours. Most commonly, you'll distinguish two general scopes:

- **Global scope:** The names that you define in this scope are available to all your code.
- **Local scope:** The names that you define in this scope are only available or visible to the code within the scope.

Scope came about because early programming languages (like BASIC) only had global names. With this kind of name, any part of the program could modify any variable at any time, so maintaining and debugging large programs could become a real nightmare. To work with global names, you'd need to keep all the code in mind at the same time to know what the value of a given name is at any time. This was an important side-effect of not having scopes.

Some languages like Python use scope to avoid this kind of problem. When you use a language that implements scope, there's no way for you to access all the variables in a program at all locations in that program. In this case, your ability to access a given name will depend on where you've defined that name.

#### Using the LEGB Rule for Python Scope
Python resolves names using the so-called LEGB rule, which is named after the Python scope for names. The letters in LEGB stand for Local, Enclosing, Global, and Built-in. Here's a quick overview of what these terms mean:

- **Local (or function) scope:** the code block or body of any Python function or lambda expression. This Python scope contains the names that you define inside the function. These names will only be visible from the code of the function. It's created at function call, not at function definition, so you'll have as many different local scopes as function calls. This is true even if you call the same function multiple times, or recursively. Each call will result in a new local scope being created.

- **Enclosing (or nonlocal) scope:** a special scope that only exists for nested functions. If the local scope is an inner or nested function, then the enclosing scope is the scope of the outer or enclosing function. This scope contains the names that you define in the enclosing function. The names in the enclosing scope are visible from the code of the inner and enclosing functions.

- **Global (or module) scope:** the top-most scope in a Python program, script, or module. This Python scope contains all of the names that you define at the top level of a program or a module. Names in this Python scope are visible from everywhere in your code.

- **Built-in scope:** a special Python scope that's created or loaded whenever you run a script or open an interactive session. This scope contains names such as keywords, functions, exceptions, and other attributes that are built into Python. Names in this Python scope are also available from everywhere in your code. It's automatically loaded by Python when you run a program or script.

The LEGB rule is a kind of name lookup procedure, which determines the order in which Python looks up names. For example, if you reference a given name, then Python will look that name up sequentially in the local, enclosing, global, and built-in scope. If the name exists, then you'll get the first occurrence of it. Otherwise, you'll get an error.

#### Scope limitations on actions
|Action|Global Code|Local Code|Nested Function Code|
|:-----|-----------|-----------|--------------------|
|Access or reference names that live in the global scope|Yes|Yes|Yes|
|Modify or update names that live in the global scope|Yes|No (unless declared global)|No (unless declared global)|
|Access or reference names that live in a local scope|No|Yes (its own local scope),No (other local scope)|Yes (its own local scope), No (other local scope)|
|Override names in the built-in scope|Yes|Yes (during function execution)|Yes (during function execution)|
|Access or reference names that live in their enclosing scope|N/A|N/A|Yes
|Modify or update names that live in their enclosing scope|N/A|N/A|No (unless declared nonlocal)|

### Event Triggers
Events are “things” that happen as a result of something occurring. On a webpage, an event can be something that the browser does or something that the user does.

These can include things like the web page finishing loading, text being typed into an input box or a button being clicked.

Many languages call certain code be executed as a result of a certain event occurring. Webpages allow event handler attributes, with JavaScript code, to be added to HTML elements

---
## Operations
Operators are used to perform operations on variables and values.
    
Python divides the operators in the following groups:
- Arithmetic operators
- Assignment operators
- Comparison operators
- Logical operators
- Identity operators
- Membership operators
- Bitwise operators

### Arithmetic Operators
Arithmetic operators are used with numeric values to perform common mathematical operations.

|Operator|Name|Example|
|:-------|:---|:------|
| + |Addition|x + y|
| - |Subtraction|x - y|
| * |Multiplication|x * y|
| / |Division|x / y|
| % |Modulus|x % y|
| ** |Exponentiation|x ** y|
|// |Floor division|x // y|

In Python addition, subtraction, and multiplication are all strait forward and do exactly like you would expect. Note: that brackets `(` and `)` work the same as they would in mathematical equations. 

It is worth checking out how division, modulus, floor division and exponentiation work. Check out the **[arithmetic operators examples](https://mybinder.org/v2/gh/DamoM73/edge-approach-to-digital-solutions/HEAD?labpath=arithmetic_ops.ipynb){:target="\_blank"}**

### Assignment Operators
The standard assignment operator `=` is used to assign values to a variable.

|Operator|Example|Same As|
|:-------|:------|:------|
|= |x = 5|x = 5|
| += |x += 3|x = x + 3|
| -= |x -= 3|x = x - 3|
| \*= |  x \*= 3 |x = x * 3|
| /= |x /= 3|x = x / 3|
| %= |x %= 3|x = x % 3|
| //= |x //= 3|x = x // 3|
| **= |x **= 3|x = x ** 3|

The other assignment operators `+=`, `-+`, `*+`, etc. adjust a variable by operation sign and the value provided. 

Try the code below for an example.
```python
num_1 = 5

print(f"Before: {num_1}")

num_1 += 1

print(f"After: {num_1}")
```

### Comparison Operators
Comparison operators are used to compare two values, and will return a value of `True` or `False`.

|Operator|Name|Example|
|:-------|:---|:------|
| == |Equal|x == y|
|!=|Not equal|x != y|
|>|Greater than|x > y|
|<|Less than|x < y|
|>=|Greater than or equal to|x >= y|
|<=|Less than or equal to|x <= y|

Comparisons can be between values, variables, calculations or even the results of a function call.

Try the code below for examples.
```python
name = "Damien"
threshold = 10

print(4 == 4)
print(name != "Damien")
print(10 > threshold)
print("a" < "c")
print(10 >= threshold)
print(4 <= 15)
```

### Logical Operators
Logical operators are used to combine conditional statements. The truthiness of the conditions is tested, and then operator combines the resulting Boolean values to produce either `True` or `False`.

|Operator|Description|Example|
|:-------|:----------|:------|
|and|Returns True if both statements are true|x < 5 and  x < 10|
|or|Returns True if one of the statements is true|x < 5 or x < 4|
|not|Reverse the result, returns False if the result is true|not(x < 5 and x < 10)|

Check the different permeations below by running the code
```python
print(f"True and True is {True and True}")
print(f"True and False is {True and False}")
print(f"False and True is {False and True}")
print(f"False and False is {False and False}")
print("")
print(f"True or True is {True or True}")
print(f"True or False is {True or False}")
print(f"False or True is {False or True}")
print(f"False or False is {False or False}")
print("")
print(f"Not True is {not True}")
print(f"Not False is {not False}")
```

It is worth noting that in Python the default Truthiness of any object is `True`. This leads to a common mistake like the exmaple below.

In the code below, the condition `10 < 1` is `False` the second condition of `3` gives a `True` and `False and True` is `True` so the code prints `Hello`.

Try it.
```python
if 10 < 1 or 3:
    print("Hello")
```

### Identity Operators
Identity operators are used to compare the objects, not if they are equal, but if they are actually the same object, with the same memory location.

|Operator|Description|Example|
|:-------|:----------|:------|
|is|Returns True if both variables are the same object|x is y|
|is not|Returns True if both variables are not the same object|x is not y|

The code below should highlight the difference.
```python
list_1 = []
list_2 = []
list_3 = list_1
 
print(list_1 == list_2)
print(list_1 is list_2)
print(list_1 == list_3)
print(list_1 is list_3)
```

### Membership Operators
Membership operators are used to test if a sequence is presented in an object (list, tuple or string).

|Operator|Description|Example|
|:-------|:----------|:------|
|in|Returns True if a sequence with the specified value is present in the object|x in y|
|not in|Returns True if a sequence with the specified value is not present in the object|x not in y|

Run the code to see who it works.
```python
print("a" in "cat")
print("a" in ["cat", "dog", "goat"])
print(1 in (34,14,1,5))
```

### Bitwise Operators
Bitwise operators are used to compare (binary) numbers. Realistically we are not going to use these, but it worth knowing they exist in case you come across them in some code.

|Operator|Name|Description|
|:-|:-|:-|
|&|AND|Sets each bit to 1 if both bits are 1|
|/||OR|Sets each bit to 1 if one of two bits is 1|
|^|XOR|Sets each bit to 1 if only one of two bits is 1|
|~|NOT|Inverts all the bits|
|<<|Zero fill left shift|Shift left by pushing zeros in from the right and let the leftmost bits fall off|
|>>|Signed right shift|Shift right by pushing copies of the leftmost bit in from the left, and let the rightmost bits fall off|