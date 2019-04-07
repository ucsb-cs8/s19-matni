---
num: "lect02"
lecture_date: 2019-04-04
desc: "Introduction to Linux OS and the Python Language"
ready: true
pdfurl: /lectures/pdf/lect02.pdf
annotatedready: false
---

<a href="{{page.pdfurl | relative_url }}" data-ajax="false">Slides PDF</a>

# Python Demo Code Used

Try these out again on IDLE and re-live the glory times from class... :)

```
Python 3.7.2 (default, Dec 29 2018, 00:00:04) 
[Clang 4.0.1 (tags/RELEASE_401/final)] on darwin
Type "help", "copyright", "credits" or "license()" for more information.
>>> 
>>> 2
2
>>> 2+3
5
>>> 2+3*3
11
>>> (2+3)*3
15
>>> 5%3
2
>>> 7/3
2.3333333333333335
>>> 7//3
2
>>> 
>>> x = 3
>>> y = 4
>>> 
>>> print(x+y)
7
>>> x = 66
>>> print(x+y)
70
>>> 
>>> 
>>> 
>>> print(type(x))
<class 'int'>
>>> 
>>> x = 1.43
>>> print(type(x))
<class 'float'>
>>> y = "hello all you happy people!"
>>> print(type(y))
<class 'str'>
>>> 
>>> 
>>> print(x + y)
Traceback (most recent call last):
  File "<pyshell#26>", line 1, in <module>
    print(x + y)
TypeError: unsupported operand type(s) for +: 'float' and 'str'
>>> 
>>> print(x, y)
1.43 hello all you happy people!
>>> 
```
