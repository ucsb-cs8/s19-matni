---
num: "lect11"
lecture_date: 2019-05-09
desc: "String Formats for Printing; namedtuple(); Random numbers"
ready: true
pdfurl: /lectures/pdf/lect11.pdf
annotatedready: false
---

<a href="{{page.pdfurl | relative_url }}" data-ajax="false">Slides PDF</a>

# Python Demo Code Used

Try these out again on IDLE and re-live the glory times from class... :)

```py
Python 3.7.2 (default, Dec 29 2018, 00:00:04) 
[Clang 4.0.1 (tags/RELEASE_401/final)] on darwin
Type "help", "copyright", "credits" or "license()" for more information.
>>> a = 19
>>> b =42
>>> print('{0:3}xyz{1:5}'.format(a, b))
 19xyz   42

>>> a = 12345
>>> print('{0:3}xyz{1:5}'.format(a, b))
12345xyz   42

>>> print('{1:3}xyz{0:15}'.format(a, b))
 42xyz          12345

>>> n = 100/3
>>> n
33.333333333333336
>>> print('{:7.3f}'.format(n))
 33.333
>>> print('{:7.3}'.format(n))
   33.3
>>> print('{:3.7f}'.format(n))
33.3333333

>>> print('{:>7.3}'.format(n))
   33.3
>>> print('{:<7.3}'.format(n))
33.3   


>>> import collections
>>> Person = collections.namedtuple('Person', 'name age gender')
>>> bob = Person(name='Bob', age=30, gender='male')
>>> print(bob)
Person(name='Bob', age=30, gender='male')
 
>>> print(bob.name)
Bob
>>> print(bob.age)
30
>>> print(bob.gender)
male
>>> bob = Person(age=30, gender='male', name='bob')
>>> print(bob.name)
bob
 
>>> print("This person's name is:", bob.name, ", aged" , bob.age)
This person's name is: bob , aged 30

>>> jenn = Person(name="Jenn", age=22, gender="Female")
>>> gorgon = Person(name="Gorgon, destroyer of worlds, harvester of souls", age = 666666, gender="You Fools!!")
>>> for p in (bob, jenn, gorgon):
	print("This person's name is:", p.name)
	print("Their gender is:", p.gender)
	print("Double their age is:", p.age*2)
	print()

This person's name is: bob
Their gender is: male
Double their age is: 60

This person's name is: Jenn
Their gender is: Female
Double their age is: 44

This person's name is: Gorgon, destroyer of worlds, harvester of souls
Their gender is: You Fools!! 
Double their age is: 1333332

>>> type(bob)
<class '__main__.Person'>
>>> type(bob.age)
<class 'int'>
>>> type(bob.age) == 'int'
False
>>> type(bob.age) == int
True
>>> type(bob.gender) == int
False
>>> type(bob.gender) == str
True
>>> type(bob) == Person
True
 
>>> import random
>>> 
>>> print(random.random())
0.12727549323836562
>>> print(random.random())
0.8781645471467662
>>> for i in range(10):
	print(random.random())
0.42577326629820667
0.05166876963672662
0.5660735439515266
0.313018297278544
0.5308803002634204
0.6360394043370114
0.129020431740404
0.040530477587570446
0.6630052694683336
0.02595175598116317

>>> for i in range(10):
	print(20*random.random())
4.142147831378475
10.481792861558517
19.5169541873648
2.729837932701511
4.743854921023791
10.396365465654426
2.4708446468771372
10.088778824106296
8.990737025157635
0.6183555584984823

>>> for i in range(10):
	print(20+random.random())
20.729445791000558
20.034645221244183
20.94982479985309
20.020860712859644
20.77596171677491
20.229997107526973
20.91619091272161
20.432042070910104
20.706088100155014
20.393184223859624

>>> print(random.randrange(5))
1
>>> print(random.randrange(5))
0
>>> print(random.randrange(5))
4
>>> for i in range(5):
	print(random.randrange(5))
1
2
4
2
2

>>> for i in range(10):
	print(random.randint(4, 42))
27
13
40
31
23
22
6
28
20
11
```
