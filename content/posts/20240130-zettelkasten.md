---
title: 'Organizing Chaos - Zettelkasten Keeps Me Sane'
date: 2024-01-30T12:00:00-05:00
images: 
- https://upload.wikimedia.org/wikipedia/commons/1/1a/Zettelkasten_paper_schematic.png
draft: true
tags: ['gtd', 'waysofworking']
---

## My Love of Notes

I take notes...lots and lots of notes. As my responsibilities have grown throughout my career so has my need to keep track of more things. I have a shelf of moleskin notebooks filled with notes. I find documenting helps me retain information so the act of note taking has benefits. But the notes themselves? I've hardly referenced. They are disorganized, unstructured, and lack context. Now they serve mostly as a catalog for my doodles.

I've tried many methods over time to structure my notes to make them more effective. For a long time I insisted on physical [writing to help retain the information](https://stackoverflow.blog/2022/11/23/why-writing-by-hand-is-still-the-best-way-to-retain-information/). But there's only so much my mind can retain. I've used the [Getting Things Done](https://gettingthingsdone.com/what-is-gtd/) and [Bullet Journal](https://bulletjournal.com/) approaches. Ultimately, I struggled to balance the tactical day-to-day TODO lists with contextual-capturing, reference notes. I really needed a "knowledge graph", that allowed me to branch off into topics, notes, and TODOs and quickly reference one from another.

## Enter Zettelkasten

[Zettelkasten](https://en.wikipedia.org/wiki/Zettelkasten) was developed as a method for organizing ideas and information based on index cards, long before the internet existed. Simply, it's providing an idea/thought/note on an index card and assigning it a alpha-numeric identifier. Notes are associated to each other by their similar numbering scheme or by adding a referenced note's identifier to the current card.

Wikipedia has a image that describes how it works:
<img src="https://upload.wikimedia.org/wikipedia/commons/1/1a/Zettelkasten_paper_schematic.png" />

In the diagram each card is an idea. In the upper left-hand corner of each card is it's unique identifier (1,2,3, etc...). The lower right-hand corner references other note cards. Tags identify the themes.

Seems a bit tedious because we live in the modern world of hyperlinks and wiki pages. So let's fast-forward to today.

## Markdown and Tooling

In modern times we can accomplish the same kind of organization and structure using hyperlinks. The [markdown](https://daringfireball.net/projects/markdown/) format makes life even easier by providing shortcuts to link to other documents.

I prefer local solutions over 3rd party hosted solutions simply for portability. Being an engineer as well I wanted as little context-switching as possible. I started with a VSCode plugin called [Foam](https://marketplace.visualstudio.com/items?itemName=foam.foam-vscode). Foam allowed me to stay within VSCode and use markdown. For a few years it worked well. I began running into performance issues as my vault grew. Using foam within VSCode along with all my other developer extensions became slow. 

I decided to move to [Obsidian](https://obsidian.md/) as my Zettelkasten tool. Obsidian is a simple markdown and file organizer and grows complexity and functionality via it's extension framework (More on that in a different blog post). Obsidian provides easy navigation between notes using tags and links. It also allows traversing the knowledge graph visually, which is handy when dealing with a large topic that organically grows. 

## Structuring My Zettelkasten

I love Zettelkasten because it allows me to organize how I see fit. My structure works for me. I don't need to prescribe to philosophy or ideology.

I have switched approaches at least twice, taking a few years to be happy and productive in my structure. I thought I'd share it with you in hopes of sparking ideas for you.

The root of my vault contains:

```
|- personal                -- Notes for my personal life,
|                             reading backlog, home improvement 
|                             ideas, etc...
|- professionalgrowth      -- Collection of feedback and growth
|                             areas across my jobs
|- <company>               -- Stores all my notes for the
|                             given company. I have a dedicated 
|                             folder per company             
README.md                  -- A dashboard of quicklinks that 
                              describes the structure of my 
                              vault.
                           
```

My root structure isn't crazy. Let me show you my `<company>` folder structure:

```

<comapny>               
 |
 |- clients                -- Notes and meeting minutes for each of 
 |                            our customers
 |- competitors            -- Notes on our competitors
 |
 |- hiring                 -- Overview of our hiring process, job role 
 |                            definitions, and interview segment definition
 |- people                 -- 1+1 notes for each person I meet with 
 | 
 |- projects               -- Project overviews, status, and meeting meeting
 |
 |- teams                  -- Overview of the various teams and groups within 
 |                            the company and how they relate to each other
 |- tools                  -- Tools and vendor contact
 |
 |- weekly                 -- Weekly TODO lists
 <company>.md              -- Company overview, mission, vision, strategy, 
                              structure, process quick links

```

I'm not attempting to reproduce existing documentation so I link off to company resources as much as possible. But many times I find that I need to convert a thought, proposal, approach into my own words to fully understand the concept.

I find these high level groupings helpful. It allows me to link `people` to `teams` and `projects`, or reference a specific TODO to a `client` conversation.

When I started I was a bit too granular with my structure which created a lot of confusion. I was mixing projects with teams and product lines. I created the mental model that everything is a `project`, that includes `people`. `teams` are a loose grouping of `people`. A team may be a group of engineers working on project, or it might be our C-suite. 

## What I've Learned

I've had to accept there is no single best way to organize all my thoughts. What I need is something flexible enough for me to change. Zettelkasten has given me a way to loosely organize the information in my head, and to change when it makes sense.