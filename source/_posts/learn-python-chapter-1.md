---
title: Learn Python - Basics
date: 2017-10-03
tag: python
---

It is very excited to learn [python](https://www.python.org) (I recommend to use python3 directly which will have better support in the future). First, let's start with an IDE. 

Here are three IDEs I like very much.
- _IDLE_, it is installed along with the Python installer, which provides a powerful shell of playing with python. 
- _PyCharm_, [JetBrains](https://jetbrains.com) provides the most powerful IDE for python, it supports many useful functions like refactoring, lint and so on.
- _VSCode_ is a lightweight IDE for python as well, but you need to install some plugins to support python better. Here are plugins recommended.
    - _Code Runner_ for executing python
    - _Python_ support code intellisence, code formatting, auto indent etc.
    - _Pylint_ is recommended as well.

Here are some points for python, I will make it simple as possible.

- Number
```
number = 51
print(number)

number = 51.3
print(number)

number1 = number / 2
print(number1)

number2 = number // 2
print(number2)
```

- String
```
str = "Hello World"
print(str)

str1 = 'Hello World'
print(str1)
print(str1[0:2])
print(str1[:6])
print(str1[6:])
print(str1.upper())
print(len(str1))
```

- List
```
ls = [1, 2, 3, 4, 5]
print(len(ls))

ls.append(6)
print(ls)

ls1 = ls + [7, 8]
print(ls1)

ls2 = ls1[:2]
print(ls2)

ls3 = range(0, 10)
for i in ls3: print(i)

ls3 = range(2, 10)
for i in ls3: print(i)

ls3 = range(0, 16, 4)
for i in ls3: print(i)
```

- if: elif: else (note: `is` and `==` are both fine to check the equalvity)
```
s = 's'
if(s == 'a'): print('alpha')
elif(s is 'b'): print('beta')
elif(s is 's'): print('superman')
else: print('unknown')
```

- for loop
```
items = [1, 4, 2, 6, 9, 7]
for i in items: 
    print(i)

for i in items[:4]:
    print(i)
```

- while loop (note: `while`, `is`, `break`, `continue`)
```
i = 0
while i < 10:
    print(i)
    i += 1
    if i is 5: break
    else: continue
```

- Comments (single-line and multi-line)
```python
# num = 20

"""
str = 'hello'
str += ' world'
print(str)
"""
```

- Function
```
# void
def say_hello(name): 
    print('Hello', name)

say_hello('Howard')

# with return value
def get_hello_message(name):
    return 'Hello ' + name

print(get_hello_message('Howard'))

# with default value
def say_hello_with_default_value(name = 'Howard'):
    print('Hello', name)
say_hello_with_default_value()
say_hello_with_default_value('Bibioo')

# with optional parameters
def someone_do_something(name = 'Howard', action = 'ate', something = 'an apple'):
    print(name, action, something)

someone_do_something()
someone_do_something('Bibioo', 'is', 'awesome')
someone_do_something(something = 'us', action = 'blesses', name = 'God')

# flexibale variables
def flexible_var(*args):
    print('it has', len(args), 'arguments')
    for i in args:
        print(i)
flexible_var('a', 'b', 'c')

# unpack aruments, watch out the compare of the last two calls
def unpack_arguments(age, apple_pw, smook_pw):
    health = (100 - age) + (apple_pw * 3.5) - (smook_pw * 4.5)
    print(health)

person_data = [35, 7, 0]
unpack_arguments(person_data[0], person_data[1], person_data[2])
unpack_arguments(*person_data)
```

Now here are the basics for Python to remember, get back if need to recall the points, I will do more excited thing in the next part.