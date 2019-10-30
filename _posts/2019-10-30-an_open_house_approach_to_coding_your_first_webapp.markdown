---
layout: post
title:      "An open house approach to coding your first webapp"
date:       2019-10-30 05:40:34 +0000
permalink:  an_open_house_approach_to_coding_your_first_webapp
---


Hello, today I am going to share with you some of the key things I learned from building my sinatra application. 

I built a projects manager app for my laboratory I currently work at. In our lab there has always been an organization problem. In my particular case, our lab constantly runs into issues when scientists are working on multiple projects at a time. So I created a web application that makes it easier to manage these projects. I used the corneal gem to get everything set up. If you are lazy like me, corneal makes it simple and easy to create large MVC template.

The main issue I ran into throughout the the Sinatra section was setting up the correct database schema. Part of the problem for most people (including myself) is we try to make things complicated. So the biggest takeaway I got was to just relax and stick to the basics. In this case, I just had to set up the proper relationships of the models.  Scientists have many projects, and projects belong to scientists, simple! One tip I recommend doing, is writing the schema down on paper and literally drawing lines to connect the models together. There are tools out there that can help create diagrams, and they are really useful. As long as it makes a complicated relationship look simple, go for it.

Once the schema was set up, everything from there was smooth. Using the fwitter lab as a guide, I started to approach my own project much in the same way. I started working on the models to reflect the schema. I added the slugs for the scientists names and also created some helper methods. I didn't know if I was going to use any of the code I wrote, but I wrote them anyway just in case I needed it. 

The second most important thing I leveraged was testing my models using tux. I love using tux, because I started to play around and try to "break" my models to see what I can do with it. This eventually came in handy when I had a weird bug with using forms. I encourage anyone reading this, to start by writing simple code and then, try to break it in and test the limits of what you wrote. The better you understand the models, the easier they will be to maintain down the road. 

After reassuring myself that my models are rock solid, I proceeded to work as if the code was like an open house. What do I mean by that? Well, imagine a house you've never been in before, how would you go about navigating through this house? Would you magically find yourself immidiately in the master bedroom? or somehow in the kitchen? No, you would need to go through the proccess of getting a key, then opening the door, then going through the door, then the hallway, then to the rooms of the house. Just like the normal process of entering a home, you need to do all these complicated things before getting to the desired location.

I first had to build a form that we would use as a "key" (username, password, email, etc. register form), so I started working and building that. Once I got the register process to cooperate with the models I created,  I made a "lock and key" mechanism that would bring the guest into the app (sign in form). Once I got the sign in and sessions working I worked on showing the different projects, so on. So the proccess of building an entire web app was condensed into building one small thing, testing the small thing to its limits, then moving on to the next "room". After building all these little things that pile on one another, eventually I found myself getting better at navigating through the different rooms of your application. 

While this all seems simple, the simplicity really comes from setting up a good foundation before doing any complicated code. I made sure the schemas, models and helper methods were as good as they can before attempting any building the webapp. After thinking about it, we programmers today are sitting on the shoulders of giants that came before us, and the foundation they set. Much in the same way, we need to imitate that same mind set before attempting to build the next big thing.

Using this "open house method" is what helped baby step my way into a simple yet powerful application. 
