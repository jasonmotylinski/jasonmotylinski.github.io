---
title: 'Rawk-it: An Introduction'
date: 2024-02-27T12:00:00-05:00
images: 
- images/idea.jpg
draft: false
tags: ['rawkit', 'project']
---

__(This is the first in a series about [Rawk-it.com](https://www.rawk-it.com), my passion project about music trends)__

## For the Love of Music

Music is a passion of mine. I'm one of those people who is [extremely moved by music](https://greatergood.berkeley.edu/article/item/where_music_and_empathy_converge_in_the_brain#:~:text=A%20new%20study%20suggests%20that,music%20differently%20in%20their%20brains.&text=Music%20seems%20to%20be%20a,with%20a%20crowd%20of%20thousands). There's nothing better than experiencing the expression of feeling through music. Whether it be my kids practicing an instrument in our house or an arena show in the city, I can't get enough of it. I have always consumed as much music as possible. 

As a kid I spent weekends in the music stores thumbing thru cassettes and CDs looking for something I hadn't heard before. I was the music director at the [my college radio station](https://www.wrfw887.com/) for a short stint. My job was to intake all the new CDs, catalog them, and provide them out to the DJs.<img align="right" style="padding-left: 10px; width:200px" src="https://upload.wikimedia.org/wikipedia/en/a/a4/Limp_Bizkit_Three_Dollar_Bill_Y%27All.jpg"> I loved that job so much. It was a constant stream of free new music and I was introduced to so many new genres. The artists were fresh, new, and undiscovered. Finding a diamond in the rough was amazing. Don't laugh - we spun Faith by Limp Bizkit 6 months before mainstream radio picked it up. I had already moved onto Ska by the time Fred Durst and Co. broke into the big leagues.

The downfall of Napster and the advent of iTunes led to easier access but at a cost. I appreciate a well-crafted album. There's an art to creating a flow and energy across a dozen songs which creates the album's identity and personality. In the early days of iTunes albums were still being pushed. The single song purchasing model hadn't taken off yet. Most singles still needed to be purchased as a full album. More music was coming online and was easily available with a click of a button. I found myself buying everything I could get my hands on. At one point I had to actually start budgeting for my monthly iTunes spend because it was getting out of control.

Not everything I was buying was good, though. I grew increasingly frustrated that I was spending money on music that had a short shelf life. I wanted find a way to be on the precipice of new music. I wanted to know about an artist __RIGHT BEFORE__ they took off. I wanted a way to replicate that same experience I had as a college radio DJ. I wanted to find those artists floating just under the mainstream. 

I was early in my data engineering career, learning that the internet was filled with free data. New tools and technologies were coming online that made acquiring and processing data easier. I figured if I could find a good source for new music then I could track up and coming songs and artists. This would give me that same "new music high" that I was chasing.

<img align="left" style="padding-right: 10px; width:200px" src="https://upload.wikimedia.org/wikipedia/commons/b/b0/KZIO_logo.svg"> Around the same time [89.3, The Current](https://www.thecurrent.org/) was finding it's place in the Minnesota music scene. It has burst on the scene in the mid-2000s, saving Minnesota from corporate radio and shepherding in the rock revival led by The Strokes.

## Origin Story: Inventing of Rawk-it.com

[The Current](https://www.thecurrent.org/)  was my inspiration. I figured if I could track the music they play then I could develop an algorithm that helped predict popularity.

I developed a data pipeline that cataloged The Current's daily playlist and a simple Ruby application that charted song popularity. It became my "Music Radar", before it existed in Spotify. I set up a simple website, published the results, and named it [Rawk-it.com](https://www.rawk-it.com). The pipeline and chart refreshed daily. At any point I could pop on to the site and see what new music I may be missing out on.


## What's Next for Rawk-it.com

What exists today is a much more mature site and analytics for music. At some point the data I collected grew too large for the basic Ruby pipeline and website. I have since retooled everything. I'll talk about the current architecture in future posts.

I've been tracking music trends now for over a decade at this point. I need to expand the sources of information and bring in more metadata about artists and genres. I love The Current but it has a midwest slant to it. I'm looking to start tracking other stations like [WXPN](https://xpn.org/) and [KUTX](https://xpn.org/).

The availability of music on digital streaming services has homogenized music. People are still able to create a better connection between music and emotion. I'm going to continue to evolve [Rawk-it.com](https://www.rawk-it.com) with new and novel ways to explore music.
