---
title: Learn Python - Module
date: 2017-10-04
tag: python
---

In the [previous topic](/2017/10/03/learn-python-chapter-1/), it includes some really useful points of Python basics. In this page, we will try to use _Modules_ in Python.

## Custom module
There are two ways of using modules. Let's first create a new Python file names _module1.py_.
```python
def say_hello(): 
    print('Hello Howard.')
```

In another Python file that wants to use the functions in the _module1.py_, we need the following ways to reference this module.
```python
# method 1. note, no file extension here
import module1 
module1.say_hello()
```
```python
# method 2. note, we don't have the module name before the function name
from module1 import say_hello
say_hello()
```

Choose the two methods above wisely and it makes your code easier to read.

## Use a build-in module
We are going to download an image from internet and store in disk. Here is the code.
```python
from urllib import request

url = 'https://avatars2.githubusercontent.com/u/8789008?v=4&s=460'
filename = '1.jpg'
request.urlretrieve(url, filename)
```

In this code, we import an _urllib_ module. You could use any module like this to support various requirements.