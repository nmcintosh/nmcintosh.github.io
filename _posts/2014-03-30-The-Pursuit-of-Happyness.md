---
layout: post
title: The Pursuit of Happyness
---

A lot of very clever people have existed on this earth and have done some very cool stuff with their minds. Collectively, they have formed a very impressive mound of achievements. To attempt to add to that mound is daunting, but doable. Those last few sentences are a bad attempt at poetically saying this past while has been tough (with respect to progress in my work; I feel quite fine otherwise).

As I am somewhat new to the whole *academic research* thing, I kind of expected to not get a whole lot done for a little while, but just recently a new genre of not getting things done has been experienced: going down the wrong path.

Not being able to see the big picture is what is going wrong here. This problem is easy to identify, but, as I see it, almost impossible to just *fix*. I've learned a few things this last week that have prompted me to start a new battle with tunnel-vision:

- other people are pretty darn smart, and
- looking for answers to poorly posed questions is a silly thing to do.

I'll elaborate on the second lesson of the week a little more. Early in the week I was poking around in the section of *the literature* that dealt with flow in porous media, specifically flow through capillaries. I quickly stumbled across a seminal work by [Edward Washburn](http://en.wikipedia.org/wiki/Washburn's_equation) which states that the distance a fluid penetrates into a capillary, driven only by surface tension at the fluid front and with viscous losses, is proportional to the square root of flow time, or:

$$
l^2 \propto t.
$$

Great, I thought, but what if there are other driving forces and/or losses? In brief, I spent a good half-day deriving another equation which took into account the effect of an expanding capillary (think squishing a straw, closing off the ends and then trying to get the straw back to it's original form, the straw is going to want to `suck' stuff in). Fantastic: I got to do some math and ended up with a result which physically made sense. In fact, *my* equation matched exactly that given by Washburn! It took a little while but I eventually realized I spent half of a day re-doing the algebra from a paper I had just read which was published in 1921\.

Later that same day I met with my supervisor and the lesson for the week presented itself. I was assured that the capillary flow direction was a good one to snoop around in, this felt good. Although it was clear I lacked an understanding of what was going on within the approach to the problem and was asked to consider the most general case possible and get a relation between the penetration distance and time (the wood soaking up liquid problem I am looking is a transient one), I did so and learned a heck of a lot because I did. What I ended up with is a force balance which I can delete terms from as I deem appropriate. For a capillary of radius $$R$$, inclined from the horizontal by an angle of $$\psi$$, it looks like:

$$
\frac{2\gamma\cos\theta}{R} = \rho g l \sin(\psi) +
                              \frac{8\mu l}{R^2} \frac{\mathrm{d}l}{\mathrm{d}t} +
                              \rho\frac{\mathrm{d}}{\mathrm{d}t}\left(l\frac{\mathrm{d}l}{\mathrm{d}t}\right)
$$

On the surface, this is a huge complicated pile of garbage. Instead it is the process I had to work through to get to it that I deem valuable: I was able to shed light on the actual problem at hand. It goes to show (to me at least), how rich and complex of a system I am dealing with. The above equation enables me to pose an intelligent, complete, and relevant problem; that's a good thing, to be sure. In my case, I hope to look into what goes on with $$l$$ if $$R$$, too, is a function of time.