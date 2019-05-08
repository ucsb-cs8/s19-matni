---
num: "lect10"
lecture_date: 2019-04-30
desc: "Debugging using Loop Exercises; String Delimiters and Formats"
ready: true
pdfurl: /lectures/pdf/lect10.pdf
annotatedready: false
---

<a href="{{page.pdfurl | relative_url }}" data-ajax="false">Slides PDF</a>

# Python Demo Code Used

Try these out again on IDLE and re-live the glory times from class... :)

```py
def drawRectangle(width, height):
    for h in range(height):
        for w in range(width):
            print('*', end='')
        print()

def drawRectangle2(width, height):
    for h in range(height):
        print('*'*width)

def countOddNumbers(lst):
    count = 0
    for i in range(len(lst)):
        if lst[i]%2 != 0:
            count += 1
    return count

def countOddNumbers2(lst):
    count = 0
    for i in lst:
        if i%2 != 0:
            count += 1
    return count

def wordCount(sentence):
# This does not pass all cases!!!
    if len(sentence) == 0:
        return 0
    else:
        words = 1
        for c in sentence:
            if c == " ":
                words += 1
        return words

def wordCount2(sentence):
# This does not pass all cases either!!!
    newlist = []
    temp = ""
    for c in sentence:
        if c != " ":
            temp += c
        else:
            newlist.append(temp)
            print(temp) # for debug!
            temp = ""
    if sentence[-1] == " ":
        words = len(newlist) + 1
    else:
        words = len(newlist)
    return words

def wordCount3(sentence):
# That's the way to do this...!    
    l = sentence.split()
    return len(l)
```

