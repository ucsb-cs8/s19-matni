---
num: "lect16"
lecture_date: 2019-06-04
desc: "Recursion"
ready: true
pdfurl: /lectures/pdf/lect16.pdf
annotatedready: false
---

<a href="{{page.pdfurl | relative_url }}" data-ajax="false">Slides PDF</a>

# Python Demo Code Used

Try these out again on IDLE and re-live the glory times from class... :)

```py
#def fac(N):
#    if N <= 1:
#        return 1
#    else:
#        return N * fac(N-1)

# Function to model factorial function using recursion
def fac(N):
    if N <= 1:
        return 1
    return N * fac(N-1)

# Function to model the Fibonnaci Series using recursion
def fibo(n):
    if n == 1 or n == 2:
        return 1
    return fibo(n-1) + fibo(n-2)

# Function to model the mathemtical linear series: a(n+1) = a(n) + 5 where a(0) = 3
def f(n):
    # base case:
    if n == 0:
        return 5
    return f(n-1)+3
```
