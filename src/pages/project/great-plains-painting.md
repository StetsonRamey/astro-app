---
layout: ../../layouts/project.astro
title: Great Plains Painting
client: Self
publishDate: 2022-20-01 00:00:00
img: /assets/gpp-shot.png
description: |
  The first business I started (in 2015), sold in 2019.  I still run the tech and help occasionally with business functions.
site: https://greatplainspaintingkc.com/
stack: This is a Wordpress site (I did not build it).  Its OK, but I planned to rebuild it in Astro.  I've done extensive work swapping over our backend scheduling, customer tracking so that it lives in one tool (Airtable) instead of many tools.
purpose: Take in leads and put them into our Airtable backend.  Then our office manager can call and schedule in person estimates and the backend automation takes care of scheduling confirmation & reminders.  The automations also create the customer in the others tools we use automatically, and if we sell the project automations move it over to production so the production team can schedule and manage things.
backend: An Airtable DB is the central hub.  Based on project status in Airtable various automations are run, either directly through webhooks from Airtable, or through Pipedream/NodeJS if I need to do fancier things.
tags:
  - back end tools and automation
---

I didn't build this site, an agency did. It's a Wordpress site built with the Elementor builder. I don't hate it, but I don't love it. We paid the agency $10k for it and I'd made my goals for SEO very clear. They didn't deliver on my expectations and I decided last year to part ways with them and rebuild the site myself this year (2022). I planned to run it in 11ty, but then Astro happened and I plan to rebuild the site with a fresh design with Astro!

Even though I didn't build the site, I do build some "back-end" tools for Great Plains Painting via [Airtable](https://www.airtable.com/) and [PipeDream](https://pipedream.com/).

We used to use lots of different tools that didn't talk to each other and various data lived in separate places. This sucked for every and in 2020 I decided to see what I could do about it. The idea was to put all data in a central tool - Airtalbe - and to kill all the tools we could and the ones we couldn't feed the data from Airtable.

### An Example:

Before a new lead workflow looked like this:

Contact form submission --><br>
email sent to Angela --><br>
Angela manually enters info in Google Sheet --><br>
Angela calls / schedules appt in [YCBM](https://youcanbook.me/) --><br>
YCBM automatically updates estimator calender --><br>
Estimator creates project in [CompanyCam](https://companycam.com) --><br>
...and there's a couple more steps but this is sufficient for this example

This of course worked for years, but if we wanted to update an appointment we had to do it in YCBM and our estimators had to create the project everytime in CompanyCam.

So I built this: https://pipedream.com/@stetsonramey/custom-schedule-workflow-p_xMCa7Wk

Now all data lives in Airtable. When a contact form submission happens, it goes straight to Airtable and Angela gets a notification. She calls the potential customer and schedules the time, directly in Airtable. The pipedream workflow adds the appointments to Google Calendar for everyone. If the appointment needs updated, we can do it in Google Cal or in Airtable. Other workflows get triggered to send a reminder 24hours before the appointment. Another workflow creates the project in CompanyCam so the estimator no longer has to manually.

Through interacting with the various APIs available (airtable/google cal/companycam) I eliminated a couple manual steps and made it so that Angela only interacts with one interface - Airtable's.

The team loves it, and I get a little more control over what happens where and how.

### What I learned

I'd never interacted with APIs much before this -- except the standard tutorial stuff like the Pokemon DB, Movies, Weather...

I got up to speed on NodeJS pretty quick. And learned how to scour docs and make sense of what needed to happen to get the data I wanted. Once I figured that out I'd simplify the code and test the requests on Postman or via the apps playground if they have one. When I was satisfied that I was getting or sending the data I wanted, I'd scaffold it out in Pipedream and debug it.

The most difficult thing for me to learn was Async/Await. At first I impatiently tried to just jam "awaits" in the code to see if I could get it running, but when that quickly didn't work I read up a bit. Pipedream has a [pretty detailed doc section](https://pipedream.com/docs/workflows/steps/code/async/) on it and that was helpful. Once I understood where I needed Node to wait on the data I needed before moving on things got easier. Sometimes I still get tripped up, but when I look at async code this year I'm amazed how differently I feel about it than I did at this time last year.

### What I want to do next

Rebuild the website with Astro...obviously. Another item is that we use Quickbooks Payments to process electronic payments from customers. Quickbooks is a fine accounting platform, but their payments setup is less than desirable for me. This year, I'd like to switch payments over to Stripe and interact with their API. I believe it's possible for me to build a little app right inside Airtable to create/send custom invoices inside Airtable without having to login to Stripe. That's the idea anyway.
