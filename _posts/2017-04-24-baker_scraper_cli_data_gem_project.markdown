---
layout: post
title:  "Baker Scraper CLI Data Gem Project"
date:   2017-04-24 14:29:25 -0400
---


As a child, I was greatly influenced by my parents. My mother was a stay-at-home mother of four, who loved to cook and bake. My father worked as a computer consultant and programmer for many years. So my mother taught me how to bake and my father taught me how to use computers.

While I love cookbooks, I've found that the web has provided a modern take on them. Websites make searching for a specific recipe easy and you can master just about any technique by watching a video tutorial. So it's no suprise that I frequent a lot of baking websites and bloggers.

For my CLI Data Gem project for the Flat Iron School, I decided to choose a baking website that I love to scrape data from. The site I chose is www.joythebaker.com. Many of the bakers I follow, including this one, use a blog format for their posts and write a story behind the recipe before posting it. I started out with the idea that it would be nice to be able to navigate through the recipe categories before getting to the recipe listings. Then you could select a recipe and go right to it.

At first, this seemed very simple in my mind, but I ran into a number of setbacks. First, the initial way that I wrote the code to scrape the categories worked, but then did not list the recipe data correctly. I had started with just pulling the caetgory titles and then adding them on to the end of www.joythebaker.com/category/ to get the list of the recipe. But I found a couple did not work because, for whatever reason, their URLs were different (some had "-2" at the end), so I had to write out the code a bit differently. I think it is a bit clunky and would like to find a more concise, elegant way to do so, but the current code has the desired effect.

Because of the blog format of the site, it was initially difficult to find the right selectors on the site to specify which data to scrape. I began by following along with a video walkthrough for a similar project, creating a gem called Daily-Deals, which scrapes infor from sites like www.woot.com and www.meh.com to put all daily deals in one place. It seemed simple in the walkthrough as it was easy to find  ID selectors in the CSS code for the site that were uniquely labeled.  With the blog format of www.joythebaker.com, I did not have unique IDs to pull. So I had to get a little creative with the selectors. I lot of trial and error went into getting the right data to show in the way that I wanted it to.  This question posted to Stack Overflow was especially helpful: http://stackoverflow.com/questions/15661125/web-scraping-with-nokogirihtml-and-ruby-how-to-get-output-into-an-array

The other major setback I encountered during this project was personal. I had a trip planned to go to my boyfriend's hometown of Minneapolis to meet his father and spend time with some of his childhood friends.  I figured it would be easy to bring my laptop with my and to work on this project during our lazy downtime. When we arrived at his father's house where we were staying, I discovered that not only did his father not have WiFi in the house, he didn't have an internet connection of any kind! Makes it hard to code a project dependent on web scraping when you can't connect to the web!

<iframe src="//giphy.com/embed/6HZ0P9IkUSfgk" width="480" height="480" frameBorder="0" class="giphy-embed" allowFullScreen></iframe><p><a href="https://giphy.com/gifs/6HZ0P9IkUSfgk"></a></p>

Several trips to a local coffee shop and some tethering off of my boyfriend's cell phone later, I was able to continue to work on the project. Learning to code in addition to working a full-time job and trying to have a social life is definitely a balancing act!

I next utilized the Colorize Ruby gem not just because I found it to be attractive, but it actually helped me figure out if my code was working faster. Each header/action had a different color associated with it, so I wouldn't have to stop and read each line to know it it was working or not; each new color signaled a step in the right direction.

While my first intention was to have each recipe display in the CLI, I found the lack of unique selectors to make it difficult. Instead, I was curious to see if I could launch the recipe URL from the CLI. A little Googling lead me to the Launchy Ruby gem: http://www.copiousfreetime.org/projects/launchy/

By adding this gem, I could have the URL open in a browser upon selection in the CLI.

I would like to continue working on this code to get to the point where it's scraping the recipe data and displaying it in Terminal without having to launch a web browser, but I am still proud of what I was able to get it to do. I'll consider that to be features deployed in the next version!
