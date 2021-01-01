---
layout: post
title:      "Model-View-Controllers"
date:       2021-01-01 17:38:11 +0000
permalink:  model-view-controllers
---


While building out my first web based application, I struggled most with two aspects of the code. 

First, the structure of model-view-controllers (MVCs) was challenging for me to nativigate. There were so many folders and the flow of the application based on these 3 elements was not something I had thought of before. However, building out my application helped me grasp these concepts. The *model* is in charge of your data structure, completely independent from the user interface. The *view* is the presentation of data to the user. And the *controller* accepts user input and includes methods that interact with the model and views. 

Next, understanding and remembering the HTTP methods (a.k.a. verbs) related to the Create, Read, Update and Delete (CRUD) methods was also unexpected. I thought CRUD would include one method per element and one HTTP method per element. That was short sighted to say the least! Each of the CRUD elements have 2 methods, with the exception of destroy:

- **C**reate: New and Create
- **R**ead: Index and Show
- **U**pdate: Edit and Update
- **D**elete: Destroy (phew!)

Each of these elements (New, Create, Index, Show, Edit, Update and Destroy) all have their own RESTful URIs and HTTP methods. (For a complete list of each function, RESTful URI and HTTP method go to [Madeline Stark](https://github.com/Madeline-Stark/sinatra_crud_cheatsheet/blob/main/README.md). This was indispensable for me to grasp CRUD!!). 

It's a relief to be able to use inheritance from ActiveRecord so I no longer need to write out has_many or belongs_to methods. But there was something very straight forward about those methods and a lot of the previous weeks of course material. As we continue through Ruby on Rails and more advance software engineering, I'm starting to realize understanding the interaction between multiple elements (e.g. MVC) will begin to be ever more important and challenging.
