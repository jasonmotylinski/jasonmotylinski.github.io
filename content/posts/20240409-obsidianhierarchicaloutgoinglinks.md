---
title: 'Obsidian Love Story: Hierarchical Outgoing Links Plugin'
date: 2024-04-09T12:00:00-05:00
draft: false
images: 
- https://upload.wikimedia.org/wikipedia/commons/1/1a/Zettelkasten_paper_schematic.png
tags: ['gtd', 'obsidian', 'project']
---

I've made no secret of [my love](https://jason.motylinski.com/posts/20240130-zettelkasten/) for [Obsidian](https://obsidian.md/), the free-form, loosely-organized, markdown-based notetaking tool. I use it for everything. I use it to organize work, I use it for drafting blog posts, and I use it when I need to get something out of my head. 

One of the super-powers of Obsidian and the [Zettlekasten](https://en.wikipedia.org/wiki/Zettelkasten) notetaking philosophy is the concept of writing stuff down now and organizing it later. Obsidian provides many different views to explore and navigate between notes. I'm going to focus on the core functionality of __Outgoing Links__.

## Outgoing Links
Outgoing links display references "outgoing" from the current note to other notes. In the example below the outgoing links are displayed on the right-hand side. The links are helpful to identify other topics associated with the active note. In this example you see people, projects, and teams referenced. The core plugin displays all the links and the file path underneath the link name. It also co-mingles resolved links (those links with files associcated) with unresolved links(links with no file associated). 

This view is helpful to see what the active note references but it's hard to tell who are all the people associted with the note or which projects are referenced.

![image](/projects/obsidian/core.png)

## Frontmatter, Tags, and File Structure - So Many Ways to Organize!
Obsidian relies less on file folder structure for organization and more on less structured methods like frontmatter data and tags. 

Frontmatter is metadata added to the top of a file which can help describe any ancillary information about a note like dates or note type. I've used frontmatter in the past in combination with the [Projects](https://github.com/marcusolsson/obsidian-projects) plugin to organize all my team's in-flight initiatives.

Example:
```
---
full_name: 2023 APIs
owners: Dave
priority: 90
status: completed
tags:
- project/2023 
---
```

Tags are the loosest method of organization. A tag is simply `#tagname` on a line in a file. You can add a bit of structure to tags by following a `#level1/level2/tag` naming scheme if you like.

Both of these methods didn't scale for me. I keep A LOT of notes. To maintain some level of sanity with the amount of files I create I organize them into file-based structure to keep the most basic things separate. I organize my notes into `people`, `projects`, `teams`, and `processes` folders. Trying to accomplish the same structure using Frontmatter would mean using another plugin like [Dataview](https://blacksmithgu.github.io/obsidian-dataview/) to query my notes. Using tags wouldn't allow me to click-through directly to the referenced note.

## A Better Outgoing Links View
What I really wanted was to view my outgoing links for the active note which mimicked the file-based organization I set up. I wanted to see all the links I had made to `people` for a given note. I wanted to see all the `projects` we had discussed during a meeting. Since each of these notes have their own detail I wanted the ability to click and navigate to those references. I couldn't find any existing Obsidian plugin to solve my problem so I decided to build something myself.

Introducing: [Hierarchical Outgoing Links](https://github.com/jasonmotylinski/hierarchical-outgoing-links)

Let's start with the example:
![image](/projects/obsidian/plugin.png)

The outgoing links on the right now mimick the structure in which the referenced note is stored. This allows me to see at a glance who is involved in the current note, what project is associated, etc... 

As a bonus, the new plugin displays __Unresolved Links__. An unresolved link is a link that exists in the active note but _does not have_ a file yet created. Why is this important? I create a link for every possible noun during a meeting, conversation, random thought. 

For example, I'll create the task: 
`-[ ] Call [[jim]] about the [[snowflake]] bill` 

 `[[jim]]` or `[[snowflake]]` may not yet exist. If they don't exist, I'll want to create them at some point. My new plugin prominantly lists those links that are dangling and help me identify gaps that I will fill in later.

## Next Steps
I developed the plugin to the level that I've started using it daily. It's not complex but I want to make sure there are no glaring bugs in it before releasing it to the general public. I'm working on getting it polished up so that it can be submitted for official inclusion into the the Obsidian plugin ecosystem. 

## 04/13/2024 UPDATE
My plugin has been officially released and is available in the Obsidian Community Plugins directory! Search for "Hierarchical Outgoing Links" to install it and let me know what you think!