---
layout: post
title:      "JS Single Page Application"
date:       2019-12-27 00:53:49 +0000
permalink:  js_single_page_application
---


I created this application as a simple way of organizing deliveries for certain farmers. The application only has two models being used: farmer and delivery. A farmer has many deliveries and deliveries belong to a farmer. This is the simplest relationship in rails that satisfies the constraints of this project.

The purpose of this application is to be able to demonstrate the capabilities of updating delivery attributes by clicking (+) or (-) buttons. The complete CRUD operation can be seen best demonstrated once the user has selected a specified farmer from the list. The user is also able to create new farmers, which updates the rails database. Currently only the deliveries have complete CRUD specifications, because farmers lack the delete/update feature. 

The rails API used in this application was created to be as lightweight as possible, while the overwhelming focus remains in the javascript side of the single page app. The rails API uses fastjsonapi gem to generate the json data used to populate the HTML. Though, because of the simplicity of the application and the nature of the model update mechanisms, the serializer was really only used on one of the models (farmer). 

For the delivery model, the update part happens on one attribute at a time. The only change is updating numerical values. This makes it easier to get small json data to update the HTML frontend as well as update the attributes in rails. 


