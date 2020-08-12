---
title: What the heck is an ORM?
layout: post
date: 2020-06-03T01:51:21.942Z
excerpt_separator: <!--more-->
---
You've heard it said a millions times by senior developers but you never quite understood what it meant. So you just put it in the bucket of weird tech terms and acronyms that I will nod my head at and maybe do a google search on when you're taking a bathroom break. 

<!--more-->

Finally after working with a few different ORMs I had the aha moment and understand what they are. I worked with `mongoose` early in my career and if you asked me what it was then I would say it's just the thing that I need to make MongoDB work. Most recently I've been working with `ActiveRecord` within Rails, and if you asked me what it was a couple months ago I would have just said it's something that rails uses, but rails has the real magic. 

It wasn't until I started building something on my own and I got to the point where I thought, Hey something to help manage my table relationships would be really great right about now, and then it clicked!

The job of an ORM is to make operations on your database in your language of choice without having to write pure SQL queries (or NoSQL whatever). It also makes it easier to map relationships between your tables so you can access your relational data with less code (and less thinking). 

At first it might seem like a lot of work, but it becomes less work when you have many tables with many relationships. You don't want to have to write the same sql queries over and over again to do simple CRUD operations on each one because this can require quite a bit of overhead. Instead you can learn the ORMs pattern and then make your queries with these simple patterns without having to worry about what is happening behind the scenes. 

I can hear people ringing sirens in the background saying "OH then we're allowing the developer to be lazy and end up making things super non-performant because they have no idea what's going on." But that's the point. We want to let the developer be lazy. We should choose a good ORM tool that can perform our basic queries in a simple and performant manner that we can trust. Then when you need to write a more complex query where the ORM doesn't work or you notice the query is slow, then you can write your custom SQL. But let's not waste time with premature optimization by writing every query to the database in pure SQL. 

You can write an entire full-stack application with no ORM in sight, but it just might be a little easier if you use an ORM.

And that's it! An ORM's job is actually pretty simple and concise. Why does it need it's own Wikipedia page? And why do senior developers talk about it like it is this complex thing that you have to be senior to understand? Those questions are for another night. 

##### But wait! You didn't answer what the heck *is* an ORM?

Right! An ORM is a library or a tool or whatever you want to call it. Some are open-source and some are not. They are just another chunk of code that you add to your toolbelt when building an application depending on what language you want to use and what type of database you are using. 

The ORMs that I am familiar with are:

### Javascript

* mongoose
* sequelize

### Python

* SQLAlchemy
* Django (lives within the Django framework)

### Ruby

* ActiveRecord (used in the Rails framework)

But [there are a TON more listed here](https://en.wikipedia.org/wiki/List_of_object-relational_mapping_software).