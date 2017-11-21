---
layout: post
title:      "Pokemon Safari Zone"
date:       2017-11-21 13:31:31 +0000
permalink:  pokemon_safari_zone
---


For my Sinatra project, I wanted to create something a little more fun than my CLI project (which was a fairly simple and straight forward informational app).  For the Sinatra project, I wanted to something that could demonstrate my knowledge and would let me solve interesting problems, but with no real-life application.

The labs for the section all seemed geared towards blog/journal apps, and applicable ideas for this project are just repurposed versions of the earlier projects.  When coming up with an idea for my project, I had a few things requirements in mind:

1. I didn't it to just be a bunch of forms - I wanted the item I was collecting to exist on its own so users wouldn't have to just sit down and type a bunch of text.
2. I wanted it to be based on some fictional property I liked.
3. I wanted to use Bootsrap

I remembered wanting to do a CLI Pokemon project off the pokeapi, but I had already finished my CLI project by the time I'd found out we could use an API.  After a little thought, I thought it'd be cool to make an app where you can collect pokemon, and have the CRUD functions be dressed up a little to match the mythology of the world.  They are as follows:

* Catch - this creates a new pokemon in your collection.  The mechanics behind the Pokedex that stores the base pokemon is a blog post on it's own, so maybe I'll get into that at a future date.  The quick and dirty of it is: Using the poke api and the official pokemon site, you can create any of the 801 current pokemon without having to know names or stats.
* Train - this is the edit. Instead of text fields, I used range sliders to give it a more playful feel, as well as exert a little control over the stats. I could write some validation to make sure the stats don't exceed the formula values, but for now it's easily hacked through the DOM.
* Relase - this the delete of CRUD.

![](https://i.imgur.com/29oGuGb.png)

I got the Pokedex working on the first night after doing my initial set up, and was catching pokemon pretty quickly.  A lot of requirements were quickly implemented, and all that was left was error checking the routes and authenticating some content. But then I got an idea:

In App Currency.

Since you could catch pokemon at will, and train them to level 100 full stats in about 5 seconds, the app really had no heart or soul.  Add in a finite resource and a random chance at a rare colored pokemon (using a CSS invert filter to give the pokemon a different look), and all of a sudden the app is becoming a game.  No longer can you just max everything out. No longer can you just catch hundreds of pokemon.  WIth a little imposed restraint, editing forms suddenly became exciting.

![](https://i.imgur.com/nuyHT47.jpg)
