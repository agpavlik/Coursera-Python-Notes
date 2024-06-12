# Python

<a href='https://www.python.org/'>Official website</a>

<a href='https://www.w3schools.com/python/default.asp'>Python Tutorial</a>

---

- [Operators](#1)
- [Variables](#2)
- [Built-in Functions](#3)
- [Defining Function](#4)
- [String](#5)
  - [Modifying Strings](#51)
  - [String Methods](#52)
  - [for loop over String](#53)
- [Converting str, int, float](#6)
- [if statements](#7)
- [Defining Functions](#4)
- [Defining Functions](#4)
- [Defining Functions](#4)
- [Defining Functions](#4)
- [Defining Functions](#4)
- [Defining Functions](#4)

### 📒 Operators <a name="1"></a>

Operators are used to perform operations on variables and values.

> Arithmetic Operators

Used with numeric values to perform common mathematical operations

| Operator | Name                   | Example  |
| -------- | ---------------------- | -------- |
| -        | Addition               | x + y    |
| -        | Subtraction            | x - y    |
| -        | Multiplication         | x \* y   |
| /        | Division               | x / y    |
| %        | Modulus                | x % y    |
| \*\*     | Exponentiation         | x \*\* y |
| //       | Floor/Intiger division | x // y   |

> Assignment Operators

Used to assign values to variables

| Operator | Example       | Same As        |
| -------- | ------------- | -------------- |
| -=       | x = 5         | x = 5          |
| +=       | x += 3        | x = x + 3      |
| -=       | x -= 3        | x = x - 3      |
| \*=      | x \*= 3       | x = x \* 3     |
| /=       | x /= 3        | x = x / 3      |
| %=       | x %= 3        | x = x % 3      |
| //=      | x //= 3       | x = x // 3     |
| \*\*=    | x \*\*= 3     | x = x \*\* 3   |
| &=       | x &= 3        | x = x & 3      |
| =\|      | x = \|3       | x = x\|3       |
| ^=       | x ^= 3        | x = x ^ 3      |
| >>=      | x >>= 3       | x = x >> 3     |
| <<=      | x <<= 3       | x = x << 3     |
| :=       | print(x := 3) | x = 3 print(x) |

> Comparison Operators

Used to compare two values

| Operator | Name                     | Example |
| -------- | ------------------------ | ------- |
| ==       | Equal                    | x == y  |
| !=       | Not equal                | x != y  |
| >        | Greater than             | x > y   |
| <        | Less than                | x < y   |
| >=       | Greater than or equal to | x >= y  |
| <=       | Less than or equal to    | x <= y- |

> Logical Operators

Used to combine conditional statements

| Operator | Description                                             | Example                |
| -------- | ------------------------------------------------------- | ---------------------- |
| and      | Returns True if both statements are true                | x < 5 and x < 10       |
| or       | Returns True if one of the statements is true           | x < 5 or x < 4         |
| not      | Reverse the result, returns False if the result is true | not(x < 5 and x < 100) |

> Identity Operators

Used to compare the objects, not if they are equal, but if they are actually the same object, with the same memory location

| Operator | Description                                            | Example    |
| -------- | ------------------------------------------------------ | ---------- |
| is       | Returns True if both variables are the same object     | x is y     |
| is not   | Returns True if both variables are not the same object | x is not y |

> Membership Operators

Used to test if a sequence is presented in an object

| Operator | Description                                                                      | Example    |
| -------- | -------------------------------------------------------------------------------- | ---------- |
| in       | Returns True if a sequence with the specified value is present in the object     | x in y     |
| not in   | Returns True if a sequence with the specified value is not present in the object | x not in y |

---

### 📒 Variables <a name="2"></a>

The general form of an assignment statement:

```
variable = expression
```

Example assignment statements:

```
>>> base = 20
>>> height = 12
>>> area = base \* height / 2
>>> area
>>> 120.0
```

The rules for executing an assignment statement:

- Evaluate the expression. This produces a memory address.
- Store the memory address in the variable.

The rules for legal variable names:

- Names must start with a letter or \_.
- Names must contain only letters, digits, and \_.
  For Python, in most situations, the convention is to use pothole_case.

---

### 📒 Built-in Functions <a name="3"></a>

The general form of a function call:

```
function_name(arguments)
```

The rules for executing a function call:

- Evaluate the arguments.
- Call the function, passing in the argument values.

Terminology:

Argument: a value given to a function
Pass: to provide to a function
Call: ask Python to evaluate a function
Return: pass back a value

Python has a set of built-in functions. To see the list of built-in functions, run dir(**builtins**):
To get information about a particular function, call help and pass the function as the argument.

---

### 📒 Defining Functions <a name="4"></a>

> Function Definitions

The general form of a function definition:

```
def function_name(parameters):
    body
    return expression
```

- def: a keyword indicating a function definition
- function_name: the function name
- parameters: the parameter(s) of the function, 0 or more and are separated by a comma, a parameter is a variable whose value will be supplied when the function is called
- body: 1 or more statements, often ending with a return statement

> Function Calls

The general form of a function call:

```
function_name(arguments)
```

The rules for executing a function call:

- Evaluate the arguments to produce memory addresses.
- Store those memory addresses in the corresponding parameters.
- Execute the body of the function.

We usually save our Python programs in ".py" files. A file can contain multiple function definitions and other statements. Before calling a function from a ".py" file in the shell in IDLE, you need to first execute Run -> Run Module, or else the shell will not recognize the function call.

> Function Design Recipe

The Six Steps:

1. Examples

- What should your function do?
- Type a couple of example calls.
- Pick a name (often a verb or verb phrase): What is a short answer to "What does your function do"?

2. Type Contract

- What are the parameter types?
- What type of value is returned?

3. Header

- Pick meaningful parameter names.

4. Description

- Mention every parameter in your description.
- Describe the return value.

5. Body

- Write the body of your function.

6. Test

- Run the examples.

Applying the Design Recipe:
The United States measures temperature in Fahrenheit and Canada measures it in Celsius. When travelling between the two countries it helps to have a conversion function. Write a function that converts from Fahrenheit to Celsius.

```
Examples
    >>> convert_to_celsius(32)
    0
    >>> convert_to_celsius(212)
    100

Type Contract
    (number) -> number

Header
    def convert_to_celsius(fahrenheit):

Description
    Return the number of Celsius degrees equivalent to fahrenheit degrees.

Body
    return (fahrenheit - 32) * 5 / 9

Test
     Run the examples.
```

Putting it all together:

```
def convert_to_celsius(fahrenheit):
''' (number) -> number

Return the number of Celsius degrees equivalent to fahrenheit degrees.

> > > convert_to_ccelsius(32)
> > > 0
> > > convert_to_celsius(212)
> > > 100
> > > '''

return (fahrenheit - 32) \* 5 / 9
```

---

### 📒 String <a name="5"></a>

A string literal is a sequence of characters. In Python, this type is called str. Strings in Python start and end with a single quotes (') or double quotes ("). A string can be made up of letters, numbers, and special characters.

To include a quote within a string, use an escape character (\) before it. Otherwise Python interprets that quote as the end of a string and an error occurs. An alternative approach is to use a double-quoted string when including a single-quote within it, or vice-versa. Single- and double-quoted strings are equivalent.

The \* and + operands obey by the standard precedence rules when used with strings. All other mathematical operators and operands result in a TypeError.

Python has a special character called an escape character: \. When the escape character is used in a string, the character following the escape character is treated differently from normal. The escape character together with the character that follows it is an escape sequence.

| Escape Sequence | Name                            | Example                     | Output         |
| --------------- | ------------------------------- | --------------------------- | -------------- |
| \n              | newline (ASCII linefeed - LF)   | print('''How are you?''')   | How are you?   |
| \t              | tab(ASCII horizontal tab - TAB) | print('3\t4\t5')            | 3 4 5          |
| \\\             | backslash (\\)                  | print('\\\\')               | \\             |
| \\'             | single quote (\')               | print('don\\'t')            | don't          |
| \\"             | double quote (")                | print("He says, \\"hi\\".") | He says, "hi". |

---

### 📒 Modifying Strings <a name="51"></a>

`Indexing`
An index is a position within the string. Positive indices count from the left-hand side with the first character at index 0, the second at index 1, and so on. Negative indices count from the right-hand side with the last character at index -1, the second last at index -2, and so on. For the string "Learn to Program", the indices are:

```
Let s refer to 'Learn to Program'.

The first character of the string is at index 0 and can be accessed using this bracket notation:

>>> s[0]
'L'
>>> s[1]
'e'
Negative indices are used to count from the end (from the right-hand side):
>>> s[-1]
'm'
>>> s[-2]
'a'
```

`Slicing`
We can extract more than one character using slicing. A slice is a substring from the start index up to but not including the end index. For example:

```
>>> s[0:5]
'Learn'
>>> s[6:8]
'to'
>>> s[9:16]
'Program'
More generally, the end of the string can be represented using its length:
>>> s[9:len(s)]
'Program'
The end index may be omitted entirely and the default is len(s):
>>> s[9:]
'Program'
Similarly, if the start index is omitted, the slice starts from index 0:
>>> s[:]
'Learn to Program'
>>> s[:8]
'Learn to'
Negative indices can be used for slicing too. The following three expressions are equivalent:
>>> s[1:8]
'earn to'
>>> s[1:-8]
'earn to'
>>> s[-15:-8]
'earn to'
```

`Modifying Strings`
The slicing and indexing operations do not modify the string that they act on, so the string that s refers to is unchanged by the operations above. In fact, we cannot change a string. Operations like the following result in errors:

```
>>> s[6] = 'd'
Traceback (most recent call last):
        File <"pyshell#19", line 1, in <module>
                s[6] = 'd'
TypeError: 'str' object does not support item assignment
```

Imagine that we want to change string s to refer to 'Learned to Program'. The following expression evaluates to that 'Learned to Program': s[:5] + 'ed' + s[5:]

Variable s gets the new string:

```
s = s[:5] + 'ed' + s[5:]
```

Notice that the string that s originally referred to was not modified: strings cannot be modified. Instead a new string was created and s was changed to point to that string.

---

### 📒 String Methods <a name="52"></a>

A `method` is a function inside of an object.

The general form of a method call is:

```
object.method(arguments)
```

Consider the code:

```
>>> white_rabbit = "I'm late! I'm late! For a very important date!"
```

To find out which methods are inside strings, use the function dir:

```
>>> dir(white_rabbit)
['__add__', '__class__', '__contains__', '__delattr__', '__doc__', '__eq__', '__format__',
'__ge__', '__getattribute__','__getitem__', '__getnewargs__', '__gt__', '__hash__', '__init__',
'__iter__', '__le__', '__len__', '__lt__', '__mod__', '__mul__', '__ne__', '__new__', '__reduce__',
'__reduce_ex__', '__repr__', '__rmod__', '__rmul__', '__setattr__', '__sizeof__', '__str__',
'__subclasshook__', 'capitalize', 'center', 'count', 'encode', 'endswith', 'expandtabs', 'find',
'format', 'format_map', 'index', 'isalnum', 'isalpha', 'isdecimal', 'isdigit', 'isidentifier',
'islower', 'isnumeric', 'isprintable', 'isspace', 'istitle', 'isupper', 'join', 'ljust', 'lower',
'lstrip', 'maketrans', 'partition', 'replace', 'rfind', 'rindex', 'rjust', 'rpartition', 'rsplit',
'rstrip', 'split', 'splitlines', 'startswith', 'strip', 'swapcase', 'title', 'translate', 'upper',
 'zfill']
```

Passing str as an argument to dir gets the same result:

```
>>> dir(str)
```

For many of the string methods, a new string is returned. Since strings are immutable, the original string is unchanged. For example, a lowercase version of the str that white_rabbit refers to is returned when the method lower is called:

```
>>> white_rabbit.lower()
>>> "i'm late! i'm late! for a very important date!"
>>> white_rabbit
>>> "I'm late! I'm late! For a very important date!"
```

To get information about a method, such as the lower method, do the following:

```
>>> help(str.lower)
```

---

### 📒 for loop over String <a name="53"></a>

The general form of a `for loop` over a string is:

```
for variable in str:
    body
```

The variable refers to each character of the string in turn and executes the body of the loop for each character. For example:

```
>>> s = 'yesterday'
>>> for char in s:
...     print(char)
...
y
e
s
t
e
r
d
a
y
```

`Accumulator pattern: numeric accumulator`
Consider the code below, in which the variable num_vowels is an accumulator:

```
def count_vowels(s):
""" (str) -> int
    Return the number of vowels in s. Do not treat letter y as a vowel
    >>> count_vowels('Happy Anniversary!')
    5
    >>> count_vowels('xyz')
    0
    """
    num_vowels = 0

    for char in s:
        if char in 'aeiouAEIOU':
            num_vowels = num_vowels + 1

    return num_vowels
```

The loop in the function above will loop over each character that s refers to, in turn. The body of the loop is executed for each character, and when a character is a vowel, the if condition is True and the value that num_vowels refers to is increased by one.

The variable num_vowels is an accumulator, because it accumulates information. It starts out referring to the value 0 and by the end of the function it refers to the number of vowels in s.

`Accumulator pattern: string accumulator`
In the following function, the variable vowels is also an accumulator:

```
def collect_vowels(s):
""" (str) -> str

    Return the vowels from s.  Do not treat the letter
    y as a vowel.

    >>> collect_vowels('Happy Anniversary!')
    'aAiea'
    >>> collect_vowels('xyz')
    ''
    """

    vowels = ''

    for char in s:
        if char in 'aeiouAEIOU':
            vowels = vowels + char

    return vowels
```

Variable vowels initially refers to the empty string, but over the course of the function it accumulates the vowels from s.

---

### 📒 Converting str, int, float <a name="6"></a>

`str`
Builtin function str takes any value and returns a string representation of that value.

```
>>> str(3)
'3'
>>> str(47.6)
'47.6'
```

`int`
Builtin function int takes a string containing only digits (possibly with a leading minus sign -) and returns the int that represents. Function int also converts float values to integers by throwing away the fractional part.

```
>>> int('12345')
12345
>>> int('-998')
-998
>>> int(-99.9)
-99
```

If function int is called with a string that contains anything other than digits, a ValueError happens.

```
>>> int('-99.9')
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
ValueError: invalid literal for int() with base 10: '-99.9'
```

`float`
Builtin function float takes a string containing only digits and zero or one decimal points (possibly with a leading minus sign -) and returns the float that represents. Function float also converts int values to floats.

```
> > > float('-43.2')
> > > -43.2
> > > float('432')
> > > 432.0
> > > float(4)
> > > 4.0
```

If function float is called with a string that can't be converted, a ValueError happens.

```
> > > float('-9.9.9')
> > > Traceback (most recent call last):
> > > File "<stdin>", line 1, in <module>
> > > ValueError: could not convert string to float: '-9.9.9'
```

---

### 📒 if statements <a name="7"></a>

`If` statements can be used to control which instructions are executed. Here is the general form:

```
if expression1:
    body1
[elif expression2:      0 or more clauses
    body2]
[else:                  0 or 1 clause
    bodyN]
```

`elif` stands for "else if", so this forms a chain of conditions.

To execute an if statement, evaluate each expression in order from top to bottom. If an expression produces True, execute the body of that clause and then skip the rest open the if statement. If there is an else, and none of the expressions produce True, then execute the body of the else.

When execution of a function body ends without having executed a return statement, the function returns value None. The type of None is NoneType.

`if-elif` vs. `if-if`
An if statement with an elif clause is a single statement. The expressions are evaluated from top to bottom until one produces True or until there are no expressions left to evaluate. When an expression produces True, the body associated with it is executed and then the if statement exits. Any subsequent expressions are ignored. For example:

```
    grade1 = 70
    grade2 = 80

    if grade1 >= 50:
        print('You passed a course with grade: ', grade1)
    elif grade2 >= 50:
        print('You passed a course with grade: ', grade2)
```

The if statement condition (grade1 >= 50) evaluates to True, so the body associated with the if is executed and then the if exits. The elif condition is not even evaluated in this case.

It is possible for if statements to appear one after another in a program. Although they are be adjacent to each other, they are completely independent of each other and it is possible for the body of each if to be executed. For example:

    grade1 = 70
    grade2 = 80

    if grade1 >= 50:
        print('You passed a course with grade: ', grade1)
    if grade2 >= 50:
        print('You passed a course with grade: ', grade2)

In the program above, the condition associated with the first if statement (grade1 >= 50) produces True, so the body associated with it is executed. The condition associated with the second if statement (grade2 >= 50) also produces True, so the body associated with it is also executed.

`Nested ifs`
It is possible to place an if statement within the body of another if statement. For example:

```
    if precipitation:
        if temperature > 0:
            print('Bring your umbrella!')
        else:
            print('Wear your snow boots and winter coat!)
```

The statement above can be simplified by removing some of the nesting. The message 'Bring your umbrella!' is printed only when both of the if statement conditions are True. The message 'Wear your snow boots and winter coat!' is printed only when the outer if condition is True, but the inner if condition is False. The following is equivalent to the code above:

```
if precipitation and temperature > 0:
print('Bring your umbrella')
elif precipitation:
print('Wear your snow boots and winter coat!')
```
