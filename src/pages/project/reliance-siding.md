---
layout: ../../layouts/project.astro
title: Reliance Siding
client: Self
publishDate: 2022-20-01 00:00:00
img: /assets/reliance.png
description: |
  I set this website up last year for a branch off of the painting company I used to own.  We launched and tested it, and ultimately ended up advertising the siding portion of the business through the painting company becuase it converted better on adwords.  But I've kept the site up because we may use it in the future and I didn't want to have to start from scratch again.
site: https://reliancesiding.com
stack:
  11ty, TailwindCSS, and just a hint of Javascript.
purpose:
    Stand up a site that would be performant for SEO and easy for us to maintain for a new branch of Great Plains Painting.
backend:
    This would eventually be hooked up to an Airtable DB to collect form submissions and then automate further from there.
tags:
  - 11ty SSG
  - TailwindCSS
  - Vanilla Javascript
---


I built this site last year and it's the second time I'd used the 11ty/TailwindCSS combo.  I liked how it came out and the images and slanted colored background effect though challenging to figure out came out looking good to me.  Though this site is live we don't do anything with it as we decided to run the siding business through the painting company and piggy-back off its SEO and general brand.

### What I'd do differently

On this site it felt like I ended up writing a bunch of custom CSS inside of Tailwind.  I like Tailwind a lot, and their docs are great.  But after building this site I decided to begin learning CSS thoroughly.  My theory was it would be ideal to use a handful of utility classes (for spacing / sizing) but write the rest of the CSS from scratch through Sass.  I looked at Andy Bell's [Gorko](https://github.com/hankchizljaw/gorko) which does exactly what I'd imagine doing.  I haven't tried it on a project yet but it looks legit.  I'm also going through Stephanie Eckles [Level Up With Modern CSS](https://smashingconf.com/online-workshops/workshops/stephanie-eckles-oct/#/) workshop to see how she thinks about setting up and running a similar combination of small utility and modern custom CSS.

Much to my delight as I read the astro docs the section on [Advanced Styling Architecture](https://docs.astro.build/en/guides/styling/#advanced-styling-architecture) recommends just such an approach for styling.  What I struggled with in 11ty is that you are left to process your own Sass/JS/whatever.  Andy Bell runs his utility generator Gorko through Gulp, which is fine but I didn't really want to spend a few hours learning Gulp.  I love that Astro handles most of this for me!
