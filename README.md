# Python

<a href='https://www.python.org/'>Official website</a>

<a href='https://www.w3schools.com/python/default.asp'>Python Tutorial</a>

---

- [Operators](#1)
- [Variables](#2)
- [Built-in Functions](#3)
- [Defining Function](#4)
- [String](#5)
- [Converting str, int, float](#6)
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
