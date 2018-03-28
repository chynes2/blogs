As we facilitators have mentioned multiple times in class, errors in Python are our friends. For the most part, errors provide helpful hints on how to make your code run.

First let's take a look at an example of an error message and dissect its components. 
```python
---------------------------------------------------------------------------
TypeError                                 Traceback (most recent call last)
<ipython-input-1-77d90ba7d4e3> in <module>()
----> 1 print("I ate " + 4 + " burritos")

TypeError: must be str, not int
```
Starting from the top, we see the error type in red (here: "TypeError"). Next, in green, we see the location of the code we just ran in memory. Indented under that we find the code snippet reproduced, with an arrow indicating the line that threw the error. Finally, we see the error type again in red, and next to that the error explanation.

Sometimes, when your code is calling other functions or libraries, you'll get a multi-step "traceback", or list of steps that caused the error. See for example the below:
```python
---------------------------------------------------------------------------
TypeError                                 Traceback (most recent call last)
<ipython-input-2-de23f2e705ef> in <module>()
      2     print("I ate " + 4 + " burritos")
      3 
----> 4 my_func()

<ipython-input-2-de23f2e705ef> in my_func()
      1 def my_func():
----> 2     print("I ate " + 4 + " burritos")
      3 
      4 my_func()

TypeError: must be str, not int
```
See how the first line of the error message says "most recent call last"? That means that the code snippet at the very bottom was the last code to execute. Typically, that last bit of code is where you'll want to look to find out what went wrong. Here we get the same error type as before but python didn't throw the error until it ran the code in my_func().  

[Here is a link](https://docs.python.org/2/library/exceptions.html) to a list of all the standard exception/error types in Python 2, if you're interested in reading about them.

The main thing to remember when reading error messages is to focus on the last (i.e. most recently executed) code snippet and the error explanation in the last line. With practice, you'll be able to take a quick look at an error message and have a pretty good idea of what went wrong. But this practice will only come with seeing lots of error messages, so don't be discouraged when code you've written throws you an error!
