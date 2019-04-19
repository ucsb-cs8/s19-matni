---
num: "lect06"
lecture_date: 2019-04-18
desc: "Data Mutation and Related Topics; Intro to Loops"
ready: true
pdfurl: /lectures/pdf/lect06.pdf
annotatedready: false
---

<a href="{{page.pdfurl | relative_url }}" data-ajax="false">Slides PDF</a>

# Python Demo Code Used

Try these out again on IDLE and re-live the glory times from class... :)

```
Python 3.7.2 (default, Dec 29 2018, 00:00:04) 
[Clang 4.0.1 (tags/RELEASE_401/final)] on darwin
Type "help", "copyright", "credits" or "license()" for more information.
>>> for x in range(5):
	print(x + 2)
	
2
3
4
5
6
>>> for x in range(5):
	print(x + 2)
	print("hello!")
	
2
hello!
3
hello!
4
hello!
5
hello!
6
hello!
>>> for x in range(5):
	print(x + 2)
	print
KeyboardInterrupt
>>> 
>>> 
>>> s = 0
>>> for x in range(5):
	s = s + 1
	print("hiya!")

	
hiya!
hiya!
hiya!
hiya!
hiya!
>>> print(s)
5
>>> 
>>> s = 0
>>> for x in range(5):
	s = s + x

	
>>> print(s)
10
>>> 
>>> 
>>> s = 0
>>> for x in range(5):
	s = s + 2*x

	
>>> print(s)
20
>>> for x in range(5):
	s = s - 3*x

	
>>> print(s)
-10
>>> 
>>> s =0
>>> for x in range(5):
	s = s - 3*x

	
>>> print(s)
-30

```
