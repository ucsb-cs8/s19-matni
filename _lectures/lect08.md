---
num: "lect08"
lecture_date: 2019-04-18
desc: "More exercises with loops"
ready: true
pdfurl: /lectures/pdf/lect08.pdf
annotatedready: false
---

<a href="{{page.pdfurl | relative_url }}" data-ajax="false">Slides PDF</a>

# Python Demo Code Used

Try these out again on IDLE and re-live the glory times from class... :)

```

def prime(n):
    p = True
    for i in range(2,n):
        if n%i == 0:
            p = False
    return p

# Testing out our prime() function
for i in range(2,3001):
    if prime(i):
        print(i)

p = 1
for x in range(1,11):
    p = p * x
print(p)
```
