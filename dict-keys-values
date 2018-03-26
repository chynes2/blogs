In a recent class, a student asked how to "flip" or reverse the keys and values in a dictionary. This can occasionally be useful for data analysis.

There are -- as usual in python -- many ways to accomplish this. I'll run through a few in this post!

Imagine that we've defined a dictionary and saved it to a variable called dictionary.

One way to create a reversed copy of dictionary is this:

   >> reverse_dictionary = {val:key for key, val in dictionary.items()}

Warning: the above is only available in Python 3. This syntax is similar to Python's list comprehensions and generators. We haven't and won't cover these in class, but I encourage you to look up the docs if you're interested. Don't worry if this looks a little strange. More importantly, now you know this does work, so you're free to use it in your own code!


Here's how you'd do the same thing as above in Python 2.

   >> reverse_dictionary = dict((val, key) for key, val in dictionary.items())

The above code generates an iterable of tuples and then casts that to a dictionary. Again, don't stress if that doesn't mean anything to you; knowing that this also works is what's important.


Here's another interesting way to reverse a dictionary.

   >> reverse_dictionary = dict(zip(dictionary.values(), dictionary.keys()))

To interpret this code, read it inside-out, starting with what's deepest inside the parentheses and working outwards. We first grab our dictionary's values and keys using their respective methods. We then utilize Python's built-in zip() function (look up the docs if you're interested in how zip() works). Finally, we cast our zip() object to a dict(). 


How do you choose which code snippet to use? Well, if you're concerned about computation time (a.k.a. efficiency), the best choice will depend on the size of dictionary. When your original dictionary is relatively small (i.e. less than 100 entries), the top code snippet is the fastest of the three. When your original dictionary is big (i.e. more than 1000 entries), the bottom code is the fastest. 


Thanks for reading this post and happy coding!
