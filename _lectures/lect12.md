---
num: "lect12"
lecture_date: 2019-05-14
desc: "File Input/Output"
ready: true
pdfurl: /lectures/pdf/lect12.pdf
annotatedready: false
---

<a href="{{page.pdfurl | relative_url }}" data-ajax="false">Slides PDF</a>

# Python Demo Code Used

Try these out again on IDLE and re-live the glory times from class... :)

```py
# Demos used in Lecture 12 (File I/O)
# * Review the syntax for writing to and reading from a file in Python (see slides)
# * Review the 4 different ways to read data from a file in Python

# First, let's open a document and WRITE to it (i.e. output file)
#
Growlers = open("MyDemoOutput.txt", "w")

for i in range(50):
    Growlers.write("Here's number " + str(i) + "\n")

Growlers.close()

# Next, let's open the document again, but this time READ from it (i.e. use it as an input file)
#
Bran = open("MyDemoOutput.txt", "r")

for item in range(50):
    line = Bran.readline()
    print(line, end="")

Bran.close()

# Another way to READ a file:
#
Bran = open("MyDemoOutput.txt", "r")

line = Bran.readlines()
print(line)

# OR do this instead:
#
for item in line:
    print(item, end="")

Bran.close()
```
