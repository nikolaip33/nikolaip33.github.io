---
layout: post
title:      "You've got to break it down, before you can build it up"
date:       2017-10-17 19:23:35 +0000
permalink:  youve_got_to_break_it_down_before_you_can_build_it_up
---


The art of programming is not in making a computer perform a task, but rather it is in making a task performable by a computer.

Someone much more worldly than I probably has a more pithy expression of this idea, and I'll elaborate a little on it for you now.  Knowledge of a programming language and how data is structured is fairly arbitrary in the grand scheme of things, and what is important is how one approaches every new problem that is presented to them.

What does success look like for my program? What are the steps my program needs to take? What are the steps inside those steps? Is this really a single problem, or is it 2 problems that eventually intersect? What can I ignore, and what do I absolutely have to make sure happens? What are my edge cases and how do they affect my algorithm?

Using the Tic-Tac-Toe AI project as an example, my expectations and goals changed dramatically day to day as I programmed it.  Initially I just wanted it to never lose, which was easy enough to accomplish with a few boardstate conditionals.  But then I started to wonder what would happen if my AI could initiate some of the patterns it was designed to defend against? How would that look? What if my opponent misplayed? How does my AI punish that? After a lot of deliberate study of the game of Tic-Tac-Toe, a few rules were discovered:


1. You can never lose going second.
2. Center square is always the safest to take.
3. Taking an edge square too early by either player instantly loses you the game.

Armed with this I was able to write some simple methods that evaluated board states and would override the basic #take_center and #take_corner methods that were the backbone of the AI.  I was pretty satisfied with my results.  It would always tie itself, and I could never beat it with the tactics I'd discovered. All was well. That was until I got curious. How would it do against other students? How would it do against the repository solution?

Not well. OK not well is a bit overdramatic, but there were some surprising outcomes.  Nothing could ever beat it, but it also wasn't winning.  After running batches of games upon batches of games, 2,000 at a time, and analyzing how the turns were playing out, more rules were discovered:

4. X never has to take center unless it is to defend. I've come to call this the "Vicious X" strategy.
5. O absolutely has to take an empty center square or it will automatically lose. I've come to call this "Defensive O."

Then came the real question - why am I doing this? My project was submitted and I was satisfied with it's results. But still I came back to it every night. Added a new turn 2 punish. Added a turn 3 punish. Added a follow up to a turn 3 attack pattern. Refined some of the code to make it more readable. Removed some of the logic that made it more whimsical and instead tuned it to always try and win.

This is why I program. I don't just want to understand the task at hand or the problem being posed. I want to dismantle it. I want to scrutinize it. I want to conquer it.
