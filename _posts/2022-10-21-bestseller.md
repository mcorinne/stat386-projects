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

# Step 1: Get Your API Key
In order to get your NYT API key, you'll need to start a developer's account (good news, it's free!). You can do that now by following [this link](https://developer.nytimes.com/accounts/create). All you'll need is your first and last name, email, and a password that you create.

![Test Image](https://raw.githubusercontent.com/mcorinne/stat386-projects/main/assets/images/Developer.png)

Once you've created your account, you can sign into the account [here](https://developer.nytimes.com/accounts/login), using the email and password you created. Afterwards, click on drop down menu under your name in the top right corner and select "Apps." In order to get your API key, you'll need to create an "app." All you need to do here is select the button in the top right corner that says "+ New App," give your app a name and description, and then choose which API you'd like to enable. In this case, you'll want the Books API, but notice how many other APIs that the NYTs offers! Now, save the changes you've made and *voila* you have your API key.
