---
author: Mauro Murru
pubDatetime: 2023-03-01T14:42:52.737Z
title: Let's start to use directus
postSlug: directus-lets-make-a-crud
featured: true
ogImage: /images/directus.png
tags:
  - codeless
  - directus
  - no-code
  - crm
  - boilerplate
  - js
  - ts
description: Creating side projects or digital products is nearly impossible in this case. My "Prof of concept" folder is full of unfinished projects, all stranded before I even started writing the business logic, and this demonstrates that theory.
---

In a sense, low code implements the basic concepts of pragmatism, so let's tinker with Directus a bit.

## The problem

Today we want to try to create a tool that works as a backend for our podcast. It should allow us to configure the podcast feed with all information and allow us to create new episodes.

Our data structure is very simple. We have three tables: 

- the first for the podcasts,
- the second for episodes,
- and the third for the chapters.

![Table struct](/images/directus-crud-1/directus-crud-11.png)

It seems a very simple table structure but being honest, ins the most significant work the podcast hosting services do, let's try to reproduce using Directus.

## Installation and bootstrapping

Installing directus on your computer is a straightforward procedure. Just one requirement, having nodejs installed on your machine is more than enough.

1. First of all, we create a folder that will hold our project
    
    ```bash
    mkdir low-code-with-directus
    cd low-code-with-directus
    ```
    
2. After we initialize the new folder as a nodejs project
    
    ```bash
    npm init
    
    ```
    
3. Once we have answered all the questions npm asks, we can use npx to initialize the directus project inside the folder.
    
    ```bash
    npx directus init
    ```
    
    The next step is to choose the database. In this tutorial, we will use SQLite, but you can use Postgres, MySQL, SqlServer, and more if you already have them installed.
    
    After choosing the database, the Directus installer cli will ask us for our admin username and password. We will choose `admin@example.com` as our username and `password` as our password. 
    
4. Now we are ready to start our directus server.
    
    ```bash
    npx directus start
    ```
    
5. Wippy! now our Directus instance will be reachable at [`http://127.0.0.1:8055/`](http://127.0.0.1:8055/)

## Inside the folder

Before starting to create our tables, let's give a look at the folders and files the Directus scaffolder created for us.

As you can see, we have no directus source file inside the folder, in fact, we run directus directly using `npx`, but no worries, you can still clone the source code following this simple guide included in the contributing area [https://docs.directus.io/contributing/running-locally.html](https://docs.directus.io/contributing/running-locally.html).

![Folder struct](/images/directus-crud-1/directus-crud-0.png)

The other little thing that catches our attention, aside from the database file, is the extension folder, it is here where we can bring into play all our skills as a developer, dancing between javascript, typescript and vuejs, but we will leave this enjoyment for the next posts.

## Creating the tables and the CRUD

Ok, the time has come to start creating our table. Going to [http://127.0.0.1:8055/](http://127.0.0.1:8055/) (if you can't reach the page, remember to run `npx directus start` from the project folder) and authenticate using the email and the password previously created.

![Directus view](/images/directus-crud-1/directus-crud-1.png)

Our application begins with a section called content modules. We will land there after logging in, but since we have no table (also called a collection) created, we will be prompted to create one. It's time to take action!

![Directus view](/images/directus-crud-1/directus-crud-2.png)

When we click on `create collection`, a side panel will appear on the right side, asking us just a few pieces of information:

**Name**: The name of the collection that will correspond with the name of the new table in the database

**Primary key field:** The name of the field used as a primary key

**Primary key type**: I like to use the generated UUID value, which works well for nearly all the situations

**Singleton:** An instance of a collection that is unique. For example, if we are using Directus to act as headless CMS, the contact page could be a singleton, it will have its own data structure, but just one entry in the database will be created.

![Directus view](/images/directus-crud-1/directus-crud-3.png)

A second part of the panel contains optional fields, which are special fields that can be enabled and inherit special features, such as sorting, publishing status, or changes tracking.

![Directus view](/images/directus-crud-1/directus-crud-4.png)

As of now, it's enough just to let them be and press the round button at the top right to begin creating the collection.

We just add a few new fields needed for our podcast hosting solution to our collection setup window, leaving aside all the configurations offered in the collection setup area.

![Directus view](/images/directus-crud-1/directus-crud-5.png)

Now it's time to create new fields based on the schema we created earlier. Let’s add the podcast name, we can create multiple field types, and if not enough, we can also create new ones just by defining a new vuejs extension (we will see how to do it soon).

Now we create a simple input and click on the proposed first field.

![Directus view](/images/directus-crud-1/directus-crud-6.png)

An accordion will be expanded, proposing some basic configurations that we fill.

![Directus view](/images/directus-crud-1/directus-crud-7.png)

We repeat all the previous steps to create all the fields without the “episodes”. That field will be a relation, and we reserve a specific 

![Directus view](/images/directus-crud-1/directus-crud-8.png)

![Directus view](/images/directus-crud-1/directus-crud-9.png)

We repeat the same process for the episode collection and for the chapters as well. 

# Enter the data

Now that all the tables/collections are correctly created we can enter our data clicking on the box icon on the left sidebar and clicking on the Podcasts collection.

![Directus view](/images/directus-crud-1/directus-crud-10.png)

Very little effort and our CRUD is in place

# Cliffhanger

We will discuss how to create relations between collections in the next blog post. We will create one-to-many and many-to-many relationships! 

See ya0