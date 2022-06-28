# Unit 1: Generate Code

In this section we will look at how we create code. We will look at  basic coding features and the types of operations. 

---
## Basic Features of Programming
Programs are created using six basic features. The skill of a programmer is knowing when and how to use these features.

### Variables
Variables are the names you give to computer memory locations which are used to store values in a computer program. Variables can store data of different types, and different variable types can do different things. 

In programming languages, there are two different type systems:

- **dynamic:** type checking only occurs as the code runs, and the type of a variable is allowed to change over its lifetime.
- **static:** type checks are performed without running the program. In most statically typed languages this is done as your program is compiled. The type of a variable is not allowed to change over its lifetime.

#### In Python

Python is a dynamically typed language. 

The Python data types that we will be using are:

- **Strings:** 
    - strings are sequences of character data
    - the string type in Python is called `str`
    - string literals may be delimited using either single or double quotes
    - **<a href="https://www.w3schools.com/python/python_strings.asp" target="_blank">Strings refresher</a>**
- **Integers:**
    - integers are whole numbers
    - the integer type in Python is called `int`
    - there is effectively no limit to how long an integer value can be, but it is constrained by the amount of memory your system has.
    - **<a href="https://www.w3schools.com/python/python_numbers.asp" target="_blank">Integer refresher</a>**
- **Floating-Point Numbers:**
    - float values are numbers specified with a decimal point
    - the `float` type in Python designates a floating-point number
    - optionally, the character e or E followed by a positive or negative integer may be appended to specify scientific notation
    - **<a href="https://www.w3schools.com/python/python_numbers.asp" target="_blank">Float refresher</a>**
- **Boolean Type:**
    - objects of Boolean type may have one of two values, `True` or `False`
    - the Boolean type in Python is called `bool`
    - a value that is true in Boolean context is sometimes said to be "truthy" and one that is false in Boolean context is said to be "falsy"
    - the "truthiness" of an object of Boolean type is self-evident: Boolean objects that are equal to `True` are truthy (true), and those equal to `False` are falsy (false)
    - https://www.w3schools.com/python/python_booleans.asp
    - **<a href="https://www.w3schools.com/python/python_numbers.asp" target="_blank">Boolean refresher</a>**

**<a href="https://mybinder.org/v2/gh/DamoM73/edge-approach-to-digital-solutions/HEAD?labpath=basic_prog_feat%2Fassigning.ipynb" target="_blank">How to assigning variables in Python</a>**

### Conditions

A condition is the way that a computer asks a question. Computers can only generate two possible  responses to questions. Yes and No, or more precisely, True and False. A more formal definition is that a condition is a logical expression that evaluates to true or false. 

#### In Python

Conditions are part of `if` and `while` statements. They have the syntax of `value` `operator` `value` with six possible operators:

- Equals: a == b
- Not Equals: a != b
- Less than: a < b
- Less than or equal to: a <= b
- Greater than: a > b
- Greater than or equal to: a >= b

### Control Structures
Flow of control through any given function is implemented with three basic types of control structures:

- **<a href="https://mybinder.org/v2/gh/DamoM73/edge-approach-to-digital-solutions/HEAD?labpath=basic_prog_feat%2Fsequence.ipynb" target="_blank">Sequential</a>**
- **<a href="https://mybinder.org/v2/gh/DamoM73/edge-approach-to-digital-solutions/HEAD?labpath=basic_prog_feat%2Fselection.ipynb" target="_blank">Selection</a>**
- **<a href="https://mybinder.org/v2/gh/DamoM73/edge-approach-to-digital-solutions/HEAD?labpath=basic_prog_feat%2Fiteration.ipynb" target="_blank">Iteration</a>**

### Modularisation (Functions)

>Modular programming refers to the process of breaking a large, unwieldy programming task into separate, smaller, more manageable subtasks or modules. Individual modules can then be cobbled together like building blocks to create a larger application {cite}`bailey_2022_python`.

There are several advantages to modularizing code in a large application:
- **Simplicity:** 
  - focusing on one relatively small portion of the problem, rather than the entire problem at hand. 
  - Wrapping your head around a smaller problem domain makes development easier and less error-prone.
- **Maintainability:** 
  - modularisation enforces logical boundaries between different problem domains. 
  - minimizing interdependency decreases likelihood that modifications to a single module will have an impact on other parts of the program. 
  - This reduced interdependency makes it more viable for a team of many programmers to work collaboratively on a large application.
- **Reusability:**
  - the code defined in a single module can be easily reused by other parts of the application. 
  - This eliminates the need to duplicate it.
- **Scoping:**
  - modules typically define a separate namespace
  - this helps avoid errors when the same name is used for different purposes.

**<a href="https://mybinder.org/v2/gh/DamoM73/edge-approach-to-digital-solutions/HEAD?labpath=basic_prog_feat%2Fmodular.ipynb" target="_blank">Using modularisation in Python</a>**

### Data Structures
> Data structures are used to store data in an organized form. No matter what problem are you solving, in one way or another you have to deal with data — whether it's an employee's salary, stock prices, a grocery list, or even a simple telephone directory. {cite}`ulhaq_2018_the`

Based on different scenarios, data will need to be stored in a specific format. 

In Python we will deal with four data structures:
- **Lists:**
  - lists are defined as an ordered collection of items
  - they are one of Python's essential data structures
  - list are defined using square brackets `[` `]` to enclose the elements, which are separated by commas 
  - For example, `[1,2,3,4]`.
  - each element in the list is referred to by its index (position number), starting at 0.
  - **<a href="https://www.w3schools.com/python/python_lists.asp" target="_blank">Lists refresher</a>**
- **Tuples:**
  - Tuples are also an ordered collection of objects, but unlike lists, they come with limited functionality.
  - The primary differing characteristic between lists and tuples is that lists are mutable, whereas tuples are immutable. This means tuples cannot be modified, added, or deleted once they've been created.
  - tuples are defined by using parentheses `(` `)` to enclose the elements, which are separated by commas 
    - For example, `(1,2,3,4)`.
  - each element in the tuple is referred to by its index (position number), starting at 0.
  - reasons for using tuples instead of lists:
    - when the developer does not want the data to be modified 
    - when speed is important as tuples use less memory, and they make program execution faster
  - **<a href="https://www.w3schools.com/python/python_tuples.asp" target="_blank">Tuples refresher</a>**
- **Sets:**
  - sets are a collection of unique elements that do not follow a specific order.
  - they are mutable – they can be modified, added, replaced, or removed
  - sets are defined by using curly brackets `{` `}` to enclose the elements, which are separated by commas 
    - For example, `{1,2,3,4}`.
  - they are used when the existence of an object in a collection of objects is more important than the number of times it appears or the order of the objects.
  - **<a href="https://www.w3schools.com/python/python_sets.asp" target="_blank">Sets refresher</a>**
- **Dictionaries:**
  - dictionaries are an ordered collection of key-value pairs. Each key-value pair maps the key to its associated value
  - they are mutable – they can be modified, added, replaced, or removed. 
  - dictionaries are defined by using curly brackets `{` `}` to enclose the elements, with a colon `:` separating a key and its value, and each key-pair separated by commas 
    - For example, `{"Doh":"Doherty","Dun":"Dunlop","Fly":"Flynn","Nic":"Nichols"}`
  - they should be used when the data has a unique reference that can be associated with the value.
  - **<a href="https://www.w3schools.com/python/python_dictionaries.asp" target="_blank">Dictionary refresher</a>**

### Syntax
The syntax of a computer language is the set of rules that defines the combinations of symbols that are considered to be correctly structured statements or expressions in that language.

**<a href="https://mybinder.org/v2/gh/DamoM73/edge-approach-to-digital-solutions/HEAD?labpath=basic_prog_feat%2Fsyntax.ipynb" target="_blank">Learn about Python's syntax</a>**


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
| `+` |Addition|`x + y`|
| `-` |Subtraction|`x - y`|
| `*` |Multiplication|`x * y`|
| `/` |Division|`x / y`|
| `%` |Modulus|`x % y`|
| `**` |Exponentiation|`x ** y`|
| `//` |Floor division|`x // y`|

In Python addition, subtraction, and multiplication are all strait forward and do exactly like you would expect. Note: that brackets `(` and `)` work the same as they would in mathematical equations. 

It is worth checking out how division, modulus, floor division and exponentiation work. 

**<a href="https://mybinder.org/v2/gh/DamoM73/edge-approach-to-digital-solutions/HEAD?labpath=operators%2Farithmetic_ops.ipynb" target="_blank">Arithmetic operators examples</a>**

### Assignment Operators
The standard assignment operator `=` is used to assign values to a variable.

|Operator|Example|Same As|
|:-------|:------|:------|
| `=` |`x = 5`|`x = 5`|
| `+=` |`x += 3`|`x = x + 3`|
| `-=` |`x -= 3`|`x = x - 3`|
| `*=` |  `x *= 3` |`x = x * 3`|
| `/=` |`x /= 3`|`x = x / 3`|
| `%=` |`x %= 3`|`x = x % 3`|
| `//=` |`x //= 3`|`x = x // 3`|
| `**=` |`x **= 3`|`x = x ** 3`|

The other assignment operators `+=`, `-=`, `*=`, etc. adjust a variable by operation sign and the value provided. 

**<a href="https://mybinder.org/v2/gh/DamoM73/edge-approach-to-digital-solutions/HEAD?labpath=operators%2Fassign_ops.ipynb" target="_blank">Assignment operators examples</a>**

### Comparison Operators
Comparison operators are used to compare two values, and will return a value of `True` or `False`.

|Operator|Name|Example|
|:-------|:---|:------|
| `==` |Equal|`x == y`|
| `!=`|Not equal|`x != y`|
| `>`|Greater than|`x > y`|
| `<`|Less than|`x < y`|
|`>=`|Greater than or equal to|`x >= y`|
|`<=`|Less than or equal to|`x <= y`|

Comparisons can be between values, variables, calculations or even the results of a function call.

**<a href="https://mybinder.org/v2/gh/DamoM73/edge-approach-to-digital-solutions/HEAD?labpath=operators%2Fcomparison_ops.ipynb" target="_blank">Comparison operators examples</a>**

### Logical Operators
Logical operators are used to combine conditional statements. The truthiness of the conditions is tested, and then operator combines the resulting Boolean values to produce either `True` or `False`.

|Operator|Description|Example|
|:-------|:----------|:------|
|`and`|Returns `True` if all statements are `True`|`x < 5 and  x < 10`|
|`or`|Returns `True` if one of the statements is `True`|`x < 5 or x < 4`|
|`not`|Reverse the result, returns `False` if the result is `True`|`not(x < 5 and x < 10)`|

**<a href="https://mybinder.org/v2/gh/DamoM73/edge-approach-to-digital-solutions/HEAD?labpath=operators%2Flogical_ops.ipynb" target="_blank">Logical operators examples</a>**

### Identity Operators
Identity operators are used to compare the objects, not if they are equal, but if they are actually the same object, with the same memory location.

|Operator|Description|Example|
|:-------|:----------|:------|
|`is`|Returns `True` if both variables are the same object|`x is y`|
|`is not`|Returns `True` if both variables are not the same object|`x is not y`|

**<a href="https://mybinder.org/v2/gh/DamoM73/edge-approach-to-digital-solutions/HEAD?labpath=operators%2Fidenity_ops.ipynb" target="_blank">Identity operators examples</a>**

### Membership Operators
Membership operators are used to test if a sequence is presented in an object (list, tuple or string).

|Operator|Description|Example|
|:-------|:----------|:------|
|`in`|Returns `True` if a sequence with the specified value is present in the object|`x in y`|
|`not in`|Returns `True` if a sequence with the specified value is not present in the object|`x not in y`|

**<a href="https://mybinder.org/v2/gh/DamoM73/edge-approach-to-digital-solutions/HEAD?labpath=operators%2Fmember_op.ipynb" target="_blank">Membership operators examples</a>**

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