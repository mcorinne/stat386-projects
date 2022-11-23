---
layout: post
title:  "Analyzing the New York Times Best Sellers List"
date:   2022-11-19 11:24:47 -0700
author: Corinne McClelland
description: Let's explore the NYT's most popular fiction books of the past decade together!
image: /assets/images/Bestsell.jpg
---

# Introduction
I work at a used bookstore, and people bring us in new books for the store everyday. Of course, not every book that someone brings in will sell, and the trick is only keeping the books you think someone would buy within a certain period of time (let's say a year). Otherwise, these books are just wasting shelf space. In this blogpost, I explore the NYT's Best Sellers List for hardcover and paperback fiction from the years 2012-2022. You can see how I gathered this data in my blogpost [here](https://mcorinne.github.io/stat386-projects/2022/10/21/bestseller.html). We'll explore which publishers and authors have been on the NYT Best Sellers List the most in the past decade, among other things. Hopefully, by the end of this blogpost I'll be able to use some of this information at my local bookstore. (Hint: I will) Let's get started!

![Pioneer Book](https://raw.githubusercontent.com/mcorinne/stat386-projects/main/assets/images/pioneerbook.jpeg)

# Exploratory Data Analysis
Let's start off with getting a basic grasp of the data we're working with. The NYT Best Seller list ranks 15-20 books each week (usually 15, but in the past it has occasionally been 20). A book is a NYT best seller if it ranks anywhere on the list, and the more consecutive weeks it's on the list, the more impressive it is. I wanted to start off my exploratory data analysis just looking at the typical range for number of weeks a book has been on the NYT best sellers list.

![Boxplot](https://raw.githubusercontent.com/mcorinne/stat386-projects/main/assets/images/Boxplot.png)

This boxplot shows that there is quite a huge range when comparing how many weeks books have been on NYT's list; in the past decade books have been on the list ranging anywhere from 0 weeks to 375. That means that there's a book that has been on the NYT's list for over 7 years! Obviously, looking at this boxplot, we can see that this is not the case for most books. Fifty percent of the books only stay on the list for a week or two. Almost all of the books only stay on the list for less than 40 weeks, and it is only the exceptional few that stay on the list for over a year (let alone seven). If you're curious about which books are the outliers, keep reading!

![Publisher](https://raw.githubusercontent.com/mcorinne/stat386-projects/main/assets/images/Publisher.png)

But first, let's look at the top publishers that have books on the NYT's list. The above graph shows the top 25 publishers that make it on the NYT's Best Sellers list. Among these, there are 5 publishers that really stand out: Grand Central; Putnam; Little, Brown and Company; Scriber; and Atria. These aren't the same book publishing companies that come up if you google which publishing companies are the most popular, so this is helpful information. Clearly, if a book by one of these publishers comes into the bookstore, it would be a good idea to keep it. Although these publishing companies might not be the most prestigious, they sell books that have become massively popular.

![Grand Central](https://raw.githubusercontent.com/mcorinne/stat386-projects/main/assets/images/GrandCentral.png)
Because I hadn't heard very much about the publishing company Grand Central, I wanted to take a closer look at their data. Looking at the authors that have made it onto the NYT's list within this publishing company, it looks like the genres they publish the most are romance (Nicholas Sparks), thriller (David Baldacci, James Patterson), or a mix of both (Colleen Hoover). The books that have stayed on the NYT's list the longest under Grand Central are usually their romance; we can see that their top two books in terms of length on NYT best seller list are by Colleen Hoover and Nicholas Sparks. We can also see that Grand Central Publishing has a few authors that consistently make it on the NYT best sellers list: Nicholas Sparks, David Baldacci, and James Patterson (as a co-author). These authors are popular prolific authors, meaning that they will write a lot of books that people will buy simply because it has their name on the front cover. These authors would be great to have in a used bookstore.  


![Author](https://raw.githubusercontent.com/mcorinne/stat386-projects/main/assets/images/Author.png)

![Colleen Hoover](https://raw.githubusercontent.com/mcorinne/stat386-projects/main/assets/images/ColleenHoover.png)

![Top25](https://raw.githubusercontent.com/mcorinne/stat386-projects/main/assets/images/Top25Titles.png)

![Ranks](https://raw.githubusercontent.com/mcorinne/stat386-projects/main/assets/images/RanksDiff.png)


# Conclusion
In this post, I showed how you can access a NYT API key, how you can use that key to get various NYT Books Bestsellers list, and how you can personalize the data you want within those Bestsellers lists. This information could be useful to see what books have been the most popular over time, what publishers are most likely to have books on the bestsellers list, and what books you might be interested in reading/buying/selling. Let me know in the comments if you have any questions regarding accessing information within these lists. In my next post, I will provide an exploratory data analysis of this data.

Here's a link to my github repo [link](https://github.com/mcorinne/NYTBestsellers.git)
