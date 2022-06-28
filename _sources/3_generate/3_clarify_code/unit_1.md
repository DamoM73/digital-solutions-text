# Unit 1: Clarify Code

Writing code that is easy to comprehend is important for it's maintainability. In Digital Solutions it is also an important way to explain your code and decisions you have made.

There are two ways that you can clarify your code:
- Using comments
- Following coding conventions

---
## Using Comments
Comments are a common tooled used by developers. They assist in communicating the intentions of the developer to other programmers, whether that developer is another member of their team, or their own future self who is trying to work out what past-self has done. Therefore, comments are important to coding convention, and will be addressed in the section.

For Digital Solutions, comments have an additional role of explaining your thinking to the person assessing your work. It is important that you use comments for the following:
- Explaining the purpose of each function
- Explaining the purposed of each class
- Explaining the purpose of each class method
- Detailing your thinking behind and 'tricky' code your created
- Structing your code by creating sections (eg. main loop, constants, etc.)

For our purposes, comments will take the place of annotations.

---
## Coding Conventions
When languages are used by many people, a consensus develops around the style of programming in that language. This style guide is called programming conventions. You don't need to follow the conventions, your program will still work, but following the conventions makes your program more readable, and therefore more maintainable, to other programmers who use the language.

For Python, these conventions are included in [PEP 8 -- Style Guide for Python Code](https://www.python.org/dev/peps/pep-0008/)

PEP 8 exists to improve the readability of Python code. This is important on three levels:
- **personal:** You may spend a few minutes, or a whole day, writing a piece of code to process user authentication. Once you've written it, you're never going to write it again. But you'll definitely have to read it again. That piece of code might remain part of a project you're working on. Every time you go back to that file, you'll have to remember what that code does and why you wrote it, so readability matters.
- **inter-personally:** You may need to collaborate with others, so writing readable code is crucial. Other people, who may have never met you or seen your coding style before, will have to read and understand your code. Having guidelines that you follow and recognize will make it easier for others to read your code.
- **professionally:** Writing clear, readable code shows professionalism. It'll tell an employer that you understand how to structure your code well.

We'll now look at the important parts of PEP 8

### Naming Conventions
When you write Python code, you have to name a lot of things: variables, functions, classes, packages, and so on. 

In choosing a name:
- choose sensible names with meaning. This will save you time and energy later (ie. you'll be able to figure out, from the name, what a certain variable, function, or class represents).
- avoid using inappropriate names that might result in errors that are difficult to debug (ie. Python keywords)
- never use l, O, or I single letter names as these can be mistaken for 1 and 0, depending on typeface.

#### Naming styles
|Type|Naming Convention|Examples|
|:---|:----------------|:-------|
|Function|Use a lowercase word or words. Separate words by underscores to improve readability.|function, my_function|
|Variable|Use a lowercase single letter, word, or words. Separate words with underscores to improve readability.|x, var, my_variable|
|Class|Start each word with a capital letter. Do not separate words with underscores. This style is called camel case.|Model, MyClass|
|Method|Use a lowercase word or words. Separate words with underscores to improve readability.|class_method, method|
|Constant|Use an uppercase single letter, word, or words. Separate words with underscores to improve readability.|CONSTANT, MY_CONSTANT, MY_LONG_CONSTANT|
|Module|Use a short, lowercase word or words. Separate words with underscores to improve readability.|module.py, my_module.py|
|Package|Use a short, lowercase word or words. Do not separate words with underscores.|package, mypackage|

### Code Layout
How you lay out your code has a huge role in how readable it is.

#### Blank Lines
Vertical whitespace, or blank lines, can greatly improve the readability of your code. Code that's bunched up together can be overwhelming and hard to read. Similarly, too many blank lines in your code makes it look very sparse, and the reader might need to scroll more than necessary. Below are three key guidelines on how to use vertical whitespace.

**Surround top-level functions and classes with two blank lines.**    
Top-level functions and classes should be fairly self-contained and handle separate functionality. It makes sense to put extra vertical space around them, so that it's clear they are separate:

```python
class MyFirstClass:
    pass


class MySecondClass:
    pass


def top_level_function():
    return None
```

**Surround method definitions inside classes with a single blank line.**  
Inside a class, functions are all related to one another. It’s good practice to leave only a single line between them:

```python
class MyClass:
    def first_method(self):
        return None

    def second_method(self):
        return None
```

**Use blank lines sparingly inside functions to show clear steps.**  
Sometimes, a complicated function has to complete several steps before the return statement. To help the reader understand the logic inside the function, it can be helpful to leave a blank line between each step.

In the example below, there is a function to calculate the variance of a list. This is two-step problem, so I have indicated each step by leaving a blank line between them. There is also a blank line before the return statement. This helps the reader clearly see what's returned:

```python
def calculate_variance(number_list):
    sum_list = 0
    for number in number_list:
        sum_list = sum_list + number
    mean = sum_list / len(number_list)

    sum_squares = 0
    for number in number_list:
        sum_squares = sum_squares + number**2
    mean_squares = sum_squares / len(number_list)

    return mean_squares - mean**2
```

If you use vertical whitespace carefully, it can greatly improved the readability of your code. It helps the reader visually understand how your code splits up into sections, and how those sections relate to one another.

#### Maximum Line Length and Line Breaking
PEP 8 suggests lines should be limited to 79 characters. This is because it allows you to have multiple files open next to one another, while also avoiding line wrapping.

Of course, keeping statements to 79 characters or less is not always possible. PEP 8 outlines ways to allow statements to run over several lines.

**Breaks within parentheses, brackets or braces.**  
Python will assume line continuation if code is contained within parentheses `()`, brackets `[]`, or braces `{}`:

```python
def function(arg_one, arg_two,
             arg_three, arg_four):
    return arg_one
```

**Implied continuation.**  
If it is impossible to use implied continuation, then you can use backslashes `\` to break lines instead:

```python
from mypkg import example1, \
    example2, example3
```

However, if you can use implied continuation, then you should do so.

**Binary operators**  
If line breaking needs to occur around binary operators, like + and *, it should occur before the operator. This rule stems from mathematics. Mathematicians agree that breaking before binary operators improves readability. Compare the following two examples.

Below is an example of breaking before a binary operator:

```python
# Recommended
total = (first_variable
         + second_variable
         - third_variable)
```

You can immediately see which variable is being added or subtracted, as the operator is right next to the variable being operated on.

Now, let's see an example of breaking after a binary operator:

```python
# Not Recommended
total = (first_variable +
         second_variable -
         third_variable)
```
Here, it's harder to see which variable is being added and which is subtracted.

Breaking before binary operators produces more readable code, so PEP 8 encourages it. Code that consistently breaks after a binary operator is still PEP 8 compliant. However, you're encouraged to break before a binary operator.

#### Indentation

Indentation, or leading whitespace, is extremely important in Python. The indentation level of lines of code in Python determines how statements are grouped together.

Consider the following example:

```python
x = 3
if x > 5:
    print('x is larger than 5')
```

The indented print statement lets Python know that it should only be executed if the if statement returns True. The same indentation applies to tell Python what code to execute when a function is called or what code belongs to a given class.

The key indentation rules laid out by PEP 8 are the following:  
- Use 4 consecutive spaces to indicate indentation.
- Prefer spaces over tabs.

### Commenting
You should use comments to document code as it's written. It is important to document your code so that you, and any collaborators, can understand it. When you or someone else reads a comment, they should be able to easily understand the code the comment applies to and how it fits in with the rest of your code.

Here are some key points to remember when adding comments to your code:
- Limit the line length of comments and docstrings to 72 characters.
- Use complete sentences, starting with a capital letter.
- Make sure to update comments if you change your code.

#### Block Comments
Use block comments to document a small section of code. They are useful when you have to write several lines of code to perform a single action, such as importing data from a file or updating a database entry. They are important as they help others understand the purpose and functionality of a given code block.

PEP 8 provides the following rules for writing block comments:
- Indent block comments to the same level as the code they describe.
- Start each line with a # followed by a single space.
- Separate paragraphs by a line containing a single #.

Here is a block comment explaining the function of a for loop. Note that the sentence wraps to a new line to preserve the 79 character line limit:

```python
for i in range(0, 10):
    # Loop over i ten times and print out the value of i, followed by a
    # new line character
    print(i, '\n')
```   

Sometimes, if the code is very technical, then it is necessary to use more than one paragraph in a block comment:

```python
def quadratic(a, b, c, x):
    # Calculate the solution to a quadratic equation using the 
    # quadratic formula.
    #
    # There are always two solutions to a quadratic equation, 
    # x_1 and x_2.
    x_1 = (- b+(b**2-4*a*c)**(1/2)) / (2*a)
    x_2 = (- b-(b**2-4*a*c)**(1/2)) / (2*a)
    return x_1, x_2
```

If you're ever in doubt as to what comment type is suitable, then block comments are often the way to go. Use them as much as possible throughout your code, but make sure to update them if you make changes to your code!

#### Inline Comments
Inline comments explain a single statement in a piece of code. They are useful to remind you, or explain to others, why a certain line of code is necessary. Here's what PEP 8 has to say about them:
- Use inline comments sparingly.
- Write inline comments on the same line as the statement they refer to.
- Separate inline comments by two or more spaces from the statement.
- Start inline comments with a # and a single space, like block comments.
- Don't use them to explain the obvious.

Below is an example of an inline comment:

```python
x = 5  # This is an inline comment
```

Sometimes, inline comments can seem necessary, but you can use better naming conventions instead. Here's an example:

```python
x = 'John Smith'  # Student Name
```

Here, the inline comment does give extra information. However using x as a variable name for a person's name is bad practice. There's no need for the inline comment if you rename your variable:

```python
student_name = 'John Smith'
```

Finally, inline comments such as these are bad practice as they state the obvious and clutter code:

```python
empty_list = []  # Initialize empty list


x = 5
x = x * 5  # Multiply x by 5
```

Inline comments are more specific than block comments, and it's easy to add them when they're not necessary, which leads to clutter. You could get away with only using block comments so, unless you are sure you need an inline comment, your code is more likely to be PEP 8 compliant if you stick to block comments.

#### Documentation Strings
Documentation strings, or docstrings, are strings enclosed in double (""") or single (''') quotation marks that appear on the first line of any function, class, method, or module. You can use them to explain and document a specific block of code. There is an entire PEP, PEP 257, that covers docstrings, but you’ll get a summary in this section.

The most important rules applying to docstrings are the following:
- Surround docstrings with three double quotes on either side, as in """This is a docstring""".
- Write them for all public modules, functions, classes, and methods.
- Put the """ that ends a multiline docstring on a line by itself:

```python
def quadratic(a, b, c, x):
    """Solve quadratic equation via the quadratic formula.

    A quadratic equation has the following form:
    ax**2 + bx + c = 0

    There always two solutions to a quadratic equation: x_1 & x_2.
    """
    x_1 = (- b+(b**2-4*a*c)**(1/2)) / (2*a)
    x_2 = (- b-(b**2-4*a*c)**(1/2)) / (2*a)

    return x_1, x_2
```

- For one-line docstrings, keep the """ on the same line:

```python
def quadratic(a, b, c, x):
    """Use the quadratic formula"""
    x_1 = (- b+(b**2-4*a*c)**(1/2)) / (2*a)
    x_2 = (- b-(b**2-4*a*c)**(1/2)) / (2*a)

    return x_1, x_2
```

### Whitespace in Expressions and Statements
Whitespace can be very helpful in expressions and statements when used properly. If there is not enough whitespace, then code can be difficult to read, as it's all bunched together. If there's too much whitespace, then it can be difficult to visually combine related terms in a statement.

Surround the following binary operators with a single space on either side:
- Assignment operators (=, +=, -=, and so forth)
- Comparisons (==, !=, >, <. >=, <=) and (is, is not, in, not in)
- Booleans (and, not, or)

Use the same amount of whitespace either side of the operator.

When to Avoid Adding Whitespace:
- Immediately inside parentheses `()`, brackets `[]`, or braces `{}`
- Before a comma `'`, semicolon `;`, or colon `:`
- Before the open parenthesis `()` that starts the argument list of a function call
- Before the open bracket `[]` that starts an index or slice
- Between a trailing comma `,` and a closing parenthesis `)`
- To align assignment operators

### Code Simplicity

You will often find that there are several ways to perform a similar action in Python (and any other programming language for that matter). 

Here are the suggestions PEP 8 provides to remove that ambiguity and preserve consistency:
- Don't compare Boolean values to True or False using the equivalence operator.
    - rather than using `if my_bool == True` use `if my_bool`
- Use the fact that empty sequences are falsy in if statements
    - given `my_list = []`
    - rather than using `if not len(my_list)` use `if not my_list`
- Use `is not` rather than `not ... is` in if statements.
    - rather than using `if not x is None` use `if x is not None`
- Don't use `if x:` when you mean `if x is not None`
    - rather than using `if var` use `if var is not None`
- Use `.startswith()` and `.endswith()` instead of slicing.
    - rather than using `my_string[:3] == 'cat'` use `my_string.startswith('cat')`