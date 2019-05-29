---
num: "lect14"
lecture_date: 2019-05-28
desc: "Dictionaries"
ready: true
pdfurl: /lectures/pdf/lect14.pdf
annotatedready: false
---

<a href="{{page.pdfurl | relative_url }}" data-ajax="false">Slides PDF</a>

# Python Demo Code Used

Try these out again on IDLE and re-live the glory times from class... :)

```py
Python 3.7.2 (default, Dec 29 2018, 00:00:04) 
[Clang 4.0.1 (tags/RELEASE_401/final)] on darwin
Type "help", "copyright", "credits" or "license()" for more information.
>>> l = [1, 2, 3, "abc", "def"]
>>> max(l)
Traceback (most recent call last):
  File "<pyshell#1>", line 1, in <module>
    max(l)
TypeError: '>' not supported between instances of 'str' and 'int'
>>> l = [1, 2, 3]
>>> max(l)
3
>>> l = ["abc", "def", "bbb"]
>>> max(l)
'def'
>>> 


>>> l = [4, 5, 8, -9, 0, 3, 1]
>>> l.sort()
>>> l
[-9, 0, 1, 3, 4, 5, 8]
>>> 


>>> ages = {'sam':19, 'alice':20, 'bertha':20, 'jim':22, 'pappy':66, 'elizabeth': 7}
>>> print(ages['alice'])
20
>>> 
>>> print(ages['pappy'])
66
>>> print(ages)
{'sam': 19, 'alice': 20, 'bertha': 20, 'jim': 22, 'pappy': 66, 'elizabeth': 7}
>>> 


>>> for a in ages:
	print(ages[a])
	
19
20
20
22
66
7

>>> del(ages['pappy'])
>>> print(ages)
{'sam': 19, 'alice': 20, 'bertha': 20, 'jim': 22, 'elizabeth': 7}
>>> 

>>> ages['sam'] = 29
>>> print(ages)
{'sam': 29, 'alice': 20, 'bertha': 20, 'jim': 22, 'elizabeth': 7}

>>> ages['shelly'] = 21
>>> print(ages)
{'sam': 29, 'alice': 20, 'bertha': 20, 'jim': 22, 'elizabeth': 7, 'shelly': 21}

>>> print(ages.keys())
dict_keys(['sam', 'alice', 'bertha', 'jim', 'elizabeth', 'shelly'])

>>> type(ages.keys())
<class 'dict_keys'>

>>> print(ages.values())
dict_values([29, 20, 20, 22, 7, 21])

>>> print(ages.items())
dict_items([('sam', 29), ('alice', 20), ('bertha', 20), ('jim', 22), ('elizabeth', 7), ('shelly', 21)])

>>> print(ages.keys()[3])
Traceback (most recent call last):
  File "<pyshell#47>", line 1, in <module>
    print(ages.keys()[3])
TypeError: 'dict_keys' object does not support indexing

>>> print(list(ages.keys())[3])
jim

```
