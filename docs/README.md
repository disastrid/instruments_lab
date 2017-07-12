# The Instruments Lab website

This is the how-to for the Augmented Instruments Lab site. This document details how to work with each section.

## People

In the folder `_data` there are three files where bios can be added: `members.yml`, and `alumni.yml` (`collaborators.yml` is in there as well but that's for organisations). 

Here's the data you need to add to list yourself:

```
- avatar: ../images/people/mypic.jpg
  name: Dr Whoever
  position: Some position
  education: PhD in something, Some university, 2056.
  socials:
    - link: http://twitter.com
      icon: twitter
    - link: http://facebook.com
      icon: facebook
    - link: http://github.com
      icon: github
    - link: http://mysite.com
      icon: link
  desc:
    Your description paragraph goes here, and will be titled "Interests".
```

You can have as many or as few social links as you want, and these can include twitter, facebook, github, youtube, dribbble, and tumblr - just add the link and list the type of icon it needs. If there's one you want that doesn't appear here, let me know and I'll add it.

To add a link in your description, just use HTML tags - the text is inserted into the DOM and therefore it will render your tags. For example: "This guy spends his time listening to <a href="https://www.youtube.com/watch?v=fWNaR-rxAic">classical music</a>."

### Your photo

All member photos should be *250x250px*. Please upload to `images/people`. 

## How to add to the Publications page

All data files that feed into the Publications are stored in _data/publications and are ordered by date: _2017.yml, _2016.yml, and so on (the underscore is because data file names that start with a number are invalid). 

An entry in these files starts with a dash. All subsequent fields are indented by *two spaces* in order to be included in that entry. If your indenting etc isn't right, the system will break,

Here's an example:

```
- title: My Amazing article
  authors: J. J. J. Schmidt, G. Costanza
  year: 2024
  venue: Journal of Intelligent Articles
  city: New York
  vol: 5
  issue: 2
  pdf: www.link.com
  link: www.otherlink.com
```

The following fields are *required*: title, authors, venue, year.

Everything else is optional, so leave it out if it doesn't apply and the system will handle the data as it appears. 

The PDF link is meant to be a direct download. "link" appears as the text Project page, so we can link the papers to specific pages in the Research section. 

## News and events

News and events are markdown posts, located in the `_posts` file. 

The news frontmatter looks like this:

```
---
layout: post
title:  "NIME 2017"
categories: [news, events]
images: /images/news/nime2017.png
front-image: /images/news/nime2017.png
event_date: May 11-16, 2017
excerpt: The Augmented Instruments Lab will be at NIME 2017, in Copenhagen.
url: www.nime2017.org
---
```

This example post would be cartegorised under news, which means it will appear in the news feed, as well as events. See below for info on both.

### News 

News posts will appear on the front page of the site, as well as on the news page, in descending order. 

Each news post requires an image. This is non-negotiable - posting news without a picture is pointless on a website, and so the layout has not been designed to ingest photoless posts. Find a picture and add it to the directory `images/news/`, so we keep all our images tidy.

The `excerpt` field is what appears on the front page and the news page, before the reader clicks on the post to read the whole thing.

### Events

News posts can also be put in the events feed. This feed appears as a sidebar on the News page, and gets the three most recent events and posts them there.

Because they are ordered by date, the `event_date` field is important here. Otherwise, the event won't be included into the feed.

## Research + Projects

Every entry in this section has three parts:

1. The front page information that appears in a grid where people click on pictures to go to the page

2. The page all about the project

3. Metadata that appears alongside the project.

It seems like a lot, but all of this is generated from the front matter (stuff at the top) of your project markdown files. You've probably written markdown, as this is what the Bela Blog runs on.

All research project files are kept in the directory `_research`.

### The front matter

Here's the fields at the top of a page:

```
layout: research
title:  "Design for Virtuosity"
tagline: An ongoing body of research
main-image: 06.jpg
tag: research-projects, studies
thumb: thumb.jpg
authors: ["Andrew McPherson", Fabio Morreale", "Jack Armitage"]
production-date: 2017-2019
links: ["http://google.com", "http://facebook.com"]
link-names: ["Google", "Facebook"]
para: "Design for virtuosity: How we design for people who are really really good at violin."
```

### layout

This tells Jekyll which page layout to use. For research posts we're using a custom layout which is in `_layouts/research.html`.

If you need changes, please create an issue.

### title

This is the text that will appear at the top of the page, on top of the main image. 

### tagline

The tagline will appear beneath the title on top of the main image. It will also appear on top of the image in the research menu.

### main-image

This is the image that will appear at the top of the page. 

Two things to keep in mind: 
- 1200x800 is a good rule of thumb for size, but make sure the resolution is good (on big displays it will be blown up really big, so the bigger the better).
- The overlaying text is white, so make sure you choose an image that will support a light text overlay.
- Put your image in `images/research`, and specify the file name and extension.

### tag

Categorise your post with an available tag. If you want to see/edit avaialble tags, they're served from `_data/research-catgeories.yml`. Currently only one tag per post is supported. 

### thumb

This is the image that will appear in the project menu. It should be 400x400px, and is served from `images/research`.

### authors

This can be one name (`"John Smith"`), or an array of names (`["Ace Freely", "Peter Chris"]`).

### production-date

The field "date" is protected, so we're using this field name instead. This can be a date, a range, whatever you like.

### links and link-names

These are two separate yet related fields.

`links` is an array of URLs that you want to link to - blog posts, press, etc.

`link-names` is the text of the anchor tag that you will click on to go to the URL at the same index.

### para

This is the lead paragraph for the post, that will be in bigger font and introduce the project. It's in the front matter so we can mess with it later if need be.

## Posting your research

Copy the front matter above, and fill in your own stuff. Then, write your post in markdown, and save in `_research/mypost.md`

This markdown has the same functionality as the Bela Blog - you can include an image wrapper with a caption:

`{% include single-image-research.html fileName="my-image.jpg" caption="Here is a caption." %}`

Bear in mind that this references the path `images/research`. To keep things neat, please make a directory for your post there, and reference that path like so: `my-project/my-image.jpg`

You can also include youtube videos, using the `youtube.html` include:

`{% include youtube.html youtube="youtube-ref-here" %}`

## Project categories

### About category filters, and adding new ones

Above the project grid on the site are links for categories, that, when clicked, highlight projects belonging to that category. Neat!

These categories are included from a data file which can be found here:

`_data/research-categories.yml`

The reason they're not hard-coded into the layout is because bringing them in from an external file makes them really easy to edit later (and we don't want lots of people having to edit the layout - this is how things get broken).

If you want to add a new category, add it to the array in the data file. Note that you should add it as a string, as you want it to be displayed: "Augmented Instruments", for example, and not augmented-instruments.

### Tagging your project to include it in a project category

In your project post frontmatter there is the following line:

`tag: "categories-go-here"`

This is where you assign your post to an existing category filter. 

Add the categories separated by spaces in quotes. This is because this whole line is imported and assigned to a CSS class attribute, and the classes have to be valid. For example, `class="augmented-instruments, studies"` isn't a valid listing of multiple classes, while `class="augmented-instruments studies" is.

Note that the tags you add have to be slugified versions of the categories in the data file - ie, all lower case, with hyphens instead of spaces.

(This is the shortest route to functionality atm but we can work out a more straightforward way to do this later with some text handling - no time right now though!)

## Ordering the projects for display

Formerly the projects were ordered alphabetically, but that's no longer the case. In order for your work to be listed, you will have to log its title in `_data/research.yml`.

This is a data file that dictates the order of display. You can change it at any time to re-order the research projects, by simply changing the order of the titles in this file. (This means there's no parameter to change in each post.)

The only thing this file needs is the title of your research, exactly as it appears in the post. Therefore, if your post's frontmatter looks like this:

```
layout: research
title:  "Design for Virtuosity"
tagline: An ongoing body of research
main-image: 06.jpg
tag: "research-projects studies"
thumb: thumb.jpg
authors: ["Andrew McPherson", Fabio Morreale", "Jack Armitage"]
production-date: 2017-2019
links: ["http://google.com", "http://facebook.com"]
link-names: ["Google", "Facebook"]
para: "Design for virtuosity: How we design for people who are really really good at violin."
```

... then you should enter it in the `_data/research.yml` file like this:

`- project-name: "Design for Virtuosity"`


