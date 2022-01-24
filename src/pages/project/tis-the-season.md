---
layout: ../../layouts/project.astro
title: Tis the Season Holiday Lighting
client: Self
publishDate: 2022-21-01 00:00:00
img: /assets/tts-shot.png
site: https://tistheseasonkc.com/
description: |
  A holiday lighting company my business partner and I started in 2016.
stack: Static, raw coded HTML, Sass, and a hint of JS (for the mobile menu and the form). There is not build tool, I did
  everything with NPM Scripts. I added Tailwind last year to quickly scaffold out on the fly pages.  Cloudinary hosts and serves the images.
purpose: Get ranked for local search. Take in leads and feed them directly to our Airtable DB. Uses a Netlify form for
  contact page. We process about 600 requests a season.
backend: Airtable DB so I can interact with it through code and team can interact through Airtable App. I’ve built many
  automations (invoice creation, text notifications, etc...) either directly with webhooks and JS in Airtable or with
  PipeDream and NodeJS.
tags:
  - design
  - front end website
  - back end tools and automation
---

## Front End

This is the first web project I made. When we starting this company, I built a Vista Print website with their website builder. It was TERRIBLE. But it got us going. 3 years ago when I made this site, I'd learned a little React, people were talking about Svelte, but I knew those were overkill for building this and that I didn't understand the basic things, like HTML & CSS. I decided I'd try to make this site as simply as I could. Hand coded HTML and Sass. No gulp/grunt, I used NPM scripts as the build tool.

Admittedly, changing something in the header or footer is a pain because it's a "find all & replace" operation in VS code, but this site gets the job done. I believe mostly due to the low competition in our area, almost immediately after I made the site live we ranked at the top of organic local search. During the holiday lighting season this site pulls organic traffic so well that we don't have to do any paid advertising. In fact I've had to come up with some methods of filtering the leads we don't want out automatically so we don't get overwhelmed.

## Back End

The setup is similar to what I've explained on the [Great Plains Painting](/projects/great-plains-painting) page. All our customers and their data live in Airtable. This company benefits more than the painting company from being able to manage a large number of customers from one set of data. With painting, the customer hires us and then they're most likely good for a long time. Hoilday lighting, we have a 95% return rate year-over-year.

I have all kinds of automations wired up, and use a couple of tools to run them. When I can, I write the Javascript and run the automations right in Airtable (which is pretty slick). When I need more control, I'll trigger a request to a webhook at Pipedream from Airtable and kickoff a workflow there. Occasionally for very simple things, I'll use Zapier.

The approach I've taken the last two years is to pick the most reptitive tasks that we do (invoicing for example) and see how I can automate them. When I've automated one task, move down a level to the next annoyingly repetitive thing and automate that. This has worked amazingly. In the last couple of years we've doubled the size of the business, and it acutally feels like we do **LESS** admin work.

## What I'd Like To Do Next

The website needs an update, and I'm all about using Astro. Everything is static, but I have an idea for a dymanic feature I think would be cool. Currently, to find out who wants to work with us in a given year, we email/text out a unique link to each customer. The link directs them to a form and they can select yes or no. I run this through an Airtable extension called [MiniExtensions](https://miniextensions.com). This works great, but I think it'd be fun to build it myself. The requirements:

1. generate and use unique links so customers don't have to create a login
2. based on link, webpage that customer lands on only shows their unique data
3. on the landing page they can review their data and check yes/no if they'd like to hire us in a given year
4. once they submit the data, Airtalbe gets updated for their record

This seems like a great use case for client side dynamic data and I think would be something fun to work on. It was going to be tough in 11ty, though easier now with 11ty serverless. In Astro it seems like it would be very straightforward!
