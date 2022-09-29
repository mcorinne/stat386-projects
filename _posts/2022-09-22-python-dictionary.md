---
layout: post
title:  "A Beginner's Guide to Python Dictionaries"
date:   2022-09-28
author: Corinne McClelland
description: A step-by-step tutorial to help you be able to create, delete, and add/remove values from a dictionary in Python
image: /assets/images/dictionary.jpeg
---

So you're new to Python and just discovering dictionaries. You're not sure what they are, what they are used for, or (most importantly) how to create one. Don't worry! We're here to answer all your questions and give you a step-by-step guide along the way. Let's begin!

## What is a Python dictionary?

Before making your own dictionary, it's important to know what it actually is. A dictionary is a data structure that is essentially a collection of items. What is unique about a dictionary is that it stores your data in key-value pairs. This may seem confusing, but it can be a really helpful tool when looking at data. A key-value pair consists of two related data elements. The key is a constant that defines the data set, and the value is something that could belong to that data set. Examples of keys include color, occupation, gender, hometown, book, etc. The values would then be something like green, data scientist, non-binary, Seattle, Jane Eyre. You get the idea.

Dictionaries are ordered and mutable, which means that the data can be changed. You can add and remove data from a dictionary after it's been created, but you can't have duplicates. Each key/value pair MUST be unique. This means you can't have two keys that are the same. If you try to do so, it will just overwrite the previous value stored in the key. However, if you need to store multiple values in a key, you can do that! Just make the value a list or another dictionary rather than a single value. 

## How do I create a dictionary in Python?

Creating a dictionary is actually relatively simple. You just put your data in curly braces {} and separate it with commas. The key-value pairs are inputted using the format (key: value). You can make an empty dictionary to fill with values later, or you can put values in your dictionary immediately. The example code below should make this more clear. 

#### An empty dictionary
`empty_dict = {}`

`print(empty_dict)`

#### A dictionary with integer keys
`my_dict = {'author': 'Charlotte Bronte', 'book': 'Jane Eyre'}`

`print(my_dict)`

#### A dictionary with mixed type keys
`example_dict = {'occupation': 'librarian', 1: [a, b, c]}`

`print(example_dict)`

#### Output:

`{}`

`{'author': 'Charlotte Bronte', 'book': 'Jane Eyre'}`

`{'occupation': 'librarian', 1: [a, b, c]}`


## How do I access dictionary items?

This can be done in seveal different ways. The standard way to access items is by using brackets [], but Python also provides many differrent built-in methods for accessing items as well. We'll explore them all below!

#### bracket notation

This notation allows you to access a single item in the dictionary. For example if you have a dictionary that looks like:

`best_song = {'red': 'all too well', '1989': 'wildest dreams', 'reputation': 'delicate', 'lover': 'afterglow', 'folklore': 'cardigan', 'evermore': 'no body no crime'}`

You can now use the bracket notation to access a single item. For example,

`print(best_song['reputation'])`

will give you the output:

`delicate`

#### get() method

Now, we're moving on to the provided Python methods for dictionaries. The get() method is very similar to the bracket notation. With get(), you access a single item in the dictionary.

`print(best_song.get('reputation'))`

`delicate`

#### keys() method

The keys method allows you to check all available keys within a dictionary. 

`print(best_song.keys())`

This will print:

`dict_keys(['red', '1989', 'reputation', 'lover', 'folklore', 'evermore'])`

#### values() method

The values method is very similar to the keys method, printing all the values in the dictionary rather than the keys.

`print(best_song.values())`

This will print:

`dict_values(['all too well', 'wildest dreams', 'delicate', 'afterglow', 'cardigan', 'no body no crime'])`

#### items() method

You can access all items in your dictionary using the items method.

`print(best_song.items())`

This will print:

`dict_items([('red', 'all too well'), ('1989', 'wildest dreams'), ('reputation', 'delicate'), ('lover', 'afterglow'), ('folklore', 'cardigan'), ('evermore', 'no body no crime')])`

## How do I change/add values to my dictionary?

Because dictionaries are mutable, it is very easy to change or add values to your dictionary. In order to change/add values in dictionaries, you simply use an assignment operator ("="). If you use the operator and the key you are assigning the value to is already present in the dictionary, it will change the value. If it is not present, it will add that key-value pair to the dictionary.

`student_dict = {'Name': 'Lars Brooks', 'Major': 'English', 'Age': 20}`

#### changing value

`student_dict['Major'] = 'Data Science'`

`print(student_dict)`

#### adding value

`student_dict['netid'] = 'lbrooks'`

`print(student_dict)`

##### Output
`{'Name': 'Lars Brooks', 'Major': 'Data Science', 'Age': 20}`

`{'Name': 'Lars Brooks', 'Major': 'Data Science', 'Age': 20, 'netid': 'lbrooks'}`

## How do I remove values from my dictionary?

To remove values from a Python dictionary, you can again use several different methods. We'll use the dictionary we created above for our examples.

#### pop() method
This method removes an item from your dictionary given the specified key name.

`print(student_dict.pop('Age'))`

`{'Name': 'Lars Brooks', 'Major': 'Data Science', 'netid': 'lbrooks'}`

#### popitem() method
This method removes the LAST inserted item on your dictionary.

`print(student_dict.popitem())`

`{'Name': 'Lars Brooks', 'Major': 'Data Science'}`

#### del
This method can either remove an item with a specified key name (like the pop() method), or it can delete the entire dictionary. Using the dictionary we created above again, we can say:

`del student_dict['Age']`

`print(student_dict)`

`{'Name': 'Lars Brooks', 'Major': 'Data Science', 'netid': 'lbrooks'}`

OR

`del student_dict`

If you try to print a dictionary after it is deleted, you will get an error message because the dictionary no longer exists.

#### clear() method
You can use this method to empty your dictionary without deleting it.

`print(student_dict.clear())`

`{}`

## Conclusion

Dictionaries are an extremely useful tool when working with data. This post was not an exhaustive look at dictionaries. There are many more methods you can use with dictionaries to explore your data! As you become more familiar with dictionaries, explore these other methods! Below are a list of resources that can help you in your dictionary journey.

[HubSpot on Python Dictionaries](https://blog.hubspot.com/website/python-dictionary)

[Learning Actors on Python Dictionaries](https://learningactors.com/a-complete-guide-to-python-dictionaries-for-beginners/)

[Real Python on Python Dictionaries](https://realpython.com/python-dicts/)

[Key-Value Pairs Explained](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/key-value-pairs-explained.html?lang=en)
