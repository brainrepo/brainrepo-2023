---
author: Mauro Murru
pubDatetime: 2023-02-19T14:42:52.737Z
title: Code or no-code, diaries of a half developer half entrepreneur using Directus
postSlug: codeless-with-directus
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

![directus ui](/images/directus.png)

# Code or no-code

I have been an entrepreneur for more than one-third of my life, and for half of that, I've also been a software engineer.

Two different identities for the same person can make some target achievements hard to be accomplished.

Creating side projects or digital products is nearly impossible in this case. My "Prof of concept" folder is full of unfinished projects, all stranded before I even started writing the business logic, and this demonstrates that theory.

# Why does this happen?

I spent a long time figuring out the causes and ended up with a simple answer.

When I start a new project, I want to reach two goals from my two personalities.
The first is to create something that resembles the product I imagined (for fulfilling my entrepreneurial soul)
the second is to learn a new language, framework or technology.

These two targets rarely blend harmoniously. And it usually happens that I kill the project for one of this two reasons:

- Learning has ended, or my interest in the tech tools I used has waned.
- I picked a technology, language or framework driven by the learning interest rather than the project needs taking me into a situation where I am trying to hammer a nail with a wrench.

# What we need from a no-code tool

To avoid this problem, I have to find a pragmatic way to create my POC as fast as possible, focusing on the functional part and letting aside all the skills from my dev side as much as possible.

Yes, I know you are starting to smell the no-code and codeless fragrance in the air, and I also know that you will begin to say that using a low-code / no-code approach can force me to create a less tailored solution.

To understand if a low-code approach could be a real option and not just a wishful thought, I had to formalize which were the requirements.

Let's imagine that I want to create a backend for creating the feed for my podcast, and let's assume that I want to shift this need to make it reusable and multitenant to allow other podcasters to host their podcast on this platform, a sort of alternative to Anchor or Spreaker.

# Those requirements are:

- A rest or graphql crud api to make the interaction from other applications possible
- A simple and extensible CRUD UI for entering data
- A system that handles roles and rights also at the record level, like "this user can see just his records or records where his ID is in the receiver field."
- A system for creating custom endpoints that run custom business logic
- A system for creating workflows based on the time (cron), data entry or changes, etc
- A system for creating custom UI
- A file storage system that manages the data according to roles and rights.
- A user management system

Ok, I can hear your thought, "ehi Mauro, you are looking for the moon", but this is the minimal structure of a minimal SaaS product.

Let's do a little exercise. Firstly, let's estimate the work needed to implement these features from scratch or with a framework.

Ok, no matter if you use a fast framework like rails o laravel, just one answer is correct: "too much code, too much time".

# Directus

After searching for a while, trying different open-source, closed-source, on-premise and "as a service" products, I finally found an open-source solution that fits nearly 100% of my needs.

Directus has all the requirements mentioned above and more features with a special plus that it has a complete set of possible extensions.

We can use our developer superpowers.
If we reach the limit of the "out of the box API or UI."
We can extend our instance with custom UIs for fields, list pages, email templates, interfaces and complete custom modules, everything possible just by creating a simple package that uses Vue js.

We can also extend the backend part by writing simple js or typescript code creating knexjs database migrations, custom hooks and endpoints.

With Directus, I felt a new feeling. Finally, being a developer could help my entrepreneurial desires without introducing too much complexity or time needs.

# The limits

Ok, All that glitters is not gold.
Until now, I spotted two limits:
A vuejs development experience is not suitable for me. Compared to react, it is more verbose and less ergonomic.
I wouldn't say I like express js. I cheer for fastify.

Do you feel them silly? 😂. I still am a developer, and cheering is our favourite sport.

Jokes aside, there is one big limit that Directus shows after a while you use it. So if you want to do something more complex than classic crud or if you want to create your extension, you need to rely on complete documentation.
I found myself digging into the source, trying to understand how things work.

What next

The lack of documentation is why I'll start a little series of tutorials in the following days.
I want to contribute to this fantastic project, and writing some blog posts could be an excellent way to do it.

See you soon with the first practical tutorial.

Ps. Here the directus website and docs

- https://directus.io/
- https://docs.directus.io/getting-started/introduction.html
