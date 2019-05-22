---
num: "lect13"
lecture_date: 2019-05-14
desc: "Examples of File Input/Output; Midterm2 Review"
ready: true
pdfurl: /lectures/pdf/lect13.pdf
annotatedready: false
---

<a href="{{page.pdfurl | relative_url }}" data-ajax="false">Slides PDF</a>

# Python Demo Code Used

Try these out again on IDLE and re-live the glory times from class... :)

There are 3 files here: **rainfall.py**, **advanced_rainfall.py**, and the input text file **rainfall.txt**.

```py
# Rainfall Example
# (c) 2017 by Ziad Matni for CS8

inputFile = open("rainfall.txt","r")
outputFile = open("report.txt", "w")

outputFile.write("Here's the rainfall report from around the nation!\n")
outputFile.write("--------------------------------------------------\n")


allLines = inputFile.readlines()

for line in allLines:    
	values = line.split()    
	outputFile.write(values[0]+" had "+values[1]+" inches of rain.\n")

inputFile.close()
outputFile.close()
```

```py
# (Advanced) Rainfall Example
# (c) 2017 by Ziad Matni for CS8

inputFile = open("rainfall.txt","r")
outputFile = open("report.txt", "w")

outputFile.write("Here's the rainfall report from around the nation!\n")
outputFile.write("--------------------------------------------------\n")


allLines = inputFile.readlines()
total = 0
numberOfLines = len(allLines)

# Alternate method:
# numberOfLines = 0

for line in allLines:
        # Alternate method:
        # numberOfLines += 1
        values = line.split()    
        outputFile.write(values[0]+" had "+values[1]+" inches of rain.\n")
        total += float(values[1])

average = total/numberOfLines
f = "The average rainfall of every town is: {0:5.2f}"
outputFile.write(f.format(average))


inputFile.close()
outputFile.close()
```

```
Akron 25.81
Albia 37.65
Algona 30.69
Allison 33.64
Alton 27.43
AmesW 34.07
AmesSE 33.95
Anamosa 35.33
Ankeny 33.38
Atlantic 34.77
Audubon 33.41
Beaconsfield 35.27
Bedford 36.35
BellePlaine 35.81
Bellevue 34.35
Blockton 36.28
Bloomfield 38.02
Boone 36.30
Brighton 33.59
Britt 31.54
Buckeye 33.66
BurlingtonKBUR 37.94
Burlington 36.94
Carroll 33.33
Cascade 33.48
```
