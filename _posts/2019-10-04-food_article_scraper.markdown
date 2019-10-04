---
layout: post
title:      "Food Article Scraper"
date:       2019-10-04 06:15:06 +0000
permalink:  food_article_scraper
---

I love traveling with my wife and eating great food, so for the CLI project I decided to build an "articles about food" scraper from famous cities across the USA.

In this CLI project, I used the eater.com website for my source on what's going on in the food scene. The website has a list of 24 cities and each city lists up to 36 of the latest food related news articles. 

To start the project, I listed the features and flow of how I wanted the program to operate.

Flow:

1. Greet the user, and list the cities available for the user to explore.
2. Once the user enters a valid index for the city, the program then scrapes the city's latest articles and publishes the title of the article, the author(s), posting date and URL to the article.
3. The program then asks the user if they are interested in another city, if they are not, exit the program.

Features:

* Create each city object instance - has a url, name, and copy of the articles the program scrapes.
* Create each article object instance - has a url, title, authors and posting date. The article also will have a relationship with the city object instance it was created from to access the information from each a lot easier.
* Build a scraper object to get information from the website.
* Have a CLI controller to make the CLI responsible for triggering which city to be scraped. I did not want to scrape the whole website just for a few articles. Since there are 24 cities and up to 36 articles each, the total could be over 800+ article objects that may not even be relevant!

Planning Phase:

Stepping away from the computer and coding environment helped me think clearly to plan out my project. I jotted down what features I wanted and how I wanted the user experience to be in my notebook. It took me three hours to plan out everything, then two hours to get a functional code. After some additional tweaking to make the code easier to understand, the project came together in just under six hours. 

Coding:

The first part I wanted to tackle was taking the url for each major city and the name of that city. Each url contributes to the collection of articles I would need to make article object instances. I used the hash system for gathering the scraped data arranged in the following manner:
```
[{:name => "New York",  :url => "https://ny.eater.com/"}, {:name => "Seattle", :url => "https://seattle.eater.com/"}]
```

Setting it up this way made it easier to use ```City``` object to create individual city instances.

The second part of the ```Scraper``` was responsible for using the city instance url to begin scraping the latest news of that city. A similar format was used to collect the data: arrange an array of hashes that stored key value pairs, which would then be inserted into the initialization of the ```Article``` object.

The first two parts were the hardest and the most time consuming to deal with. However, once I figured out the ```Scraper```  object, it wasn't long until I was able to use the collected data to start generating useful objects for my CLI controller to use.

The  ```City ``` object interacted with the ```Article``` object as both objects collaborate with each other, and article instances cannot exist without city instances. The general hierarchy I started with was to pass a city instance to the article scraper method. Since, the article scraper method would need a url passed in at some point, I just passed in the city instance as an argument to take advantage of the features known only to the ```City``` class, which includes ```:url``` as one of its attributes. From the article scraper method, I was able to simultaneously generate article instances, set each article instance's city to the current city instance ```:name```, and add the generated article instances to the city instance ```:articles``` array. I was able to take advantage of three different objects to make a complex task simple and easy to understand.

Using the ```CommandLineInterfaceControls``` object, all I needed to do was arrange the instance methods such that everytime a user selects a city, the scraping and storing of object instances happens during that time. I did not want to have to scrape data from the whole website, then present it. I wanted the user to be in control of what data is being retreived and what is being shown. This also improves the speed of the program, because instead of creating new objects from previous selections, the program just shows what it already collected.

I thought this project was extremely fulfilling to build, making use of everything I've learned so far. It also gave me a deep appreciation for OOP. Though I do not consider this project to be harder than the tic tac toe AI, I think this is the most fun I've had creating something from start to finish.
