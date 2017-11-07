---
layout: post
title:      "CLI Data Gem - The Night Sky"
date:       2017-10-20 19:24:22 -0400
permalink:  cli_data_gem_-_the_night_sky
---


The Night Sky started off as a simple idea to turn a fairly tabular list of events into filterable and searchable Gem, but it eventually morphed into an experiment in CLI design and function.

The Gem mechanics themselves are pretty simple - scrape a page based on a year from user input with a class Scraper, create each event in a class Event, and orgainze them into digestable packages for the CLI.  Surprisingly, the Scraper and Event classes were the easiest functionality to build and I almost instantly had all the data available to built my CLI.

Upon initial design, I made a class function called #select_by that would run #collect on the entire collection for Events and filter them out by a keyword.  This function is still the backbone of how I break out the navigational screens, but it also led me to play around with it as a method that could receive user input.  My #search_by method experiment proved to be far more robust and useful than the rest of CLI, I quickly decided that it needed to be a feature.  This is when things got interesting.

How do I marry the rigid and streamlined structure of a good CLI, with the nebulous and free-form nature of a search function?  Where would it live? How would I get out of it?  What about the rest of the program? There's probably not a correct answer or even a "best" answer, but I came up with my answer.

Secret Functionality.

Most programs have shortcuts and hotkeys, so why not build something similar into the CLI?  Whenever you're the user receives an input prompt, they always have access to a few keywords to quickly navigate to key parts of the program. They are mentioned in the main nav, but the users are not prompted at every step that these commands are available.  Access the search through 'search', acces the the main menu through 'main', change the year within the program through 'change', and quit the program through 'quit'.  With these "escape ropes" in place, I could then refocus on making the CLI straight forward and streamlined without having to worry about every step requiring some option of retreat.  For savvy users the program is quick and nimble, and for the first time users and the casuals, it's easy to understand and still robust.  And isn't that is the goal for all UX?
