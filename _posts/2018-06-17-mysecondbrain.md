---
layout: post 
title: Building a Second Brain
---

![Second Brain]({{ site.url}}/public/mysecondbrain/brain.jpg){:class="book-images"}

# Building a Second Brain
In [Part 1](http://julyandavey.com/2018/05/22/secondbrain/) I explained why I’m trying to build a Second Brain or Zettelkasten and what features it needs to have.

I’ve now spent a couple of weeks experimenting with different solutions and now want to present to you my Second Brain Version 1.0.

I’ll try and make this as non-technical as possible for those of you who aren’t programmers.

## Software
There are literally thousands of different note taking programs that could be a solid base for my Second Brain. I tried out a tonne of them from [Evernote](https://evernote.com/) to [Workflowy](https://workflowy.com/). 

In fact, pretty much any of them would do the job. But some are definitely better long term solutions than others. Here are my criteria to find the best solution:

+ Notes stored in text files with markdown.
+ Fast, simple and easy to use.
+ Open Source

Firstly, the software needs an easy way for me to export the notes. Or even better it should store the data in an easy to use format like markdown text files. Markdown is a universal way of telling the computer when I want things like a header or a list. Why is this important? Well what happens if venture capital funding dries up and Evernote dies? Then I’m stuck with my notes on a system that will take time to migrate away from. Also another benefit of just text files is that I can easily store them on Dropbox or Github.

Secondly, it needs to be super fast and easy to use. Lots of commercially designed software like Evernote suffers from feature creep. i.e. they build way too many features that most people don’t need. And this results in the software being bloated and slow to use.

Thirdly, the software should be open source. What happens if Evernote deletes a feature that is vital to my Zettelkasten. Then I’m stuck. But if it’s open source I can just use the existing code and make my own version where the feature still exists. Also open source is the future!

These criteria might seem anal. But I’m hoping that now it’s setup my Zettelkasten will last for the rest of my life. Will Evernote last the rest of my life? Who knows.. But it seems worth it to be careful now rather than pay the consequences later.

## Sublimeless
So after lots of searching I came across some software called [Sublimeness](https://github.com/renerocksai/sublimeless_zk). 

It’s still in an alpha version but fulfils all of the criteria laid out above. It uses text files + markdown. It’s purpose built to be a Zettelkasten so only has the features I need. And even better it’s totally open source! 

If you’re interested the creator discusses Sublimeness in this forum: [https://forum.zettelkasten.de/discussion/226/renes-sublimeless-zettelkasten](https://forum.zettelkasten.de/discussion/226/renes-sublimeless-zettelkasten)

So here is a first look at my Zettelkasten Version 1.0.
![Zettelkasten]({{ site.url}}/public/mysecondbrain/zettelkasten1.png)

If you want to follow along you can see how to install the software here: [https://github.com/renerocksai/sublimeless\_zk#installation](https://github.com/renerocksai/sublimeless_zk#installation)

And here are some Keyboard Shortcuts (for mac) to get you going:
+ Create a new note ⌘N
+ Search Notes ⌘P
+ Search Commands ⌘⇧P

You can store the folder containing the notes in Dropbox or if you’re technically minded have it automatically ‘version controlled’ with git. ([here](https://github.com/larriant/zettelkastenScripts/blob/master/autoCommit.sh) is my script for this)

## Note Layout
I think the most important part of my Zettelkasten isn’t actually the software I’m using but the layout of the notes. 

Most notes I’ve made in the past end up lasting pages and pages. This means that I never actually go back to them. And never absorb any of the information.

My Zettelkasten has one fundamental rule:
> One Idea -> One Note

Here’s what the layout of my notes looks like:
```
---
title: 201806162019 Altruism
date: 2018-06-16 20:19
tags: #philosophy #humannature
---

{key information}

# More 

{extra information}

# References
```

To achieve this I have a key information section and a place for any extra information. I’m keeping the key information to a paragraph length maximum. This forces me to dilute down an idea to its simplest, most easy to understand form.

In Sublimeness you can set the new note template to mirror this layout by entering the following into preferences.

```
"new_note_template": "---\ntitle: {title}\ndate: {timestamp: %Y-%m-%d %H:%M}\ntags: \n---\n",
```

I’ve also setup a bibliography in a program called [BibDesk](https://bibdesk.sourceforge.io/) which integrates with Sublimeness and allows me to do references super easily. So that when I come to use some of this information in a paper or project I know where it actually came from. Other solutions exist for windows and linux.

## Note Relations
Another important thing I had to decide was how the notes would relate to each other. 

I have two solutions for this.
+ Interlinked Notes
+ Summary Notes

Interlinked notes is simply where I have a link to related notes inside of an existing note. This means I can traverse the ‘tree’ of my notes by clicking through these links. 

Summary notes are where I layout a sort of ‘table of contents’ for a particular area.

For example here is my table of contents for human behaviour from the book [Behave](https://www.amazon.co.uk/Behave-Biology-Humans-Best-Worst/dp/009957506X/ref=sr_1_1?ie=UTF8&qid=1529307843&sr=8-1&keywords=Behave):
![Summary Note]({{ site.url}}/public/mysecondbrain/summarynote.png)

I also make use of tags so that I can easily find notes that are connected together. 

Maybe at some point I will simplify this system for note relations or come up with something better. But for now I think this approach will maximise my ability to easily access information and generate new ideas.

## Printing Scripts + Anki Scripts
So one of the key requirements for my Zettelkasten was for it to be both a physical and a digital system.

To achieve this I have written a [script](https://github.com/larriant/zettelkastenScripts/blob/master/textToCards.py) that exports the title of each note and the ‘key information’ and places them on each side of a printable flash card.

![Flash Cards]({{ site.url}}/public/mysecondbrain/flashcards.png)

This means that my Zettelkasten will exist in both the physical and the digital realms! Whooopeee!

I’ll be able to lay out my cards on the table and spot patterns. Thus creating totally new ideas!

I also intended on writing a similar script to create digital flash cards for the [Anki](https://ankiweb.net/) space repetition software but I realised this is going to take some more time so it’s not part of my Version 1.0.

## Conclusion
So there you have it! My first version second brain. I think I will make adjustments to this setup in the future. But this seems like a great first step to having a managed knowledge system that I can build upon for the rest of my life. Setting this up and making my first few notes has made me think a lot about the way we read effects what we learn. So my next post is going to be an introduction to reading with my Second Brain in mind.
