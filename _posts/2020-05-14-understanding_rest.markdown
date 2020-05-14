---
layout: post
title:      "Understanding REST"
date:       2020-05-14 23:21:33 +0000
permalink:  understanding_rest
---

When coming to the message board app the '/' route is set up in the application controller to redirect to '/login'. On this page a user can either create an account or login. I'll be giving a detailed explation on the flow of both of these options. Everytime a user clicks on a link or submits a form, they're making an HTTP request to a specific URL in this application. When a user selects the link to create an account it sends a GET request to '/users/signup' which renders a signup form. Once the form is completed, it will send a POST request to '/users' which will check to see if the user was correctly created and assign a session id and redirect to '/posts'. The '/posts' route first checks to see if you are logged in then serves as a page where create a post, view your post if you have any, and view what everyone else has posted on the message board. 

If you have an account the  '/login' page has fields where you can log in to the app. After entering your information then selecting submit, it sends a POST request to '/login' that will authenticate the user's information, assign a session id, and redirect to the '/posts' page. I struggle with finding the appropriate way to explain the flow of requests and responses, but I feel that writing this blog has given me a clearer image of what that flow looks like. 
