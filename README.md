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
  - [for loops over String](#53)
- [Converting str, int, float](#6)
- [if statements](#7)
- [while loop](#8)
- [Type list](#9)
  - [list methods](#91)
- [Mutability and Aliasing](#10)
- [range function](#11)
- [for loops over indices](#12)
- [Parallel Lists and Strings](#13)
- [Nested lists and loops](#14)
- [Read and Write files](#15)
- [Tuples](#16)
- [Type dict](#17)
- [Operators](#1)
- [Operators](#1)
- [Operators](#1)
- [Operators](#1)
- [Operators](#1)
- [Operators](#1)
- [Operators](#1)
- [Operators](#1)

- [Examples](#100)
  - [while loop vs for loop with range](#101)

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

---

### 📒 while loop <a name="8"></a>

The general form of a `while loop`:

```
while expression:
    statements
```

The while condition, num < 100, is evaluated, and if it is True the statements in the loop body are executed. The loop condition is rechecked and if found to be True, the body executes again. This continues until the loop condition is checked and is False. For example:

```
num = 2
while num < 100:
  num = num * 2
  print(num)

4
8
16
32
64
128
```

In the example above, there are 6 iterations: the loop body executes 6 times.

`Loops Conditions and Lazy Evaluation`
The problem: print the characters of str s, up to the first vowel in s.

The first attempt at solving this problem works nicely when s contains one or more vowel, but results in an error if there are no vowels in s:

```
i = 0
s = 'xyz'
while not (s[i] in 'aeiouAEIOU'):
        print(s[i])
        i = i + 1

x
y
z

Traceback (most recent call last):
File "<pyshell#73>", line 1, in <module>
while not (s[i] in 'aeiouAEIOU'):
IndexError: string index out of range
```

In the code above, the error occurs when s is indexed at i and i is outside of the range of valid indices. To prevent this error, add an additional condition is added to ensure that i is within the range of valid indices for s:

```
i = 0
s = 'xyz'
while i < len(s) and not (s[i] in 'aeiouAEIOU'):
        print(s[i])
        i = i + 1

x
y
z
```

Because Python evaluates the and using lazy evaluation, if the first operand is False, then the expression evaluates to False and the second operand is not even evaluated. That prevents the IndexError from occurring.

---

### 📒 Type list <a name="9"></a>

Our programs will often work with collections of data. One way to store these collections of data is using Python's `type list`.

The general form of a list is:

```
[expr1, expr2, ..., exprN]
```

For example, here is a list of three grades:

```
grades = [80, 90, 70]
```

Like strings, lists can be indexed:

```
grades[0]
80
grades[1]
90
grades[2]
70
```

Lists can also be sliced, using the same notation as for strings:

```
grades[0:2]
[80, 90]
```

The in operator can also be applied to check whether a value is an item in a list.

```
90 in grades
True
60 in grades
False
```

Several of Python's built-in functions can be applied to lists, including:

```
len(list): return the length of list.
min(list): return the smallest element in list.
max(list): return the largest element in list.
sum(list): return the sum of elements of list (where list items must be numeric).
```

Lists elements may be of any type.
Similar to looping over the characters of a string, it is possible to iterate over the elements of a list.
The general form of a for loop over a list is:

```
for variable in list:
body
```

---

### 📒 list methods <a name="91"></a>

list.append(object) - Append object to the end of list.
list.extend(list) - Append the items in the list parameter to the list.
list.pop([index]) - Remove the item at the end of the list; optional index to remove from anywhere.
list.remove(object) - Remove the first occurrence of the object;  
list.reverse() - Reverse the list.
list.sort() - Sort the list from smallest to largest.
list.insert(int, object) - Insert object at the given index, moving items to make room.

---

### 📒 Mutability and aliasing <a name="10"></a>

We say that lists are `mutable`: they can be modified. All the other types we have seen so far (str, int, float and bool) are `immutable`: they cannot be modified.

Here are several examples of lists being modified:

```
> > > classes = ['chem', 'bio', 'cs', 'eng']
> > >
> > > # Elements can be added:
> > >
> > > classes.append('math')
> > > classes
> > > ['chem', 'bio', 'cs', 'eng', 'math']
> > >
> > > # Elements can be replaced:
> > >
> > > classes[1] = 'soc'
> > > classes
> > > ['chem', 'soc', 'cs', 'eng', 'math']
> > >
> > > # Elements can be removed:
> > >
> > > classes.pop()
> > > 'math'
> > > classes
> > > ['chem', 'soc', 'cs', 'eng']
```

`Aliasing`. Consider the following code:

```
> > > lst1 = [11, 12, 13, 14, 15, 16, 17]
> > > lst2 = lst1
> > > lst1[-1] = 18
> > > lst2
> > > [11, 12, 13, 14, 15, 16, 18]
```

After the second statement executes, lst1 and lst2 both refer to the same list. When two variables refer to the same objects, they are aliases. If that list is modified, both of lst1 and lst2 will see the change.

---

### 📒 range function<a name="11"></a>

In Python, `range` is a built-in function that generates a sequence of numbers. It's commonly used for iterating over a sequence of numbers in for-loops.
The form of range is:

```
range([start,] stop[, step]):
    return a virtual sequence of numbers from start to stop by step
```

There are other options you can specify to range. One option is to let range generate the numbers corresponding to indices of a string or a list.

```
s = 'computer science'
for i in range(len(s)):
print(i)
```

You can also tell range what index to start at. For instance, the example below starts at index 1 (as opposed to the default which is 0).

```
for i in range(1, len(s)):
print(i)
```

You can even specify the "step" for range. The default stepping size is 1, which means that numbers increment by 1. The example below starts at index 1 and its step size is there (goes to every third index).

```
for i in range(1, len(s), 3):
print(i)
```

Practical Notes:

- The stop value in range(stop) is exclusive, meaning it is not included in the generated sequence.
- If step is not specified, it defaults to 1.
- If start is not specified, it defaults to 0.

---

### 📒 for loops over indices<a name="12"></a>

`Range` is typically used in a for loop to iterate over a sequence of numbers. Here are some examples:

```
# Iterate over the numbers 0, 1, 2, 3, and 4.
for i in range(5):

# Iterate over the numbers 2, 3, and 4.
for i in range(2, 5):

# Iterate over the numbers 3, 6, 9, 12, 15, and 18.
for i in range(3, 20, 3):
```

Because `len` returns the number of items in a list, it can be used with `range` to iterate over all the indices. This loop prints all the values in a list:

```
for i in range(len(lst)):
    print(lst[i])
```

This also gives us flexibility to process only part of a list. For example, We can print only the first half of the list:

```
for i in range(len(lst) // 2):
    print(lst[i])
```

Or every other element:

```
for i in range(0, len(lst), 2):
print(lst[i])
```

---

### 📒 Parallel Lists and Strings<a name="13"></a>

Two lists are `parallel` if they have the same length and the items at each index are somehow related. The items at the same index are said to be at `corresponding positions`.

Consider these two lists:

```
list1 = [1, 2, 3]
list2 = [2, 4, 2]
```

In these two lists, the corresponding element of list1[0] is list2[0], the corresponding element of list2[1] is list1[1], and so on.

```
def count_matches(s1, s2):
    ''' (str, str) -> int

    Return the number of positions in s1 that contain the
    same character at the corresponding position of s2.

    Precondition: len(s1) == len(s2)

    >>> count_matches('ate', 'ape')
    2
    >>> count_matches('head', 'hard')
    2
    '''

    num_matches = 0

    for i in range(len(s1)):
        if s1[i] == s2[i]:
            num_matches = num_matches + 1

    return num_matches
```

```
def sum_items(list1, list2):
''' (list of number, list of number) -> list of number

    Return a new list in which each item is the sum of the items at the
    corresponding position of list1 and list2.

    Precondition: len(list1) == len(list2)

    >> sum_items([1, 2, 3], [2, 4, 2])
    [3, 6, 5]
    '''

    sum_list = []

    for i in range(len(list1)):
        sum_list.append(list1[i] + list2[i])

    return sum_list
```

---

### 📒 Nested lists and loops<a name="14"></a>

Lists can contain items of any type, including other lists. These are called `nested lists`.

Here is an example.

```

> > > grades = [['Assignment 1', 80], ['Assignment 2', 90], ['Assignment 3', 70]]
> > > grades[0] > > > ['Assignment 1', 80]
> > > grades[1] > > > ['Assignment 2', 90]
> > > grades[2] > > > ['Assignment 3', 70]

```

To access a nested item, first select the sublist, and then treat the result as a regular list.

For example, to access 'Assignment 1', we can first get the sublist and then use it as we would a regular list:

```

> > > sublist = grades[0]
> > > sublist
> > > ['Assignment 1', 80]
> > > sublist[0]
> > > 'Assignment 1'
> > > sublist[1]
> > > 80

```

Both sublist and grades[0] contain the memory address of the ['Assignment 1', 80] nested list.

We can access the items inside the nested lists like this:

```

> > > grades[0][0]
> > > 'Assignment 1'
> > > grades[0][1]
> > > 80
> > > grades[1][0]
> > > 'Assignment 2'
> > > grades[1][1]
> > > 90
> > > grades[2][0]
> > > 'Assignment 3'
> > > grades[2][1]
> > > 70

```

The bodies of loops can contain any statements, including other loops. When this occurs, this is known as a `nested loop`.

Here is a nested loop involving 2 for loops:

```

for i in range(10, 13):
for j in range(1, 5):
print(i, j)

```

Here is the output:

```

10 1
10 2
10 3
10 4
11 1
11 2
11 3
11 4
12 1
12 2
12 3
12 4

```

Notice that when i is 10, the inner loop executes in its entirety, and only after j has ranged from 1 through 4 is i assigned the value 11.

---

### 📒 Read and Write files<a name="15"></a>

Information stored in files can be accessed by a Python program. To get access to the contents of a file, you need to open the file in your program. When you are done using a file, you should close it.
Python has a built-in function `open` that can open a file for reading.

The form of `open` is `open(filename, mode)`, where `mode` is 'r' (to open for reading), 'w' (to open for writing), or 'a' (to open for appending to what is already in the file).

Note that if the file is saved in the same directory as your program, you can simply write the name of the file. However, if it is not saved in the same directory, you must provide the path to it.

To close a file, you write `filename.close()`.

There are four standard ways to read from a file. Some use these methods:

- readline(): read and return the next line from the file, including the newline character (if it exists). Return the empty string if there are no more lines in the file.

- readlines(): read and return all lines in a file in a list. The lines include the newline character.

- read(): read the whole file as a single string.

- The for line in file approach: When you want to process every line in the file one at a time.

In order to write to a file, we use `file.write(str)`. This method writes a string to a file. Method write works like Python's print function, except that it does not add a newline character.

Module `tkinter` has a submodule called `filedialog`.
Function askopenfilename asks the user to select a file to open:

```

tkinter.filedialog.askopenfilename()

```

This function returns the full path to the file, so we can use that when we call function open to open that file.

```

from_filename = tkinter.filedialog.askopenfilename()

```

Function `asksaveasfilename` asks the user to select a file to save to, and provides a warning if the file already exists.

Examples:
Now we can open the file we want to read from and get the contents:

```

from_file = open(from_filename, 'r')
contents = from_file.read()
from_file.close()

```

And we can open the file we want to write to and write the contents:

```

to_file = open(to_filename, 'w')
to_file.write('Copy\n') # We have to add the newline ourselves.
to_file.write(contents) # Now write the contents of the file.
to_file.close()

```

---

### 📒 Tuples<a name="16"></a>

`Tuples` are immutable sequences: they cannot be modified. Tuples and lists have much in common, but lists are mutable sequences.

Tuples use parentheses instead of square brackets:

```
lst = ['a', 3, -0.2]
tup = ('a', 3, -0.2)
```

Once created, items in lists and tuples are accessed using the same notation. Tuples have fewer methods than lists. In fact, the only regular methods ('append', 'count', extend', 'index', 'insert', 'pop', 'remove', 'reverse', sort') and 'count' and 'index'. The rest of the list methods are not available for tuple because they modify the object, and tuples, being immutable, cannot be modified.
A tuple can be passed as an argument to the built-in function len:
It is also possible to iterate over the indices of a tuple.

Tuples are ideal for representing fixed collections of heterogeneous data, ensuring data integrity, and facilitating multiple value returns in functions.

---

### 📒 Type dict<a name="17"></a>

Another way to store collections of data is using Python's `dictionary type`: `dict`.

The general form of a dictionary is:

```
{key1: value1, key2: value2, ..., keyN: valueN}
```

Keys must be unique. Values may be duplicated. For example:

```
asn_to_grade = {'A1': 80, 'A2': 90, 'A3': 90}
```

Dictionaries are mutable: they can be modified. There are a series of operations and methods you can apply to dictionaries which are outlined below.

| Operation         | Description                                                                                                                                                      | Example                                                                                                                                      |
| ----------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------- |
| object in dict    | Checks whether object is a key in dict.                                                                                                                          | >>> asn_to_grade = {'A1': 80, 'A2': 90, 'A3': 90} >>> 'A1' in asn_to_grade >>> True                                                          |
| len(dict)         | Returns the number of keys in dict.                                                                                                                              | >>> asn_to_grade = {'A1': 80, 'A2': 90, 'A3': 90} >>> len(asn_to_grade) >>> 3                                                                |
| del dict[key]     | Removes a key and its associated value from dict.                                                                                                                | >>> asn_to_grade = {'A1': 80, 'A2': 90, 'A3': 90} >>> del asn_to_grade['A1'] >>> asn_to_grade >>> {'A3': 90, 'A2': 90}                       |
| dict[key] = value | If key does not exist in dict, adds key and its associated value to dict. If key exists in dict, updates dict by setting the value associated with key to value. | >>> asn_to_grade = {'A1' : 80, 'A2': 90, 'A3' : 90} >>> asn_to_grade['A4'] = 70 >>> asn_to_grade >>>{'A1': 80, 'A3': 90, 'A2': 90, 'A4': 70} |

Dictionaries are unordered. That is, the order the key-value pairs are added to the dictionary has no effect on the order in which they are accessed.
For example:

```
>>> asn_to_grade = {'A1': 80, 'A2': 70, 'A3': 90}
>>> for assignment in asn_to_grade:
    print(assignment)

A1
A3
A2
```

The for-loop above printed out the keys of the dictionary. It is also possible to print out the values:

```
>>> asn_to_grade = {'A1': 80, 'A2': 70, 'A3': 90}
>>> for assignment in asn_to_grade:
    print(asn_to_grade[assignment])

80
90
70
```

Finally, both the keys are values can be printed:

```
>>> asn_to_grade = {'A1': 80, 'A2': 70, 'A3': 90}
>>> for assignment in asn_to_grade:
    print(assignment, asn_to_grade[assignment])

A1 80
A3 90
A2 70

```

The keys of a dictionary must be immutable. Therefore, lists, dictionary and other mutable types cannot be used as keys. The following results in an error:

```
d[[1, 2]] = 'banana'
```

Since lists are mutable, they cannot be keys. Instead, to use a sequence as a key, type tuple can be used:

```
d[(1, 2)] = 'banana'
```

---

### 📒 Examples<a name="100"></a>

### 📒 while loop vs for loop with range<a name="101"></a>

> Task 1

What is the sum of the odd numbers from 1523 through 10503, inclusive? Hint: write a
while loop to accumulate the sum and print it. Then copy and paste that sum. For maximum learning, do it with a for loop as well, using range.

> Solution

```
def odd(start, end):
sum_odd = 0
i = start
while i <= end:
if i % 2 != 0:
sum_odd += i
i += 1
return sum_odd
```

```
def odd2(start, end):
sum_odd = 0

    for i in range(start, end + 1):
        if i % 2 != 0:
            sum_odd += i
    return sum_odd
```

> Task 2

Shift each item in L one position to the righthand and shift the last item to the first position.

> Solution

```
def shift_right(L):
''' (list) -> NoneType
Precondition: len(L) >= 1
'''
    last_item = L[-1]

    for i in range(1, len(L)):
        L[len(L) - i] = L[len(L) - i - 1]

    L[0] = last_item

    return L
```

> Task 3

Return a new list in which each item is a 2-item list with the string from the corresponding position of list1 and the int from the corresponding position of list2.

```
(list of str, list of int) -> list of [str, int] list
Precondition: len(list1) == len(list2) >>> make_pairs(['A', 'B', 'C'], [1, 2, 3])
[['A', 1], ['B', 2], ['C', 3]]
```

> Solution

```
def make_pairs(list1, list2):

    pairs = []

    for i in range(len(list1)):
        pairs.append([list1[i], list2[i]])

    return pairs
```

```
def make_pairs(list1, list2):

    pairs = []

    for i in range(len(list1)):
        inner_list = []
        inner_list.append(list1[i])
        inner_list.append(list2[i])
        pairs.append(inner_list)

    return pairs
```

> Task 4

Return whether value is an element of one of the nested lists in lst.

```
(object, list of list) -> bool

> > > contains('moogah', [[70, 'blue'], [1.24, 90, 'moogah'], [80, 100]])
> > > True

```

> Solution

```
def contains(value, lst):

    found = False
    for i in range(len(lst)):
        for j in range(len(lst[i])):
            if lst[i][j] == value:
                found = True

    return found
```

```
def contains(value, lst):

    for sublist in lst:
        if value in sublist:
            found = True

    return found
```
