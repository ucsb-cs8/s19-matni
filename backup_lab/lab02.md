---
layout: lab
num: lab02
ready: true
desc: "Writing functions and tests"
assigned: 2019-1-22 13:00:00.00-7
due: 2019-1-25 23:59:00.00-7
csxx: cs8
---

In this lab, you'll get more practice with:

* Wrting functions
* Testing functions with pytest

## This lab must be done solo

<p>This is a somehow "easy" lab - you are going to write 2 simple functions (one to find the perimeter of a rectangle and another to calculate the area of a triangle). The main point is HOW TO BEST TEST FUNCTIONS once they are written. The writing of a function is fun and can be creative, but we HAVE to be able to test it properly and thoroughly and that often involves not just good creativity, but good technique.</p>
<p>We will be using `pytest`, like we did before in lab01 in order to write TEST CASES. When you finally submit your work on Gradescope, the autograder will go ahead and test your code in even more ways.</p>

## Step 1: Verify that `pytest` is working on the machine you plan to work on

Similar to lab01, you can check whether pytest is installed by typing in the following command in the Python shell prompt. If it returns no error message, then `pytest` is installed. If you get an error, refer back to lab01 from last week for instructions on installing it.

```
[cgaucho@csil-12 ~]$ python3
Python 3.4.3 (default, Aug 9 2016, 15:36:17)
[GCC 5.3.1 20160406 (Red Hat 5.3.1-6)] on linux
Type "help", "copyright", "credits" or "license" 
for more information.
>>> import pytest
>>>
```

## Step 2: Make a `~/cs8/{{page.num}}` folder.

The easiest way to create this is to do the following, which will work from any directory:

`mkdir -p ~/cs8/{{page.num}}`

That form of the `mkdir` command, with the `-p` has the advantage that

* It creates the entire path of directories in case any of the intermediate
   ones don't exist (that is, it will create a `~/cs8` directory too if it
   isn't there yet).
* If the directory being create already exists, it won't complain.
* Since the directory being created starts with `~`, it's an absolute path, and thus the command works regardless of the current directory.

Then, to get yourself into that directory, type:

`cd ~/cs8/{{page.num}}`

Again, since that's an absolute path, it works from any directory.

## Step 3: Create a file called `{{page.num}}.py` in your `~/cs8/{{page.num}}` directory

To start out {{page.num}}, write the line:

```
import pytest
```

Then, copy this function definition into your
{{page.num}}.py file.

```
def perimRect(length,width):
   """ Compute perimeter of a rectangle """
   return -42.0 # stub  @@@ replace this stub with the correct code @@@   
```

Then, copy these function definitions into your file. These are a special kind of function called a <em>test case</em>.  These particular test cases are written in the style used by the <em>pytest</em> testing framework, and they follow these rules:

1. The name of each test cases function must start with `test_`.
2. Each one ends (typically) with a line of code that starts with the keyword `assert`, followed by a boolean expression.
   * If the expression is `True`, the test case <em>passes</em>
   * If the expression if `False`, the test case <em>fails</em>
3. Each test case function must have a different name (hence: `test_perimRect_1`, `test_perimRect_2`, `test_perimRect_3`, etc.)  They don't have to be consecutive numbers&mdash;we could use `_a`, `_b`, `_c` or anything really, as long as they are all different. In general though, your parameter, variable, and function names should be descriptive for better readability.

```
def test_perimRect_1():
   assert perimRect(4,5)==18

def test_perimRect_2():
   assert perimRect(7,3)==20

def test_perimRect_3():
   assert perimRect(2.1,4.3)==pytest.approx(12.8)
```

Finally, run the code, and ensure that you don't have any syntax errors in your Python code.

## Step 4: Test your code by hand

Because we want to be sure that you continue to practice the skill, test your code by hand first.

That is, select "Run Module" in IDLE, and then type in a few function calls at the Python Shell Prompt. Here are a few:

```
>>> perimRect(4,5)
-42.0
>>> perimRect(7,3)
-42.0
>>> 
```

Ok, so that's sort of pointless as long as we haven't fixed the function yet. The point is that
* you need to know how to check the value of a function call by typing it in.
* you need to see that right now, the function *always* returns -42.0, no matter what.

There is a reason for that.  We call this a "stub value".  It returns the wrong answer *on purpose* so that we can check that all of the tests fail. We want to see all of the tests fail, THEN see all of the tests pass. That's the general idea.

* We want so see them *all fail* when the function is wrong.
* Then if they *pass* when the function is right, we *trust* the test.

## Step 5: Run pytest on the file so far

As a reminder, you run pytest OUTSIDE of idle, at the regular terminal
prompt.

You may find it helpful to bring up a second terminal window and use

```
cd ~/cs8/{{page.num}}
```

to get into the correct directory.  Then use:

```
python3 -m pytest {{page.num}}.py
```

You should see three test failures. If you do, then you ready to fix the code so that it works, which is the next step.

(If you need a refresher on how to interpret the output of `pytest`, refer back to lab01 from last week!)

## Step 6: Fixing the code for `perimRect`

So, if you have failing test cases, the thing to do is fix the code so that the test cases pass.

Of course the formula for the perimiter of a rectangle with length $$ l $$ and width $$ w $$ is, in math notation: $$ p = 2l + 2w $$. But you'll have to convert that into Python, and use the variables `length` and `width` to get it to work properly.   

Once you have the code correct, try testing both using interactive testing as well as by running `pytest`.

You are by no means finished with this lab. But, we want to encourage you to make a submission to Gradescope now anyway. Here is why:

1. After you upload your file (and this must be done each time someone uploads a file), you must add your partner (if you're working with one) on Gradescope by selecting "Group Members" -> "Add Member" and selecting your partner from the list.

2. It will be a way that you can share your work in progress with your pair partner. Both of you will be able to login to Gradescope and access the file(s) you uploaded.

3. It provides a backup copy of your work in case something goes wrong with your computer (yes, this happens and you want to make sure there is a backup somewhere).
    
4. It provides a staging ground for you to move your file between you and your partner.

5. You also will be able to see some progress towards completion of the lab&mdash; partial credit for completion of this step.

Once you've submitted and you see that you have 50/100 points, you are ready to continue with the rest of the lab.

## Step 7: Write a `areaTriangle` function and test cases.

You will write your own function `areaTriangle(base, height)` and some test cases in your {{page.num}}.py file. Be sure you define your function's signature with the exact name shown here. It's also a good habit to define comments for all the functions you write. Include a comment for `areaTriangle` to describe what this function does. Note that the function comments have to either be in a string (as explained in the textbook), enclosed in triple single-quotes, or enclosed in triple double-quotes (as shown in the `perimRect` function). Your function should return the area of a triangle using the base and height parameter values.

You should try to make the function pass the test cases that you put in.

In some cases you'll be given the test cases. In other cases, you have to supply these test cases yourself.

At each step, you should first try to get the test cases to pass by running pytest at the Unix command line as discussed above.

* Please do this BEFORE submitting to Gradescope.
* Please DO NOT upload your file to Gradesope without testing locally first.

Once you see your tests are passing, THEN submit a version to Gradescope to see if you also pass the test cases the instructor defined in Gradescope.

If you pass your own tests, but NOT the instructor supplied tests, then try to see if you can figure out why. Are there some cases that you did not consider?

In this step, you must define three test cases to test `areaTriangle`. The code for the first test case looks like this

```
def test_areaTriangle_1():
  assert areaTriangle(4,5) == 10
```

The second and third test case should be one that you come up with yourself. The restrictions are:

* the test functions must be called `test_areaTriangle_2` and `test_areaTriangle_3`
* they should have an `assert` statement
* the assert keyword should be followed by a call to `areaTriangle` with different parameter values in each test. This is followed by a test for equality using `==`, which is followed by the value that you expect `areaTriangle` to return for those argument values.

Once this is done, then:

* test your code with "Run Module" to make sure your code compiles without errors (i.e. no red messages).
* use `python3 -m pytest {{page.num}}.py -k areaTriangle` to run just the test cases for the `areaTriangle` function (there should be three of them, and three skipped test cases for perimRect).

Once everything passes correctly with `pytest`, submit your `{{page.num}}.py` file to Gradescope again to see if your submission passes the `areaTriangle` tests. You should see that you now have 100/100 points if the `perimRect` and `areaTriangle` tests pass. 
 

## Step 8: Uploading your files to Gradescope

Navigate to the Lab assignment {{page.num}} on Gradescope and upload your `{{page.num}}.py`. 
Your Gradescope submission will be autograded out of 100 points. 

