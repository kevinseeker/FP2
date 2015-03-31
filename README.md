# Final Project Assignment 2: Explore One More! (FP2) 
DUE March 30, 2015 Monday (2015-03-30)

This is just like FP1, but where you do a different library. (Full description of FP1 is [on Piazza.][piazza])

During this assignment, you should start looking for teammates. See the project schedule [on Piazza.][schedule]

Write your report right in this file. Instructions are below. You can delete them if you like, or just leave them at the bottom.
You are allowed to change/delete anything in this file to make it into your report. It will be public.

This file is formatted with the [**markdown** language][markdown], so take a glance at how that works.

This file IS your report for the assignment, including code and your story.

Code is super easy in markdown, which you can easily do inline `(require net/url)` or do in whole blocks:
```
#lang racket

(require net/url)
```

### My Library: (turtles/graphics)

I decided to investigate the turtle graphics library. I began by reading the very beginning of the documentation at racket-lang and included the mandatory:

(require graphics/turtles) 

followed by the line that makes the turtle appear
(turtles #t)

After attempting some freelance turtling briefly, I used the examples, which required the additional line to link to the library:
(require graphics/turtle-examples)

Next, I began utilizing the polygon creating function regular-polys and created what appeared to be concentric circles but in actuality was concentric polygons for a large n . I also used regular-poly and I created some basic polygons such as a pentagon:
(regular-poly 5 20)

Wrapping it around and filling it by 20 sided polygons with the code following the above code:
(regular-polys 20 6)

This created a reasonable but more interesting picture.

Changing the inner turtle to something resembling an 8-sided star by adding (radial-turtles 3)
, I then expanded the size of the points of the star by including (spaced-turtles 3)

Next, I experimented with spokes, though it made the presentation look messy.
Using the (spyro-gyra) method call followed by (neato), created a donut-like image, which is available at:

http://i296.photobucket.com/albums/mm177/kevinseeker10/donut_ready_zpsqzahcfif.png

To recap, the code that leads to that image was:
(regular-poly 5 20)
 (regular-polys 20 6)
 (radial-turtles 3)
(spaced-turtles 3)
(spyro-gyra) ; interesting to look at
(neato)

I next played with the pre-made sierpinski triangle-creating methods. After several poor performances,
I followed the advice of the guide and tried calling the draw on an integer value 10, which I later adjusted to 8.
I also turned the image by 2 radians. So my code looked like:

(sierp 150)
(draw 8)
(turn/radians 2)

And the picture that it draws is available at:
http://i296.photobucket.com/albums/mm177/kevinseeker10/sierp_triangle_zps0fuipwfe.png


I also played with the Koch snow-flake-like images using home to give it an interesting edge.
The code:
(home)
(koch-split 400)

generated the Koch image available at:

http://s296.photobucket.com/user/kevinseeker10/media/koch_with_home_zpscyakveuz.png.html

I tried playing with peano and peano-position-turtle to fill the snowflake but it didn't work out.

I also tried using the fractal creating fern1 method, with the call (fern1 91) after a few attempts at different parameter values.  I took a screenshot using shutter and it's available here, though it ran out of memory before completing the call:
http://i296.photobucket.com/albums/mm177/kevinseeker10/fern_leaf_zpsvinvu2yn.png

That's it.













Remember that this report must include:
 
* a narrative of what you did
* the code that you wrote
* output from your code demonstrating what it produced
* any diagrams or figures explaining your work 
 
The narrative itself should be no longer than 350 words. Yes, you can add more files and link or refer to them. This is github, handling files is awesome and easy!

Ask questions publicly in the Piazza group.

### How to Do and Submit this assignment

1. To start, [**fork** this repository][forking].
1. Modify the README.md file and [**commit**][ref-commit] changes to complete your solution.
  2. (This assignment is just one README.md file, so you can edit it right in github without cloning)
  3. (You may need to clone and push if you want to add extra files)
1. [Create a **pull request**][pull-request] on the original repository to turn in the assignment.

<!-- Links -->
[piazza]: https://piazza.com/class/i55is8xqqwhmr?cid=411
[schedule]: https://piazza.com/class/i55is8xqqwhmr?cid=453
[markdown]: https://help.github.com/articles/markdown-basics/
[forking]: https://guides.github.com/activities/forking/
[ref-clone]: http://gitref.org/creating/#clone
[ref-commit]: http://gitref.org/basic/#commit
[ref-push]: http://gitref.org/remotes/#push
[pull-request]: https://help.github.com/articles/creating-a-pull-request

