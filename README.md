---
title: Behind the Scenes
---

> On the third day of the year 47 BC, the most renowned library of antiquity burned to the ground.  
>  
> Throughout the history of humanity, only one refuge kept books safe from war and conflagration: the walking library, an idea that occurred to the grand vizier of Persia, Abdul Kassem Ismael, at the end of the tenth century.  
>  
> This prudent and tireless traveler kept his library with him. One hundred and seventeen thousand books aboard four hundred camels formed a caravan a mile long. The camels were also the catalogue  
>  
> ~ "January 3rd" from *Children of the Days* by Eduardo Galeano

> Alas! Asaṅga spent twelve years in the wilderness, practising meditation.  
> Without achieving any success in meditation,  
> He has instead compiled these treatises  
> As a burden for an elephant’s back.  
>  
> ~ [Vasubandhu](https://www.lotsawahouse.org/tibetan-masters/khenpo-shenga/life-of-vasubandhu)

# History

This GitHub Page started life as [my personal library of Buddhist stuff on Google Drive](https://drive.google.com/open?id=1RJi6bEXa25zizGdsm5evCycYuY6a2D8r). 

Now, a personal library, especially when shared, has two audiences (and thus two priorities): 

1. First, a library is there to organize one's own media for their safe-keeping, retrieval and study. 
2. Second, a library is there for others (hi!) to peruse and, hopefully, benefit from

These two practical aims find unity in the pride that any book-worm feels towards their library: 

**The library is a reflection of its creator**---who they are and what they'd like to be.

Given that I'm a Buddhist monk, naturally my personal library represents a course of study in Buddhism.

In translating this proud, ancient tradition to the digital age, different constraints and possibilities emerged. Reflecting on the structure of the internet, I opted to express myself in a giant [mind map](https://photos.app.goo.gl/Z8nvMf3Cbup6WA418). 

As a map of my mind, this library contains (editorially and structurally) my own biases. This is a feature not a bug. I named my camels with a great deal of thought, care, and delight and I hope that, as you explore my library, you will feel some of that delight too. 😊 🐪

# Studying

There are two primary ways to study here: taking [the courses](https://buddhist-uni.github.io/courses/) or hanging out at [the library](https://buddhist-uni.github.io/library/).

The library contains all the best content I've found on the internet, [organized primarily by topic](https://buddhist-uni.github.io/tags/).  After reading a work, I contemplate what I learned and who I'd recommend it to. Only then do I file away the piece into topics, based on my answers to those questions.

Once a given topic has accumulated sufficient material, I then take some time to organize it into an undergraduate-style syllabus: identifying the themes and connections across different works and putting them into dialogue with each-other. Of course, as I review the material again to create the classes, I inevitably learn a lot---as anyone who tries to teach finds out.  As I go through, some works may be added to the topic that were originally categorized elsewhere, some works might be moved out of the topic, and some may even be rejected entirely. (These last pieces of `_content` get `status: "rejected"` in their [frontmatter](https://jekyllrb.com/docs/front-matter/))

Once published, these lesson plans may be studied online as-is or reworked for in-person use by a study group or class. There are already students and teachers around the world using the courses in a variety of ways and I couldn't be prouder!

While some Buddhist countries (like Thailand) have official curricula for teaching Buddhism to e.g. new monks, no such comprehensive curriculum yet existed in the English language.  It was towards filling this gap that I decided to dedicate my studies and this website.

# The Source Code

You can think of each of the folders in [the main folder](https://github.com/buddhist-uni/buddhist-uni.github.io/tree/master) as representing individual object types. Each is a different "table" in the hardcoded "database."

- [_authors](https://github.com/buddhist-uni/buddhist-uni.github.io/tree/master/_authors) - Each author with their own page.
- [_content](https://github.com/buddhist-uni/buddhist-uni.github.io/tree/master/_content) - All of the individual works in the library, divided by `category` based on the type. Each content item has a number of [metadata fields](https://jekyllrb.com/docs/front-matter/) listing its bibliographic information (e.g. `pages`) in Bibtex format, or linking the entry out to its file (e.g. `external_url`) or linking it to its internal groups (e.g. `authors`). Conventionally, I put raw strings in `"Quotes"` and I represent links to other objects as `unquoted-slugs`. The templates then use these slugs to fetch the related objects at page render time.
- [_categories](https://github.com/buddhist-uni/buddhist-uni.github.io/tree/master/_categories) - This folder houses the `index.html` pages for the `/content/*` folders and contains a little metadata about the categories, such as their plain English titles.
- [_courses](https://github.com/buddhist-uni/buddhist-uni.github.io/tree/master/_courses) - The University's courses.
- [_data](https://github.com/buddhist-uni/buddhist-uni.github.io/tree/master/_data) - Site configuration [variables](https://jekyllrb.com/docs/datafiles/).
- [_drafts](https://github.com/buddhist-uni/buddhist-uni.github.io/tree/master/_drafts) - Unpublished courses or blog posts.
- [_includes](https://github.com/buddhist-uni/buddhist-uni.github.io/tree/master/_includes) - A Jekyll folder which houses the site's [reusable UI components](https://jekyllrb.com/docs/includes/).
- [_journals](https://github.com/buddhist-uni/buddhist-uni.github.io/tree/master/_journals) - Periodicals which get their own page.
- [_layouts](https://github.com/buddhist-uni/buddhist-uni.github.io/tree/master/_layouts) houses the [html page templates](https://jekyllrb.com/docs/layouts/).
- [_posts](https://github.com/buddhist-uni/buddhist-uni.github.io/tree/master/_posts) are the [blog posts](https://jekyllrb.com/docs/posts/) which make up the newsletter.
- [_publishers](https://github.com/buddhist-uni/buddhist-uni.github.io/tree/master/_publishers) are the publishers which I have granted their own hub.
- [_sass](https://github.com/buddhist-uni/buddhist-uni.github.io/tree/master/_sass) contains [the site's css](https://jekyllrb.com/docs/assets/).
- [_series](https://github.com/buddhist-uni/buddhist-uni.github.io/tree/master/_series) - Are collections of `_content` items that were published as part of a `number`ed `series` (specified by fields on the content item)
- [_tags](https://github.com/buddhist-uni/buddhist-uni.github.io/tree/master/_tags) - The bibliographic topics, arranged in a directed, ontological graph via the `parents` field.
- [_tests](https://github.com/buddhist-uni/buddhist-uni.github.io/tree/master/_tests) - A couple of pages with Integration Tests I have used during development in the past, and decided to keep around in case the code is useful in the future.

To run the site locally, clone the repo, then run "[`bundle`](https://bundler.io/) `install`" and "`bundle run` [`jekyll`](https://jekyllrb.com/) `serve`" keeping in mind that the site will take up to 30 mins to build. Once the site is built, it will start serving at `localhost:4000`

For more information on the build process, see [the Jekyll docs](https://jekyllrb.com/docs/).  For questions about the source code, feel free to message me.

# Contributions

The beauty of Jekyll is that it outputs plain HTML, which can be reworked in a variety of ways.  The code here is released under an MIT Licence, so feel free to reuse it in any (ethical) way you like. If you would like to contribute anything back, please feel free to email me or simply fork the repository and open a pull request!  

# Future Directions

Over the next few years, I would like to expand the University's offerings further and further: into various regional forms of Buddhism, subtler points of Buddhist philosophy, the grand arcs of Buddhist history, and much, much more. I'd also like to continue to improve the site's design and marketing, so it can be as accessible as possible to as many people as possible.

I have also tried to select content with "staying power" to avoid, as much as possible, anything that will become outdated in a few years.  This site is technically a "blog," but it is **not** another newsfeed of digital ephemera. It is an experiment in a slower technology. It is my hope that this curriculum will provide a solid basis for Buddhist Studies for the next 50--100 years.

# Disclaimers

- This repository, like all other things in life, is subject to change.
- While I have taken some pains to ensure that everything here is trustworthy and legal, please know that you use the University at your own risk.
- The views expressed in each work are the opinions of the author(s) and may not reflect my own.

# Acknowledgements

A big thank you to [the content sources](https://buddhist-uni.github.io/sources/), to Google (for hosting [the Drive library](https://drive.google.com/drive/folders/1RJi6bEXa25zizGdsm5evCycYuY6a2D8r)), to GitHub for hosting the site, and to all the various content creators and publishers who generously put their work out there for free. It's a testament to Buddhist generosity that such an expansive and outstanding collection can be compiled (almost entirely) from free material.

# Dedication

To all my teachers---past, present and future. Especially you.
