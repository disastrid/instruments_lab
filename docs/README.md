# The Instruments Lab website

Welcome to the AIL website! Finally.

Here's how to work each section.

## People

This data is managed through _data > people. in this folder there are three files where bios can be added: members.yml, and alumni.yml (collaborators.yml is in there as well but that's for organisations). Here's the data you need to add to list yourself:

```
- avatar: ../images/people/mypic.jpg
  name: Dr Whoever
  position: Some position
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
    Your description paragraph goes here. 
```

You can have as many or as few social links as you want, and these can include twitter, facebook, github, youtube, dribbble, and tumblr. If there's one you want that doesn't appear here, let me know and I'll add it.

### Your photo

All member photos are 250x250px. Please upload to images/people. 

## How to add to the Publications page

All data files that feed into the Publications are stored in _data/publications and are ordered by date: _2017.yml, _2016.yml, and so on (the underscore is because data file names that start with a number are invalid). 

An entry in these files starts with a dash. All subsequent fields are indented by *two spaces* in order to be included in that entry. If your indenting etc isn't right, the system will break,

Here's an example:

- title: My Amazing article
  authors: J. J. J. Schmidt, G. Costanza
  year: 2024
  venue: Journal of Intelligent Articles
  city: New York
  vol: 5
  issue: 2
  pdf: www.link.com
  link: www.otherlink.com

The following fields are *required*: title, authors, venue, year.

Everything else is optional, so leave it out if it doesn't apply and the system will handle the data as it appears. 

The PDF link is meant to be a direct download. "link" appears as the text Project page, so we can link the papers to specific pages in the Research section. 

## News items

## Research + Projects

Every entry in this section has three parts:

1. The front page information that appears in a grid where people click on pictures to go to the page

2. The page all about the project

3. Metadata that appears alongside the project.

It seems like a lot, but all of this is generated from the front matter (stuff at the top) of your project markdown files. You've probably written markdown, as this is what the Bela Blog runs on.

All research project files are kept in _research.

### The front matter

Here's the fields at the top of a page:

layout: research\
title:  "Design for Virtuosity"\
tagline: An ongoing body of research\
main-image: 06.jpg\
tag: research-projects, studies\
thumb: thumb.jpg\
authors: ["Andrew McPherson", Fabio Morreale", "Jack Armitage"]\
production-date: 2017-2019\
links: ["http://google.com", "http://facebook.com"]\
link-names: ["Google", "Facebook"]\
para: "Design for virtuosity: How we design for people who are really really good at violin."\

### layout

This tells Jekyll which page layout to use. For research posts we're using a custom layout which is in _layouts > research.html.

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
- Put your image in images > research, and specify the file name and extension.

### tag

Categorise your post with an available tag. If you want to see/edit avaialble tags, they're served from _data > research-catgeories.yml. Currently only one tag per post is supported. 

### thumb

This is the image that will appear in the project menu. It should be 400x400px, and is served from images > research.

### authors

This can be one name ("John Smith"), or an array of names (["Ace Freely", "Peter Chris"]).

### production-date

The field "date" is protected, so we're using this field name instead. This can be a date, a range, whatever you like.

### links and link-names

These are two separate yet related fields.

'links' is an array of URLs that you want to link to - blog posts, press, etc.

'link-names' is the text of the anchor tag that you will click on to go to the URL at the same index.

### para

This is the lead paragraph for the post, that will be in bigger font and introduce the project. It's in the front matter so we can mess with it later if need be.

## Posting your research

Copy the front matter above, and fill in your own stuff. Then, write your post in markdown, and save in _research > mypost.md

This markdown has the same functionality as the Bela Blog - you can include an image wrapper with a caption:

{% include single-image-research.html fileName="my-image.jpg" caption="Here is a caption." %}

Bear in mind that this references the path images > research. To keep things neat, please make a directory for your post there, and reference that path like so: "my-project/my-image.jpg".

You can also include youtube videos, using the youtube.html include:

{% include youtube.html youtube="youtube-ref-here" %}
