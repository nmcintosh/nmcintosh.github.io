---
layout: post
title: Seven Pounds
---

A first has occured: a first term of graduate school has been completed. And boy does it feel great. The end of courses, the start of warm weather, the end of madding crowds at every coffee store on campus, and the beginning of full-time research all smell great, and this time of year stinks of them. Fantastic.

While preparing for finals, I came upon a problem I thought was pretty neat and is given in the excellent text *'Transport Phenomena, 2nd Revised Edition'* by R. Byron Bird, Warren E. Stewart, and Edwin N. Lightfoot as problem 6C.1. The situation at hand is as follows:

> A sphere of radius $$R$$ is fired horizontally ($$x$$ direction) at high velocity in still air above ground level, an identical sphere is dropped from the same height above the ground (in the $$y$$ direction).

What we are tasked with figuring out is which sphere will hit the ground first and if that result would be the same if the sphere was fired horizontally very slowly.

This kinetic sort of stuff begs to have a force balance performed. We shall oblige.

There are three forces at play on the spheres:

1. frictional drag, $$F_1$$
2. gravity, $$F_2$$
3. buoyancy, $$F_3$$

If we take 'down' to be the positive $$y$$ direction (with unit vector $$\delta_y$$) we can write:

$$
\mathbf{F}_\mathrm{net} = (F_2 - F_3)\delta_y - F_1\mathbf{n},
$$

where $$\mathbf{n}$$ is normal to the sphere's motion.

Now, the gravity and buoyancy forces are equal to the product of the sphere's volume and the density of the sphere ($$\rho_s$$) and the air ($$\rho$$), respectively. The frictional drag force is proportional to the product of its charachteristic area ($$\pi R^2$$) and kinetic energy ($$\frac{1}{2}\rho_sv^2$$) by a constant known as a friction factor ($$f$$). Substituting all of this and replacing the force on the left of the equality with a rate of momentum change we get:

$$
\frac{\mathrm{d}}{\mathrm{d}t}\left(\frac{4}{3} \pi R^3 \rho_s \mathbf{v}\right) = \frac{4}{3} \pi R^3 g (\rho_s - \rho) \delta_y - \frac{1}{2} \pi R^2 \rho_s (v_x^2 + v_y^2) f \mathbf{n}.
$$

The above equation is pretty great, but not all that useful in its current form. To make it a little bit more manageable, we can replace $$\mathbf{n}$$ with

$$
\frac{\mathbf{v}}{v} = \frac{\mathbf{v}}{\sqrt{v_x^2 + v_y^2}},
$$

with the velocity vector, $$\mathbf{v}$$, having $$x$$ and $$y$$ components of $$v_x$$ and $$v_y$$.

Inserting this result into the previous, cancelling terms, and rearranging, we finally get:

$$
\frac{\mathrm{d}\mathbf{v}}{\mathrm{d}t} = \left(1 - \frac{\rho}{\rho_s}\right)g\delta_y - \frac{3}{8}\frac{\rho}{\rho_s}\frac{f}{R}v\mathbf{v}.
$$

This vector equation can be separated into two scalar equations in the $$x$$ and $$y$$ directions to give the accelerations $$a_x$$ and $$a_y$$:

$$
a_x = \frac{\mathrm{d}v_x}{\mathrm{d}t} = -\frac{3}{8}\frac{\rho}{\rho_s}\frac{f}{R}vv_x
$$

$$
a_y = \frac{\mathrm{d}v_y}{\mathrm{d}t} = \left(1 - \frac{\rho}{\rho_s}\right)g - \frac{3}{8}\frac{\rho}{\rho_s}\frac{f}{R}vv_y.
$$

Now we are getting somewhere. Next, since we care about the vertical *'who touches the ground first'* kind of motion, let's look at what form $$a_y$$ takes for the dropped and fired spheres.

Working from left to right, we see both the fired and dropped spheres will include the same gravity/buoyancy term, however the definition of the velocity magnitude, $$v$$, in the second term will change. In the case of the dropped sphere, $$v_x = 0$$ and so $$v = v_y$$, but in the case of the fired sphere $$v$$ will include a $$v_x$$ term and be equal to $$\sqrt{v_x^2 + v_y^2}$$.

Now, since:

$$
\sqrt{v_x^2 + v_y^2} > v_y \quad\forall\quad v_x \neq 0,
$$

the second term in the $$a_y$$ equation is smaller in the dropped case, which in turn means $$a_y$$ in this case is larger. Fantastic, we can now say that, as the dropped sphere accelerates faster downward than the fired one, **the dropped sphere hits the ground first**. This is contradictory to what [others](http://mythbustersresults.com/knock-your-socks-off) have 'proven' empirically, although their problem geometry was slightly different.

The above result is pretty cool, but does it apply to all regimes of sphere motion? What if our sphere launcher is weak and pitiful?

Let's consider the effect of the friction factor, $$f$$, in the above.

When the sphere is fired horizontally very slowly, when so called *creeping flow* is achieved, the friction factor is proportional to the inverse of the magnitude of the sphere velocity.

$$
f \propto \frac{1}{v}
$$

Inserting this relation (the result is true for any constant of proportionality) into the $$a_y$$ relation above, we can see that we eliminate any term that may contain $$v_x$$. This means that if the sphere is moving really slowly (for $$\mathrm{Re}_\mathrm{sphere} < 0.1$$), $$a_y$$ will be equal for the fired and dropped spheres and thus **they will hit the ground at the same time**.

Given the large number of moving spheres in this world, the above problem's applicability to all kinds of sports and daily occurences is worth noting. It is also interesting to note that not a single bit of any of the above analysis is any newer than the mid 1800's; it's amazing to think of not just applying something like [Stokes' Law](http://en.wikipedia.org/wiki/Stokes'_law), but [inventing it altogether](http://en.wikipedia.org/wiki/George_Gabriel_Stokes).

NM