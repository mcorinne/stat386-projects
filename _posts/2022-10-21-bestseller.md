---
layout: post
title:  "Finding the Most Popular Books of the Past Decade"
date:   2022-10-21 11:24:47 -0700
author: Corinne McClelland
description: How to collect custom bestseller book lists using the New York Times API.
image: /assets/images/Books.jpeg
---

# Introduction
Working at a bookstore, it's important to know which books are going to sell. The New York Times Bestsellers list is one of the most authorative rankings of bookselling out there, and luckily you can customize your own book listing depending on what information you want to know. On its list, the New York Times provides how many weeks the book has been on its list, the publisher, and the author. This information is helpful to me to get an idea of what books are going to be more likely to sell, what publishers and authors I should buy from, etc. It could be helpful to you in knowing what books you want to read! Let's begin.

# Get Your API Key
In order to get your NYT API key, you'll need to start a developer's account (good news, it's free!). You can do that now by following [this link](https://developer.nytimes.com/accounts/create). All you'll need is your first and last name, email, and a password that you create.

![Test Image](https://raw.githubusercontent.com/mcorinne/stat386-projects/main/assets/images/Developer.png)

Now, follow these steps:
1. Once you've created your account, you can sign into the account [here](https://developer.nytimes.com/accounts/login), using the email and password you created. 
2. Afterwards, click on drop down menu under your name in the top right corner and select "Apps." In order to get your API key, you'll need to create an "app." 
3. All you need to do here is select the button in the top right corner that says "+ New App," give your app a name and description, and then choose which API you'd like to enable. In this case, you'll want the Books API, but notice how many other APIs that the NYTs offers! 
4. Now, save the changes you've made and *voila* you have your API key.

# Find the Required Endpoint Parameters
On their website, the New York Times has a nice overview of the Books API that you can find [here](https://developer.nytimes.com/docs/books-product/1/overview). Basically, there are two main kind of lists that the Books API provides: rankings according to how many books have been sold or a list of book reviews. We'll be focusing on the rankings in this article. 

When obtaining a list with your API key, the url will look something like this:

`my_url = "https://api.nytimes.com/svc/books/v3/lists/current/hardcover-fiction.json?api-key=yourkey"`

The two main features that we'll want to pay attention to in this url are the list data, or the information that comes after lists/ in the url. According to the website, "the lists/{date}/{name} service returns the books on the best sellers list for the specified date and list name." 

#### {date}
If you want the current NYT Bestsellers list, you just put "current" in the date section of the url. However, if you want the NYT Bestsellers list for a specific date, you put in the date in this format: YEAR-MONTH-DATE. For example, 2012-05-30 for May 30, 2012. 

#### {name}
The New York Times has lists for books in different formats (hardcover, paperback, and e-book) and genres (fiction and non-fiction). In order to get a list of a cetain format and genre, you would need to put in one of these values: hardcover-fiction, trade-fiction-paperback, e-book-fiction, hardcover-nonfiction, paperback-nonfiction, e-book-nonfiction.  


