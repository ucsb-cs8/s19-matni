---
num: "lect09"
lecture_date: 2019-04-30
desc: "More exercises with loops ; Turtle graphics"
ready: true
pdfurl: /lectures/pdf/lect09.pdf
annotatedready: false
---

<a href="{{page.pdfurl | relative_url }}" data-ajax="false">Slides PDF</a>

# Python Demo Code Used

Try these out again on IDLE and re-live the glory times from class... :)

```
# Drawing functions for use with Turtle Graphics
def drawRectangle(t, side):
    for k in range(4):
        t.forward(side)
        t.right(90)

def drawPolygon(myTurtle, sideLength, numSides):
    turnAngle = 360 / numSides
    for i in range(numSides):
        myTurtle.forward(sideLength)
        myTurtle.right(turnAngle)

def drawSpiral(myTurtle, maxSide):
    for sideLength in range(1, maxSide+1, 5):
        myTurtle.forward(sideLength)
        myTurtle.right(90)


# MY MAIN PROGRAM
import turtle
boris = turtle.Turtle()
boris.color("blue")

drawRectangle(boris, 420)

# Let's draw different size polygons with boris!
drawPolygon(boris, 200, 3)
drawPolygon(boris, 200, 4)
drawPolygon(boris, 200, 5)
drawPolygon(boris, 5, 1000)

# Introducing a new purple turtle: samuel
samuel = turtle.Turtle()
samuel.color("purple")

drawPolygon(samuel, 150, 8)
samuel.circle(100)

# Draw a spiral
drawSpiral(boris, 200)

# Natascha example
natascha = turtle.Turtle()
natascha.color("red")

for k in range(6):
    natascha.forward(100)
    natascha.left(60)
    
#natascha.forward(100)
#natascha.left(60)
#natascha.forward(100)
#natascha.left(60)
#natascha.forward(100)
#natascha.left(60)
#natascha.forward(100)
#natascha.left(60)
#natascha.forward(100)
#natascha.left(60)

```
