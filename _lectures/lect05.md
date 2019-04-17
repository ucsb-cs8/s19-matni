---
num: "lect05"
lecture_date: 2019-04-16
desc: "Modules in Python; Conditionals"
ready: true
pdfurl: /lectures/pdf/lect05.pdf
annotatedready: false
---

<a href="{{page.pdfurl | relative_url }}" data-ajax="false">Slides PDF</a>

# Python Demo Code Used

Try these out again on IDLE and re-live the glory times from class... :)

```
def return_dbl( x ):
    return x*2

def print_dbl( x ):
    return(x*2)
    print(x*2)
    
a = 13
x = return_dbl(a)
print("x =", x)

y = print_dbl(a)
print("y = ", y)

a = int(input("Enter a number: "))
# The above line makes the program
# ask the user for a direct input
# into an integer. 

if (a < 5):
    print("It’s less than five!")

if (a < 5):
    print("It’s more than five!!!")

else:
    print("It’s equal to five!!!!!")
```

```
Python 3.7.2 (default, Dec 29 2018, 00:00:04) 
[Clang 4.0.1 (tags/RELEASE_401/final)] on darwin
Type "help", "copyright", "credits" or "license()" for more information.

>>> L = [1,2,3]
>>> print(L*2)
[1, 2, 3, 1, 2, 3]
>>> 
>>> print(L*20)
[1, 2, 3, 1, 2, 3, 1, 2, 3, 1, 2, 3, 1, 2, 3, 1, 2, 3, 1, 2, 3, 1, 2, 3, 1, 2, 3, 1, 2, 3, 1, 2, 3, 1, 2, 3, 1, 2, 3, 1, 2, 3, 1, 2, 3, 1, 2, 3, 1, 2, 3, 1, 2, 3, 1, 2, 3, 1, 2, 3]
>>> 
>>> print(L[0])
1
>>> print(L[0]*2)
2
```
