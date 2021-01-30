# Ping Pong CSS
> Jan 2021

Fun play around project to learn more CSS positioning, shapes and animations. [Resources](https://github.com/richardaspinall/pingpong-css#resources)

## Goals
* Learn about CSS animations and how to create complex shapes.

## Results
* The initial goal was to just create a cloud in CSS. I thought I'd carry on and create a few more complex shapes and animations.
![Full Image](https://user-images.githubusercontent.com/15721687/105628045-9601cf00-5e8e-11eb-9ad9-2c437eb89c7b.png)
![finished gif](https://user-images.githubusercontent.com/15721687/106345344-96252300-6303-11eb-9ce2-3ce6b6e5fd74.gif)
## Steps

### Create a cloud!

I started off by researching how to create a complex shape such as a cloud. I came across a very simple way to do this via 3 rectangles with full border radius: a long rectangle as the base, then two more rectangles (squares) relatively positioned to the base rectangle using pseudo selectors. 

![Cloud Gif](https://user-images.githubusercontent.com/15721687/105627436-1a525300-5e8b-11eb-8738-ef970cbc99d7.gif)

### Creating the rackets

I used the same method as creating a cloud to create the rackets. Then rotated them to face off. Exact positioning was made a lot easier by putting a red box around the bat.

![Racket positioning](https://user-images.githubusercontent.com/15721687/105627896-9057b980-5e8d-11eb-9162-41d9b23adfe1.png)

### Bouncing ball with shadow

Created a small ball and a shadow ball to animate. Using keyframes and animation, I mapped out a route for the ball to bounce up and down towards the screen and the shadow path casted from the light source (upper leftish). 

Timing of the bounces is a bit floaty but it works! 

![Bouncing Ball Gif](https://user-images.githubusercontent.com/15721687/105627970-1e33a480-5e8e-11eb-8f5b-564f8b20333b.gif)

### Make it interestsing and mesmerizing.

It was very boring with just the bouncing ball, it kind of looked like it was supposed to be a game rather than an animation. Also, it seems pretty obvious to make the ball bounce between the two sides. 

I just added more keyframes and mapped the route in a more interesting way. Made size of the ball bigger and increase of width as it crossed the middle making it look like it's being hit up and towards the viewer in a speedy way.

Rackets just need to move to the balls positioning on alternating quarter intervals. Added a few more keyframes for the rackets just before the ball landed to make it seem like they didn't know exactly where the ball was always going. 

Clouds needed to move. This was fairly simple once I realized I should use the margin on the clouds to determine the start and end of the paths. 

Additionally I needed to wrap everything in another div because mobile doesn't respect `overflow-x` on the body which meant the clouds would cause the annoying horizontal scroll as they were absolutely positioned. ref: https://stackoverflow.com/questions/24193272/overflow-xhidden-on-mobile-device-not-working

## Resources
### CSS Clouds and movement:
* https://codepen.io/Mark_Bowley/pen/xEbuI
* https://lauryndbrown.github.io/2017/06/08/creating-clouds-in-css.html
* https://codepen.io/antonioescudero/pen/zrxGve (moving clouds)

### Shapes
* https://css-tricks.com/the-shapes-of-css/
