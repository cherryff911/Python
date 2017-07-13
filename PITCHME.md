<span style="color:#ffd241"><h1>Python</h1></span>
<br>
<span style="color:#536DFE"><h2>Training</h2></span>

---

## Introduction

### Python Keywords
<br>
Keywords are the reserved words in Python.
We cannot use a keyword as variable name, function name or any other identifier. They 
are used to define the syntax and structure of the Python language.

In Python, keywords are case sensitive.
There are 33 keywords in Python 3.3. This number can vary slightly in course of time.

All the keywords except True, False and None are in lowercase and they must be written 
as it is. The list of all the keywords are given below.

---

### Keywords in Python programming language

| False | class	| finally | is	|return |
|------|--------|---------|-----|-------|
| None	| continue | for | lambda | try |
|True | def | from | nonlocal | while |
| and | del | global | not | with |
| as | elif | if | or |	yield |
| assert | else	| import | pass |
| break	| except | in | rais |
 <br>
Looking at all the keywords at once and trying to figure out what they mean might be 
overwhelming.

---

### Python Identifiers
<br>
Identifier is the name given to entities like class, functions, variables etc. in 
Python. It helps differentiating one entity from another.

## Rules for writting Identifiers
<li>Identifiers can be a combination of letters in lowercase (a to z) or uppercase (A to Z) or digits (0 to 9) or an underscore (_). Names like myClass, var_1 and print_this_to_screen, all are valid example.</li>
<li>An identifier cannot start with a digit. 1variable is invalid, but variable1 is perfectly fine.</li>

---

```python
>>> global = 1
  File "<interactive input>", line 1
    global = 1
           ^
SyntaxError: invalid syntax
```
<li>Keywords cannot be used as identifiers.</li>
---


```python
>>> a@ = 0
  File "<interactive input>", line 1
    a@ = 0
     ^
SyntaxError: invalid syntax
```
<li>We cannot use special symbols like !, @, #, $, % etc. in our identifier.</li>
<li>Identifier can be of any length.</li>

---

#### Things to care about
<br>
Python is a case-sensitive language. This means, Variable and variable are not the same. 
Always name identifiers that make sense.

<br>
While, c = 10 is valid. Writing count = 10 would make more sense and it would be easier 
to figure out what it does even when you look at your code after a long gap.
Multiple words can be separated using an underscore, this_is_a_long_variable.

---

<br>
We can also use camel-case style of writing, i.e., capitalize every first letter of the 
word except the initial word without any spaces. For example: camelCaseExample

---

## Python Statement, Indentation and Comments

#### Python Statement

<br>
Instructions that a Python interpreter can execute are called statements. For example, a 
= 1 is an assignment statement. if statement, for statement, while statement etc. are 

other kinds of statements which will be discussed later.

---

#### Multi-line statement

<br>
In Python, end of a statement is marked by a newline character. But we can make a 
statement extend over multiple lines with the line continuation character (\). For 
example:

```python
a = 1 + 2 + 3 + \
    4 + 5 + 6 + \
    7 + 8 + 9
```
---

<br>
This is explicit line continuation. In Python, line continuation is implied inside 
parentheses ( ), brackets [ ] and braces { }. For instance, we can implement the above 
multi-line statement as

```pyhton
a = (1 + 2 + 3 +
    4 + 5 + 6 +
    7 + 8 + 9)
```
---

<br>
Here, the surrounding parentheses ( ) do the line continuation implicitly. Same is the 
case with [ ] and { }. For example:
 
```python
colors = ['red',
          'blue',
          'green']
```
<br>
We could also put multiple statements in a single line using semicolons, as follows

```python
a = 1; b = 2; c = 3
```
---

#### Python Indentation

<br>
Most of the programming languages like C, C++, Java use braces { } to define a block of 
code. Python uses indentation.

<br>
A code block (body of a function, loop etc.) starts with indentation and ends with the 
first unindented line. The amount of indentation is up to you, but it must be consistent 
throughout that block.

---

Generally four whitespaces are used for indentation and is preferred over tabs. Here is 
an example.

```python
for i in range(1,11):
	print(i)
	if i == 5:
		break
```
<br>
The enforcement of indentation in Python makes the code look neat and clean. This 
results into Python programs that look similar and consistent.

Indentation can be ignored in line continuation. But it's a good idea to always indent. 
It makes the code more readable. For example:

```python
if True:
    print('Hello')
    a = 5
```
and
---
```python
if True: print('Hello'); a = 5
```
<br>
both are valid and do the same thing. But the former style is clearer.

Incorrect indentation will result into IndentationError

---
#### Python Comments
<br>
Comments are very important while writing a program. It describes what's going on inside 
a program so that a person looking at the source code does not have a hard time figuring 
it out. You might forget the key details of the program you just wrote in a month's 
time. So taking time to explain these concepts in form of comments is always fruitful.

---

In Python, we use the hash (#) symbol to start writing a comment.

<br>
It extends up to the newline character. Comments are for programmers for better 
understanding of a program. Python Interpreter ignores comment.

```python
#This is a comment
#print out Hello
print('Hello')
```
---

#### Multi-line comments
<br>
If we have comments that extend multiple lines, one way of doing it is to use hash (#) 
in the beginning of each line. For example:

```python
#This is a long comment
#and it extends
#to multiple lines
```
---

Another way of doing this is to use triple quotes, either ''' or """.
These triple quotes are generally used for multi-line strings. But they can be used as 
multi-line comment as well. Unless they are not docstrings, they do not generate any 
extra code.

```python
"""This is also a
perfect example of
multi-line comments"""
```
---

## Docstring in Python
<br>
Docstring is short for documentation string.

It is a string that occurs as the first statement in a module, function, class, or 
method definition. We must write what a function/class does in the docstring.

Triple quotes are used while writing docstrings. for example

```python
def doublele(num):
	"""Function to double the value"""
	return 2*num
```
---
<br>
Docstring is available to us as the attribute __doc__ of the function. Issue the 
following code in shell once you run the above program.

```python
>>> print(double.__doc__)
Function to double the value
```
---
### Python Variables

A variable is a location in memory used to store some data (value).
<br>
They are given unique names to differentiate between different memory locations. The rules for writing a variable name is same as the rules for writing identifiers in Python.
<br>
We don't need to declare a variable before using it. In Python, we simply assign a value to a variable and it will exist. We don't even have to declare the type of the variable. This is handled internally according to the type of value we assign to the variable.

---

### Variable assignment
<br>
We use the assignment operator (=) to assign values to a variable. Any type of value can be assigned to any valid variable.
```python
a = 5
b = 3.2
c = "Hello"
```
<br>
Here, we have three assignment statements. 5 is an integer assigned to the variable a.
Similarly, 3.2 is a floating point number and "Hello" is a string (sequence of characters) assigned to the variables b and c respectively.

---

### Multiple assignments
In Python, multiple assignments can be made in a single statement as follows:

```python
a, b, c = 5, 3.2, "Hello"
```
If we want to assign the same value to multiple variables at once, we can do this as

```python
x = y = z = "same"
```
This assigns the "same" string to all the three variables.

---

### Data types in Python

<br>
Every value in Python has a datatype. Since everything is an object in Python programming, data types are actually classes and variables are instance (object) of these classes.

There are various data types in Python. Some of the important types are listed below.
---

### Python Numbers
<br>
Integers, floating point numbers and complex numbers falls under Python numbers category. They are defined as int, float and complex class in Python.

---

We can use the type() function to know which class a variable or a value belongs to and the isinstance() function to check if an object belongs to a particular class.
```python
a = 5
print(a, "is of type", type(a))

a = 2.0
print(a, "is of type", type(a))

a = 1+2j
print(a, "is complex number?", isinstance(1+2j,complex))
```
---
<br>
Integers can be of any length, it is only limited by the memory available.

A floating point number is accurate up to 15 decimal places. Integer and floating points are separated by decimal points. 1 is integer, 1.0 is floating point number.
Complex numbers are written in the form, x + yj, where x is the real part and y is the imaginary part. Here are some examples.

---

```python
>>> a = 1234567890123456789
>>> a
1234567890123456789
>>> b = 0.1234567890123456789
>>> b
0.12345678901234568
>>> c = 1+2j
>>> c
(1+2j)
```
Notice that the float variable b got truncated.

---

### Python List
List is an ordered sequence of items. It is one of the most used datatype in Python and is very flexible. All the items in a list do not need to be of the same type.

Declaring a list is pretty straight forward. Items separated by commas are enclosed within brackets [ ].

```python
>>> a = [1, 2.2, 'python']
```

---

We can use the slicing operator [ ] to extract an item or a range of items from a list. Index starts form 0 in Python.

```python
a = [5,10,15,20,25,30,35,40]

# a[2] = 15
print("a[2] = ", a[2])

# a[0:3] = [5, 10, 15]
print("a[0:3] = ", a[0:3])

# a[5:] = [30, 35, 40]
print("a[5:] = ", a[5:])
```

---

Lists are mutable, meaning, value of elements of a list can be altered.

```python
>>> a = [1,2,3]
>>> a[2]=4
>>> a
[1, 2, 4]
```

---

## Python Tuple

<br>
Tuple is an ordered sequence of items same as list.The only difference is that tuples are immutable. Tuples once created cannot be modified.

Tuples are used to write-protect data and are usually faster than list as it cannot change dynamically.

```python
>>> t = (5,'program', 1+3j)
```

---

We can use the slicing operator [] to extract items but we cannot change its value.

```python
t = (5,'program', 1+3j)

# t[1] = 'program'
print("t[1] = ", t[1])

# t[0:3] = (5, 'program', (1+3j))
print("t[0:3] = ", t[0:3])

# Generates error
# Tuples are immutable
t[0] = 10
```

---

### Python Strings
<br>
String is sequence of Unicode characters. We can use single quotes or double quotes to represent strings. Multi-line strings can be denoted using triple quotes, ''' or """.

It is defined within parentheses () where items are separated by commas.
```python
>>> s = "This is a string"
>>> s = '''a multiline
```
---

Like list and tuple, slicing operator [ ] can be used with string. Strings are immutable.
```python
s = 'Hello world!'

# s[4] = 'o'
print("s[4] = ", s[4])

# s[6:11] = 'world'
print("s[6:11] = ", s[6:11])

# Generates error
# Strings are immutable in Python
s[5] ='d'
```

---

### Python Set
<br>
Set is an unordered collection of unique items. Set is defined by values separated by comma inside braces { }. Items in a set are not ordered.
```python
a = {5,2,3,1,4}

# printing set variable
print("a = ", a)

# data type of variable a
print(type(a))
```

---

We can perform set operations like union, intersection on two sets. Set have unique values. They eliminate duplicates.

```python
>>> a = {1,2,2,3,3,3}
>>> a
{1, 2, 3}
```

---

Since, set are unordered collection, indexing has no meaning. Hence the slicing operator [] does not work.
```python
>>> a = {1,2,3}
>>> a[1]
Traceback (most recent call last):
  File "<string>", line 301, in runcode
  File "<interactive input>", line 1, in <module>
TypeError: 'set' object does not support indexing
```

---

### Python Dictionary
<br>
Dictionary is an unordered collection of key-value pairs.

It is generally used when we have a huge amount of data. Dictionaries are optimized for retrieving data. We must know the key to retrieve the value.

In Python, dictionaries are defined within braces {} with each item being a pair in the form key:value. Key and value can be of any type.
```python
>>> d = {1:'value','key':2}
>>> type(d)
<class 'dict'>
```

---

We use key to retrieve the respective value. But not the other way around.
```python
d = {1:'value','key':2}
print(type(d))

print("d[1] = ", d[1]);

print("d['key'] = ", d['key']);

# Generates error
print("d[2] = ", d[2]);
```

---

### Conversion between data types
<br>
We can convert between different data types by using different type conversion functions like int(), float(), str() etc.
```python
>>> float(5)
5.0
```
Conversion from float to int will truncate the value (make it closer to zero).
```python
>>> int(10.6)
10
>>> int(-10.6)
-10
```

---

Conversion to and from string must contain compatible values.
```python
>>> float('2.5')
2.5
>>> str(25)
'25'
>>> int('1p')
Traceback (most recent call last):
  File "<string>", line 301, in runcode
  File "<interactive input>", line 1, in <module>
ValueError: invalid literal for int() with base 10: '1p'
```

---

We can even convert one sequence to another.
```python
>>> set([1,2,3])
{1, 2, 3}
>>> tuple({5,6,7})
(5, 6, 7)
>>> list('hello')
['h', 'e', 'l', 'l', 'o']
```

---

To convert to dictionary, each element must be a pair
```python
>>> dict([[1,2],[3,4]])
{1: 2, 3: 4}
>>> dict([(3,26),(4,44)])
{3: 26, 4: 44}
```

---

### Python Input, Output and Import
<br>
Python provides numerous built-in functions that are readily available to us at the Python prompt.

Some of the functions like input() and print() are widely used for standard input and output operations respectively. Let us see the output section first.
```python
print('This sentence is output to the screen')
# Output: This sentence is output to the screen

a = 5

print('The value of a is', a)
# Output: The value of a is 5
```

---

<br>
In the second print() statement, we can notice that a space was added between the string and the value of variable a.This is by default, but we can change it.

The actual syntax of the print() function is
```python
print(*objects, sep=' ', end='\n', file=sys.stdout, flush=False)
```

---
<br>
Here, objects is the value(s) to be printed.

The sep separator is used between the values. It defaults into a space character.

After all values are printed, end is printed. It defaults into a new line.

---
<br>
The file is the object where the values are printed and its default value is sys.stdout (screen). Here are an example to illustrate this.
```python
print(1,2,3,4)
# Output: 1 2 3 4

print(1,2,3,4,sep='*')
# Output: 1*2*3*4

print(1,2,3,4,sep='#',end='&')
# Output: 1#2#3#4&
```

---

### Output formatting

<br>
Sometimes we would like to format our output to make it look attractive. This can be done by using the str.format() method. This method is visible to any string object.

```python
>>> x = 5; y = 10
>>> print('The value of x is {} and y is {}'.format(x,y))
The value of x is 5 and y is 10
```

---
<br>
Here the curly braces {} are used as placeholders. We can specify the order in which it is printed by using numbers (tuple index).

```python
print('I love {0} and {1}'.format('bread','butter'))
# Output: I love bread and butter

print('I love {1} and {0}'.format('bread','butter'))
# Output: I love butter and bread
```

---

We can even use keyword arguments to format the string.
```python
>>> print('Hello {name}, {greeting}'.format(greeting = 'Goodmorning', name = 'John'))
Hello John, Goodmorning
```
---
<br>
We can even format strings like the old sprintf() style used in C programming language. We use the % operator to accomplish this.
```python
>>> x = 12.3456789
>>> print('The value of x is %3.2f' %x)
The value of x is 12.35
>>> print('The value of x is %3.4f' %x)
The value of x is 12.3457
```

---

### Python Input
Up till now, our programs were static. The value of variables were defined or hard coded into the source code.

To allow flexibility we might want to take the input from the user. In Python, we have the input() function to allow this. The syntax for input() is
```python
input([prompt])
```
---

where prompt is the string we wish to display on the screen. It is optional.

```python
>>> num = input('Enter a number: ')
Enter a number: 10
>>> num
'10'
```
---

Here, we can see that the entered value 10 is a string, not a number. To convert this into a number we can use int() or float() functions.
```python
>>> int('10')
10
>>> float('10')
10.0
```
---

This same operation can be performed using the eval() function. But it takes it further. It can evaluate even expressions, provided the input is a string
```python
>>> int('2+3')
Traceback (most recent call last):
  File "<string>", line 301, in runcode
  File "<interactive input>", line 1, in <module>
ValueError: invalid literal for int() with base 10: '2+3'
>>> eval('2+3')
5
```
---

### Python Import

<br>
When our program grows bigger, it is a good idea to break it into different modules.

A module is a file containing Python definitions and statements. Python modules have a filename and end with the extension .py.

Definitions inside a module can be imported to another module or the interactive interpreter in Python. We use the import keyword to do this.

For example, we can import the math module by typing in import math.
```python
import math
print(math.pi)
```
---
<br>
Now all the definitions inside math module are available in our scope. We can also import some specific attributes and functions only, using the from keyword. For example:

```python
>>> from math import pi
>>> pi
3.141592653589793
```
---

While importing a module, Python looks at several places defined in sys.path. It is a list of directory locations.
```python
>>> import sys
>>> sys.path
['', 
 'C:\\Python33\\Lib\\idlelib', 
 'C:\\Windows\\system32\\python33.zip', 
 'C:\\Python33\\DLLs', 
 'C:\\Python33\\lib', 
 'C:\\Python33', 
 'C:\\Python33\\lib\\site-packages']
 ```
 ---
 
 ### Python Operators
 Operators are special symbols in Python that carry out arithmetic or logical computation. The value that the operator operates on is called the operand.
For example:
```python
>>> 2+3
5
```
---

Here, + is the operator that performs addition. 2 and 3 are the operands and 5 is the output of the operation.

Python has a number of operators which are classified below.

#### Type of operators in Python

<li>Arithmetic operators</li>
<li>Comparison (Relational) operators</li>
<li>Logical (Boolean) operators</li>
<li>Bitwise operators</li>
<li>Assignment operators</li>
<li>Special operators</li>

---

#### Arithmetic operators
Arithmetic operators are used to perform mathematical operations like addition, subtraction, multiplication etc.
---
| operator | Meaning | Example |
|---|--------------------------------|---------|
| + | Add two operands or unary plus | x + y +2 |
| - | Subtract right operand from the left or unary minus | x - y -2 |
| * |	Multiply two operands |	x * y |

---
| operator | Meaning | Example |
|---|--------------------------------|---------|
| / |	Divide left operand by the right one (always results into float) | x / y |
| % |	Modulus - remainder of the division of left operand by the right | x % y (remainder of x/y) |
| // |	Floor division - division that results into whole number adjusted to the left in the number line | x // y |
| ** |	Exponent - left operand raised to the power of right | x**y (x to the power y) |

---
#### Example #1: Arithmetic operators in Python
```python
y = 4

# Output: x + y = 19
print('x + y =',x+y)

# Output: x - y = 11
print('x - y =',x-y)

# Output: x * y = 60
print('x * y =',x*y)

# Output: x / y = 3.75
print('x / y =',x/y)

# Output: x // y = 3
print('x // y =',x//y)

# Output: x ** y = 50625
print('x ** y =',x**y)
```

---

#### When you run the program, the output will be:
```python
x + y = 19
x - y = 11
x * y = 60
x / y = 3.75
x // y = 3
x ** y = 50625
```
### Comparison operators

Comparison operators are used to compare values. It either returns True or False according to the condition.

---

#### Comparision operators in Python

| Operator | Meaning | Example |
|----------|---------|---------|
| > | Greater that - True if left operand is greater than the right | x > y |
| < | Less that - True if left operand is less than the right | x < y |
| == | Equal to - True if both operands are equal | x == y |
| != | Not equal to - True if operands are not equal | x != y |
| >= | Greater than or equal to - True if left operand is greater than or equal to the right | x >= y |
| <= | Less than or equal to - True if left operand is less than or equal to the right | x <= y |

---

#### Example #2: Comparison operators in Python
```python
x = 10
y = 12

# Output: x > y is False
print('x > y  is',x>y)

# Output: x < y is True
print('x < y  is',x<y)

# Output: x == y is False
print('x == y is',x==y)

# Output: x != y is True
print('x != y is',x!=y)

# Output: x >= y is False
print('x >= y is',x>=y)

# Output: x <= y is True
print('x <= y is',x<=y)
```

---

### Logical operators
Logical operators are the and, or, not operators.

Logical operators in Python

| Operator | Meaning | Example |
|----------|---------|---------|
| and | True if both the operands are true | x and y |
| or | True if either of the operands is true | x or y |
| not | True if operand is false (complements the operand) | not x |

---

#### Example #3: Logical Operators in Python
```python
x = True
y = False

# Output: x and y is False
print('x and y is',x and y)

# Output: x or y is True
print('x or y is',x or y)

# Output: not x is False
print('not x is',not x)
```

---
Here is the truth table for these operators.
#### Bitwise operators

Bitwise operators act on operands as if they were string of binary digits. It operates bit by bit, hence the name.

For example, 2 is 10 in binary and 7 is 111.

*In the table below:* Let x = 10 (0000 1010 in binary) and y = 4 (0000 0100 in binary)

---

#### Bitwise operators in Python

| Operator | Meaning | Example |
|----------|---------|---------|
| & | Bitwise AND | x& y = 0 (0000 0000) |
| | | Bitwise OR | x | y = 14 (0000 1110) |
| ~ | Bitwise NOT | ~x = -11 (1111 0101) |
| ^ | Bitwise XOR | x ^ y = 14 (0000 1110) |
| >> | Bitwise right shift | x>> 2 = 2 (0000 0010) |
| << | Bitwise left shift | x<< 2 = 40 (0010 1000) |

---

#### Assignment operators

Assignment operators are used in Python to assign values to variables.

a = 5 is a simple assignment operator that assigns the value 5 on the right to the variable a on the left.

There are various compound operators in Python like a += 5 that adds to the variable and later assigns the same. It is equivalent to a = a + 5.

---

#### Assignment operators in Python
| Operator | Example | Equivatent to |
|----------|---------|---------------|
| = | x = 5 | x = 5 |
| += | x += 5 | x = x + 5 |
| -= | x -= 5 | x = x - 5 |
| *= | x *= 5 | x = x * 5 |
| /= | x /= 5 | x = x / 5 |
| %= | x %= 5 | x = x % 5 |

---
| Operator | Example | Equivatent to |
|----------|---------|---------------|
| //= | x //= 5 | x = x // 5 |
| **= |	x **= 5 | x = x ** 5 |
| &= |x &= 5 | x = x & 5 |
| |= | x |= 5 | x = x | 5 |
| ^= | x ^= 5 | x = x ^ 5 |
| >>= | x >>= 5 | x = x >> 5 |
| <<= | x <<= 5 | x = x << 5 |

---

#### Special operators
Python language offers some special type of operators like the identity operator or the membership operator. They are described below with examples.
#### Identity operators
is and is not are the identity operators in Python. They are used to check if two values (or variables) are located on the same part of the memory. Two variables that are equal does not imply that they are identical.

---

#### Identity operators in Python
| Operator | Meaning | Example |
|----------|---------|---------|
| is | True if the operands are identical (refer to the same object) | x is True |
| is not | True if the operands are not identical (do not refer to the same object) | x is not True |

---

#### Example #4: Identity operators in Python
```python
x1 = 5
y1 = 5
x2 = 'Hello'
y2 = 'Hello'
x3 = [1,2,3]
y3 = [1,2,3]

# Output: False
print(x1 is not y1)

# Output: True
print(x2 is y2)

# Output: False
print(x3 is y3)
```

---
<br>
Here, we see that x1 and y1 are integers of same values, so they are equal as well as identical. Same is the case with x2 and y2 (strings).

But x3 and y3 are list. They are equal but not identical. Since list are mutable (can be changed), interpreter locates them separately in memory although they are equal.

---

#### Membership operators
<br>
in and not in are the membership operators in Python. They are used to test whether a value or variable is found in a sequence (string, list, tuple, set and dictionary).

---

In a dictionary we can only test for presence of key, not the value.

| Operator | Meaning | Example |
|----------|---------|---------|
| in | True if value/variable is found in the sequence | 5 in x |
| not in | True if value/variable is not found in the sequence | 5 not in x |

---

#### Example #5: Membership operators in Python
```python
x = 'Hello world'
y = {1:'a',2:'b'}

# Output: True
print('H' in x)

# Output: True
print('hello' not in x)

# Output: True
print(1 in y)

# Output: False
print('a' in y)
```

---

### Python Introduction Quiz

#### Which of the following statements is true? Choose one
	
Python is a high level programming language.	

Python is an interpreted language.
	
Python is an object-oriented language.
	
All of the above.

---

#### What is used to define a block of code (body of loop, function etc.) in Python? Choose one
	
Curly braces
	
Parenthesis
	
Indentation
	
Quotation

---

#### Which of the following is correct? Choose one
	
Comments are for programmers for better understanding of the program.	

Python Interpreter ignores comment.	

You can write multi-line comments in Python using triple quotes, either ''' or """.	

All of the above

---

#### Which of the following is correct? Choose one
	
Comments are for programmers for better understanding of the program.

Python Interpreter ignores comment.	

You can write multi-line comments in Python using triple quotes, either ''' or """.	

All of the above

---

#### What is the output of the following code?
```PYTHON
print(1, 2, 3, 4, sep='*')
```
Choose one
	
1 2 3 4
	
1234
	
1*2*3*4
	
24

---

#### What is used to take input from the user in Python? Choose one
	
cin	

scanf()	

input()	

<>

---

#### What is the output of the following code?
```python
numbers = [2, 3, 4]
print(numbers)
```
Choose one
	
2, 3, 4
	
2 3 4
	
[2, 3, 4]

---

#### What is the output of the following code?
```python
print(3 >= 3)
```
Choose one 
	
3 >= 3	

True	

False	

None

[2 3 4]

---

## THE END OF DAY 1

---
