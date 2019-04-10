---
num: "lect03"
lecture_date: 2019-04-09
desc: "Variables and Strings"
ready: true
pdfurl: /lectures/pdf/lect03.pdf
annotatedready: false
---

<a href="{{page.pdfurl | relative_url }}" data-ajax="false">Slides PDF</a>

# Python Demo Code Used

Try these out again on IDLE and re-live the glory times from class... :)

```py
Python 3.7.2 (default, Dec 29 2018, 00:00:04)
[Clang 4.0.1 (tags/RELEASE_401/final)] on darwin
Type "help", "copyright", "credits" or "license()" for more information.
>>>
>>> type(2)
<class 'int'>
>>> str(2)
'2'
>>> int(4.2)
4
>>> int(4.9)
4
>>> True
True
>>> False
False
>>> int(True)
1
>>> int(False)
0
>>> float(True)
1.0
>>> int("42")
42
>>> pi = 3.14159
>>> radian_angle = 0.7853975
>>> degree_angle = radian_angle*180/pi
>>> print(degree_angle)
45.0
>>>
>>> a = 3
>>> b = 4
>>> print(a)
3
>>> print(a==b )
False
>>> print(a != b)
True
Traceback (most recent call last):
  File "<pyshell#28>", line 1, in <module>
    print(a=b)
TypeError: 'a' is an invalid keyword argument for print()
>>>
>>> name = input("Do you like cats? What is your name?")
Do you like cats? What is your name?Joe
>>> print(name)
Joe
>>> age = input("What is your age? ")
What is your age? 99
>>> print(age)
99
>>> type(name)
<class 'str'>
>>> type(age)
<class 'str'>
>>>
>>> print("Your age plus 2 is: ", age + 2)
Traceback (most recent call last):
  File "<pyshell#60>", line 1, in <module>
    print("Your age plus 2 is: ", age + 2)
TypeError: can only concatenate str (not "int") to str
>>> print("Your age plus 2 is: ", int(age) + 2)
Your age plus 2 is:  101
>>>
>>>
>>> name = "Roger"
>>> print(name + "!!")
Roger!!
>>> print((name + "!!")*9)
Roger!!Roger!!Roger!!Roger!!Roger!!Roger!!Roger!!Roger!!Roger!!
```

The little program we did was this one:
```py
print("Hello! Let's play a game!")
name = input("What's your name? ")
age = input("What's your age? ")

myage = 99.5
print("That's awesome,", name, "!")
print("My name is Supreme and I am", myage, "years old")

diff = myage - float(age)
print("Our age difference is: ", diff)
```
