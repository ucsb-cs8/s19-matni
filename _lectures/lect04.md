---
num: "lect04"
lecture_date: 2019-04-11
desc: "Operations on Strings and Lists; Intro to Functions"
ready: true
pdfurl: /lectures/pdf/lect04.pdf
annotatedready: false
---

<a href="{{page.pdfurl | relative_url }}" data-ajax="false">Slides PDF</a>

# Python Demo Code Used

Try these out again on IDLE and re-live the glory times from class... :)

```
Python 3.7.2 (default, Dec 29 2018, 00:00:04) 
[Clang 4.0.1 (tags/RELEASE_401/final)] on darwin
Type "help", "copyright", "credits" or "license()" for more information.

>>> ( ("o" + "Gaucho"[2:5] + "  " ) * 3 ) + "!"

'ouch  ouch  ouch  !'
>>> 
>>> s = "hello"
>>> print(s[1:3])
el
>>> print(s[1:])
ello
>>> print(s[3:])
lo
>>> print(s[:3])
hel
>>> print(s[-2:])
lo
>>> print(s[-2:2])

>>> def dbl(x):
	"""This function returns double its input x"""
	print("I'm doubling the number to:", 2*x)
	return 2*x	# I need to “return” the result

>>> print(dbl(55))
I'm doubling the number to: 55
110
>>> 

>>> def add2(a, b):
	c = a + b
	return c

>>> print(add2(4,5))
9

>>> print(3* add2(4,5))
27

>>> def add2(a, b):
	c = a + b
	print(c)
	return c

>>> print(add2(4,5))
9
9
>>> print(3 * add2(4,5))
9
27

>>> def printabunchastuff(a,b,c):
	print(a, b, c, " there you go!!!")
	
>>> printabunchastuff(5,6,7)
5 6 7  there you go!!!
>>> printabunchastuff("larry", "moe", "curly")
larry moe curly  there you go!!!
>>> 

>>> def x(a):
	b = a + 5
	print(b)
	
>>> print(x(10))
15
None
>>> x(10)
15
>>> print(3*x(10))
15
Traceback (most recent call last):
  File "<pyshell#54>", line 1, in <module>
    print(3*x(10))
TypeError: unsupported operand type(s) for *: 'int' and 'NoneType'
>>> 
```
