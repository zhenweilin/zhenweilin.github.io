---
title: Introduction to pathlib package (Not carefully corrected)
date: 2020-12-11 10:46:01
tags:
---
<a name="pathlib"/>
I will introduce pathlib that is a cross-platform and objected-oriented package in this page. Pathlib encapsulates **os.path** and provided a convenient, objected-orient operation method. It's really for humans comparing to **os.path** which is a package multiplate path as string.


First let me give some examples about traditional package

```python
import os
print(os.getcwd())
### C:\Users\lzw
import sys
print(sys.path[0])
### c:\Users\lzw\Desktop
```
From the simple code example, you will find **os.getcwd()** can return your working directory, which is where you run your code. And the **sys.path[0]** can return directory where your file locates.

Next, I will introduce the advantage of **pathlib**.

Now, I will show it by taking an example.
```python
import pathlib
pme = pathlib.Path.home()
pwd = pathlib.Path.cwd()
print(pwd.parent)
print(pwd.parent.parent)
```
