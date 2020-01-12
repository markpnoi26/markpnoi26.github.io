---
layout: post
title:      "PetFolio React-Redux-App with Material UI "
date:       2020-01-12 11:48:37 +0000
permalink:  petfolio_react-redux-app_with_material_ui
---


First of all, I want to get it out of my chest, I finished! This was probably the most technically challenging project I attempted so far. However, I was able to get through with a simple application and am very relieved about it.

Lets get started. The app is built on the idea that someone can create an account and list their pets and their pet needs,  so pet sitters can view them and know what to do. I am going to walk through the three levels of difficulty in assembling this simple project. I knew I wanted to build a beautiful, modular, relatively easy to build application so I decided to go with a material-ui theme with some free templates found online.

The first level difficulty. This is the easiest part of the project, laying out the whole application on paper and building my rails api. I knew I wanted a simple application that did not need any backend authentication, so I decided to keep the authentication (for an admin user) to the frontend side. Rails really made the work simple, along with the gem Faker, I was able to set up my User and Pet models with corresponding serialized json.

The second level of difficulty was assembling the frontend backbone, meaning assembling the individual containers, components, components from material-ui templates and so forth. I must admit, I had to read through some heavy documentation to get through the styling portion of the app.  It took some time, but once I figured out how to generate HOC (Higher Order Components) using the given methods by material-ui package and the style sheets from Creative-Tim, I was able to generate a beautiful looking UI. All of the reference material used functional components, so I had to convert most of them (for CRUD operations) into class components, then use a higher order component function.

The final level, and the most challenging was redux. I had made the decision to create individual action creators for asynchronous javascript, and add the action object for other simpler functions. This is where using the class components really came in handy, because I ran quite a few of the action methods through the componentDidMount life cycle method. What I found that really helped me was separating out my reducers into their own individual pieces at first. After I started using portions of the redux global state, I took quite a few reducers out, leaving me with the simplest global state I could work with. 

